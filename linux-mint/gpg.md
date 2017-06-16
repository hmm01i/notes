# Setting up and using gnuPG / GPG
## Basic Usage
### Packages
gnupg2


### Useful comands
```
gpg2 --key-gen
gpg2 --list-keys
```

## Smart Card support (eg YubiKey)
### Additional Packages
- pcscd
- pcsc-tools
- scdaemon
- monkeysphere

### Services
- pcscd
- scdaemon

### Commands
```
gpg2 --card-status
gpg2 --card-edit
```

### Common Error messages
(wip)

# (WIP: YubiKey)
## References
https://occamy.chemistry.jhu.edu/references/pubsoft/YubikeySSH/index.php

https://www.jfry.me/articles/2015/gpg-smartcard/

## HowTo
### Generate key on air-gapped system
### Put Key on YubiKey
### Set up GPG->SSH
