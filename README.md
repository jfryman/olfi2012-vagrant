olfi2012-vagrant
================

Bootstrap Vagrant Environment for OLFI 2012 Beginners and Advanced Classes

Pre-Requsites
-------------

+ Ruby (1.9.2) [1.8.7 is known to have errors]
+ VirtualBox (>= 4.0)
+ Vagrant (>= 1.0.5)
+ Vagrant-Hitch (>= 0.0.1)
+ Veewee (>= 0.2.3)
+ Bundler ( >= 1.1.0 )


### Exceptions
#### Windows 64-bit

This should work on any OS with VirtualBox installed with the
exception of 64-bit OS Windows XP/Vista/7/8. These OS versions are known
to have issues with win32-ole. There are known workarounds, but please
be advised none of them are well tested.
![Reference](https://github.com/mitchellh/vagrant/issues/423) 

#### OSX Mountain Lion (10.8.2)

If you are running OSX Mountain Lion and happen to be one of the
fortunate folks with a Retina MacBook Pro, please make sure to upgrade
to VirtualBox 4.2.1. ![Reference](http://news.ycombinator.com/item?id=4553414])

## Installation

    git clone https://github.com/jfryman/olfi2012-vagrant.git
    cd olfi2012-vagrant
    git submodule init
    git submodule update
    bundle install
 
### Validation

    cd vagrant
    vagrant up

Look for the text `notice: Installation was successful` in the output from Vagrant

## Usage

The main manifest for this environment can be located at `puppet/manifests/site.pp`. All modules are located in the `puppet/modules/site` and `puppet/modules/dist` directory. 

### Vagrant

All of the following commands should be executed from the directory `vagrant`

To startup the development environment, use the command

> vagrant up

To SSH into the development environment, use the command

> vagrant ssh

To re-run Puppet in the development environment, use the command

> vagrant provision

To restart the development environment non-destructively, use the command

> vagrant reload

To destroy the development environment, use the command

> vagrant destroy
