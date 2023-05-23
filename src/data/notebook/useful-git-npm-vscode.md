---
title: "Useful: Git, NPM, VSCode"
publishDate: 23 May 2023
description: Useful and or interesting commands for git, npm and vscode.
tags: ['useful', 'cli', 'git', 'npm', 'vscode']
---

- [Git](#git)
- [NPM](#npm)
- [VSCode](#vscode)

## Git
```shell
git checkout - # checkout the last branch you were on
```

```shell
npm install -g degit
```

```shell
git remote add origin https://github.com/<YOUR-ACCOUNT>/<YOUR-REPO>
git branch -M master
git push -u origin master
```

## NPM
```shell
# Time stats on start up
Measure-command {npm start}

# Add scripts in package.json
npm pkg set scripts.dev='nodemon index.js --port 8000'
npm pkg set scripts.format='prettier --write "**/*.{js,jsx,ts,tsx}"'
```

## VSCode
```shell
# List all extensions installed on you local VSCode instance 
code --list-extensions | xargs -L 1 echo code --install-extension
```

