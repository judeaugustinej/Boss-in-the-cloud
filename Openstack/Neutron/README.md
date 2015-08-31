##Neutron

```
Neutron is the networking component of OpenStack, and is a standalone service
alongside other services such as Nova (Compute),
Glance (Image), Keystone (authentication), and Horizon (Dashboard).
Like those services, the deployment of Neutron involves deploying several processes on each host.
```
```
Neutron provides cloud operators
and users with an API to create and manage networks in the cloud.
An extension
framework allows for additional network services, such as load balancing, firewalls,
and virtual private networks, to be deployed and managed.
```
###network
```
A network provides connectivity to and from instances.

Tenant networks are networks created by users within tenants, or groups of users. 
By default, networks created with tenants are not shared among other tenants.
Useful network types in this category are vlan (802.1q tagged) and gre (unique id).
With the use of the L3 agent and Neutron routers, it is possible to route between GRE-based tenant networks. 
Without a Neutron router, these networks are effectively isolated from each other (and everything else, for that matter).
```

###subnets
```
A subnetwork, or subnet, is a logical, visible subdivision of an IP network.
The practice of dividing a network into two or more networks is called subnetting.
Computers that belong to a subnet are addressed with a common, identical, most-significant bit-group in their IP address. This results in the logical division of an IP address into two fields, a network or routing prefix and the rest field or host identifier. The rest field is an identifier for a specific host or network interface.
```

###ports
```
In computer networking, a port is a software construct serving as a communications endpoint in a computer’s host operating system.
A port is always associated with an IP address of a host and the protocol type of the communication.
It completes the destination or origination address of a communications session. A port is identified for each address and protocol by a 16-bit number, commonly known as the port number.
```

###Security Groups
```
Create and enforce ingress and egress traffic rules per-port
```

###Virtual Interfaces 
```
Use the Cloud Networks virtual interface extension to create a virtual interface to a specified network and attach that network to an existing server instance. You can attach either an isolated network that you have created or a Rackspace network.

A virtual interface works in the same way as the network interface card (NIC) inside your laptop. Like a NIC, a virtual interface is the medium through which you can attach a network to your server. You create a virtual interface for a specified network, and the network, which is composed of logical switches, is attached to your server instance through the virtual interface.

You can create a maximum of one virtual interface per instance per network.
```
##Features of OpenStack Networking
###Virtual switch
```
Connect VM at layer 2.
Neutron supports multiple virtual switching platforms, including built-in Linux bridging
and Open vSwitch.
Open vSwitch, also known as OVS, is an open source virtual
switch that supports standard management interfaces and protocols, including
NetFlow, SPAN, RSPAN, LACP, and 802.1q, though many of these features are not
exposed to the user through the OpenStack API.
In addition to VLAN tagging, users
can build overlay networks in software using L2-in-L3 tunneling protocols, such as
GRE or VXLAN. Open vSwitch can be used to facilitate communication between
instances and devices outside the control of OpenStack, which include hardware
switches, network firewalls, storage devices, dedicated servers, and more. 
```
###Routing
```
NAT capabilities through the use of IP
forwarding, iptables, and network namespaces.
Each network
namespace has its own routing table and iptables process that provide filtering
and network address translation, also known as NAT.
Configuring a router within Neutron enables
instances to interact and communicate with outside networks
```

###Load balancing
```
First introduced in the Grizzly release of OpenStack, Load-Balancing-as-a-Service,
also known as LBaaS, provides users the ability to distribute client requests across
multiple instances or servers. Havana is equipped with a plugin for LBaaS that
utilizes HAProxy as the load balancer.
```
###Firewalling
```
In Havana, there are two methods of providing security to instances or networks:
security groups and firewalls
```
### Virtual private networks
```
A VPN enables a computer to send and receive data across
public networks as if it were directly connected to the private network.
Neutron
provides a set of APIs to allow tenants to create IPSec-based VPN tunnels to remote
gateways.
```

## Types of network traffic
* Management
* API
* External
* Guest
### Management
```
The management network is used for internal communication between hosts
for services, such as the messaging service and database service. All hosts will
communicate with each other over this network. 

Used for internal communication between OpenStack Components.
IP address reachable within the data-center(Management Security Domain)
```
### API
```
The API network is used to expose OpenStack APIs to users of the cloud and services
within the cloud. Endpoint addresses for services, such as Keystone, Neutron,
Glance, and Horizon, are procured from the API network.

 This network is considered the Public Security Domain.
```
### External
```
 The IP addresses on this network should be reachable by anyone
on the Internet(Public security Domain).

Once a router has been configured, this network becomes the source of floating IP addresses for
instances and load balancer VIPs. IP addresses in this network should be reachable
by any client on the Internet.
```
### Guest
```
Used for VM data communication within the cloud deployment. 
 (Guest Security Domain)
The guest network is a network dedicated to instance traffic
```

### Contents

* [Articles](#articles)
   * [Rackspace](#racespace)
   * [Mirantis](#mirantis)
   * [Go](#goland)
* [python-neturonclient](#python-neutronclient)

* [Maths](#maths)
* [Misc](#misc)
* [Questions](#questions)
* [Systems Design](#systems-design)
* [Unix](#unix)
* [Videos](#videos)
* [other repos](#similar-github-repos)


## Articles
https://wiki.openstack.org/wiki/Neutron
### Racespace
* James Thorne – **Beginning to Understand Neutron Provider and Tenant Networks in OpenStack** [[web][a_cb]]
* James Thorne -  **Neutron Networking: The Building Blocks of an OpenStack Cloud** [[web][a_c1]]
* James Denton - **Neutron Networking: Simple Flat Network** [[web][a_c2]]
* James Denton - **Neutron Networking: VLAN Provider Networks** [[web][a_c4]]
* James Denton - **Neutron Networking: Neutron Routers and the L3 Agent** [[web][a_c3]]
* Racespace - **Quickstart for Cloud Networking** [[docs][a_c6]]
[a_cb]: https://developer.rackspace.com/blog/beginning-to-understand-neutron-provider-and-tenant-networks-in-openstack/
[a_c1]: https://developer.rackspace.com/blog/beginning-to-understand-neutron-provider-and-tenant-networks-in-openstack/
[a_c2]: https://developer.rackspace.com/blog/neutron-networking-simple-flat-network/
[a_c3]: https://developer.rackspace.com/blog/neutron-networking-l3-agent/
[a_c4]: https://developer.rackspace.com/blog/neutron-networking-vlan-provider-networks/
[a_c6]: https://developer.rackspace.com/docs/cloud-networks/getting-started/

### Mirantis

* Nir Yechiel **What’s Coming in OpenStack Networking for Juno Release** [[web][m_m2]]
* Damian Igbe - **Neutron Network Namespaces and IPtables** [[web][m_m1]]
* Eugene Kirpichev - **OpenStack Networking Tutorial: Single-host FlatDHCPManager** [[web][m_m3]]
* **OpenStack Networking – FlatManager and FlatDHCPManager** [[web][m_m4]]
* Piotr Siwczak - **Configuring Floating IP addresses for Networking in OpenStack Public and Private Clouds** [[web][m_m5]]
* Piotr Siwczak - **Openstack Networking for Scalability and Multi-tenancy with VlanManager** [[web][m_m6]]
* 

[m_m1]: https://www.mirantis.com/blog/the-road-to-hong-kong-openstack-summit-speakers-4-neutron-network-namespaces-and-iptables/
[m_m2]: http://redhatstackblog.redhat.com/2014/09/11/whats-coming-in-openstack-networking-for-juno-release/
[m_m3]: https://www.mirantis.com/blog/openstack-networking-single-host-flatdhcpmanager/
[m_m4]: https://www.mirantis.com/blog/openstack-networking-flatmanager-and-flatdhcpmanager/
[m_m5]: https://www.mirantis.com/blog/configuring-floating-ip-addresses-networking-openstack-public-private-clouds/
[m_m6]: https://www.mirantis.com/blog/openstack-networking-vlanmanager/

#python-neturonclient
```
Create Network
List Networks
Create Subnet
List Subnets
Create Port
List Ports
Create Security Group
Create Security Group Rule
```
##TODO
```

*What is a Neutron plugin
*how Neutron API calls are dispatched to it
*Do I need to write a new plugin? * What are my options for adding capabilities to existing plugins? 
** Where to start from * Implementing the Neutron API - the 'sendmail' plugin
https://www.openstack.org/summit/openstack-summit-hong-kong-2013/session-videos/presentation/how-to-write-a-neutron-plugin-if-you-really-need-to

```
