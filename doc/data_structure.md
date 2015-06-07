---
title:文档的数据结构
author:zozoh
tags:
- markdown
- 解析
---

# markdown会被解析成什么

1. 会被解析成一个 HTML 
2. 不同的 markdown 语义会对应到特殊的标签
3. Java 的数据结构参见 [jsoup](http://jsoup.org/)
4. Javascript 直接就解析成 DOM 好了

# 文档元数据

1. 解析到 `<html><head>` 标签下的 `<meta>` 里
2. 元数据如果是列表，则用多个同名 `<meta>`
3. 名称为 *title* 的元数据，用 `<title>` 标签

比如

```html
<title>文档的数据结构</title>
<meta name="author" content="zozoh"/>
<meta name="tags" content="markdown"/>
<meta name="tags" content="解析"/>
```

# 标题

```markdown
This is an H1
=============

This is an H2
-------------

# 这是 H1

## 这是 H2

###### 这是 H6
```

解析成

```html
<h1>This is an H1</h1>
<h2>This is an H2</h2>

<h1>这是 H1</h1>
<h2>这是 H2</h2>
<h6>这是 H6</h6>
```

还有很多，待我一个个写来，基本上会先抄：
http://wowubuntu.com/markdown/





