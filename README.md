# ansible-playbook
just another ansible playbook

of course you can use it, fork it, distribute it. as said on license. :D

## what it do?
this playbooks will install some dependencies on a servers. at current time the playbook
only usable for installing both db server and webservers dependency on centos/7 machine.

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

**dbservers part still on testing**
- mongodb
- elasticsearch
