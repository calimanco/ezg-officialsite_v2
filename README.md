# 亿账柜官网v2

> 亿账柜官网2.0，基于vue-cli(vue2.X，webpack2.X，sass)多页面开发。

## 说明

项目使用vue-cli官方的webpack脚手架搭建，未加入vue-route。<br>
改造webpack入口实现多页面输出，新增对sass文件的支持。<br>
考虑到目前后端架构，很难实现SEO，项目搁置。。。

## 使用命令（脚手架默认，测试部分为配置）

```bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```

## 问题收集

1、改造多页面<br>
原理就是改造webpack的入口，通过glob（需要npm安装并引入）读取pages文件夹下的js文件，拼接出多个页面的入口地址。<br>
参考了下面：<br>
<https://github.com/jarvan4dev/vue-multi-page>

2、chromedriver安装失败<br>
一般是网络问题或是Node.js 内置的 http 对象的get方法无法处理302跳转的情况，解决办法是使用国内阿里源。<br>

```bash
npm install chromedriver --chromedriver_cdnurl=http://cdn.npm.taobao.org/dist/chromedriver
```

3、SEO（搜索引擎优化）的考量<br>
vue官方的解决方法是通过服务端渲染，但现在的情况是后端没有node服务器，强行加入新的node显然风险很大，所以暂时搁置项目。<br>
计划参考webpack使用gulp完成模块化构建。
