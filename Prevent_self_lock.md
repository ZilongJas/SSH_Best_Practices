Let's imagine this, we are a system admin working remotely connected to a machine using ssh, and we disable the ssh connection with `sudo systemctl stop sshd` when testing. Although we won't be kicked off right away, but if our internet connection goes down or we open a new terminal or close our current one, we just locked ourselfs out.

1. If you do plan on disabling ssh on the remote machine while remote, at least always keep a open terminal of the connected machine. 
