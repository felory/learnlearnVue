# need to know
vue create appname
npm run serve

Follow vedio  to learn:
https://www.bilibili.com/video/BV1Vf4y1T7bw?p=5

* 配置运行自动打开:
1、package.json 配置npm serve --open
2、vue.config.js 配置devServer 指定host

##
### constructor
* public文件夹（存放静态资源）会原封不动直接打包到dist中。
而src/assets里的静态资源，会被打包成一个module到js文件里。

* components一般放非路由组件。(.vue)(react中是jsx)(ag中是ts)。

* App.vue是唯一的根组件。
<template></template>
<script></script>
<style></style>

* main.js 是程序的入口文件。==》引入根组件，并挂载到#app（public/index.html里）。

* babel.config.js（es6==>es5)

* package.json记录项目依赖、怎么运行。
package-lock.json 缓存依赖


### 关闭语法检测eslint：
若声明变量却未使用，如果校验打开，会直接报错。
vue.config.js中 lintOnSave: false,

### 配置文件夹别名
jsconfig.json中 compilerOptions
    "paths": {
      "@/*": [
        "src/*"
      ]

### 浏览器不识别less样式，通过less, less-loader ==> css
1.npm install --save less less-loader
2.组件识别less: <style lang="less">


## Route
划分页面：header/content/footer
路由改变：只改变中间的content。#/home, #/search, #/login, #/register,
非路由组件:共用头足。
### 1.完成非路由组件
header在所有页面都有。
footer在login,register页面没有。


## ts
* 安装 
npm  install -g typescript
tsc -v
* 1.使用ts自动编译：
tsc --init 会生成tsconfig.json配置文件。
在tsconfig中outDir: "./js" //即是把ts编译后放在/js目录下。









