# Vapor-Vagrant
This project is the start of a compilation of examples and hopefully best
practices for creating vapor based solutions using Swift.

## 🔧 Requirements

This project is setup to buildout a repeatable idempotent process for spinning
up and configuring an environment suitable for deployment of Swift based Vapor
services. You will need to first install the following tools before running
this project.

### [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
Used for virtualization of the Ubuntu 14.04 OS.

### [Vagrant](https://www.vagrantup.com/)
Used for initial configuration and instantiation of the Ubuntu virtual environment.

### [Ansible](http://docs.ansible.com/ansible/intro_installation.html)
Used for all other configuration and buildout of the Ubuntu virtual environment
and also for buildout of vapor-examples project.

### Supported Platforms
* Mac OS X
* Windows
* Linux (Ubuntu)


## 💧 Getting started

### Video how-to guide

Coming soon.

### Cloning and building the box
```sh
git clone https://github.com/spotted-dog-photo/vapor-vagrant <project-directory>
cd <project-directory>
vagrant up
```

### Building the Vapor-Example project

```sh
cd <project-directory>
ansible-playbook --private-key=.vagrant/machines/default/virtualbox/private_key -u vagrant -i .vagrant/provisioners/ansible/inventory/vagrant_ansible_inventory vapor-examples.yml
```

### Running the Vapor-Example project

```sh
vagrant ssh
cd /vagrant/www
vapor run
```
#### Access Vapor Running Service
Simply open your a browser and go to: http://192.168.33.10

# 📖 Other links

* Swift: https://swift.org/
* Vapor: https://vapor.codes
* Vapor Docs: https://vapor.github.io/documentation/
