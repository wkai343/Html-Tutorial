# Html Tutorial

---

---

- html主要包含标签、属性
- 标签有单标签和双标签
  - 双标签用来给标签之间的内容设置属性
  - 单标签常用的有br,hr,link,可以用 **/** 结尾，如`<hr/>`
- 有些属性是布尔属性，不需要给定值，如ol中的reversed
- 代码不区分大小写

---

注释:

```html
<!-- -->
```

特殊字符

|符号代码|显示结果|说明|
|---|---|---|
|`&nbsp;`|&nbsp;|不断行空格|
|`&ensp;`|&ensp;|半角空格|
|`&emsp;`|&emsp;|全角空格|
|`&lt;`|<|小于|
|`&gt;`|>|大于|
|`&amp;`|&|&符|
|`&times;`|×|乘|
|`&divide;`|÷|除|
|`&quot;`|"|双引号|
|`&copy;`|©|版权|
|`&reg;`|®|注册商标|
|`&trade;`|™|商标|

*其他特殊字符可参阅文档*

---

## 全局属性

html具有一些全局属性，全局属性是通用的，所有HTML元素都可以指定。

<small>
accesskey
autocapitalize
autofocus
contenteditable
dir
draggable
enterkeyhint
hidden
inert
inputmode
is
itemid
itemprop
itemref
itemscope
itemtype
lang
nonce
popover
spellcheck
style
tabindex
title
translate
</small>

### lang属性

- 指定了该元素内容， 以及该元素包含文本的属性的主要语言。
- 如果元素省略了这些属性，该元素的语言就是其父元素的语言（如果有的话）。
- 鼓励作者在根 html 元素上指定 lang 属性，给出文档的语言。这可以帮助语音合成工具确定要使用的发音，帮助翻译工具确定要使用的规则，等等。

### title属性

- 表示元素的建议信息。
  - 在链接上，这可能是目标资源的标题或描述；在图片上，它可以是图片来源或图片的描述；在段落上，它可能是文本的脚注或评论；在引用上，可以是来源的进一步信息； 在交互式内容上，它可能是元素的标签或使用说明；等等。
- 有些元素比如 link， abbr，和 input 为 title 属性定义了额外的语义。

### id属性

- 定义唯一标识符（ID）

*其他全局可参阅[文档](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Global_attributes#id)*

---

---

html文件结构大抵如此

```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Document</title>
    </head>
    <body>
        Hello
    </body>
</html>
```

`<!DOCTYPE html>`是html文档声明，页面需要处于第一行的文档声明

html可以有属性lang，如`lang="en"`

---

---

## Head

- head中主要包含元数据内容
  - 元数据内容是设置其余内容的呈现或行为，设置文档与其他文档的关系，传达其他“带外”信息的内容。
  - ⇒ base, link, meta, noscript, script, style, template, title等

|标签名|描述|
|:---:|---|
|head|文档信息|
|title|标题|
|base|链接的默认地址或默认目标|
|link|文档与外部资源之间的关系|
|meta|元信息|
|script|客户端脚本|
|style|文档样式|

### title

- 表示文档的标题或名称
- 必须要有的

```html
<head>
    <title>Title of the document</title>
</head>
```

### base

- 为页面上的所有链接规定默认根地址
- 只能有一个

属性有href和target

```html
<!-- 引用自w3c -->
<head>
    <title>This is an example for the &lt;base&gt; element</title>
    <base href="https://www.example.com/news/index.html">
</head>
<body>
    <!-- https://www.example.com/news/archives.html -->
    <p>Visit the <a href="archives.html">archives</a>.</p>
</body>
```

### link

- 链接一个与当前文档存在关系的外部资源

```html
<!-- 加载图标 -->
<link rel="icon" href="img/icon.jpg">
```

### meta

- 不会显示在页面上，但是对于机器是可读的
- 可以有多个

meta常用属性有charset, http-equiv, name, content

|属性|值|说明|
|---|---|---|
|charset||字符集编码|
|name|author\|description\|keywords\|generator|作者\|描述\|关键字\|编辑器|
|name|[viewport](#viewport)|设置视口，改善网站在各种设备上的外观|
|name|application-name|Web应用程序的名称(如果不是，不得使用)|
|http-equiv|refresh|文档的刷新时间（和刷新后的地址）|
|http-equiv|set-cookie|设置cookie|
|http-equiv|content-security-policy|内容安全策略|
|http-equiv|default-style|预定义样式表,content须匹配同一文档中的一个link或style元素上title|
|content|\<context\>|name或http-equiv属性关联的值|

#### viewport

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

---

---

## Body

- body属性有text,bgcolor,alink,link,vlink,background,top(bottom/left/right)margin...
- 以上属性已弃用，用CSS代替

[Body属性](Body.md)

---

### 段落与换行

#### 段落

- align已弃用

```html
<p>段落</p>
```

#### 换行

- clear已弃用

```html
<br>
```

### 分隔线

- 属性已弃用

<!-- |属性|值|说明|
|:---:|---|---|
|width|px或%|宽度|
|size|px(整数)|高度|
|color|rgb,十六进制,英文名|颜色|
|align|left\|center\|right|对齐方式| -->

```html
<hr>
```

### 文本修饰

|标签名|效果预览|说明|
|:---:|---|---|
|strong|<strong>你好</strong>|定义粗体|
|em|<em>你好</em>|定义斜体|
|del|<del>你好</del>|定义删除|
|sup|<sup>你好</sup>|定义上标|
|sub|<sub>你好</sub>|定义下标|
|small|<small>你好</small>|变小|

#### ruby标记

- 用来注音

```html
<ruby>
    中<rt>zhong</rt>
</ruby>
```

效果:
<ruby>
    中<rp>(</rp><rt>zhong</rt><rp>(</rp>
</ruby>

### 标题

- 6级

```html
<h1></h1>...<h6></h6>
```

### 列表

- 有序列表
- 无序列表
- 定义列表
- 菜单列表
- 目录列表


```html
<li>列表项</li>
```

#### 无序列表

|属性|值|说明|
|---|---|---|
|type|disc|实心圆形|
|type|circle|空心圆形|
|type|square|实心正方形|

```html
<ul>
    <li>stdin</li>
    <li>stdout</li>
    <li>stderr</li>
</ul>
```

#### 有序列表

|属性|值|说明|
|---|---|---|
|reversed||降序，布尔类型|
|type|a\|A|小写\|大写英文|
|type|i\|l|小写\|大写罗马|
|type|1|数字(默认)|
|start|"<数字>"|开始|
|value|"<数字>"|对于**li**,改变当前列表项的值，并影响其后|

```html
<ol>
    <li>stdin</li>
    <li>stdout</li>
    <li>stderr</li>
</ol>
```

#### 定义列表

```html
<dl>
    <dt>项目1</dt>
        <dd>描述1</dd>
        <dd>描述2</dd>
    <dt>项目2</dt>
        <dd>描述1</dd>
        <dd>描述2</dd>
</dl>
```

### 表格

- 部分属性已弃用

|标签名|说明|
|:---:|---|
|table|表格|
|tr|行|
|th|标题|
|td|数据|

#### 合并单元格

|属性|值|说明|
|:---:|---|---|
|rowspan|"\<整数\>"|跨行|
|colspan|"\<整数\>"|跨列|

#### 结构化

- 按行分组
- body可以有多个

|标签名|说明|
|:---:|---|
|caption|表格|
|thead|头|
|tbody|主体|
|tfoot|尾|

#### 直列化

- 按列分组

|标签名|说明|
|:---:|---|
|colgroup|列组|

```html
<!-- 前两列为一组 -->
<colgroup>
    <col>
    <col>
</colgroup>
```

### 预格式化

```html
<pre>预格式化文本</pre>
```

### 引用

|属性|值|说明|
|:---:|---|---|
|cite|\<url\>||

#### 行引用

- 用来引用短的文本

```html
<q>行引用</q>
```

#### 块引用

- 会将标签内的文字缩进

```html
<blockquote>块引用<blockquote>
```

### 代码

```html
<code>print(x)</code>
```

### 链接

#### target属性

|属性|值|说明|
|:---:|:---:|---|
|target|_self|在当前页面打开被链接文档（默认值）|
||_blank|通常在新标签页打开，但用户可以通过配置选择在新窗口打开。|
||_parent|在父框架中打开被链接文档|
||_top|在最顶级打开|

#### a

|属性|值|说明|
|:---:|---|---|
|href|锚#\<id\>\|本地\|网络\|tel:\|mailto:|链接对象|
|target|_self\|_blank\|_parent\|_top|打开方式|

```html
<a href="minecraft.jpg" title="minecraft">链接</a>
<a href="#书签id">书签标题</a> <!-- 同一页面 -->
<a href="url#书签id">书签标题</a> <!-- 不同页面 -->
```

##### onclick事件

- 锚点元素经常被滥用为假按钮，将其 href 设置为 # 或 javascript:void(0) 以防止页面刷新，然后监听其 click 事件。
- 这些假的 href 值在复制/拖动链接、在新的标签/窗口中打开链接、书签，或当 JavaScript 正在加载、出错或被禁用时，会导致意外行为。它们还向辅助技术（如屏幕阅读器）传达不正确的语义。

### 图片

- src必须，其他可选
- allign已弃用
- 可套超链接

|属性|值|说明|
|:---:|:---:|---|
|src|本地/网络|路径地址|
|alt||替换文本|
|width\|height|整数(px)|宽度\|高度|

```html
<img alt="替换文本" src="minecraft.jpg" title="图片">
```

#### 热区链接

|标签名|说明|
|:---:|---|
|map|图像映射元素|
|area|热点区域|

#### map

|属性|值|说明|
|:---:|:---:|---|
|name||必须存在，值不得为空并且不能带空格;如果还指定了 id 属性，则两个属性的值必须相同|

##### area

|属性|值|说明|
|:---:|:---:|---|
|href|||
|alt||在href使用时是必须的|
|shape|default(默认)\|rect\|circle\|poly|整个\|矩形\|圆形\|多边形|
|coords|整数(px)|[坐标值](#坐标)|
|target|||

```html
<!-- 引用自https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/map -->
<map name="primary">
  <area
    shape="circle"
    coords="75,75,75"
    href="https://developer.mozilla.org/docs/Web/JavaScript"
    target="_blank"
    alt="JavaScript" />
  <area
    shape="circle"
    coords="275,75,75"
    href="https://developer.mozilla.org/docs/Web/CSS"
    target="_blank"
    alt="CSS" />
</map>
<img
  usemap="#primary"
  src="parrots.jpg"
  alt="两只鹦鹉的照片，大小为 350 x 150" />
```

###### 坐标

> 对于矩形或长方形，这个 coords 值为两个 x,y 对：左上、右下。对于圆形，这个值是 x,y,r，这里的 x,y 是一对确定圆的中心的坐标而 r 则表示的是半径值。对于多边和多边形，这个值是用 x,y 对表示的多边形的每一个点：x1,y1,x2,y2,x3,y3 等等。

### 行级和块级

- 块级自动换行，宽度默认100%
- 行级不会自动换行，宽度由内容决定

#### 行级

##### span

- 短语内容通用行容器
- 使用class或是id属性定义内容的格式

#### 块级

##### div

- 流内容通用块容器
- 使用class或是id属性定义内容的格式
- allign已弃用

### 结构标签

section, article, aside, header, footer, nav, hgroup

Todo

### 表单

- 由表单控件组成，主要包括输入信息和表单提交

|属性|值|说明|
|:---:|:---:|---|
|action||服务器地址|
|method|get(默认)\|post|提交数据的方法|
|enctype||发送编码的方式，当method="post"|
|novalidate||表示不需要验证表单，布尔类型|
|target||提交表单后，显示响应信息位置|

#### enctype属性

- application/x-www-form-urlencoded(默认)
- multipart/form-data: 不对字符编码，用于上传文件时使用
- text/plain: 将空格转换为“+”符号，但不编码特殊字符，通常在将表单发送到电子
邮箱时使用。

#### label

- 用户界面中某个元素的说明
- 程序上与元素关联，扩展可点击区域

|属性|值|说明|
|:---:|:---:|---|
|for|\<元素的id\>|与元素建立关联|

#### input

|属性|值|说明|
|:---:|:---:|---|
|type|text(默认)...|类型|
|name\|id|||
|placeholder||提示信息|
|value||默认值|
|tabindex||tab顺序|
|checked||默认选中|
|disabled||不能使用|

##### type属性

- text: 文本输入框
- password: 密码输入框
- radio: 单选按钮
- checkbox: 复选框
- file: 文件上传按钮
- submit: 表单提交按钮
- image: 图形提交按钮
  - 用src属性设置图片路径
- reset: 重置按钮
- button: 可单击按钮
  - 可设置onclick事件

Todo

### 附录

#### 内容分类

<!-- 
## 内容模型

- "nothing"内容模型
- 内容种类
  - 元数据内容
  - 流式内容
  - 切片内容
  - 标题内容
  - 措辞内容
  - 嵌入内容
  - 互动内容
  - 可触及的内容
  - 脚本支持元素
- 透明内容模型
- 段落

### 元数据内容

元数据内容是设置其余内容的呈现或行为， 设置文档与其他文档的关系，传达其他“带外”信息的内容。
⇒ base, link, meta, noscript, script, style, template, title等

*其他内容模型可参阅文档* -->