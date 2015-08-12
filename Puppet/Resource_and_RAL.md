###Resources
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

