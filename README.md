# Evaluation

```shell
# What is AppArmor?
Restricts the actions of applications (Mandatory Access Control)

# UFW status
sudo ufw status

# SSH status
sudo systemctl status ssh

# Check OS
uname -a

# Check that agenow belongs to sudo and user42
sudo groups agenow

# Create a new user
sudo adduser [name]
	sudo deluser [name]
sudo groupadd [name]
	getent group [name1] [name2] ...
	groups [name (of user)]
	sudo groupdel [name]
sudo usermod -aG group1,group2 username

# Password Policy
passwd # to change pwd

sudo vim /etc/pam.d/common-password
# (retries for meeting requisites), minimal length, uppercase, lowercase, digits, maximal consecutive repetitions, no username in passw, use these rules for root too! difference ok -> 7 characters must differ

# PASS_MAX_DAYS, PASS_MIN_DAYS and PASS_WARN_AGE
sudo vim /etc/login.defs
# for one user is
sudo chage -m 2 -M 30 -W 7 username
chage -l [username] # list user password expirey info

# Show and change hostname
hostname
sudo hostname [new name] # temporary
sudo vim /etc/hostname # permanent # 1/2
sudo hostnamectl set-hostname [new name] # permanent # 2/2

# Partitions
lsblk # lvm control, security, flexibility

# sudo
sudo -V
sudo usermod -aG group1,group2 username
sudo visudo
ls /var/log/sudo
cat /var/log/sudo/sudo.log

# ufw
sudo ufw version
sudo ufw status
sudo ufw allow 8080
sudo ufw status numbered
sudo ufw delete [num]

# ssh 14242 - 4242
ssh -V

# script
sudo vim /usr/local/bin/monitoring.sh
sudo crontab -e
```
