# Setting up and using gnuPG / GPG
## Basic Usage
### Packages
- gnupg2
- pinentry-curses

### Useful comands
```
gpg2 --full-gen-key
gpg2 --key-gen # just prompts for name
gpg2 --list-keys
gpg2 --list-secret-keys
```

### Creating key
```
gpg2 --full-gen-key
Please select what kind of key you want:
   (1) RSA and RSA (default)
   (2) DSA and Elgamal
   (3) DSA (sign only)
   (4) RSA (sign only)
Your selection? 4

What keysize do you want? (2048) 4096

Please specify how long the key should be valid.
Key is valid for? (0) 1m # 1 month
Is this correct? (y/N) y

Real name: Jacob Sohl
Email address: jacobsohl@gmail.com
Comment: 
You selected this USER-ID:
    "Jacob Sohl <jacobsohl@gmail.com>"

Change (N)ame, (C)omment, (E)mail or (O)kay/(Q)uit? O
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
#### No Pinentry
```
gpg2 --gen-key
<snip>
gpg: agent_genkey failed: No pinentry
Key generation failed: No pinentry
```
*Resolution:* Install pinentry-curses


# (WIP: YubiKey)
## References
https://occamy.chemistry.jhu.edu/references/pubsoft/YubikeySSH/index.php

https://www.jfry.me/articles/2015/gpg-smartcard/

## HowTo
### Generate key on air-gapped system
### Put Key on YubiKey
### Set up GPG->SSH
