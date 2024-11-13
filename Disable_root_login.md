- in `/etc/ssh/sshd_config` search for permitrootlogin

- change `#PermitRootLogin prohibit-password` to `PermitRootLogin no` so that root login is not possible

- `sudo ssh -t` check for errors in the sshd-config file

- `sudo systemctl restart sshd` 
