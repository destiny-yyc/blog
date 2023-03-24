---
title: 二次封装 Axios (javascript)
date: 2022/02/12
tags: [axios]
categories: [javascript, typescript]
author: 枫🍁川
permalink: second-axios.html
---

> 我分了`javascript`和`typescript`两个版本的axios,虽然两份的逻辑都是一样的，但是写法上会有不同的方式

### **安装 axios**

```bash
npm install axios element-plus
```

这里我用了ElementPlus的轻量弹窗，安装成功后就可以在项目中使用了，[具体使用方法可以查看 github](https://github.com/axios/axios)，然后先在 src 目录下创建一个 utils 目录，再创建一个 https.js 文件，里面的编写如下：

### javascript的写法：直接在响应拦截里把处理逻辑

```javascript
//引入 axios
import axios from "axios";
import { ElMessage } from 'element-plus';

const request = axios.create({
  baseURL: '/api',
  timeout: 5000
})

// 数据请求拦截
request.interceptors.request.use((config) => {
  return config;
}, (error) => {
  return Promise.reject(error);
});

// 返回响应数据拦截
request.interceptors.response.use((res) => {
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
export { request };
```

### typescript的写法：新增了类型声明

```typescript
import type { AxiosResponse } from "axios";
import axios from "axios";
import { ElMessage } from "element-plus";

// 请求拦截
axios.interceptors.request.use((config: any) => {
	// 可在此处添加token等信息
  return config
}, (error) => {
  return error
})

// 响应拦截
axios.interceptors.response.use((config: any) => {
	 return config
},(error) => {
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
  return error
})

const request = <T>(url: string, options?: { [key: string]: any }) => {
  return new Promise<T>((resolve, reject) => {
    const option = {
      url,
      ...options,
      baseURL: "/api",
    }
    axios(option).then((res: AxiosResponse<T & { success: boolean, data: any, msg?: string, token?: string,  }>) => {
      const { success, msg, } = res.data
      if (success) {
        resolve(res.data)
      } else {
        ElMessage.error(<string>msg)
        reject(res.data)
      }
    }).catch(error => {
      reject(error)
    })
  })
}

exprot { request }
```

编写完成后，这个 axios 就已经完成了简单的二次封装。封装后就开始引入使用了，我这里是把所有的请求放到了一个 js 文件里面，在 **src** 目录创建一个 **api** 目录，再创建一个 index.js 文件，

```typescript
// 把封装好的 axios 引入
import { request } from '@/utils/http';

type IDP.LoginInParam = {
    password?: string | undefined;
    username?: string | undefined;
}

type IDP.LoginInResponse = {
    code: number;
    data: UserInfo;
    msg: string;
    success: boolean;
}

/** 登录 POST /login */
export async function idpLogin(body: IDP.LoginInParam, options?: { [key: string]: any }) {
  return request<IDP.LoginInResponse>(`/idp/login`, {
    method: 'POST',
    headers: {
      'Content-Type': 'application/json',
    },
    data: body,
    ...(options || {}),
  });
}
```

我看网上那些都是进行全局引入，我觉得那样不好，后面能按需导入就按需导入，这样能提高性能，毕竟总有几个页面不需要使用axios的。

```vue
// 调用
<template>
	...
</template>
<script lang="ts" setup>
  import { idpLogin } from "@/api/index"
  import { ElMessage } from "element-plus";
  
  const loading = ref<boolean>(false)
  const username = ref<string>("")
  const password = ref<string>("")
  
  const login = async () => {
    loading.value = true
    try {
      const { data, success, msg } = await idpLogin({
        username: username.value,
        password: password.value
      })
      if(success){
        ElMessage.success(<string>msg)
      }
    } catch (error) {
      console.log(error)
    } finally {
      loading.value = false
    }
  }
</script>
```

