###
#Roles
Organizing things into roles also allows you to reuse common configuration.
This is already possible by "including" other files within a playbook, but with roles,
these types of links between files are automatic based on a specific directory hierarchy.

#File structure
```
+--Roles--+
   `-- git_ansible
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
meta: This directory can contain files that establish role dependencies. You can list roles that must be applied before the current role can work correctly.

##templates
You can place all files that use variables to substitute information during creation in this directory.

##tasks
This directory contains all of the tasks that would normally be in a playbook. These can reference files and templates contained in their respective directories without using a path.

##vars
Variables for the roles can be specified in this directory and used in your configuration files.
