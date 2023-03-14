---
title: Hexo 文章写作
date: 2022/01/21
tags: [hexo文章]
categories: [hexo]
author: 枫🍁川
permalink: hexo-active.html
---

## 文章配置(文末有我一般配置)

```markdown
---
title: 文章标题
date: 2022/7/13 20:46:25
---
```

| 参数              | 描述                                                         | 默认值                                                       |
| :---------------- | :----------------------------------------------------------- | :----------------------------------------------------------- |
| `layout`          | 布局                                                         | [`config.default_layout`](https://hexo.io/zh-cn/docs/configuration#文章) |
| `title`           | 标题                                                         | 文章的文件名                                                 |
| `date`            | 建立日期                                                     | 文件建立日期                                                 |
| `updated`         | 更新日期                                                     | 文件更新日期                                                 |
| `comments`        | 开启文章的评论功能                                           | true                                                         |
| `tags`            | 标签（不适用于分页）                                         |                                                              |
| `categories`      | 分类（不适用于分页）                                         |                                                              |
| `permalink`       | 覆盖文章的永久链接，永久链接应该以 `/` 或 `.html` 结尾       | `null`                                                       |
| `excerpt`         | 纯文本的页面摘要。使用 [该插件](https://hexo.io/zh-cn/docs/tag-plugins#文章摘要和截断) 来格式化文本 |                                                              |
| `disableNunjucks` | 启用时禁用 Nunjucks 标签 `{{ }}`/`{% %}` 和 [标签插件](https://hexo.io/zh-cn/docs/tag-plugins) 的渲染功能 | false                                                        |
| `lang`            | 设置语言以覆盖 [自动检测](https://hexo.io/zh-cn/docs/internationalization#路径) | 继承自 `_config.yml`                                         |
| `hide`            | 首页隐藏文章                                                 | false                                                        |

```markdown
categories:
- 分类名称
tags:
- 标签名称
- 标签名称2
```

#### 便签

```markdown
{% note success %}
文字 或者 `markdown` 均可
{% endnote %}
```

可选便签：

{% note primary %}
primary
{% endnote %}

{% note secondary %}
secondary
{% endnote %}

{% note success %}
success
{% endnote %}

{% note danger %}
success
{% endnote %}

{% note warning %}
success
{% endnote %}

{% note info %}
success
{% endnote %}

{% note light %}
success
{% endnote %}

#### 行内便签

{% label primary @你好 %}

```markdown
{% label primary @你好 %}
```

可选 label ：

{% label primary @primary %}{% label default @default %}{% label info @info %}{% label success @success %}{% label warning @warning %}{% label danger @danger %}

`你好` =  {% label default @你好 %}

```markdown
`你好` = {% label default @你好 %}
```



#### 按钮

```markdown
{% btn url路径, 显示的文字, 鼠标悬停的文字 %}
```

{% btn #, 显示的文字, 鼠标悬停的文字 %}

#### 组图

如果想把多张图片按一定布局组合显示，你可以在 markdown 中按如下格式：

```markdown
{% gi total n1-n2-... %}
  ![](url)
  ![](url)
  ![](url)
  ![](url)
  ![](url)
{% endgi %}
```

total：图片总数量，对应中间包含的图片 url 数量
n1-n2-...：每行的图片数量，可以省略，默认单行最多 3 张图，求和必须相等于 total，否则按默认样式

如下图为 `{% gi 5 3-2 %}` 示例，代表共 5 张图，第一行 3 张图，第二行 2 张图。

![组图](https://hexo.fluid-dev.com/docs/assets/img/group_image.c1b58381.png)

### 配置

```markdown
title: 标题
date: 时间
tags: [标签, 标签1]
categories: [分类]
author: 作者
permalink: 永久链接.html
hide: false
```

