# SB DBA
Default working version is for M1 Mac - Arm architecture, how to use in amd64 architecture is under.
### Description
Playbooks that contain "provision" are only for setting up VM-s with Vagrant. Playbooks that are in separate folder named playbooks are used in actual ansibleserver. 
There are 2 playbooks in playbooks folder - 1 for database server and 1 for application server. These are copied to ansibleserver while provision with vagrant.
The desired file for this project gathered_data.csv is different when building from scratch. Because I used random generated data for dummy data.
## Automation task - M1 Mac - ARM architecture

1. Install vagrant <br />
macOS - ```brew install vagrant```
2. Install ansible  <br />
https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#installing-ansible-on-specific-operating-systems
3. Install vmware utility <br />
https://www.vagrantup.com/vmware/downloads
4. Install vagrant plugin <br />
```vagrant plugin install vagrant-vmware-desktop```š
5. Git clone this repo <br />
```git clone https://github.com/rolex135/sb_dba.git```
6. Go to cloned directory <br />
```cd sb_dba ```
7. Build and provision machines defined in Vagrantfile <br />
```vagrant up```
8. SSH into ansibleserver that was built with Vagrant <br />
```vagrant ssh ansibleserver```
9. Run plabook from ansibleserver to setup database server <br />
```ansible-playbook dbserver.yaml```
10. Run plabook from ansibleserver to setup app server <br />
```ansible-playbook appserver.yaml```

## Automation task - Linux - AMD64 architecture

1. Install vagrant <br />
Linux has separate commands for every distro - better information at https://www.vagrantup.com/downloads
2. Install ansible <br />
https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#installing-ansible-on-specific-operating-systems
3. Install virtualbox <br />
https://www.virtualbox.org/wiki/Downloads
4. Git clone this repo <br />
```git clone https://github.com/rolex135/sb_dba.git```
5. Go to cloned directory <br />
```cd sb_dba ```
6. Change Vagrantfile-virtualbox to Vagrantfile and also original Vagrantfile to something else <br />
```mv Vagrantfile Vagrantfile-arm && mv Vagrantfile-virtualbox Vagrantfile```
7. Build and provision machines defined in Vagrantfile <br />
```vagrant up```
8. SSH into ansibleserver that was built with Vagrant <br />
```vagrant ssh ansibleserver```
9. Run plabook from ansibleserver to setup database server <br />
```ansible-playbook dbserver.yaml```
10. Run plabook from ansibleserver to setup app server <br />
```ansible-playbook appserver.yaml```