---
title: "Useful: Shell, etc"
publishDate: 25 May 2023
description: Useful and or interesting commands for bash, shell and related.
tags: ['useful', 'cli', 'shell', 'bash', 'packer', 'linode']
---

## Shell
```shell
# list contents with file information
ls -a
```
```shell
# la == ls -a ? (...perhaps theres... can't find an alias anywhere)
la
```

```shell
# Tree search and print you target <dir> contents
tree <dir> 
	tree node_modules
	# Current directory
	tree . 

# Tree search and print you current dir, except that which you want <excluded> i.e:
tree -I <excluded> 
	tree -I node_modules
	tree -I 'node_modules|cache|test_*'
```

```shell
# Delete the <dir> its contents and sub-folders i.e:
rm -rf <dir> 
	rm -rf node_modules

# All <dir> in all folders below the current i.e:
rm -rf */<dir> 
	rm -rf */node_modules
```

```shell
# find location of <executable>
which <executable> 
```

```shell
# Redo last command
!!
```
```shell
# Redo last command with sudo
sudo !! 
```

```shell
# home
cd      
cd -    # back to the last dir you came from
```

## Unsorted
```shell
uname -m # x86_64 or 32?

curl -v --trace out.txt http://google.com

# Redo last command but as root
sudo !!

# Open an editor to run a command
ctrl+x+e

# Create a super fast ram disk
mkdir -p /mnt/ram
mount -t tmpfs tmpfs /mnt/ram -o size=8192M

# Don't add command to history (note the leading space)
ls -l

# Fix a really long command that you messed up
fc

# Tunnel with ssh (local port 3337 -> remote host's 127.0.0.1 on port 6379)
ssh -L 3337:127.0.0.1:6379 root@emkc.org -N

# Quickly create folders
mkdir -p folder/{sub1,sub2}/{sub1,sub2,sub3}

# Intercept stdout and log to file
cat file | tee -a log | cat > /dev/null

# Exit terminal but leave all processes running
disown -a && exit

# Grep lines not containing "pattern" (inverse grep)
grep -v "pattern" file.txt
```

## Packer
```shell
packer build -var-file=variables.json linode-example.json
```

## Linode
```shell
# Get all available images from Linode
curl -H "Authorization: Bearer $LINODE_TOKEN" https://api.linode.com/v4/images
```
