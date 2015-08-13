##What is a Manifest ??
```
Puppet programs are called “manifests,” and they use the .pp file extension.

In a manifest which represents the desired state of one resource.
Manifests can also use conditional statements, group resources into collections,
generate text with functions, reference code in other manifests, and do many other things,
but it all ultimately comes down to making sure the right resources are being managed the right way.
```
* Note: To apply manifest on the local machine *
```
$ puppet apply my_test_manifest.pp
```

### Puppet run flow
![puppet-run-flow](https://cloud.githubusercontent.com/assets/3624858/9242896/6fd1ef8c-41a6-11e5-93bb-e6ee32c7b013.png)

*catalog*
```
manifests get compiled into a “catalog,” which is a directed acyclic graph that
only represents resources and the order in which they need to be synced. All of the conditional
logic, data lookup, variable interpolation, and resource grouping gets computed away during
compilation, and the catalog doesnʼt have any of it.
```
*Example 1- 1.file.pp*
```
# /root/training-manifests/1.file.pp
file {'testfile':
path => '/tmp/testfile',
ensure => present,
mode => 0640,
content => "I'm a test file.",
}
```
*Lets run it*
```
# puppet apply 1.file.pp
notice: /Stage[main]//File[testfile]/ensure: created
# cat /tmp/testfile
I'm a test file.
# ls -lah /tmp/testfile
-rw-r----- 1 root root 16 Feb 23 13:15 /tmp/testfile
```
*Example 2 - one more*
```
# /root/training-manifests/2.file.pp
file {'/tmp/test1':
ensure => present,
content => "Hi.",
}
file {'/tmp/test2':
ensure => directory,
mode => 0644,
}
file {'/tmp/test3':
ensure => link,
target => '/tmp/test1',
}
notify {"I'm notifying you.":} # Whitespace is fungible, remember.
notify {"So am I!":}

```
####Namevars and Titles
