#VAGRANT?
* Quickly spin up new developers with a powerful, custom stack
* Share your environment with your team
* Maintain multiple environments
* Emulate a production environment

###Vagrant  commands 

* vagrant init - initialize a new vagrant box in the current directory
* vagrant up - start an existing vagrant environment (box) and provision it
* vagrant ssh - shell into a running vagrant box
* vagrant halt - stop a running vagrant box (shut down the computer)
* vagrant destroy - completely destroy a vagrant box (delete all the things)


#####Vagrant box 
An instance of a VirtualBox VM that has been provisioned and
started using Vagrant

#####Base box  
Stored VirtualBox machine packaged into a single file. Think of this
as the template for your Vagrant box.

#####Provision 
Configuration step that comes after the Vagrant box loads.

#####Vagrantfile 
A single file that defines what a particular Vagrant box is, including
the base box, network settings, and provisioning.

#####package.box
When using the VirtualBox provider, it’s a tarred, gzip file containing the following:
Vagrantfile 
box-disk.vmdk --- box-disk.vmdk is the virtual hard disk drive
box.ovf       --- defines the virtual hardware for the box.
metadata.json --- tells vagrant what provider the box works with
