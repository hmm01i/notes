# Using ansible with Linux mint workstation

## Installing
```
sudo apt-add-repository ppa:ansible/ansible
sudo apt-get update
sudo apt-get install ansible
```

## Setting up hosts file
```
vim /etc/ansible/hosts
```

## Variables for BSD
```
[freebsd:vars]
ansible_python_interpreter=/usr/local/bin/python2.7
```
