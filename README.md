# vue-first

> 安装vuejs的方法

```
sudo npm install -g vue-cli
vue init webpack vue-first-project
```
> vue-first

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

# hello world

- vue.js组件的重要选项-data
```
new Vue({
  data:{
    a:1,
    b:2
  }
  })
```
- vue.js组件的重要选项-methods
- vue.js组件的重要选项-watch

> 数据渲染 v-text v-html {{}}

> 控制模块隐藏 v-if v-show

> 事件绑定 v-on

> v-for 循环渲染

# vue 组件

一个 vue 组件通常就写成一个 .vue 文件，里面内容分三类：

- 模板， template 标签内
- JS 代码， script 标签内
- CSS ，写到 style 标签内

> 每一个 vue 组件中的 <style> 都可以加上 scoped 修饰符，这样，保证了本文件的 css 不会影响其他文件。
