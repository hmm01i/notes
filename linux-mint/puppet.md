# Using puppet to manage a Mint Workstation (eg. laptop, desktop)

## Packages
- puppet-agent
- librarian-puppet-simple

## Control repo
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
