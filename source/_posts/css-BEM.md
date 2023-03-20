---
title: css 命名规范 BEM
date: 2022/04/11
tags: []
categories: [css]
author: 枫🍁川
permalink: version-detail.html
---

### 前言

  没有太重视“命名”这个似乎不在技术范畴之内的东西，随着项目更新迭代变得庞大，维护起来欲哭无泪。尤其是在CSS中，一个高效的命名规范到底有多重要？

> - 代码结构更加清晰有意义
> - 维护变得简单
> - 同事看代码的时候不骂街了

  之前看到过一种丑丑的命名（"__"和"--"）不以为然，这正是本文探讨的主题——BEM命名规范。

### 1. BEM简介

  BEM(Block Element Modifier)是由Yandex(俄罗斯的网络服务门户之一)团队提出的一种前端命名规范，这里讲的BEM风格是经过改良的（没有具体阅读过相关文章，不探讨有关如何改良的细节）：

> - Block：块
> - Element：元素——块的组成部分
> - Modifier：修饰符——表示一种形态/状态

```css
.block {}
.block__element {}
.block--modifier
```

举一个很好理解的例子：

```css
人            #Block
人__手          #Element
人__手--小手      #Modifier
人__手--大手      #Modifier
人__脚          #Element

人--男人        #Modifier
人--男人__手      #Element
人--男人__脚      #Element

人--女人        #Modifier
人--女人__手      #Element
人--女人__脚      #Element
```

### 2. BEM命名 vs 传统命名

好与不好，代码为证：

#### 2.1 BEM命名

```vue
<!-- app.vue -->
<aside class="aside">
  <!-- 显示/隐藏侧边栏 -->
  <img :class="['aside__toggle--show', {'aside__toggle--hide': isHide}]" />
  <ul class="aside__menu">
    <li class="aside__menu__item">首页</li>
  </ul>
</aside>
```

```css
/*css*/
.aside {}
.aside__toggle--show {}
.aside__toggle--hide {}
.aside__menu {}
.aside__menu__item {}
```

```less/scss
/*scss或less*/
.aside {
  &__toggle {
    &--show {}
    &--hide {}
  }

  &__menu {
    &__item {}
  }
}
```

#### 2.2 传统命名

```vue
<!-- app.vue -->
<aside class="aside">
  <!-- 显示/隐藏侧边栏 -->
  <img :class="['toggle', {'hide': isHide}]" />
  <ul class="menu">
    <li class="item">首页</li>
  </ul>
</aside>
```

```css
/* css */
.aside {}
.toggle {}
.menu {}
.item {}
```

当然也有一些针对传统命名的优化，尽管看起来清晰很多，但意图的表达仍然有些不明确

```vue
<!-- app.vue -->
<aside class="aside">
  <!-- 显示/隐藏侧边栏 -->
  <img :class="['aside-toggle-show', {'aside-toggle-hide': isHide}]" />
  <ul class="aside-menu">
    <li class="aside-menu-item">首页</li>
  </ul>
</aside>
```

```css
/*css*/
.aside {}
.aside-toggle-show {}
.aside-toggle-hide {}
.aside-menu {}
.aside-menu-item {}
```

```scss/less
/*scss或less*/
.aside {
  &-toggle {
    &-show {}
    &-hide {}
  }
  &-menu {
    &-item {}
  }
```

**通过对比可以看到，BEM命名使得代码结构清晰多了，并且能把代码的意图表达得很明确。**

### 3. 正确地使用BEM

  举一个例子，你的手里拿着一本书，但你不能说这本书是人的一部分。这就好比在代码中，有一个元素刚好某个块中，但它本身并不属于这个块，按照BEM原则，此元素的命名不该包含进去：

```html
<nav class="nav">
  <ul class="nav__menu">
    <li class="nav__menu__item">首页</li>
  </ul>
  <!-- 显示用户名 -->
  <span class="username">XXX 你好！</span>
</nav>
```