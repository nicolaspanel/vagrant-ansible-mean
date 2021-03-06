# MEAN.JS with Vagrant and Ansible

Setup MEAN.JS development environment using vagrant and ansible.


## Requirements

1. [Vagrant](http://downloads.vagrantup.com/)
2. [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
3. [Ansible](http://www.ansibleworks.com/docs/intro_installation.html)


## Usage

1. Check requirements
2. Clone this repo: `git clone https://github.com/nicolaspanel/vagrant-ansible-mean.git <project_name> && cd <project_name>`
3. Setup and provision vagrant box: `vagrant up`
4. Take a cup of coffee...
5. Connect to the vagrant vm: `vagrant ssh`
6. Generate project template using yeoman `cd /vagrant/src/ && yo meanjs`

Note: part of the provisioning process ensures that Mongo is installed and running on it's default port.

## Installed 
 - Git
 - Nodejs
 - Mongodb
 - Ruby 2.1.2
 - Gems :
 	- compass
 - NPM packages: 
	- yo
	- generator-meanjs (yo generator for MEAN.JS)
	- express
	- grunt-cli
	- bower

VM Configuration
----------------
For more on VM configuration options, check out the docs at [Vagrant](http://docs.vagrantup.com/v2/virtualbox/configuration.html)
