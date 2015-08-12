###What is Resources ?
```
Collection of system configuration is known as resources.
Any resource is very similar to a class of related things: every file has a path and an owner, and􀀀
every user has a name, a UID, and a group.

Which is to say: similar resources can be grouped into types.

Furthermore, the most important attributes of a resource type are usually conceptually
identical across operating systems, regardless of how the implementations differ. That is, 􀀀the
description of a resource can be abstracted away from its implementation.

The RAL splits resources into
types (high-level models) and providers (platform-specific implementations), and lets you describe􀀀
resources in a way that can apply to any system.
```
####Read,check,write
```
Puppet reads the current state of resource.
Check what the resource state should be,
if there is difference in current and expected state
do the needful.
```

###Resource---(type, title, attributes, and values)
![puppet-resource](https://cloud.githubusercontent.com/assets/3624858/9223139/11e6ae9e-4115-11e5-898d-3f5898bbcf04.png)

#### Resource shell
```
Puppet ships with a tool called puppet resource, which uses the RAL to let you query and modify
your system from the shell.
```
*Puppet resourceʼs first argument is a resource type.*
```
$ puppet resource user
```
*Retrieving a specific resourceʼs state by providing a resource name as a second argument*
```
$ puppet resource user root

user { 'root':
Puppet Documentation • Learning — Resources and the RAL 7/311
home => '/var/root',
shell => '/bin/sh',
uid => '0',
ensure => 'present',
password => '*',
gid => '0',
comment => 'System Administrator'
}

```
*Overwriting resource attributes*
```
$ puppet resource user dave ensure=present shell="/bin/zsh" home="/home/dave"
managehome=true
notice: /User[dave]/ensure: created
user { 'dave':
ensure => 'present',
home => '/home/dave',
shell => '/bin/zsh'
}
```
*More on each type*
```
$ puppet describe -s user
Puppet Documentation • Learning — Resources and the RAL 8/311
user
====
Manage users. This type is mostly built to manage system
users, so it is lacking some features useful for managing normal
users.
This resource type uses the prescribed native tools for creating
groups and generally uses POSIX APIs for retrieving information
about them. It does not directly modify `/etc/passwd` or anything.
Parameters
----------
allowdupe, auth_membership, auths, comment, ensure, expiry, gid, groups,
home, key_membership, keys, managehome, membership, name, password,
password_max_age, password_min_age, profile_membership, profiles,
project, role_membership, roles, shell, uid
Providers
---------
directoryservice, hpuxuseradd, ldap, pw, user_role_add, useradd
```

