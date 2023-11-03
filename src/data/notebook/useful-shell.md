---
title: "Useful: Shell, etc"
publishDate: 25 May 2023
description: Useful and or interesting commands for bash, shell and related.
tags: ['useful', 'cli', 'shell', 'bash', 'packer', 'linode']
---

## Shell

### list contents with file information
```shell
ls -a
```

# la == ls -a ? (...perhaps theres... can't find an alias anywhere)
```shell
la
```

### Tree search and print you target <dir> contents "tree <dir>"
```shell
tree node_modules
```
or for current dir
```shell
tree . 
```

### Tree search and print you current dir, except that which you want <excluded> i.e: "tree -I <excluded> 
```shell
tree -I node_modules
```
or
```shell
tree -I 'node_modules|cache|test_*'
```


### Delete the <dir> its contents and sub-folders i.e: "rm -rf <dir>" 
```shell
rm -rf node_modules
```

### All <dir> in all folders below the current i.e: "rm -rf */<dir>" 
```shell
rm -rf */node_modules
```

### Find location of <executable>
```shell
which <executable> 
```

### Redo last command
```shell
!!
```

### Redo last command with sudo
```shell
sudo !! 
```

### home
```shell
cd      
```

### back to the last dir you came format
```shell
cd -    
```

## Grep

### Lines not containing "pattern" (inverse grep)
```shell
grep -v "pattern" file.txt
```

### Lines that contain a word ending with "word":
```shell
grep -w '[^ ]*word' file.txt
```

### Lines containing the word "word":
```shell
grep -w 'word' file.txt
```

### Lines beginning with "one" and containing "two"
```shell
grep '^one.*two' file.txt
```

### Lines that end with "end"
```shell
grep 'end$' file.txt
```

## Packer
```shell
packer build -var-file=variables.json linode-example.json
```

## Linode

### Get all available images from Linode
```shell
curl -H "Authorization: Bearer $LINODE_TOKEN" https://api.linode.com/v4/images
```

## Unsorted

```shell
uname -m # x86_64 or 32?
```

```shell
curl -v --trace out.txt http://google.com
```

### Redo last command but as root
```shell
sudo !!
```

### Open an editor to run a command
```shell
ctrl+x+e
```

### Create a super fast ram disk
```shell
mkdir -p /mnt/ram
mount -t tmpfs tmpfs /mnt/ram -o size=8192M
```

### Don't add command to history (note the leading space)
```shell
ls -l
```

### Fix a really long command that you messed up
```shell
fc
```

### Tunnel with ssh (local port 3337 -> remote host's 127.0.0.1 on port 6379)
```shell
ssh -L 3337:127.0.0.1:6379 root@emkc.org -N
```

### Quickly create folders
```shell
mkdir -p folder/{sub1,sub2}/{sub1,sub2,sub3}
```

### Intercept stdout and log to file
```shell
cat file | tee -a log | cat > /dev/null
```

### Exit terminal but leave all processes running
```shell
disown -a && exit
```
