# Nuxt 3 Starter

# 工程搭建日志

### [Eslint](https://github.com/nuxt/eslint-config) Setup with Typescript

```bash
yarn add -D @nuxtjs/eslint-config-typescript eslint
```

`.eslintrc` configuration

```json
{
  "extends": ["@nuxtjs/eslint-config-typescript"]
}
```

`.vscode/settings.json` configuration

```json
  "[javascript]": {
    "editor.defaultFormatter": "dbaeumer.vscode-eslint"
  },
  "[typescript]": {
    "editor.defaultFormatter": "dbaeumer.vscode-eslint"
  },
  "[vue]": {
    "editor.defaultFormatter": "dbaeumer.vscode-eslint"
  },
  "editor.codeActionsOnSave": {
    "source.fixAll": false,
    "source.fixAll.eslint": true
  },
```

### husky & lint-staged

```
yarn add -D husky lint-staged typescript
```
`package.json` configuration

```json
"scripts": {
  "prepare": "husky install"
},
"lint-staged": {
  "**/*.{js,ts,vue}": [
    "npm run lint:fix"
  ]
}
```
```bash
npm run prepare
npx husky add .husky/pre-commit "npx --no-install lint-staged"
```
