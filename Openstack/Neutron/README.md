##Neutron

```
Neutron is the networking component of OpenStack, and is a standalone service
alongside other services such as Nova (Compute),
Glance (Image), Keystone (authentication), and Horizon (Dashboard).
Like those services, the deployment of Neutron involves deploying several processes on each host.
```

###network
```
A network provides connectivity to and from instances.

Tenant networks are networks created by users within tenants, or groups of users. By default, networks created with tenants are not shared among other tenants. Useful network types in this category are vlan (802.1q tagged) and gre (unique id). With the use of the L3 agent and Neutron routers, it is possible to route between GRE-based tenant networks. Without a Neutron router, these networks are effectively isolated from each other (and everything else, for that matter).
```

###subnets
```
A subnetwork, or subnet, is a logical, visible subdivision of an IP network. The practice of dividing a network into two or more networks is called subnetting.

Computers that belong to a subnet are addressed with a common, identical, most-significant bit-group in their IP address. This results in the logical division of an IP address into two fields, a network or routing prefix and the rest field or host identifier. The rest field is an identifier for a specific host or network interface.
```

###ports
```
In computer networking, a port is a software construct serving as a communications endpoint in a computer’s host operating system. A port is always associated with an IP address of a host and the protocol type of the communication. It completes the destination or origination address of a communications session. A port is identified for each address and protocol by a 16-bit number, commonly known as the port number.
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