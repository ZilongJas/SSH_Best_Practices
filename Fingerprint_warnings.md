# Fingerprints
- Whenever we try to connect to a remote server and get a fingerprint warning it COULD mean we might have a connection to the wrong server, and we might be a victim of a man-in-the-middle attack.
- https://en.wikipedia.org/wiki/Man-in-the-middle_attack
___
If we have access to the main server, we can check if the fingerprint is correct before remote connecting.
- `ssh-keygen -E sha256 -lf /etc/ssh/ssh_host_ed25519_key.pub`
  - check the fingerprint on the server side
