After setting up private/public key, disable password login.

- sudo nano `/etc/ssh/sshd_config`
- `PasswordAuthentication no`
___
- `sudo shd -t`
- `systemctl restart sshd`
