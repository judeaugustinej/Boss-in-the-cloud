*What is the OpenStack Neutron ML2 plugin?*
```
ML2 can really be broken down into two camps working together: 
types and mechanisms.

Types typically refer to the type of network being implemented (notice nova-network isn’t an option).

Mechanisms on the other hand generally refer to how that network type should be implemented.

It’s important to understand, within the greater context of this plugin,
that ML2 separates network types from vendor-specific mechanisms to access those networks.

Network types and mechanisms are handled as modular drivers (swappable) and 
supplants legacy/monolithic plugins such as openvswitch and linuxbridge.
ML2 still supports existing Layer2 agents via RPC interface however.
Some examples include openvswitch, linuxbridge and Hyper-V.
```
![ml2-type-mechanism](https://cloud.githubusercontent.com/assets/3624858/9327996/6e7cb76e-45c2-11e5-91e8-37658a0cf614.png)

*How does the ML2 plugin work?*

*How can I use Neutron’s ML2 plugin in my OpenStack cloud?*

*Where can I get more information about ML2?*
http://aqorn.com/understanding-openstack-neutron-ml2-plugin/
