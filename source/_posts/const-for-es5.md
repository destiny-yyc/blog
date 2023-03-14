---
title: 如何在 ES5 环境下实现一个const？
date: 2022/02/28
tags: [es5, const]
categories: [javascript]
author: 枫🍁川
permalink: const-for-es5.html
hide: true
---

## 属性描述符：

### 对象里目前的属性描述符有两种：

- 数据描述符：**具有值的属性**
- 存取描述符：**由getter与setter函数对描述的属性**

### 描述符功能：

#### 数据描述符与存取描述符皆可修改:

- configurable：当前对象元素的属性描述符是否可改，是否可删除
- enumerable：当前对象元素是否可枚举

#### 唯有数据描述符可以修改：

- value: 当前对象元素的值
- writable：当前对象元素的值是否可修改

#### 唯有存取描述符可以修改：

- get：读取元素属性值时的操作
- set：修改元素属性值时的操作

### 描述符可同时具有的键值：

|            | configurable | enumerable | value | writable | get  | set  |
| ---------- | ------------ | ---------- | ----- | -------- | ---- | ---- |
| 数据描述符 | Yes          | Yes        | Yes   | Yes      | No   | No   |
| 存取描述符 | Yes          | Yes        | No    | No       | Yes  | Yes  |

## const 实现原理

> 由于ES5环境没有block的概念，所以是无法百分百实现const，只能是挂载到某个对象下，要么是全局的window，要么就是自定义一个object来当容器

```javascript
var __const = function __const (data, value) {
	window.data = value // 把要定义的data挂载到window下，并赋值value
	Object.defineProperty(window, data, { // 利用Object.defineProperty的能力劫持当前对象，并修改其属性描述符
		enumerable: false,
  	configurable: false,
  	get: function () {
  		return value
  	},
  	set: function (data) {
  		if (data !== value) { // 当要对当前属性进行赋值时，则抛出错误！
   		 	throw new TypeError('Assignment to constant variable.')
    	} else {
				return value
    	}
  	}
	})
}
__const('a', 10)
console.log(a)
delete a
console.log(a)
for (let item in window) { // 因为const定义的属性在global下也是不存在的，所以用到了enumerable: false来模拟这一功能
	if (item === 'a') { // 因为不可枚举，所以不执行
  	console.log(window[item])
  }
}
a = 20 // 报错
```