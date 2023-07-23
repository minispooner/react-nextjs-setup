# React NextJS Web App

## Install Node
1. `brew install nvm`
2. `mkdir ~/.nvm`
3. Add this to `~/.bash_profile` and then `source ~/.bash_profile`

```
export NVM_DIR="$HOME/.nvm"
[ -s "/opt/homebrew/opt/nvm/nvm.sh" ] && \. "/opt/homebrew/opt/nvm/nvm.sh"  # This loads nvm
[ -s "/opt/homebrew/opt/nvm/etc/bash_completion.d/nvm" ] && \. "/opt/homebrew/opt/nvm/etc/bash_completion.d/nvm"  # This loads nvm bash_completion
```

4. `nvm install 18` to install Node v18
5. `nvm use 18`
6. `nvm alias default 18` # set Node v18 as default for all projects

## Install NextJS
1. `npx create-next-app@latest`
 - typescript: yes; eslint: yes; tailwind: yes; src directory: yes; app router: yes; customize default import alias: no

## Linters and Pretty Printers Setup

1. `npm i prettier-plugin-tailwindcss --save-dev`
2. `npm install --save-dev --save-exact prettier eslint-config-prettier`
   1. \[optional\] Add `prettier . --check` to CI (fails if not formatted)
3. Pre-commit hook: Install `npx mrm@2 lint-staged` (see prettier [docs](https://prettier.io/docs/en/precommit.html) for more info) to run prettier on git commit
4. Add this into settings json of VS Code (page+arrow icon at top right):
```
"[typescriptreact]": {
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  }
```
5. `npx prettier . --write` to run prettier over all files

## To Run
`npm run dev` to serve at localhost:3000

## Helpers
VS Code install extensions
- Typescript (Microsoft's JS/TS helper). Typescript syntax herlpers.
- ESLint (orange ball). ES Linting.
- Prettier 34.4m install at top. Pretty print formatter.
- Tailwind CSS IntelliSense. Shows valid classes as you type.
- VS Code Settings > Format on Save > Check it
