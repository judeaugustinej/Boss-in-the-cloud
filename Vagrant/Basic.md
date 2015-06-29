###Vagrant is a command line tool. Here are the most important commands:

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
