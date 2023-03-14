---
title: 防抖节流
date: 2022/02/01
tags: [防抖, 节流]
categories: [javascript]
author: 枫🍁川
permalink: debounce-throttle.html
---

防抖和节流，这个在我们的前端生涯中，这两个名词肯定不陌生，甚至经常被人问起：

- 两者有什么区别？
- 分别用于什么场景？ **ps：这就是高频的面试题了吧！**

## 防抖

防抖是什么呢？

形象的的说就是：防止抖动（防抖函数内心独白：“你就抖动吧！等你不抖动了，我们在进行下一步”）

### 例如

一个搜索输入框， 用户不停的进行输入（**这个时候就是抖动的过程**）， 等用户输入停止之后，再触发搜索。

### 代码演示

```typescript
function debounce(fn, delay = 200) {
  let timer = 0
  return function() {
    // 如果这个函数已经被触发了
    if(timer){
      clearTimeout(timer)
    }
    timer = setTimeout(() => {
      fn.apply(this, arguments); // 透传 this和参数
      timer = 0
    },delay)
  }
}
```

[![image.png](https://p1-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/46181f1811fa4a99a1659c324c677014~tplv-k3u1fbpfcp-zoom-in-crop-mark:3024:0:0:0.awebp)](https://p1-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/46181f1811fa4a99a1659c324c677014~tplv-k3u1fbpfcp-zoom-in-crop-mark:3024:0:0:0.awebp)

## 节流

节流：节省交互沟通。

形象的的说就是：no！no！no！一个一个来，按照时间节奏来！插队禁止！

### 例如

drag（拖动）事件或者 scroll（滚动） 期间触发某个毁掉，要设置一个时间间隔。这时候就**不能使用防抖**了，为什么呢？

防抖是拖拽或者滚动结束之后才返回回调，但是我是需要在过程中进行触发回调，但是又不需要那么的频繁；这时候就使用**节流函数**，每隔一定的时间进项触发就好了！

### 代码演示

```javascript
// 节流函数
function throttle(fn, delay = 200) {
  let  timer = 0
  return function () {
    if(timer){
      return
    }
    timer = setTimeout(() =>{
      fn.apply(this, arguments); // 透传 this和参数
      timer = 0
    },delay)
  }
}
```

咋一看，怎么和防抖函数好像怎么这么像？

区别仅仅在：

防抖：

```javascript
 if(timer){
  clearTimeout(timer)
}
```

节流：

```javascript
if(timer){
  return
}
```

他们在定时器已经有任务的时候的操作的不同。在我们上面介绍了防抖和节流的概念之后，大家应该都懂了。

防抖函数在每一次都有内容后进行清除是为了保证当前执行的函数就是当前规定的时间内执行的最后一次操作

```javascript
 if(timer){
  clearTimeout(timer)
}
```

节流函数如此操作是为了保证，在规定的时间内只会执行一次这个操作，这就是两个函数从代码上看到的不同

```javascript
if(timer){
  return
}
```
