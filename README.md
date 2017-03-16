# 亿账柜官网v2

> 亿账柜官网2.0，基于vue-cli(vue2.X，webpack2.X，sass)多页面开发。

## 说明

项目使用vue-cli官方的webpack脚手架搭建，未加入vue-route。<br>
改造webpack入口实现多页面输出，新增对sass文件的支持。

## 使用命令（脚手架默认）

```bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report

# run unit tests
npm run unit

# run e2e tests
npm run e2e

# run all tests
npm test
```

## 问题收集

1、改造多页面<br>
原理就是改造webpack的入口，参考了下面：<br>
<https://github.com/jarvan4dev/vue-multi-page>

2、chromedriver安装失败<br>
一般是网络问题或是Node.js 内置的 http 对象的get方法无法处理302跳转的情况，解决办法是使用国内阿里源。<br>

```bash
npm install chromedriver --chromedriver_cdnurl=http://cdn.npm.taobao.org/dist/chromedriver
```
