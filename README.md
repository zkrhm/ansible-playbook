# ansible-playbook
just another ansible playbook

of course you can use it, fork it, distribute it. as said on license. :D

## Operating System Support

at current time the playbook
only usable for installing both db server and webservers dependency on centos/7 machine.

## Dependencies
you will need ansible ver.2 to run this playbook

## Authentication
Configuring ssh key to permit ansible to be able to log in without password is
strongly recomended. but if you don't want to do that, you'll just have to add
*--ask-key* when you execute the ansible-playbook.

## Configuration

you will need to edit host info on inventory file (development, staging, production).
if you need to set different port for your server, just change it in __group_vars__ directory

## Usage

simply just issue following command (ssh-key has been set)
```bash
ansible-playbook -i <inventory> <playbook>.yml
```
or 
```bash
ansible-playbook -i <inventory> <playbook>.yml --ask-pass
```
if you love to be ask about the password

available inventory:
- development
- staging
- production

available playbook:
- db.yml
- web.yml

## what it do?
this playbooks will install some dependencies on a servers.

on webserver it will install :

- git client
- epel-repo
- c compilers
- iptable-services
- php
- composer
- pip
- supervisor
- nginx 1.8
- http 2.4

**webservers part is tested**

on db server it will install:
- iptables
- epel-repo
- c compilers
- redis cache
- mongodb
- elasticsearch

**dbservers part still on testing**


