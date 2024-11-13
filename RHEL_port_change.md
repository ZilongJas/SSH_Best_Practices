For added security on RHEL (changing from the default ssh port 22 to something else)
___
- `sudo dnf install openssh-server`
  - installs the ssh server

- `systemctl status sshd`
  - check the ssh status, if sshd does not work try ssh

- `systemctl enable sshd`
  - enable ssh connections

- `sudo dnf install policycoreutils`
  - a package that provides utilities for managing SELinux policies (semanage, restorecon, setfiles)

- `semanage port -a -t ssh_port_t -p tcp [custom_ssh_port]`
  - tells SELinux to allow SSH daemon to use a custom port for connections

- `sudo firewall-cmd --add-port=[custom_ssh_port]/tcp --permanent`
  - allows the firewall to let incoming SSH traffic through a custom port
  - since on RHEL, firewall are automaically enabled by default, on ubuntu it is disabled by default

- `sudo firewall-cmd --reload`
  - reloads the firewall config

- `sudo nano /etc/ssh/sshd_config`
  - uncomment SSH and edit the desired custom port
 
- `sudo systemctl restart ssh`
  - final restart to apply changes
___
### Remove the default port 22 for SSH
- `sudo firewall-cmd --remove-service=ssh --permanent`
  - `sudo firewall-cmd --reload` reload 
