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

[freebsd]
freenas ansible_host=192.168.1.10
```

## Variables for BSD
```
[freebsd:vars]
ansible_python_interpreter=/usr/local/bin/python2.7
```

## Example ansible commands
```
ansible all -m ping
ansible freebsd -m ping
ansible <host> -a "/bin/echo hello"
```
