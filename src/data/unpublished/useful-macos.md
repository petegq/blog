---
title: "Useful: MacOS"
publishDate: ?
description: Useful and or interesting commands for MacOS, zsh, etc.
tags: ['useful', 'cli', 'macos', 'zsh']
---

## XCode Command-Line Tools
**Install**
```shell
xcode-select --install
```

**Check for updates** *(not just for xcode of course)*
```shell
softwareupdate --list
```
*Example output:*
```shell
Finding available software
Software Update found the following new or updated software:
* Label: Command Line Tools for Xcode-14.2
	Title: Command Line Tools for Xcode, Version: 14.2, Size: 687573KiB, Recommended: YES,
# ...
# ...
```

**Install all**
```shell
softwareupdate --install -a
```

**Install a single update**
```shell
softwareupdate --install '<product label>'
```
*... using the exact label from the --list output above , spaces and all!*
```shell
softwareupdate --install 'Command Line Tools for Xcode-14.2'
```

**Sometimes, its better to burn it with fire and install again**
```shell
sudo rm -rf /Library/Developer/CommandLineTools
xcode-select --install
```
