# Debian Security Notes


## Automatic updates
* apt install unattended-upgrades
* dpkg-reconfigure --priority=low unattended-upgrades

## Non-root user
* adduser [user] 
* usermod -aG sudo [user]

## Keys
* mkdir ~/.ssh
* chmod 700 ~/.ssh
* ssh-keygen -b [4096]
* ssh-copy-id [user]@[ip]  

## Harden SSH
* sudo nano /etc/ssh/sshd_config
    `Port [22]`
    `AddressFamily [inet]`
    `PermitRootLogin [no]`
    `PasswordAuthentication [no]`

## Firewall
* sudo apt install ufw
* sudo ufw allow [port]
* sudo ufw enable
* sudo ufw status
### List network connections
 * sudo ss -tupln
### Disable pings
* sudo nano /etc/ufw/before.rules
    `-A ufw-before-input -p icmp --icmp-type echo-request -j DROP`
* reboot
