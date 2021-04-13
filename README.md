# Bidding :

## Cli Setup :

```sh
---------------------------------
# project init:

$ npx create-nuxt-app bidding

create-nuxt-app v3.6.0
✨  Generating Nuxt.js project in bidding
? Project name: bidding
? Programming language: TypeScript
? Package manager: Npm
? UI framework: Vuetify.js
? Nuxt.js modules: Axios - Promise based HTTP client, Progressive Web App (PWA)
? Linting tools: ESLint, Prettier, Lint staged files, StyleLint, Commitlint
? Testing framework: Jest
? Rendering mode: Universal (SSR / SSG)
? Deployment target: Server (Node.js hosting)
? Development tools: (Press <space> to select, <a> to toggle all, <i> to invert selection)
? Continuous integration: GitHub Actions (GitHub only)
? What is your GitHub username? varaisyssaras
? Version control system: Git

```

## Build Setup :

```bash
---------------------------------
# install dependencies:

$ npm install

# format and lint:

$ npm run format
$ npm run lint

# serve with hot reload at localhost:3000:

$ npm run dev

# build for production and launch server:

$ npm run build
$ npm run start

# generate static project:

$ npm run generate

```

For detailed explanation on how things work, check out [Nuxt.js docs](https://nuxtjs.org).

## Vuetify Offline mode :

```sh
---------------------------------
# Online mode:

- https://cdn.jsdelivr.net/npm/@mdi/font@latest/fonts/materialdesignicons-webfont.woff2?v=5.9.55
- https://fonts.googleapis.com/css?family=Roboto:100,300,400,500,700,900&display=swap

# Offline mode:

- https://github.com/nuxt-community/vuetify-module#defaultassets
- https://github.com/nuxt-community/vuetify-module#offline-applications
- https://google-webfonts-helper.herokuapp.com/fonts/roboto?subsets=latin
- https://stackoverflow.com/questions/64206283/how-to-import-the-mdi-icons-module-inside-nuxt-config-js-in-nuxt

```

# package.json :

```js
{
  "name": "bidding",
  "version": "1.0.0",
  "private": true,
  "scripts": {
    "dev": "nuxt",
    "build": "nuxt build",
    "start": "nuxt start",
    "generate": "nuxt generate",
    "lint:js": "eslint --ext \".js,.vue\" --ignore-path .gitignore .",
    "lint:style": "stylelint \"**/*.{vue,css}\" --ignore-path .gitignore",
    "lint": "npm run lint:js && npm run lint:style",
    "test": "jest",
    "format": "prettier \"**/*.{js,vue,css,md}\" --write"
  },
  "lint-staged": {
    "*.{js,vue}": "eslint",
    "*.{css,vue}": "stylelint"
  },
  "husky": {
    "hooks": {
      "commit-msg": "commitlint -E HUSKY_GIT_PARAMS",
      "pre-commit": "lint-staged"
    }
  },
  "dependencies": {
    "@mdi/font": "^5.9.55", // materialdesignicons
    "@nuxtjs/axios": "^5.13.1",
    "@nuxtjs/pwa": "^3.3.5",
    "core-js": "^3.9.1",
    "nuxt": "^2.15.3"
  },
  "devDependencies": {
    "@commitlint/cli": "^12.0.1",
    "@commitlint/config-conventional": "^12.0.1",
    "@nuxt/types": "^2.15.3",
    "@nuxt/typescript-build": "^2.1.0",
    "@nuxtjs/eslint-config-typescript": "^6.0.0",
    "@nuxtjs/eslint-module": "^3.0.2",
    "@nuxtjs/stylelint-module": "^4.0.0",
    "@nuxtjs/vuetify": "^1.11.3",
    "@vue/test-utils": "^1.1.3",
    "babel-core": "7.0.0-bridge.0",
    "babel-eslint": "^10.1.0",
    "babel-jest": "^26.6.3",
    "eslint": "^7.22.0",
    "eslint-config-prettier": "^8.1.0",
    "eslint-plugin-nuxt": "^2.0.0",
    "eslint-plugin-prettier": "^3.3.1",
    "eslint-plugin-vue": "^7.7.0",
    "husky": "^4.3.8",
    "jest": "^26.6.3",
    "lint-staged": "^10.5.4",
    "prettier": "^2.2.1",
    "stylelint": "^13.12.0",
    "stylelint-config-prettier": "^8.0.2",
    "stylelint-config-standard": "^21.0.0",
    "ts-jest": "^26.5.4",
    "vue-jest": "^3.0.4"
  }
}

```
