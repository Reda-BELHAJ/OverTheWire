# Bandit Level 17
## Part I
```bash
    ssh -i rsakey_private bandit17@localhost
    # Paste the password 
    # Correct!
    # -----BEGIN RSA PRIVATE KEY-----
    # ...
    # -----END RSA PRIVATE KEY-----
```
And copy the text to your clipboard (or try [the scp Method](https://github.com/Reda-BELHAJ/OverTheWire/blob/main/Bandit/Bandit0-9/Level1.md#part-i))

```bash
    mkdir /tmp/reda2
    cd /tmp/reda2
    touch rsakey_private
    vim rsakey_private
    # Paste [ESC] and type :wq to save and quit
    chmod 600 rsakey_private
    ssh -i rsakey_private bandit17@localhost
```
