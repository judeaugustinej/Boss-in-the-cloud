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
