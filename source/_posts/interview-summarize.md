---
title: 面试题总结
date: 2022/06/20
tags: [面试题总结]
categories: [前端面试题]
author: 枫🍁川
permalink: interview-summarize.html
hide: false
---

### 1. 前端知识体系

在说前端面试体系之前，先来看一下之前整理的前端知识体系图（可能不太完整，毕竟我只是一个刚毕业一个多月的小菜鸡），这只是一个基础版的前端知识体系图，适合刚入门前端的小伙伴参考，大佬勿喷： ![前端.png](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/e752a753f4a04bae948f410d483d9b83~tplv-k3u1fbpfcp-zoom-in-crop-mark:1512:0:0:0.awebp)

### 2. HTML

#### （1）面试题目

常考的HTML面试题：

1. src和href的区别
2. 对HTML语义化的理解
3. DOCTYPE(⽂档类型) 的作⽤
4. script标签中defer和async的区别
5. 常⽤的meta标签有哪些
6. HTML5有哪些更新
7. img的srcset属性的作⽤？
8. 行内元素有哪些？块级元素有哪些？ 空(void)元素有那些？
9. 说一下 web worker
10. HTML5的离线储存怎么使用，它的工作原理是什么
11. 浏览器是如何对 HTML5 的离线储存资源进行管理和加载？
12. title与h1的区别、b与strong的区别、i与em的区别？
13. iframe 有那些优点和缺点？
14. label 的作用是什么？如何使用？
15. Canvas和SVG的区别
16. head 标签有什么作用，其中什么标签必不可少？
17. 文档声明（Doctype）和有何作用? 严格模式与混杂模式如何区分？它们有何意义?
18. 浏览器乱码的原因是什么？如何解决？
19. 渐进增强和优雅降级之间的区别
20. 说一下 HTML5 drag API

#### （2）思维导图

下图对HTML面试题的考察频率进行了大致的区分，可以选择性的学习： ![HTML面试题.png](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/469624491eda40dabdecfe2fbb45a6aa~tplv-k3u1fbpfcp-zoom-in-crop-mark:1512:0:0:0.awebp)

#### （3）答案解析

**既然有面试题，那面试题答案也是必不可少的，参考文章：**[**「2021」高频前端面试题汇总之HTML篇**](https://juejin.cn/post/6905294475539513352)

### 2. CSS

#### （1）面试题目

常考的CSS面试题：

**一、CSS基础**

1. CSS选择器及其优先级
2. CSS中可继承与不可继承属性有哪些
3. display的属性值及其作用
4. display的block、inline和inline-block的区别
5. 隐藏元素的方法有哪些
6. link和@import的区别
7. transition和animation的区别
8. display:none与visibility:hidden的区别
9. 伪元素和伪类的区别和作用？
10. 对requestAnimationframe的理解
11. 对盒模型的理解
12. 为什么有时候⽤translate来改变位置⽽不是定位？
13. li 与 li 之间有看不见的空白间隔是什么原因引起的？如何解决？
14. CSS3中有哪些新特性
15. 替换元素的概念及计算规则
16. 常见的图片格式及使用场景
17. 对 CSSSprites 的理解
18. 什么是物理像素，逻辑像素和像素密度，为什么在移动端开发时需要用到@3x, @2x这种图片？
19. margin 和 padding 的使用场景
20. 对line-height 的理解及其赋值方式
21. CSS 优化和提高性能的方法有哪些？
22. CSS预处理器/后处理器是什么？为什么要使用它们？
23. ::before 和 :after 的双冒号和单冒号有什么区别？
24. display:inline-block 什么时候会显示间隙？
25. 单行、多行文本溢出隐藏
26. Sass、Less 是什么？为什么要使用他们？
27. 对媒体查询的理解？
28. 对 CSS 工程化的理解
29. 如何判断元素是否到达可视区域
30. z-index属性在什么情况下会失效
31. CSS3中的transform有哪些属性 **二、页面布局**
32. 常见的CSS布局单位
33. px、em、rem的区别及使用场景
34. 两栏布局的实现
35. 三栏布局的实现
36. 水平垂直居中的实现
37. 如何根据设计稿进行移动端适配？
38. 对Flex布局的理解及其使用场景
39. 响应式设计的概念及基本原理

**三、定位与浮动**

1. 为什么需要清除浮动？清除浮动的方式
2. 使用 clear 属性清除浮动的原理？
3. 对BFC的理解，如何创建BFC
4. 什么是margin重叠问题？如何解决？
5. 元素的层叠顺序
6. position的属性有哪些，区别是什么
7. display、float、position的关系
8. absolute与fixed共同点与不同点
9. 对 sticky 定位的理解

**四、场景应用**

1. 实现一个三角形
2. 实现一个扇形
3. 实现一个宽高自适应的正方形
4. 画一条0.5px的线
5. 设置小于12px的字体
6. 如何解决 1px 问题？

#### （2）思维导图

下图对CSS面试题的考察频率进行了大致的区分，可以选择性的学习： ![CSS面试题.png](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/64931630a728403bb0caa99f86f5f662~tplv-k3u1fbpfcp-zoom-in-crop-mark:1512:0:0:0.awebp)

#### （3）答案解析

**既然有面试题，那面试题答案也是必不可少的，参考文章：**[「2021」高频前端面试题汇总之CSS篇](https://juejin.cn/post/6905539198107942919)

### 3. JavaScript

#### （1）面试题目

**一、数据类型**

1. JavaScript有哪些数据类型，它们的区别？
2. 数据类型检测的方式有哪些
3. 判断数组的方式有哪些
4. null和undefined区别
5. typeof null 的结果是什么，为什么？
6. intanceof 操作符的实现原理及实现
7. 为什么0.1+0.2 ! == 0.3，如何让其相等
8. 如何获取安全的 undefined 值？
9. typeof NaN 的结果是什么？
10. isNaN 和 Number.isNaN 函数的区别？
11. == 操作符的强制类型转换规则？
12. 其他值到字符串的转换规则？
13. 其他值到数字值的转换规则？
14. 其他值到布尔类型的值的转换规则？
15. || 和 && 操作符的返回值？
16. Object.is() 与比较操作符 “===”、“==” 的区别？
17. 什么是 JavaScript 中的包装类型？
18. JavaScript 中如何进行隐式类型转换？
19. +操作符什么时候用于字符串的拼接？
20. 为什么会有BigInt的提案？
21. object.assign和扩展运算法是深拷贝还是浅拷贝，两者区别

**二、ES6**

1. let、const、var的区别
2. const对象的属性可以修改吗
3. 如果new一个箭头函数的会怎么样
4. 箭头函数与普通函数的区别
5. 箭头函数的this指向哪⾥？
6. 扩展运算符的作用及使用场景
7. Proxy 可以实现什么功能？
8. 对对象与数组的解构的理解
9. 如何提取高度嵌套的对象里的指定属性？
10. 对 rest 参数的理解
11. ES6中模板语法与字符串处理

**三、JavaScript基础**

1. new操作符的实现原理
2. map和Object的区别
3. map和weakMap的区别
4. JavaScript有哪些内置对象
5. 常用的正则表达式有哪些？
6. 对JSON的理解
7. JavaScript脚本延迟加载的方式有哪些？
8. JavaScript 类数组对象的定义？
9. 数组有哪些原生方法？
10. Unicode、UTF-8、UTF-16、UTF-32的区别？
11. 常见的位运算符有哪些？其计算规则是什么？
12. 为什么函数的 arguments 参数是类数组而不是数组？如何遍历类数组?
13. 什么是 DOM 和 BOM？
14. 对类数组对象的理解，如何转化为数组
15. escape、encodeURI、encodeURIComponent 的区别
16. 对AJAX的理解，实现一个AJAX请求
17. JavaScript为什么要进行变量提升，它导致了什么问题？
18. 什么是尾调用，使用尾调用有什么好处？
19. ES6模块与CommonJS模块有什么异同？
20. 常见的DOM操作有哪些
21. use strict是什么意思 ? 使用它区别是什么？
22. 如何判断一个对象是否属于某个类？
23. 强类型语言和弱类型语言的区别
24. 解释性语言和编译型语言的区别
25. for...in和for...of的区别
26. 如何使用for...of遍历对象
27. ajax、axios、fetch的区别
28. 数组的遍历方法有哪些
29. forEach和map方法有什么区别

**四、原型与原型链**

1. 对原型、原型链的理解
2. 原型修改、重写
3. 原型链指向
4. 原型链的终点是什么？如何打印出原型链的终点？
5. 如何获得对象非原型链上的属性？

**五、执行上下文/作用域链/闭包**

1. 对闭包的理解
2. 对作用域、作用域链的理解
3. 对执行上下文的理解

**六、this/call/apply/bind**

1. 对this对象的理解
2. call() 和 apply() 的区别？
3. 实现call、apply 及 bind 函数

**七、异步编程**

1. 异步编程的实现方式？
2. setTimeout、Promise、Async/Await 的区别
3. 对Promise的理解
4. Promise的基本用法
5. Promise解决了什么问题
6. Promise.all和Promise.race的区别的使用场景
7. 对async/await 的理解
8. await 到底在等啥？
9. async/await的优势
10. async/await对比Promise的优势
11. async/await 如何捕获异常
12. 并发与并行的区别？
13. 什么是回调函数？回调函数有什么缺点？如何解决回调地狱问题？
14. setTimeout、setInterval、requestAnimationFrame 各有什么特点？

**八、面向对象**

1. 对象创建的方式有哪些？
2. 对象继承的方式有哪些？

**九、垃圾回收与内存泄漏**

1. 浏览器的垃圾回收机制
2. 哪些情况会导致内存泄漏

#### （2）思维导图

下图对JavaScript面试题的考察频率进行了大致的区分，可以选择性的学习： ![JavaScript面试题.png](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/b48c47f54a944f21aea3696e6b413d17~tplv-k3u1fbpfcp-zoom-in-crop-mark:1512:0:0:0.awebp)

#### （3）答案解析

**既然有面试题，那面试题答案也是必不可少的，参考文章：**

- [「2021」高频前端面试题汇总之JavaScript篇（上）](https://juejin.cn/post/6940945178899251230)
- [「2021」高频前端面试题汇总之JavaScript篇（下）](https://juejin.cn/post/6941194115392634888)

### 4. Vue

#### （1）面试题目

**一、Vue 基础**

1. Vue的基本原理
2. 双向数据绑定的原理
3. 使用 Object.defineProperty() 来进行数据劫持有什么缺点？
4. MVVM、MVC、MVP的区别
5. Computed 和 Watch 的区别
6. Computed 和 Methods 的区别
7. slot是什么？有什么作用？原理是什么？
8. 过滤器的作用，如何实现一个过滤器
9. 如何保存页面的当前的状态
10. 常见的事件修饰符及其作用
11. v-if、v-show、v-html 的原理
12. v-if和v-show的区别
13. v-model 是如何实现的，语法糖实际是什么？
14. v-model 可以被用在自定义组件上吗？如果可以，如何使用？
15. data为什么是一个函数而不是对象
16. 对keep-alive的理解，它是如何实现的，具体缓存的是什么？
17. $nextTick 原理及作用
18. Vue 中给 data 中的对象属性添加一个新的属性时会发生什么？如何解决？
19. Vue中封装的数组方法有哪些，其如何实现页面更新
20. Vue 单页应用与多页应用的区别
21. Vue template 到 render 的过程
22. Vue data 中某一个属性的值发生改变后，视图会立即同步执行重新渲染吗？
23. 简述 mixin、extends 的覆盖逻辑
24. 描述下Vue自定义指令
25. 子组件可以直接改变父组件的数据吗？
26. Vue是如何收集依赖的？
27. 对 React 和 Vue 的理解，它们的异同
28. Vue的优点
29. assets和static的区别
30. delete和Vue.delete删除数组的区别
31. vue如何监听对象或者数组某个属性的变化
32. 什么是 mixin ？
33. Vue模版编译原理
34. 对SSR的理解
35. Vue的性能优化有哪些
36. 对 SPA 单页面的理解，它的优缺点分别是什么？
37. template和jsx的有什么分别？
38. vue初始化页面闪动问题
39. extend 有什么作用
40. mixin 和 mixins 区别
41. MVVM的优缺点?

**二、生命周期**

1. 说一下Vue的生命周期
2. Vue 子组件和父组件执行顺序
3. created和mounted的区别
4. 一般在哪个生命周期请求异步数据
5. keep-alive 中的生命周期哪些

**三、组件通信**

1. 组件通信的方式

四、路由

1. Vue-Router 的懒加载如何实现
2. 路由的hash和history模式的区别
3. 如何获取页面的hash变化
4. route和route 和route和router 的区别
5. 如何定义动态路由？如何获取传过来的动态参数？
6. Vue-router 路由钩子在生命周期的体现
7. Vue-router跳转和location.href有什么区别
8. params和query的区别
9. Vue-router 导航守卫有哪些
10. 对前端路由的理解

**五、Vuex**

1. Vuex 的原理
2. Vuex中action和mutation的区别
3. Vuex 和 localStorage 的区别
4. Redux 和 Vuex 有什么区别，它们的共同思想
5. 为什么要用 Vuex 或者 Redux
6. Vuex有哪几种属性？
7. Vuex和单纯的全局对象有什么区别？
8. 为什么 Vuex 的 mutation 中不能做异步操作？
9. Vuex的严格模式是什么,有什么作用，如何开启？
10. 如何在组件中批量使用Vuex的getter属性
11. 如何在组件中重复使用Vuex的mutation **六、Vue 3.0**
12. Vue3.0有什么更新
13. defineProperty和proxy的区别
14. Vue3.0 为什么要用 proxy？
15. Vue 3.0 中的 Vue Composition API？
16. Composition API与React Hook很像，区别是什么

**七、虚拟DOM**

1. 对虚拟DOM的理解？
2. 虚拟DOM的解析过程
3. 为什么要用虚拟DOM
4. 虚拟DOM真的比真实DOM性能好吗
5. DIFF算法的原理
6. Vue中key的作用
7. 为什么不建议用index作为key?

#### （2）思维导图

下图对Vue面试题的考察频率进行了大致的区分，可以选择性的学习： ![Vue面试题.png](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/666ec009cd6c478d82fc11c2a89f31a5~tplv-k3u1fbpfcp-zoom-in-crop-mark:1512:0:0:0.awebp)

#### （3）答案解析

**既然有面试题，那面试题答案也是必不可少的，参考文章：**

- [「2021」高频前端面试题汇总之Vue篇（上）](https://juejin.cn/post/6919373017218809864)
- [「2021」高频前端面试题汇总之Vue篇（下）](https://juejin.cn/post/6964779204462247950/)

### 5. React

#### （1）面试题目

**一、组件基础**

1. React 事件机制
2. React的事件和普通的HTML事件有什么不同？
3. React 组件中怎么做事件代理？它的原理是什么？
4. React 高阶组件、Render props、hooks 有什么区别，为什么要不断迭代
5. React如何获取组件对应的DOM元素？
6. React中可以在render访问refs吗？为什么？
7. 对React的插槽(Portals)的理解，如何使用，有哪些使用场景
8. 在React中如何避免不必要的render？
9. 对 React-Intl 的理解，它的工作原理？
10. 对 React context 的理解
11. 为什么React并不推荐优先考虑使用Context？
12. React中什么是受控组件和非控组件？
13. React中refs的作用是什么？有哪些应用场景？
14. React组件的构造函数有什么作用？它是必须的吗？
15. React.forwardRef是什么？它有什么作用？
16. 类组件与函数组件有什么异同？
17. React中可以在render访问refs吗？为什么？
18. 对React的插槽(Portals)的理解，如何使用，有哪些使用场景
19. 在React中如何避免不必要的render？
20. 对 React-Intl 的理解，它的工作原理？
21. 对 React context 的理解
22. 为什么React并不推荐优先考虑使用Context？
23. React中什么是受控组件和非控组件？
24. React中refs的作用是什么？有哪些应用场景？
25. React组件的构造函数有什么作用？它是必须的吗？
26. React.forwardRef是什么？它有什么作用？
27. 类组件与函数组件有什么异同？

**二、数据管理**

1. React setState 调用的原理
2. React setState 调用之后发生了什么？是同步还是异步？
3. React中的setState批量更新的过程是什么？
4. React中有使用过getDefaultProps吗？它有什么作用？
5. React中setState的第二个参数作用是什么？
6. React中的setState和replaceState的区别是什么？
7. 在React中组件的this.state和setState有什么区别？
8. state 是怎么注入到组件的，从 reducer 到组件经历了什么样的过程
9. React组件的state和props有什么区别？
10. React中的props为什么是只读的？
11. 在React中组件的props改变时更新组件的有哪些方法？
12. React中怎么检验props？验证props的目的是什么？

**三、生命周期**

1. React的生命周期有哪些？
2. React 废弃了哪些生命周期？为什么？
3. React 16.X 中 props 改变后在哪个生命周期中处理
4. React 性能优化在哪个生命周期？它优化的原理是什么？
5. state 和 props 触发更新的生命周期分别有什么区别？
6. React中发起网络请求应该在哪个生命周期中进行？为什么？
7. React 16中新生命周期有哪些

**四、组件通信**

1. 父子组件的通信方式？
2. 跨级组件的通信方式？
3. 非嵌套关系组件的通信方式？
4. 如何解决 props 层级过深的问题
5. 组件通信的方式有哪些

**五、路由**

1. React-Router的实现原理是什么？
2. 如何配置 React-Router 实现路由切换
3. React-Router怎么设置重定向？
4. react-router 里的 Link 标签和 a 标签的区别
5. React-Router如何获取URL的参数和历史对象？
6. React-Router 4怎样在路由变化时重新渲染同一个组件？
7. React-Router的路由有几种模式？
8. React-Router 4的Switch有什么用？

**六、Redux**

1. 对 Redux 的理解，主要解决什么问题
2. Redux 原理及工作流程
3. Redux 中异步的请求怎么处理
4. Redux 怎么实现属性传递，介绍下原理
5. Redux 中间件是什么？接受几个参数？柯里化函数两端的参数具体是什么？
6. Redux 请求中间件如何处理并发
7. Redux 状态管理器和变量挂载到 window 中有什么区别
8. mobox 和 redux 有什么区别？
9. Redux 和 Vuex 有什么区别，它们的共同思想
10. Redux 中间件是怎么拿到store 和 action? 然后怎么处理?
11. Redux中的connect有什么作用

**七、Hooks**

1. 对 React Hook 的理解，它的实现原理是什么
2. 为什么 useState 要使用数组而不是对象
3. React Hooks 解决了哪些问题？
4. React Hook 的使用限制有哪些？
5. useEffect 与 useLayoutEffect 的区别
6. React Hooks在平时开发中需要注意的问题和原因
7. React Hooks 和生命周期的关系？

**八、虚拟DOM**

1. 对虚拟 DOM 的理解？虚拟 DOM 主要做了什么？虚拟 DOM 本身是什么？
2. React diff 算法的原理是什么？
3. React key 是干嘛用的 为什么要加？key 主要是解决哪一类问题的
4. 虚拟 DOM 的引入与直接操作原生 DOM 相比，哪一个效率更高，为什么
5. React 与 Vue 的 diff 算法有何不同？

**九、其他**

1. React组件命名推荐的方式是哪个？
2. react 最新版本解决了什么问题，增加了哪些东西
3. react 实现一个全局的 dialog
4. React 数据持久化有什么实践吗？
5. 对 React 和 Vue 的理解，它们的异同
6. 可以使用TypeScript写React应用吗？怎么操作？
7. React 设计思路，它的理念是什么？
8. React中props.children和React.Children的区别
9. React的状态提升是什么？使用场景有哪些？
10. React中constructor和getInitialState的区别?
11. React的严格模式如何使用，有什么用处？
12. 在React中遍历的方法有哪些？
13. 在React中页面重新加载时怎样保留数据？
14. 同时引用这三个库react.js、react-dom.js和babel.js它们都有什么作用？
15. React必须使用JSX吗？
16. 为什么使用jsx的组件中没有看到使用react却需要引入react？
17. 在React中怎么使用async/await？
18. React.Children.map和js的map有什么区别？
19. 对React SSR的理解
20. 为什么 React 要用 JSX？
21. HOC相比 mixins 有什么优点？
22. React 中的高阶组件运用了什么设计模式？

#### （2）思维导图

下图对React面试题的考察频率进行了大致的区分，可以选择性的学习： ![React面试题.png](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/a72ebc3a1f9f47c7a333976769740e7e~tplv-k3u1fbpfcp-zoom-in-crop-mark:1512:0:0:0.awebp)

#### （3）答案解析

**既然有面试题，那面试题答案也是必不可少的，参考文章：**

- [「2021」高频前端面试题汇总之React篇（上）](https://juejin.cn/post/6941546135827775525)
- [「2021」高频前端面试题汇总之React篇（下）](https://juejin.cn/post/6940942549305524238)

### 6. 浏览器原理

#### （1）面试题目

**一、浏览器安全**

1. 什么是 XSS 攻击？
2. 如何防御 XSS 攻击？
3. 什么是 CSRF 攻击？
4. 如何防御 CSRF 攻击？
5. 什么是中间人攻击？如何防范中间人攻击？
6. 有哪些可能引起前端安全的问题?
7. 网络劫持有哪几种，如何防范？

**二、进程与线程**

1. 进程与线程的概念
2. 进程和线程的区别
3. 浏览器渲染进程的线程有哪些
4. 进程之前的通信方式
5. 僵尸进程和孤儿进程是什么？
6. 死锁产生的原因？ 如果解决死锁的问题？
7. 如何实现浏览器内多个标签页之间的通信?
8. 对Service Worker的理解

三、浏览器缓存

1. 对浏览器的缓存机制的理解
2. 浏览器资源缓存的位置有哪些？
3. 协商缓存和强缓存的区别
4. 为什么需要浏览器缓存？
5. 点击刷新按钮或者按 F5、按 Ctrl+F5 （强制刷新）、地址栏回车有什么区别？

**四、浏览器组成**

1. 对浏览器的理解
2. 对浏览器内核的理解
3. 常见的浏览器内核比较
4. 常见浏览器所用内核
5. 浏览器的主要组成部分
6. 五、浏览器渲染原理
7. 浏览器的渲染过程
8. 浏览器渲染优化
9. 渲染过程中遇到 JS 文件如何处理？
10. 什么是文档的预解析？
11. CSS 如何阻塞文档解析？
12. 如何优化关键渲染路径？
13. 什么情况会阻塞渲染？

**六、浏览器本地存储**

1. 浏览器本地存储方式及使用场景
2. Cookie有哪些字段，作用分别是什么
3. Cookie、LocalStorage、SessionStorage区别
4. 前端储存的⽅式有哪些？
5. IndexedDB有哪些特点？

**七、浏览器同源策略**

1. 什么是同源策略
2. 如何解决跨越问题
3. 正向代理和反向代理的区别
4. Nginx的概念及其工作原理

**八、浏览器事件机制**

1. 事件是什么？事件模型？
2. 如何阻止事件冒泡
3. 对事件委托的理解
4. 事件委托的使用场景
5. 同步和异步的区别
6. 对事件循环的理解
7. 宏任务和微任务分别有哪些
8. 什么是执行栈
9. Node 中的 Event Loop 和浏览器中的有什么区别？process.nextTick 执行顺序？
10. 事件触发的过程是怎样的

**九、浏览器垃圾回收机制**

1. V8的垃圾回收机制是怎样的
2. 哪些操作会造成内存泄漏？

#### （2）思维导图

下图对浏览器原理面试题的考察频率进行了大致的区分，可以选择性的学习： ![浏览器原理面试题.png](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/bc2c03a1285049428ce6769269d948b3~tplv-k3u1fbpfcp-zoom-in-crop-mark:1512:0:0:0.awebp)

#### （3）答案解析

**既然有面试题，那面试题答案也是必不可少的，参考文章：**[「2021」高频前端面试题汇总之浏览器原理篇](https://juejin.cn/post/6916157109906341902/)。

### 7. 计算机网络

#### （1）面试题目

**一、HTTP协议**

1. GET和POST的请求的区别
2. POST和PUT请求的区别
3. 常见的HTTP请求头和响应头
4. HTTP状态码304是多好还是少好
5. 常见的HTTP请求方法
6. OPTIONS请求方法及使用场景
7. HTTP 1.0 和 HTTP 1.1 之间有哪些区别？
8. HTTP 1.1 和 HTTP 2.0 的区别
9. HTTP和HTTPS协议的区别
10. GET方法URL长度限制的原因
11. 当在浏览器中输入 Google.com 并且按下回车之后发生了什么？
12. 对keep-alive的理解
13. 页面有多张图片，HTTP是怎样的加载表现？
14. HTTP2的头部压缩算法是怎样的？
15. HTTP请求报文的是什么样的？
16. HTTP响应报文的是什么样的？
17. HTTP协议的优点和缺点
18. 说一下HTTP 3.0
19. HTTP协议的性能怎么样
20. URL有哪些组成部分
21. 与缓存相关的HTTP请求头有哪些

**二、HTTPS协议**

1. 什么是HTTPS协议？
2. TLS/SSL的工作原理
3. 数字证书是什么？
4. HTTPS通信（握手）过程
5. HTTPS的特点
6. HTTPS是如何保证安全的？

**三、HTTP状态码**

1. 常见的状态码
2. 同样是重定向，307，303，302的区别？

**四、DNS协议介绍**

1. DNS 协议是什么
2. DNS同时使用TCP和UDP协议？
3. DNS完整的查询过程
4. 迭代查询与递归查询
5. DNS 记录和报文

**五、网络模型**

1. OSI七层模型
2. TCP/IP五层协议

**六、TCP与UDP**

1. TCP 和 UDP的概念及特点
2. TCP和UDP的区别
3. TCP和UDP的使用场景
4. UDP协议为什么不可靠？
5. TCP的重传机制
6. TCP的拥塞控制机制
7. TCP的流量控制机制
8. TCP的可靠传输机制
9. TCP的三次握手和四次挥手
10. TCP粘包是怎么回事，如何处理?
11. 为什么udp不会粘包？

**七、WebSocket**

1. 对 WebSocket 的理解
2. 即时通讯的实现：短轮询、长轮询、SSE 和 WebSocket 间的区别？

#### （2）思维导图

下图对计算机网络面试题的考察频率进行了大致的区分，可以选择性的学习：![计算机网络面试题.png](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/e3746a6a0a8c4dc3a220ecd3de62f1a0~tplv-k3u1fbpfcp-zoom-in-crop-mark:1512:0:0:0.awebp)

#### （3）答案解析

**既然有面试题，那面试题答案也是必不可少的，参考文章：**[「2021」高频前端面试题汇总之计算机网络篇](https://juejin.cn/post/6908327746473033741)。

### 8. 前端性能优化

#### （1）面试题目

**一、CDN**

1. CDN的概念
2. CDN的作用
3. CDN的原理
4. CDN的使用场景

**二、懒加载**

1. 懒加载的概念
2. 懒加载的特点
3. 懒加载的实现原理
4. 懒加载与预加载的区别

**三、回流与重绘**

1. 回流与重绘的概念及触发条件
2. 如何避免回流与重绘？
3. 如何优化动画？
4. documentFragment 是什么？用它跟直接操作 DOM 的区别是什么？

**四、节流与防抖**

1. 对节流与防抖的理解
2. 实现节流函数和防抖函数

**五、图片优化**

1. 如何对项目中的图片进行优化？
2. 常见的图片格式及使用场景

**六、Webpack优化**

1. 如何提⾼webpack的打包速度?
2. 如何减少 Webpack 打包体积
3. 如何⽤webpack来优化前端性能？
4. 如何提⾼webpack的构建速度？

#### （2）思维导图

下图对前端性能优化面试题的考察频率进行了大致的区分，可以选择性的学习： ![性能优化面试题.png](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/ea2f509436de4e32b0a2072ad4dcdf47~tplv-k3u1fbpfcp-zoom-in-crop-mark:1512:0:0:0.awebp)

#### （3）答案解析

**既然有面试题，那面试题答案也是必不可少的，参考文章：**[「2021」高频前端面试题汇总之性能优化篇](https://juejin.cn/post/6941278592215515143)。

### 9. 手写代码

#### （1）面试题目

**一、JavaScript 基础**

1. 手写 Object.create
2. 手写 instanceof 方法
3. 手写 new 操作符
4. 手写 Promise
5. 手写 Promise.then
6. 手写 Promise.all
7. 手写 Promise.race
8. 手写防抖函数
9. 手写节流函数
10. 手写类型判断函数
11. 手写 call 函数
12. 手写 apply 函数
13. 手写 bind 函数
14. 函数柯里化的实现
15. 实现AJAX请求
16. 使用Promise封装AJAX请求
17. 实现浅拷贝
18. 实现深拷贝

**二、数据处理**

1. 实现日期格式化函数
2. 交换a,b的值，不能用临时变量
3. 实现数组的乱序输出
4. 实现数组元素求和
5. 实现数组的扁平化
6. 实现数组去重
7. 实现数组的flat方法
8. 实现数组的push方法
9. 实现数组的filter方法
10. 实现数组的map方法
11. 实现字符串的repeat方法
12. 实现字符串翻转
13. 将数字每千分位用逗号隔开
14. 实现非负大整数相加
15. 实现 add(1)(2)(3)
16. 实现类数组转化为数组
17. 使用 reduce 求和
18. 将js对象转化为树形结构
19. 使用ES5和ES6求函数参数的和
20. 解析 URL Params 为对象

**三、场景应用**

1. 循环打印红黄绿
2. 实现每隔一秒打印 1,2,3,4
3. 小孩报数问题
4. 用Promise实现图片的异步加载
5. 实现发布-订阅模式
6. 查找文章中出现频率最高的单词
7. 封装异步的fetch，使用async await方式来使用
8. 实现prototype继承
9. 实现双向数据绑定
10. 实现简单路由
11. 实现斐波那契数列
12. 字符串出现的不重复最长长度
13. 使用 setTimeout 实现 setInterval
14. 实现 jsonp
15. 判断对象是否存在循环引用

#### （2）思维导图

下图对手写代码面试题的考察频率进行了大致的区分，可以选择性的学习： ![手写代码面试题.png](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/de74df757b684584b10480cd6f95a4dc~tplv-k3u1fbpfcp-zoom-in-crop-mark:1512:0:0:0.awebp)

#### （3）答案解析

**既然有面试题，那面试题答案也是必不可少的，参考文章：**[「2021」高频前端面试题汇总之手写代码篇](https://juejin.cn/post/6946136940164939813)。

### 10. 代码输出结果

**代码输出结果**是面试中常考的题目，一段代码中可能涉及到很多的知识点，这就考察到了应聘者的基础能力。在前端面试中，常考的代码输出问题主要涉及到以下知识点：**异步编程、事件循环、this指向、作用域、变量提升、闭包、原型、继承**等，这里就不一一列举相关的面试题了，已经在另外一篇文章写的很清楚了，参考文章：[「2021」高频前端面试题汇总之代码输出结果篇](https://juejin.cn/post/6959043611161952269)。

如果这一篇文章中的面试题都能搞懂了，那面试中的代码输出结果问题基本都很容易就解决了。

### 11. 前端工程化

#### （1）面试题目

**一、Git**

1. git 和 svn 的区别
2. 经常使用的 git 命令？
3. git pull 和 git fetch 的区别
4. git rebase 和 git merge 的区别

**二、Webpack**

1. webpack与grunt、gulp的不同？
2. webpack、rollup、parcel优劣？
3. 有哪些常⻅的Loader？
4. 有哪些常⻅的Plugin？
5. bundle，chunk，module是什么？
6. Loader和Plugin的不同？
7. webpack的构建流程?
8. 编写loader或plugin的思路？
9. webpack的热更新是如何做到的？说明其原理？
10. 如何⽤webpack来优化前端性能？
11. 如何提⾼webpack的打包速度?
12. 如何提⾼webpack的构建速度？
13. 怎么配置单⻚应⽤？怎么配置多⻚应⽤？

**三、其他**

1. Babel的原理是什么?

**注：** 关于前端工程相关的面试题，由于个人还在整理中，还不是很全面，会尽快发在掘金上，暂时就不给出答案了，大家可以自行查找学习。

### 12. 其他

除了上面给出的这些类别的面试题，其实还有很多，比如数据结构与算法，前端业务实现等。关于数据结构与算法，主要考察方向就是LeetCode题目，可以参考**一个搬砖的胖子**大佬的[codeTop](https://link.juejin.cn?target=https%3A%2F%2Fcodetop.cc%2F%23%2Fhome)来针对性的刷题。下面只给出几个业务实现的问题，大家可以参考：

1. 如何优化长列表
2. 如何实现一个dialog组件
3. 服务端渲染的原理
4. 项目打包到服务器的整个过程
5. 以前端角度出发做好 SEO 需要考虑什么？
6. 如何实现前端登录
7. 如何实现扫码登录

**最后，这篇文章只给出了前端面试中经常考察到的“八股文”，基本没有涉及到项目经历相关的问题， 只能根据自己的实际情况去作答了**
