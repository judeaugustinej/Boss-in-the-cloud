#Openstack

OpenStack is a cloud operating system that controls large pools of compute, storage, and networking resources throughout a datacenter, all managed through a dashboard that gives administrators control while empowering their users to provision resources through a web interface.


##Process WorkFlow
####Horzion 
This component provides a web-based portal to interact with all the underlying OpenStack services,
such as NOVA, Neutron, etc.
![horizon](https://cloud.githubusercontent.com/assets/3624858/8539652/d21592e8-249b-11e5-8938-3796c2f81ada.png)

####Nova
OpenStack compute (codename: Nova) is the component which allows the user to create and manage virtual servers using the machine images. It is the brain of the Cloud. OpenStack compute provisions and manages large networks of virtual machines.
![nova](https://cloud.githubusercontent.com/assets/3624858/8539654/d49f4b80-249b-11e5-8573-7dc1a8b852e0.png)

####Keystone
This provides a central directory of users mapped to the OpenStack services. It is used to provide an authentication and authorization service for other OpenStack services.
![Keystone](https://cloud.githubusercontent.com/assets/3624858/8539655/d60ac1f2-249b-11e5-9de8-2c7e18d32791.png)

####Neutron
It is a pluggable, scalable and API-driven system for managing networks. OpenStack networking is useful for VLAN management, management of IP addresses to different VMs and management of firewalls using these components.
![neutron](https://cloud.githubusercontent.com/assets/3624858/8539656/d7773944-249b-11e5-9671-e5114b23b30e.png)

####Glance
This provides the discovery, registration and delivery services for the disk and server images. It stores and retrieves the virtual machine disk image.
![glance](https://cloud.githubusercontent.com/assets/3624858/8539657/d87b6ca2-249b-11e5-8033-abec6f72758a.png)

### Contents


* [Articles](#articles)
* [Guides](#guides)
* [Language-specific](#language-specific)
    * [Python](#python)
* [Videos](#videos)
* [other repos](#similar-github-repos)


## Articles

* **OpenStack Juno Neutron Deployment**[[web][a_cc]]
* **OpenStack Fundamentals Training Part 2 Compute**[[pdf][a_wb]]
* Anuj Sehgal     - **Introduction to OpenStack**[[pdf][a_pd]]
* Sharone Zitzman – **OpenStack Wiki in Short – A Quick Guide to Open Cloud** [[web][a_cc]]
* Sharone Zitzman - **What is Openstack?** [[web][a_ac]]
* Anita Kuno  - **Installing Devstack With Vagrant** [[web][a_cb]]                      

[a_cb]: http://getcloudify.org/2014/07/18/openstack-wiki-open-cloud.html#at_pco=cfd-1.0&at_ab=per-2&at_pos=0&at_tot=3&at_si=5593a074a7e071e7
[a_wb]: http://cdn.oreillystatic.com/en/assets/1/event/61/OpenStack%20Fundamentals%20Training%20Part%202%20-%20Compute%20Presentation.pdf
[a_pd]: http://cnds.eecs.jacobs-university.de/slides/2012-aims-openstack-handouts.pdf
[a_cc]: http://www.opencloudblog.com/?p=557
[a_ac]: http://getcloudify.org/2014/07/10/what-is-openstack-tutorial.html
[a_cb]: http://anteaya.info/blog/2013/09/01/installing-devstack-with-vagrant/

## Language-specific

### Python

* [debian-ubuntu-centos-rhel-linux-install-pipclient](http://www.cyberciti.biz/faq/debian-ubuntu-centos-rhel-linux-install-pipclient/)
* [Python APIs: The best-kept secret of OpenStack](http://www.ibm.com/developerworks/cloud/library/cl-openstack-pythonapis/)
* [How to launch an instance on OpenStack (III): Python novaclient library](https://albertomolina.wordpress.com/2013/11/20/how-to-launch-an-instance-on-openstack-iii-python-novaclient-library/)
* [Installing and Configuring Piston OpenStack](http://docs.pistoncloud.com/installation/index.html)
