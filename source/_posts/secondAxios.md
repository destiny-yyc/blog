---
title: 二次封装 Axios
date: 2022/02/12
tags: [axios]
categories: [javascript]
author: 枫🍁川
permalink: second-axios.html
---

**安装 axios**

```bash
npm install axios --save
```

安装成功后就可以在项目中使用了，[具体使用方法可以查看 github](https://link.juejin.cn/?target=https://github.com/axios/axios)，接下来我就粘贴一下我个人的操作方法。 先在 src 目录下创建一个 utils 目录，再创建一个 https.js 文件，里面的编写如下：

```
//引入 axios
import axios from "axios";
import { ElMessage } from 'element-plus';

const http = axios.create({
  baseURL: '/api',
  timeout: 50000
})

// 数据请求拦截
http.interceptors.request.use((config) => {

  return config;
}, (error) => {
  return Promise.reject(error);
});

// 返回响应数据拦截
http.interceptors.response.use((res) => {
  const data = res.data;
  // 状态码为 2xx 范围时都会调用该函数，处理响应数据
  if (res.status === 200) {
    const code = data.code;
    return Promise.resolve(data);
  }
}, (error) => {
  if (error.response.status) {
    // 状态码超过 2xx 范围时都会调用该函数，处理错误响应
    switch (error.response.status) {
      case 404:
        ElMessage({
          type: 'error',
          message: '请求路径找不到！',
          showClose: true
        });
        break;
      case 502:
        ElMessage({
          type: 'error',
          message: '服务器内部报错！',
          showClose: true
        });
        break;
      default:
        break;
    }
  }
  return Promise.reject(error);
});
//这是一位大佬指点的方法，更加简单
export default http;
// 这是我原来的写法。
// post 请求方法
// export const post = (url, params) => {
//  return new Promise((resolve, reject) => {
//    http.post(url, params).then(res => {
//      resolve(res);
//    }).catch(error => {
//      reject(error);
//   })
//  });
//}
// get 请求方法
//export const get = (url) => {
//  return new Promise((resolve, reject) => {
//    http.get(url).then(res => {
//      resolve(res);
//    }).catch(error => {
//      reject(error);
//    })
//  });
//}


JS
```

编写完成后，这个 axios 就已经完成了简单的二次封装。封装后就开始引入使用了，我这里是把所有的请求放到了一个 js 文件里面，在 **src** 目录创建一个 **api** 目录，再创建一个 index.js 文件，

```
// 把封装好的 axios 引入
//import { post, get } from '../utils/https';
import http from '../utils/https';
// 创建一个业务接口对象
const test = {
  query(params) {
    return http.post('/url', params);
  },
  test_get() {
    return http.get('/url')
  }
}

export default { test }


JS
```

然后就可以在需要调用接口的组件中使用了，我习惯了在 main.js 里面进行全局注册。

```
// 导入共用 api 文件
import api from './api/index'
......
// 我这里用的是 provide inject 这个组件通信的方法
app.provide('$api', api);

//也可以使用 app.config.globalProperties.$api = api; (vue3) -- 挂载到原型链上
// Vue.prototype.$api = api; (vue2.x)
```

#### 使用

```javascript
<script setup>
import { getCurrentInstance, inject, ref, useAttrs, useSlots } from "vue";

// provide 对应的使用方法
const $api = inject('$api')

// app.config.globalProperties 
// const { proxy } = getCurrentInstance();
// const $api = proxy.$api;

function test() {
    $api.test.query(params).then(res => {
        console.log(res);
    }).catch(error => {
        console.log(error);
    })
}

</script>
```
