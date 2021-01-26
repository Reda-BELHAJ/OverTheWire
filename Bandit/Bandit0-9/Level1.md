# Bandit Level 1

Enter the following command in your Terminal :  

```bash
ls -la
# List  information  about  the  FILEs with the author of each file and also without ignoring entries (files) starting with .
```
```bash
cat readme
# Concatenate files and print on the standard output
```
```bash
realpath readme
# Return the canonicalised absolute pathname 
```

```bash
scp -P 2220 bandit0@bandit.labs.overthewire.org:/home/bandit0/readme <LocalMachinePATH>
# <LocalMachinePATH> : your temporary file to copy the ascii text
# Password           : bandit0
```
We are using realpath and [scp commands](https://linuxize.com/post/how-to-use-scp-command-to-securely-transfer-files/) to copy ***readme*** file from OTW server to our Machine, and using it for the next Level.
