# Initial setup of server

## Install ubuntu 20.4 LTS

- manual <https://downloads.dell.com/manuals/all-products/esuprt_ser_stor_net/esuprt_poweredge/poweredge-t110-2_owner%27s%20manual_en-us.pdf>
- had to enable usb ports and ethernet from system setup
- kept bios, uefi made grub come up

## Install openssh-server

- guide <https://help.ubuntu.com/community/SSH/OpenSSH/Configuring>

```bash
sudo apt install openssh-server
```

- edited `/etc/ssh/sshd_config` to disable password login

- set up key with my solokey `ssh-keygen -t ecdsa-sk -C $(date +'%d-%m-%Y')-solo-red`
- copied pub key to `~/.ssh/authorized-keys`
- restarted sshd `sudo systemctl restart ssh`
