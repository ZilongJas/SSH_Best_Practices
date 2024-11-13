in `/etc/ssh/sshd_config`

add in `AllowUsers [username]` on a new line if it does not exist already

___ 
`sudo sshd -t`

`sudo systemctl restart sshd`
