##Meta-parameters
*metaparameters that let you arrange resources in order: before, require, notify,
and subscribe.*

* Metaparameters
  * before
     * Resource is applied before the target resource.
  * require
     * Resource is applied after the target resource.
  * notify
     * similar to before but the target resource will be refreshed if the notify resource changes
  * subscribe
     * similar to require but the subscribing resource will refresh if the target resource changes
  
  
####Before
```
before is used in the earlier resource, and lists resources that depend on it
file {'/tmp/test1':
ensure => present,
content => "Hi.",
before => Notify['/tmp/test1 has already been synced.'],
# (See what I meant about symbolic titles being a good idea?)
}
notify {'/tmp/test1 has already been synced.':}
```
####Require
```
```
####Notify

####Subscribe
