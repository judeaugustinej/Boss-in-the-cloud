###
#Roles
Organizing things into roles also allows you to reuse common configuration.
This is already possible by "including" other files within a playbook, but with roles,
these types of links between files are automatic based on a specific directory hierarchy.

#File structure
```
+--Roles--+
   `-- nginx_ansible
         `--
            |-- files
            |   `-- main.yml
            |-- handlers
            |   `-- main.yml
            |-- meta
            |   `-- main.yml
            |-- tasks
            |   `-- main.yml
            |-- templates
            |    `-- main.yml
            |-- vars
                `-- main.yml
            
```
##files
This directory contains regular files that need to be transferred to the hosts you are configuring for this role. This may also include script files to run.

##handlers
All handlers that were in your playbook previously can now be added into this directory.

##meta
This directory can contain files that establish role dependencies. You can list roles that must be applied before the current role can work correctly.

##templates
You can place all files that use variables to substitute information during creation in this directory.

##tasks
This directory contains all of the tasks that would normally be in a playbook. These can reference files and templates contained in their respective directories without using a path.

##vars
Variables for the roles can be specified in this directory and used in your configuration files.

#Without roles Playbook
```
---
- hosts: droplets
  tasks:
    - name: Installs nginx web server
      apt: pkg=nginx state=installed update_cache=true
      notify:
        - start nginx

    - name: Upload default index.php for host
      copy: src=static_files/index.php dest=/usr/share/nginx/www/ mode=0644
      register: php
      ignore_errors: True

    - name: Remove index.html for host
      command: rm /usr/share/nginx/www/index.html
      when: php|success

    - name: Upload default index.html for host
      copy: src=static_files/index.html dest=/usr/share/nginx/www/ mode=0644
      when: php|failed

  handlers:
    - name: start nginx
      service: name=nginx state=started
```
#With roles
#### In tasks/main.yml
```
---
- name: Installs nginx web server
      apt: pkg=nginx state=installed update_cache=true
      notify:
        - start nginx

    - name: Upload default index.php for host
      copy: src=static_files/index.php dest=/usr/share/nginx/www/ mode=0644
      register: php
      ignore_errors: True

    - name: Remove index.html for host
      command: rm /usr/share/nginx/www/index.html
      when: php|success

    - name: Upload default index.html for host
      copy: src=static_files/index.html dest=/usr/share/nginx/www/ mode=0644
      when: php|failed
```

### In handlers/main.yml

```
---
- name: start nginx
      service: name=nginx state=started
```
### In meta/main.yml
If our role depended on another role, we could add a file in the meta directory called main.yml. This file might specify that this role depends on a role called "apt".
```
---
dependencies:
  - { role: apt }
```

#nignx.yml
```
---
- hosts: localhost
  roles:
    - role: nginx_ansible
```
#----END
```
$ansible-playbook nignx.yml
```
