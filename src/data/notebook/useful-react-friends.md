---
title: "Useful: React & Friends"
publishDate: 29 Jul 2023
description: Useful and or interesting commands for React, Next, etc.
tags: ['useful', 'cli', 'react', 'next', 'vite', 'prettier']
---

## React and friends

### Create Vite...
create-react-app is dead... long live vite!
```shell
npm create vite@latest <app-name> -- --template react
```
*Vite (npm 7+, extra double-dash is needed)*

### Create next app
`npx create-next-app <app-name> <options> --example <example>`
```shell
npx create-next-app <app-name> --js --eslint --use-npm -e <example>
```

```shell
# Options:
--js, --javascript # Initialize as a JavaScript project
--no-tailwind # Initialize without Tailwind CSS config.
--eslint # Initialize with ESLint config.
--experimental-app # Initialize as a 'app/' directory project.
--src-dir # Initialize inside a 'src/' directory.
--import-alias <alias> # Specify import alias to use (default "@/*").
--use-npm # Explicitly tell the CLI to bootstrap the app using npm
-e, --example # Example i.e. '-e auth0' or '-e [name]|[github-url'
```

A couple of perhaps useful starter examples
```shell
npx create-next-app gitnotes --js --eslint --use-npm -e with-electron with-electron-app
```
```shell
npx create-next-app blog --js --eslint --use-npm -egithub-pages nextjs-github-pages
```

### Prettier 
*... dont judge*
```shell
wget https://raw.githubusercontent.com/petegq/config/master/.prettierignore
```
```shell
wget https://raw.githubusercontent.com/petegq/config/master/.prettierrc
```
```shell
"format": "prettier --write '**/*.{js,jsx,ts,tsx}'"
```

