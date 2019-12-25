# SSH setup

1. Check to see if there is already ssh key

```
    ls -al ~/.ssh
```

2. Create keys using this command

```
    ssh-keygen -t rsa -b 4096 -C "ashwin.achu.1311@gmail.com"
    -t rsa : Specifies the type of key to create. The possible values are “rsa1” for protocol version 1 and “dsa”, “ecdsa”, “ed25519”, or “rsa” for protocol version 2.
    -b 4096 : Specifies the number of bits in the key to create
    -f ~/.ssh/github.key : Specifies the filename of the key file.(for new file name give from root path in format mentioned)
    -C for comment.
```

## or you can just use ssh keygen command to create

3. Start the ssh-agent in the background

```
    eval "$(ssh-agent -s)"
```

4. Add your SSH private key to the ssh-agent.

```
    ssh-add ~/.ssh/github.key
```

5. copy the key content

```
    cat ~/.ssh/github.key.pub
```

6. Open scm portal and add ssh key to ssh option from profile.

7. Try cloning ssh git link and first time it will prompt for passphrase if you assigned then it will be cloned successfully.
