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
