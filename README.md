# DynamiComponent

## Build Setup

```bash
# install dependencies
$ yarn install

# serve with hot reload at localhost:3000
$ yarn dev

# build for production and launch server
$ yarn build
$ yarn start

# generate static project
$ yarn generate
```
### Demo Information

All the steps in the demo are in different branch, if you are lost at some point, check the branch with :

```bash
git branch -r
```

# Useful Link

## Webpack dynamic imports

**Summary** : Importing the components dynamically, we are isolating the given component which will be added to the dependency graph and it'll will be downloaded but only when it's required.

[More information](https://vueschool.io/articles/vuejs-tutorials/lazy-loading-and-code-splitting-in-vue-js/)


## Vue.js dynamic components

**Summary** : The tag `<component :is="aComponent" />` enables the user to pass component dynamically or even switch between them.

[More information](https://fr.vuejs.org/v2/guide/components.html#Composants-dynamiques)

[Even More information :)](https://fr.vuejs.org/v2/guide/components-dynamic-async.html)