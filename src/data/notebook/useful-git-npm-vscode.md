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

Checkout the last branch you were on
```shell
git checkout -
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

Time stats on start up
```shell
Measure-command {npm start}
```

Add scripts in package.json
```shell
npm pkg set scripts.dev='nodemon index.js --port 8000'
npm pkg set scripts.format='prettier --write "**/*.{js,jsx,ts,tsx}"'
```

## VSCode

List all extensions installed on you local VSCode instance
```shell 
code --list-extensions | xargs -L 1 echo code --install-extension
```

