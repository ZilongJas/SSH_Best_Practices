Instead of a password, we use a public/private key

We will be generating a key pair
  - Private key: never share
  - Public key: could share, used to verify our private key
___
We generate a key on our client, not on the server machine.
`ssh-keygen -t rsa -b 4096`
  - uses rsa algorithm
  - uses 4096 bits long key length (default is 2048)
  - Private key will be saved in ~/.ssh/id_rsa
  - Public key will be saved in ~/.ssh/id_rsa.pub
___
- Transfer the public key into `~/.ssh/authorized_keys` on remote server manually
- `chmod 700 ~/.ssh`
- `chmod 600 ~/.ssh/authorized_keys`
___
- or use `ssh-copy-id -i ~/.ssh/id_rsa.pub user@server` for automatic transfer and permission setups


