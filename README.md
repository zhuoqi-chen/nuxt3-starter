# Nuxt 3 Starter

# 工程搭建日志

### [Eslint](https://github.com/nuxt/eslint-config) setup with Typescript

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

### [Prettier](https://prettier.io/docs/en/integrating-with-linters.html) setup

```bash
yarn add -D prettier eslint-config-prettier eslint-plugin-prettier eslint-plugin-nuxt
```

`.eslintrc` configuration

```js
{
  "extends": [
    ...,
    "plugin:nuxt/recommended",
    "plugin:prettier/recommended",
  ]
}
```

`.prettierrc` configuration

```json
{
  "tabWidth": 2,
  "useTabs": false,
  "semi": true,
  "singleQuote": true,
  "jsxBracketSameLine": true,
  "maxLength": 80,
  "trailingComma": "es5"
}
```

### [tailwindcss](https://tailwindcss.com/docs/guides/nuxtjs) setup

```bash
yarn add -D @nuxtjs/tailwindcss
```

`nuxt.config.ts` configuration

```ts
export default defineNuxtConfig({
  modules: ['@nuxtjs/tailwindcss'],
});
```

### [pinia](https://pinia.vuejs.org/) setup

```bash
yarn add pinia @pinia/nuxt
```

`nuxt.config.ts` configuration

```ts
export default defineNuxtConfig({
  modules: [..., '@pinia/nuxt'],
});

```
