```
OpenStack Networking provides virtual networking services to
resources managed by the Nova (Compute) service.
```
![neturon-architecture](https://cloud.githubusercontent.com/assets/3624858/9194449/ebe47b5e-4038-11e5-9ba6-fa2d483d84f3.png)

##Neutron componets
* [Neutron API server](#neutron-api-server) 
* [Switching plugins](#switching-plugins)
* [DHCP agent](#dhcp-agent)
* [Metadata agent](#metadata-agent)

### Neutron API server
```
It runs on the network node to service the Networking API and its extensions.
It also enforces the network model and IP addressing of each port.
The neutron-server and plugin agents require access to a database for persistent storage and
access to a message queue for inter-communication
```
### Switching plugins
```
Runs on each compute node to manage local virtual switch (vswitch) configuration.
The plug-in that you use determine which agents run. 
This service requires message queue access and depends on the plugin used.
```
### DHCP agent
```
Provides DHCP services to tenant networks for providing DHCP services.
```
### Metadata agent
```
Provides L3/NAT forwarding for external network access of VMs on tenant networks.
Requires message queue access.
```
