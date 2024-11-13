Configure keep-live packets on client side

![Screenshot from 2024-11-13 08-08-53](https://github.com/user-attachments/assets/26f4be5b-9ef4-49f1-9e67-d209bf3dec69)
in `~/.ssh/config`
- `chmod 600 ~/.ssh/config`
  - principle of least privilege
- sends an empty packet every 60 seconds to keep connection open
- allow up to 3 of those packets to fail, and the connection will reman open
