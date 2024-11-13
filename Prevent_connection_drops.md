Configure keep-live packets on client side

![image](https://github.com/user-attachments/assets/95f94c32-3f6d-4db1-bf62-2bb91ca6fb47)

in `~/.ssh/config`
- `chmod 600 ~/.ssh/config`
  - principle of least privilege
- sends an empty packet every 60 seconds to keep connection open
- allow up to 3 of those packets to fail, and the connection will reman open
