# SSH How-To's

```
$ cd ~/.ssh
```

Navigate to the SSH directory

```
$ ssh-keygen -t rsa -b 4096 -C "mstrblonde@gmail.com"
```

Generate an SSH key in the current directory (should be ~/.ssh) of 4096 bits of type rsa using an email address.

```
$ cat REPONAME.pub
```

Show the contents of the key file

```
$ eval $(ssh-agent -s)
```

Start the SSH agent in the background.

```
$ ssh-add ~/.ssh/KEYNAME
```

Add the new private key to the SSH agent.
