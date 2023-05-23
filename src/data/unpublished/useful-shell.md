---
title: "Useful: Shell, etc"
publishDate: ?
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

# 1. redo last command but as root
sudo !!

# 2. open an editor to run a command
ctrl+x+e

# 3. create a super fast ram disk
mkdir -p /mnt/ram
mount -t tmpfs tmpfs /mnt/ram -o size=8192M

# 4. don't add command to history (note the leading space)
 ls -l

# 5. fix a really long command that you messed up
fc

# 6. tunnel with ssh (local port 3337 -> remote host's 127.0.0.1 on port 6379)
ssh -L 3337:127.0.0.1:6379 root@emkc.org -N

# 7. quickly create folders
mkdir -p folder/{sub1,sub2}/{sub1,sub2,sub3}

# 8. intercept stdout and log to file
cat file | tee -a log | cat > /dev/null

# bonus: exit terminal but leave all processes running
disown -a && exit
```

## Todo
```shell
awk(1) # pattern-directed scanning and processing language
sed # stream editor
grep # utility searches any given input files, selecting lines that match one or more patterns (Also: zgrep, zegrep, and zfgrep, egrep, and fgrep, bzgrep, bzegrep, and bzfgrep, act like grep but for compressed formats).

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
