## HTML 概念

HTML 是用来描述网页的一种语言。

- HTML 指的是超文本标记语言: **H**yper**T**ext **M**arkup **L**anguage
- HTML 不是一种编程语言，而是一种**标记**语言
- 标记语言是一套**标记标签** (markup tag)
- HTML 使用标记标签来**描述**网页
- HTML 文档包含了HTML **标签**及**文本**内容
- HTML文档也叫做 **web 页面**

## HTML 基础

### HTML 标签

HTML 文档由 HTML 元素定义。元素通常由标签表示。

HTML 标记标签通常被称为 HTML 标签 (HTML tag)。

- HTML 标签是由_尖括号_包围的关键词，比如 `<html>`
- HTML 标签通常是_成对出现_的，比如 `<b>` 和 `</b>`
- 标签对中的第一个标签是_开始标签_，第二个标签是_结束标签_
- 开始和结束标签也被称为_开放标签_和_闭合标签_

**<标签>内容</标签>**

[HTML 标签列表(字母排序)](https://www.runoob.com/tags/html-reference.html)

### HTML 属性

属性是 HTML 元素提供的附加信息。

属性总是以 name="value" 的形式写在标签内，**name** 是属性的名称，**value** 是属性的值。

```html
<a href="http://www.runoob.com">这是一个链接</a>
```

## 实例解析

```html
<!DOCTYPE html>
<html> 
<head> 
	<meta charset="utf-8"> 
	<title>菜鸟教程(runoob.com)</title> 
</head> 
<body> 
	<h1>我的第一个标题</h1> 
	<p>我的第一个段落。</p> 
</body> 
</html>
```

- `<!DOCTYPE html>`： 声明为HTML5文档
- `<html>`~`</html>`：一个完整的HTML页面，所有内容包含在其中
- `<head>`~`</head>`：包含了文档的元（meta）数据
- `<body>`~`</body>`：包含了可见的页面内容

## `<head>`

`<head>` 元素包含了所有的头部标签元素。在 `<head>`元素中你可以插入脚本（scripts）, 样式文件（CSS），及各种meta信息。

可以添加在头部区域的元素标签为: `<title>, <style>, <meta>, <link>, <script>, <noscript> 和 <base>`。

### `<title>`

```html
<title>页面标题</title>
```

### `<base>`

描述基本的链接地址/链接目标，作为HTML文档中所有的链接标签的默认链接

```html
<head>
<base href="http://www.runoob.com/images/" target="_blank"> </head>
```

### `<link>`

定义了文档与外部资源之间的关系，通常用于链接到样式表

```html
<head> 
<link rel="stylesheet" type="text/css" href="mystyle.css">
</head>
```

### `<style>`

定义了HTML文档的样式文件引用地址

默认为全局样式
`.classname`类选择器，对具体的类确定规则
`.classname a`仅对该类中的`<a>`确定规则

```html
<head>
<style type="text/css">
body { background-color:yellow;
}
p { color:blue }
.header {
text-decoration: none;
color: rgba(14, 14, 14, 0.734);
}
.headerItem a {
text-decoration: none;
color: rgba(14, 14, 14, 0.734);
}
</style>
</head>
```
### `<meta>`

描述了一些基本的元数据，不显示在页面上，但会被浏览器解析

```html
<meta charset="UTF-8">
<meta name="author" content="Runoob">
<meta http-equiv="refresh" content="30">
```

### `<script>`

用于加载脚本文件

## `<body>`

### 标题

```html
<h1>一级标题</h1>
<h2>二级标题</h2>
<h3>三级标题</h3>
<h4>四级标题</h4>
<h5>五级标题</h5>
<h6>六级标题</h6>
```

不要仅仅是为了生成**粗体**或**大号**的文本而使用标题，搜索引擎使用标题为您的网页的结构和内容编制索引。

### 链接

```html
<a href="https://www.runoob.com">这是一个链接使用了 href 属性</a>
```

#### 锚点链接

```html
<a href="#section2">跳转到第二部分</a>
<!-- 在页面中的某个位置 -->
<a name="section2"></a>
```

#### 下载链接

```html
<a href="document.pdf" download="filename">下载文档</a>
```

#### target属性

定义链接打开的位置

```html
<a href="https://www.runoob.com/" target="_blank" rel="noopener noreferrer">访问菜鸟教程!</a>
```

#### id属性

创建一个HTML文档书签，在页面中不显示，可以通过链接访问跳转

```html
<a id="tips">有用的提示部分</a>
```

```html
<a href="#tips">访问有用的提示部分</a>
<a href="https://www.runoob.com/html/html-links.html#tips">
访问有用的提示部分</a>
```

### 图片

``` html
<img src="/images/logo.png" width="258" height="39" alt="xxx"/>
```

可嵌套在*链接*中，点击图片跳转

alt代表无法加载图像时的替代文本信息

#### 图像映射

```html
<img src="planets.gif" width="145" height="126" alt="Planets" usemap="#planetmap">

<map name="planetmap">
  <area shape="rect" coords="0,0,82,126" alt="Sun" href="sun.htm">
  <area shape="circle" coords="90,58,3" alt="Mercury" href="mercur.htm">
  <area shape="circle" coords="124,58,8" alt="Venus" href="venus.htm">
</map>
```

设定图片中的某部分区域，点击后映射到另一链接

### 水平线

```html
<hr />
<hr>
```

### 段落

```html
<p>段落1</p>
<p>段落2</p>
```

段落在源代码中的分行不会体现在浏览器中，浏览器根据串钩大小改变段落行数。

### 分行

```html
<p>这个<br>段落<br>演示了分行的效果</p>
```

### 文本格式化

#### 加粗（bold）

```html
<b>xxx</b>
<strong>xxx</strong>
```

#### 斜体（italic）

```html
<i>xxx</i>
<em>xxx</em>
```

更多标签[HTML 文本格式化 | 菜鸟教程 (runoob.com)](https://www.runoob.com/html/html-formatting.html)

### 表格

```html
<table>  
  <thead>  
    <tr>  
      <th>列标题1</th>  
      <th>列标题2</th>  
      <th>列标题3</th>  
    </tr>  
  </thead>  
  <tbody>  
    <tr>  
      <td>行1，列1</td>  
      <td>行1，列2</td>  
      <td>行1，列3</td>  
    </tr>  
    <tr>  
      <td>行2，列1</td>  
      <td>行2，列2</td>  
      <td>行2，列3</td>  
    </tr>  
  </tbody>  
</table>
```

### 列表

#### 无序列表

```html
<ul style="xxx">  
<li>Coffee</li>  
<li>Milk</li>  
</ul>
```

#### 有序列表

```html
<ol type="xxx">  
<li>Coffee</li>  
<li>Milk</li>  
</ol>
```

#### 自定义列表

```html
<dl>  
<dt>Coffee</dt>  
<dd>- black hot drink</dd>  
<dt>Milk</dt>  
<dd>- white cold drink</dd>  
</dl>
```

### 区块

使用 `<div>` 和 `<span>`将元素组合起来

#### 区块元素

大多数 HTML 元素被定义为**块级元素**或**内联元素**。

块级元素在浏览器显示时，通常会以新行来开始（和结束）。

实例: `<h1>, <p>, <ul>, <table>`

#### 内联元素

内联元素在显示时通常不会以新行开始。

实例: `<b>, <td>, <a>, <img>`

#### `<div>`

块级元素，用于组合其他HTML元素，与CSS共同使用，可以对其中的块内容设置样式

#### `<span>`

内敛元素，与CSS共同使用，可以对部分文本设置样式

### 布局

通过`<div>`为元素布局，可以创建多列布局

### 框架

在同一个浏览器窗口中显示不止一个页面

```html
<iframe src="URL"></iframe>
```

### 脚本

JavaScript 使 HTML 页面具有更强的动态和交互性

[JavaScript 教程 | 菜鸟教程 (runoob.com)](https://www.runoob.com/js/js-tutorial.html)

JavaScript 可以触发事件，就像按钮点击

### 速查列表

[HTML 速查列表 | 菜鸟教程 (runoob.com)](https://www.runoob.com/html/html-quicklist.html)

### 样式CSS

#### 内联样式

```html
<body style="background-color:yellow;">
<h2 style="background-color:red;">这是一个标题</h2>
<p style="background-color:green;font-size:20px;">这是一个段落</p>
</body>
```

#### 内部样式表

```html
<head>
<style type="text/css">
body {background-color:yellow;}
p {color:blue;}
</style>
</head>
```

#### 外部样式表

当样式需要被应用到很多页面的时候，外部样式表将是理想的选择。使用外部样式表，你就可以通过更改一个文件来改变整个站点的外观。

```html
<head>
<link rel="stylesheet" type="text/css" href="mystyle.css">
</head>
```

引入外部样式表后，可以直接使用内部的样式类别