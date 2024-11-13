SCP (Secure Copy Protocol) is a command-line tool for securely transferring files between a local machine and a remote server, or between two remote servers. It uses SSH (Secure Shell) to encrypt the transfer, ensuring the data is secure in transit.

- `scp file.txt user@remote_host:/path/to/destination`
  - Copy a file from local to remote
- `scp user@remote_host:/path/to/file.txt /local/path`
  - Copy a file from remote to local
- `scp -r /local/directory user@remote_host:/remote/directory`
  - Copy a directory (with -r flag for recursion)
- `-P [port]` captial P for different ports
___
For Windows/Mac
- https://cyberduck.io/
