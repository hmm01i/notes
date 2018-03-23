# Using puppet to manage a Mint Workstation (eg. laptop, desktop)

## Packages
Puppet Collection apt repo

`https://apt.puppetlabs.com/puppetlabs-release-pc1-xenial.deb`

Packages
- puppet-agent
- librarian-puppet-simple

## Control git repo

As root
```
mkdir -p /etc/facter/facts.d/
echo 'role=workstation' > /etc/facter/facts.d/role.txt
cd /etc/puppetlabs/code/environments/
rm -rf production
git clone https://github.com/hmm01i/puppet-ctrl.git production
cd /etc/puppetlabs/code/environments/production/
librarian-puppet install
```

##
