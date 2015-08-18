http://docs.openstack.org/admin-guide-cloud/content/section_lbaas-overview.html

*what on earth is it ??*

```
Load-Balancer-as-a-Service (LBaaS) enables Networking to distribute incoming requests evenly
among designated instances. This distribution ensures that the workload is shared predictably 
among instances and enables more effective use of system resources.
Use one of these load balancing methods to distribute incoming requests:
```
*Round robin*
```
Rotates requests evenly between multiple instances
```
*Source IP*
```
Requests from a unique source IP address are consistently directed to the same instance.
```
*Least connections*
```
Allocates requests to the instance with the least number of active connections.
```
how to install it ?? how to use it ?? fix bugs ??

http://www.yet.org/2015/05/mos6-lbaas/
http://www.yet.org/2014/09/openvswitch-troubleshooting/
http://www.yet.org/2014/12/mos-6/
http://blog.anynines.com/openstack-neutron-lbaas/
https://access.redhat.com/documentation/en-US/Red_Hat_Enterprise_Linux_OpenStack_Platform/4/html/Installation_and_Configuration_Guide/Configuring_Load_Balancing_as_a_Service_LBaas.html
http://networkstatic.net/installing-openstack-ml2-neutron-plugin-devstack-fedora/
