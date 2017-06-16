# general commands run to bootstrap a freenas jail for puppet management
## Packages
[FreeBSD package management](https://www.freebsd.org/doc/en_US.ISO8859-1/books/handbook/pkgng-intro.html)
[Package DB - freshports.org](http://www.freshports.org/)

## Example: Installing puppet
```
pkg update
pkg install puppet4
```


## Using ports
[FreeBSD Ports](https://www.freebsd.org/doc/en_US.ISO8859-1/books/handbook/ports-using.html)

## Setting up SUDO
Install package
```
pkg install sudo
```

Create rule in /usr/local/etc/sudoers.d/wheel
```
%wheel ALL= NOPASSWD: ALL
```
