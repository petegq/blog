---
title: "Useful: Shell, etc"
publishDate: 25 May 2023
description: Useful and or interesting commands for bash, shell and related.
tags: ['useful', 'cli', 'shell', 'bash', 'packer', 'linode']
---

## Shell
```shell
ls -a # list contents with file information
la # la == ls -a ? (...perhaps theres... no, no alias in .zshrc)
```

```shell
tree <dir> # Tree search and print you target <dir> contents
	tree node_modules
	tree . # Current directory

tree -I <excluded> # Tree search and print you current dir, except that which you want <excluded> i.e:
	tree -I node_modules
	tree -I 'node_modules|cache|test_*'
```

```shell
rm -rf <dir> # Delete the <dir> its contents and sub-folders i.e:
	rm -rf node_modules

rm -rf */<dir> # All <dir> in all folders below the current i.e:
	rm -rf */node_modules
```

```shell
which <executable> # find location of <executable>
```

```shell
!!      # Redo last command
sudo !! # Redo last command with sudo

cd      # home
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
