---
title: SEO 优化、前端优化 
date: 2022/02/10
tags: [seo优化, vue优化]
categories: [性能优化]
author: 枫🍁川
permalink: seo-optimize.html
---

## vue优化

1. Vue-Router路由懒加载：Vue异步组件、Webpack的require.ensure()、ES6的import、
2. 按需加载UI库
3. 如果首屏为登录页，可以做成多入口
4. 页面使用骨架屏Skeleton Screen
5. 服务端渲染SSR（将组件或页面通过服务器生成html字符串，再发送到浏览器，最后将静态标记”混合”为客户端上完全交互的应用程序）

## 网络优化

1. 减少 HTTP 请求数量
2. 利用浏览器缓存，减小`cookie`大小，尽量用`localStorage`代替
3. CDN加速，托管静态文件
4. 开启 Gzip 压缩：Nginx的gzip缓存压缩、Webpack开启gzip压缩

## js优化

1. 节流、防抖
2. 动态加载、分页加载（大数据渲染）
3. 图片懒加载（data-src）减少占用网络带宽
4. 使用闭包时，在函数结尾手动删除不需要的局部变量，尤其在缓存dom节点的情况下
5. 异步加载js，async解析dom树同时加载js，加载完暂停解析执行js、defer解析dom树同时加载js，解析完执行js

## css优化

不使用css表达式

减少回流（重排）

避免使用css文件嵌套过深

## SEO优化

突出重要内容—合理的设计`title`、`description`和`keywords`

语义化书写HTML代码，符合W3C标准

图片`img`标签添加`alt`和`title`属性

链接`<a>`页内标签添加`title`属性

使用h1标签自带权重