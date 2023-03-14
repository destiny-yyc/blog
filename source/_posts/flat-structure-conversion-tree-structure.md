---
title: 扁平数组与JSON树结构互转
date: 2022/01/25
tags: [扁平数组, 树结构]
categories: [javascript]
author: 枫🍁川
permalink: flat-structure-conversion-tree-structure.html
---

### 第一种

##### 扁平数组

```json
{
    "id": "01",
    "name": "张大大",
    "pid": "-1",
    "job": "项目经理"
  },
  {
    "id": "02",
    "name": "小亮",
    "pid": "01",
    "job": "产品leader"
  },
  {
    "id": "03",
    "name": "小美",
    "pid": "01",
    "job": "UIleader"
  },
  {
    "id": "04",
    "name": "老马",
    "pid": "01",
    "job": "技术leader"
  },
  {
    "id": "05",
    "name": "老王",
    "pid": "01",
    "job": "测试leader"
  },
  {
    "id": "06",
    "name": "老李",
    "pid": "01",
    "job": "运维leader"
  },
  {
    "id": "07",
    "name": "小丽",
    "pid": "02",
    "job": "产品经理"
  },
  {
    "id": "08",
    "name": "大光",
    "pid": "02",
    "job": "产品经理"
  },
  {
    "id": "09",
    "name": "小高",
    "pid": "03",
    "job": "UI设计师"
  },
  {
    "id": "10",
    "name": "小刘",
    "pid": "04",
    "job": "前端工程师"
  },
  {
    "id": "11",
    "name": "小华",
    "pid": "04",
    "job": "后端工程师"
  },
  {
    "id": "12",
    "name": "小李",
    "pid": "04",
    "job": "后端工程师"
  },
  {
    "id": "13",
    "name": "小赵",
    "pid": "05",
    "job": "测试工程师"
  },
  {
    "id": "14",
    "name": "小强",
    "pid": "05",
    "job": "测试工程师"
  },
  {
    "id": "15",
    "name": "小涛",
    "pid": "06",
    "job": "运维工程师"
  }
]
```

##### 树形结构

```json
[
  {
    "id": "01",
    "name": "张大大",
    "pid": "",
    "job": "项目经理",
    "children": [
      {
        "id": "02",
        "name": "小亮",
        "pid": "01",
        "job": "产品leader",
        "children": [
          {
            "id": "07",
            "name": "小丽",
            "pid": "02",
            "job": "产品经理",
            "children": []
          },
          {
            "id": "08",
            "name": "大光",
            "pid": "02",
            "job": "产品经理",
            "children": []
          }
        ]
      },
      {
        "id": "03",
        "name": "小美",
        "pid": "01",
        "job": "UIleader",
        "children": [
          {
            "id": "09",
            "name": "小高",
            "pid": "03",
            "job": "UI设计师",
            "children": []
          }
        ]
      },
      {
        "id": "04",
        "name": "老马",
        "pid": "01",
        "job": "技术leader",
        "children": [
          {
            "id": "10",
            "name": "小刘",
            "pid": "04",
            "job": "前端工程师",
            "children": []
          },
          {
            "id": "11",
            "name": "小华",
            "pid": "04",
            "job": "后端工程师",
            "children": []
          },
          {
            "id": "12",
            "name": "小李",
            "pid": "04",
            "job": "后端工程师",
            "children": []
          }
        ]
      },
      {
        "id": "05",
        "name": "老王",
        "pid": "01",
        "job": "测试leader",
        "children": [
          {
            "id": "13",
            "name": "小赵",
            "pid": "05",
            "job": "测试工程师",
            "children": []
          },
          {
            "id": "14",
            "name": "小强",
            "pid": "05",
            "job": "测试工程师",
            "children": []
          }
        ]
      },
      {
        "id": "06",
        "name": "老李",
        "pid": "01",
        "job": "运维leader",
        "children": [
          {
            "id": "15",
            "name": "小涛",
            "pid": "06",
            "job": "运维工程师",
            "children": []
          }
        ]
      }
    ]
  }
]
```

##### 转换算法

**「扁平数组」转「树形结构」**

```javascript
function treeing (arr) {
  let tree = []
  const map = {}
  for (let item of arr) {
    // 一个新的带children的结构
    let newItem = map[item.id] = {
      ...item,
      children: []
    }
    if (map[item.pid]) { // 父节点已存进map则在父节点的children添加新元素
      let parent = map[item.pid]
      parent.children.push(newItem)
    } else { // 没有父节点，在根节点添加父节点
      tree.push(newItem)
    }
  }
  return tree
}
```

**「树形结构」转「扁平数组」**

```javascript
function flatten (tree, arr = []) {
  tree.forEach(item => {
    const {children, ...props} = item
    // 添加除了children的属性
    arr.push(props)
    if (children) {
      // 递归将所有节点加入到结果集中
      flatten(children, arr)
    }
  })
  return arr
}
```

## 第二种

**菜单数据结构转换（扁平化数据和树形结构互转）**
数据格式如下：

```javascript
const treeData = [
  {
    id: 1,
    title: "课程1",
    children: [
      { id: 4, title: "课程1-1" },
      {
        id: 5,
        title: "课程1-2",
        children: [
          { id: 6, title: "课程1-2-1" },
          { id: 7, title: "课程1-2-2" },
        ],
      },
    ],
  },
  { id: 2, title: "课程2" },
  { id: 3, title: "课程3" },
];
const flatData = [
  { id: 1, parent: 0, title: "课程1" },
  { id: 4,parent: 1, title: "课程1-1" },
  { id: 5,parent: 1, title: "课程1-2" },
  { id: 6,parent: 5, title: "课程1-2-1" },
  { id: 7,parent: 5, title: "课程1-2-2" },
  { id: 2,parent: 0, title: "课程2" },
  { id: 3,parent: 0, title: "课程3" },
]
```

**1.树形结构转扁平化**

```javascript
function TreeToFlat(data) { 
  let formatData = []
  for (var i = 0; i < data.length; i++) {
    formatData.push({
      id: data[i].id,
      title: data[i].title,
    })
    if (data[i].children) {
      formatData = formatData.concat(TreeToFlat(data[i].children));
    }
  }
  return formatData;
}
console.log(TreeToFlat(treeData),'输出为扁平化结构')
```

**2.扁平化数据转为树形结构**

```javascript
function FlatToTree(arr) {
  const map = arr.reduce((acc, val) => {
    acc[val.id] = val
    return acc
  }, {})
  const tree = []
  arr.forEach(region => {
    if (region.parent) {
      const parent = map[region.parent]
      if (!parent.children) {
        parent.children = [region]
      }
      else {
        parent.children.push(region)
      }
    }
    else {
      tree.push(region)
    }
  })
  return { tree }
}
console.log(FlatToTree(flatData),'输出为树形结构')
```