# vue3.x_Beta

vue3.x_Beta，基于[vue-cli](https://cli.vuejs.org/zh/)，参考[Composition API](https://vue-composition-api-rfc.netlify.app/)搭建。


## 项目搭建步骤
```
安装 vue-cli3
npm install -g @vue/cli
# OR
yarn global add @vue/cli
```
```
创建项目
vue create my-project
# OR
vue ui
```
```
在项目中安装 composition-api 体验 vue3 新特性

npm install @vue/composition-api --save
# OR
yarn add @vue/composition-api
```

```
在使用任何 @vue/composition-api 提供的能力前，必须先通过 Vue.use() 进行安装

import Vue from 'vue'
import VueCompositionApi from '@vue/composition-api'

Vue.use(VueCompositionApi)
```

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run dev
```

### Compiles and minifies for production
```
npm run build
```

### Lints and fixes files
```
npm run lint
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).
