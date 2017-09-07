# manage-web

> A Vue.js project

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

For detailed explanation on how things work, checkout the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).


删除node_modules文件，运行npm(cnpm) install和npm run

**引入Element**
1.打开cmd，在当前目录中运行：npm i element-ui -S

2.src/main.js（红色的）
````
// The Vue build version to load with the `import` command
// (runtime-only or standalone) has been set in webpack.base.conf with an alias.
import Vue from 'vue'
import App from './App'
import router from './router'
/* 新增两行 */
import ElementUI from 'element-ui'
import 'element-ui/lib/theme-default/index.css'

Vue.config.productionTip = false

/* 新增一行 */
Vue.use(ElementUI)

new Vue({  
    el: '#app',  
    router,  
        template: '<App/>', 
components: { App }
})
````
**3.然后在.vue文件里就直接可以用了**
例如：在**src/components/Hello.vue**做一下修改
````
<template>  
  <div class="hello">  
    <h1>{{ msg }}</h1>  
    <h2>Essential Links</h2>  
    <el-button>默认按钮</el-button>  
    <el-button type="primary">主要按钮</el-button>  
    <el-button type="text">文字按钮</el-button>  
  </div>  
</template>  
