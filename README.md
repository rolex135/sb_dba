# SB DBA
## Automation task

### 1. Install vagrant
macOS - ```brew install vagrant``` <br />
Linux has separate commands for every distro - better information at https://www.vagrantup.com/downloads

### 2. Install ansible
https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#installing-ansible-on-specific-operating-systems

### 3. Install vmware utility
https://www.vagrantup.com/vmware/downloads

### 4. Install vagrant plugin
```vagrant plugin install vagrant-vmware-desktop```

### 5. Git clone this repo
```git clone https://github.com/rolex135/sb_test_dba.git```

### 6. Build and provision machines defined in Vagrantfile
```vagrant up```

### 7. SSH into ansibleserver that was built with Vagrant
```vagrant ssh ansibleserver```

### 8. Run plabook from ansibleserver to setup database server
```ansible-playbook dbserver.yaml```

### 9. Run plabook from ansibleserver to setup app server
```ansible-playbook appserver.yaml```