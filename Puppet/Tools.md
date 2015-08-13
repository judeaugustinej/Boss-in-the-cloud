## List of puppet tools

```
puppetmasterd → puppet master

puppetd → puppet agent

puppet → puppet apply

puppetca → puppet cert

ralsh → puppet resource

puppetrun → puppet kick

puppetqd → puppet queue

filebucket → puppet filebucket􀀀􀀀

puppetdoc → puppet doc

pi → puppet describe
```
####puppet master (or puppetmasterd)
```
1)Central management deamon,usually the setup involes one puppet master and many slaves.

2)By default, puppet master operates a certificate authority, which can be managed using puppet cert.

3)Puppet master serves compiled configurations, files, templates, and custom plugins to managed􀀀􀀀 nodes.

4)The main configuration file for puppet master, puppet agent, and puppet apply is􀀀􀀀
/etc/puppet/puppet.conf, which has sections for each application.

5)It send puppet agent a compiled catalog.

6)If pluginsync is enabled in a given nodeʼs configuration, custom plugins stored on the Puppet Master server are􀀀
transferred to it automatically.

```

####puppet agent (or puppetd)
```
1)Puppet agent runs on each managed node. By default, it will wake up every 30 minutes
(configurable),

2)Puppet􀀀 agent is then responsible for making the system match the compiled catalog.

3)The puppet master server determines what information a given managed node should see based
on its unique identifier (“certname”);
```

####puppet apply (or puppet)
```
Used to apply manifest on the local machine(for instance, to test manifests, or in a non-networked disconnected
case).
```

####puppet cert (or puppetca)
*The puppet cert command is used to sign, list and examine certificates used by Puppet to secure􀀀
the connection between the Puppet master and agents.*
*Certificates with a + next to them are signed.*
https://hurricanelabs.com/blog/managing-puppet-certificates/
```
> puppet cert --list
agent.example.com
> puppet cert --sign agent.example.com
> puppet cert --all and --list
+ agent.example.com
agent2.example.com

```
####puppet doc (or puppetdoc)
```
Puppet doc generates documentation about Puppet and your manifests, which it can output in
HTML, Markdown and RDoc.
```
####puppet resource (or ralsh)
```
Interactively view and manipulate the local system resources.
```
####puppet inspect
```

```
####factor
```
1)It is used by the puppet agent to gather the current state of resources

2)It is accessible by the manifest global variables
```
