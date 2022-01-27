# SB DBA
## Automation task - M1 Mac - ARM architecture

### 1. Install vagrant
macOS - ```brew install vagrant```

#### 2. Install ansible
https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#installing-ansible-on-specific-operating-systems

#### 3. Install vmware utility
https://www.vagrantup.com/vmware/downloads

#### 4. Install vagrant plugin
```vagrant plugin install vagrant-vmware-desktop```

#### 5. Git clone this repo
```git clone https://github.com/rolex135/sb_dba.git```

#### 6. Go to cloned directory
```cd sb_dba ```

#### 7. Build and provision machines defined in Vagrantfile
```vagrant up```

#### 8. SSH into ansibleserver that was built with Vagrant
```vagrant ssh ansibleserver```

#### 9. Run plabook from ansibleserver to setup database server
```ansible-playbook dbserver.yaml```

#### 10. Run plabook from ansibleserver to setup app server
```ansible-playbook appserver.yaml```


## Automation task - Linux - AMD64 architecture

#### 1. Install vagrant
Linux has separate commands for every distro - better information at https://www.vagrantup.com/downloads

#### 2. Install ansible
https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html#installing-ansible-on-specific-operating-systems

#### 3. Install virtualbox
https://www.virtualbox.org/wiki/Downloads

#### 4. Git clone this repo
```git clone https://github.com/rolex135/sb_dba.git```

#### 5. Go to cloned directory
```cd sb_dba ```

#### 6. Change Vagrantfile-virtualbox to Vagrantfile and also original Vagrantfile to something else
```mv Vagrantfile Vagrantfile-arm && mv Vagrantfile-virtualbox Vagrantfile```

#### 7. Build and provision machines defined in Vagrantfile
```vagrant up```

#### 8. SSH into ansibleserver that was built with Vagrant
```vagrant ssh ansibleserver```

#### 9. Run plabook from ansibleserver to setup database server
```ansible-playbook dbserver.yaml```

#### 10. Run plabook from ansibleserver to setup app server
```ansible-playbook appserver.yaml```