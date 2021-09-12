# Ansible Assingment
## Problem Statement
* Deploy three (3) Virtual Machines
* Configure Ansible server on VM 1 to deploy a webserver to VM2 and VM3 on port 8080 that displays the message: “Hello World from SJSU”
* Include in the Ansible playbook, plays to deploy and un-deploy all the webserver resources
## Pre-Requisites
* Three Servers(or machines) with ansible installed on machine1(VM1) 
* user with sudo role on the webservers machine2(VM2) and machine3(VM3) for example ansibleuser
* make sure python is installed on those servers
## Pre-Setup
* Replace the vm2 and vm3 ansible_host values from hostinventory.cfg
* Replace the serviceuser with user who has superuser access for respective vms in hostinventory.cfg
* Replace the ssh private key location for respective vms in hostinventory.cfg
## To Execute
#### To Deploy Webserver and the resources
```
ansible-playbook -i hostinventory.cfg webserver.yaml --tags "deploy"
```
#### To Deploy Webserver and the resources
```
ansible-playbook -i hostinventory.cfg webserver.yaml --tags "undeploy"
```