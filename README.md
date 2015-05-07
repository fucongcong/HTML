# HTML

####1.[HTML简介](#user-content-html简介)
- [开发工具](#user-content-1开发工具)
- [HTML是什么？](#user-content-2html是什么)
- [HTML这四个字母代表什么呢？](#user-content-3html这四个字母代表什么呢)

####2.[标签与元素](#user-content-标签与元素)
- [认识标签，元素和属性](#user-content-认识标签元素和属性)
    - 标签
    - 属性
    - 元素
    - 空元素
    - 块元素和内联元素
    - 素之间是可以嵌套的
- [标题与段落](#user-content-标题与段落)
    - 标题
    - 段落
- [链接与图像](#user-content-链接与图像)
    - 链接
    - 图像
- [列表](#user-content-列表)
    - 无序列表
    - 有序列表
    - 定义列表
- [表单](#user-content-表单)
    - 输入标签(`<input>`)
    - 文本标签(`<textarea>`)
    - 控制标签(`<label>`)
    - 选择列表标签(`<select>`)
    - 定义域标签(`<fieldset>`)
    - 按钮标签(`<button>`)
- [表格](#user-content-表格)

####3.[HTML的头部元素](#user-content-html的头部元素)
- [文档的类型](#user-content-文档的类型)
- [标题](#user-content-标题)
- [外部资源](#user-content-外部资源)
- [元数据](#user-content-元数据)
- [针对搜索引擎的关键词](#user-content-针对搜索引擎的关键词)
- [属性](#user-content-属性)
- [JS脚本](#user-content-js脚本)

####4.[HTML布局](#user-content-html布局)

####5.[完成你的第一个网站](#user-content-完成你的第一个网站)

访问[php.xitongxue.com观看课程](http://php.xitongxue.com)

## HTML简介
####1.开发工具
（1）浏览器：浏览你写的网站
          推荐：谷歌（chrmoe），火狐（firefox），当然还有360，IE，猎豹，腾讯等等浏览器

（2）开发工具：Sublime Text （请观看Sublime Text 课程），记事本，eclipse， netbeans等等

####2.HTML是什么？
简要的说HTML 是用来描述网页的一种语言。

####3.HTML这四个字母代表什么呢？
HTML是“HyperText Mark-up Language（超文本标记语言）”的缩写

“超文本”就是指页面内可以包含图片、链接，甚至音乐、程序等非文字元素。
标记语言是一套标记标签 (markup tag)
HTML 使用标记标签来描述网页

## 标签与元素

###认识标签，元素和属性
------
    
####1.标签
    标签就是<head>、<body>、<table>等被尖括号“<”和“>”包起来的对象，绝大部分的标签都是成对出现的，如<table></talbe>、<form></form>。当然还有少部分不是成对出现的，如<br>、<hr>等。
    
####2.属性
    HTML 标签可以拥有属性。属性提供了有关 HTML 元素的更多的信息。
    属性总是在 HTML 元素的开始标签中规定，并且它以名称/值的形式出现。如
    <a href="http://superu.org">Hello World！
    </a>
    链接的地址在href属性中指定！
    常用的一些元素属性：class，id，style，title

####3.元素
    HTML元素是构建网页的一种单位,是由HTML标签和HTML属性组成的,HTML元素也是网页中的一种基本单位.如
    <a href="http://superu.org">
        Hello World！！
    </a>
    这是一段HTML链接元素
    
####4.空元素（没有内容的 HTML 元素被称为空元素，如\<br/>,\<hr/>）
    
####5.块元素和内联元素
    块级元素，通常会以新行来开始（和结束），内联元素通常不会。
####6.元素之间是可以嵌套的。
    （<div><span>Hello!</span></div>）

### 标题与段落
------
    
####1.标题
    标题（Heading）是通过 <h1> ~ <h6> 等标签进行定义的。如
    <h1>Hello World! </h1>
    <h2>Hello World! </h2>
    <h3>Hello World! </h3>
    <h4>Hello World! </h4>
    <h5>Hello World! </h5>
    
####2.段落
    段落是通过 <p> 标签(块元素)定义的。如
    <p>Hello World!</p>
    
### 链接与图像
------
####1.链接
    超链接可以是一个字，一个词，也可以是一幅图像，您可以点击这些内容来跳转到新网页或者当前网页中的某个部分。
    我们通过使用 <a> 标签在 HTML 中创建链接。
    常见属性：
    (1) href
    (2) target
    (3) name和id (可以用于锚点)

    锚点,跳转到当前网页中的某个部分,如:
        <a href="#tip1">go to tip1</a>
        <br/>
        <a href="#tip2">go to tip2</a>
        <div style="margin-top:1000px">
           <a id="tip1">这是tip1</a>
        </div>
        <div style="margin-top:1000px;margin-bottom:1000px">
           <a name="tip2"> 这是tip2</a>
        </div>
####2.图像
    在 HTML 中，图像由 <img> 标签定义。
    图像标签没有闭合标签,只有属性。
    (1)要在页面上显示图像，你需要使用源属性（src）。src 指 "source"。源属性的值是图像的 URL 地址。
    语法：
    <img src="URL" />

    URL 指存储图像的位置。

    (2)替换文本属性（alt）
    在浏览器无法载入图像时，替换文本属性告诉读者她们失去的信息。

    注意事项:一个网页，图片不予过多，并且过大的图片应该进行压缩裁剪。

### 列表
------
####1.无序列表
    无序列表是一个项目的列表，此列项目使用粗体圆点进行标记。
    <ul>
    <li>HTML</li>
    <li>CSS</li>
    </ul>
####2.有序列表
    有序列表也是一列项目，列表项目使用数字进行标记。
    <ol>
    <li>HTML</li>
    <li>CSS</li>
    </ol>
####3.定义列表
    自定义列表不仅仅是一列项目，而是项目及其注释的组合。
    <dl>
    <dt>HTML</dt>
    <dd>网站的基础语言</dd>
    </dl>

### 表单
------
    表单使用表单标签（<form>）定义。
    
    <form method="" action="" enctype="multipart/form-data"></form>
    
    enctype属性:
    application/x-www-form-urlencoded  : 在发送前编码所有字符（默认）
    multipart/form-data                : 在使用包含文件上传控件的表单时，必须使用该值。
    text/plain                         : 空格转换为 "+" 加号，但不对特殊字符编码。

####1.输入标签(\<input>)
    常见type属性:
    (1)文本域
    <input type="text" name="email" />
    (2)密码域
    <input type="password" name="name" />
    (3)单选按钮
    <input type="radio" name="sex" value="male"/>男
    <input type="radio" name="sex" value="female"/>女
    (4)复选框
    <input type="checkbox" name="address" value="杭州"/>杭州
    <input type="checkbox" name="address" value="上海"/>上海
####2.文本标签(\<textarea>)
    <textarea name="about" cols="2" rows="5"></textarea>
####3.控制标签(\<label>)
    <label for="male">男</label>
    <input type="radio" name="sex" value="male" id="male"/>
    <label for="female">女</label>
    <input type="radio" name="sex" value="female" id="female"/>
####4.选择列表标签(\<select>)
    <select name="address">
      <option value ="杭州">杭州</option>
      <option value ="上海">上海</option>
    </select>
####5.定义域标签(\<fieldset>)
    <fieldset>
        <legend>
        性别
        </legend>
        <label for="male">男</label>
        <input type="radio" name="sex" value="male" id="male"/>
        <label for="female">女</label>
        <input type="radio" name="sex" value="female" id="female"/>
    </fieldset> 
####6.按钮标签(\<button>)
    <form>
        <input type="password" name="name" />
        <button name="" type="button" >按钮</button>
        <button name="" type="reset" >重置</button>
        <button name="" type="submit" >提交</button>
    </form>

### 表格
-----------
    表格由 <table> 标签来定义。
    表格中的表头我们用<th>标签来定义。
    表格中的每一行我们用<tr>标签来定义，而每一行中的每一列用<td>来定义。
    
    ````
    <table>
    <tr>
    <th>表头1</th>
    <th>表头2</th>
    </tr>
    <tr>
    <td>第一行第一列</td>
    <td>第一行第二列</td>
    </tr>
    <tr>
    <td>第二行第一列</td>
    <td>第二行第二列</td>
    </tr>
    </table>
    ````
## HTML的头部元素
    
    这是一个最简单的HTML文件结构
    <!DOCTYPE html>
    <html>
        <head>
            <title></title>
        </head>
        <body>
        </body>
    </html>

### 文档的类型
    <!DOCTYPE> 声明帮助浏览器正确地显示网页。

### 标题
    <title> 标签定义文档的标题。

### 外部资源
    <link>  标签定义文档与外部资源之间的关系。

    链接CSS样式表,rel="stylesheet"告诉浏览器这是一个样式文件
    <head>
    <link rel="stylesheet" href="mystyle.css" />
    </head>

### 元数据
    <meta> 标签提供关于 HTML 文档的元数据。

#### 针对搜索引擎的关键词
    <meta name="description" content="系统学，学习技能的网站" />
    <meta name="keywords" content="系统学" />
    
#### 属性
    http-equiv 属性,超文本传输协议标题信息
    //最常用的字符编码
    <meta http-equiv="Content-Type" content="text/html; charset=UTF-8">
    //自动刷新跳转页面
    ＜meta http-equiv="Refresh" content="2；URL=http://xitongxue.com"＞

### JS脚本
    <script> 标签用于定义客户端脚本。
    
    <script src="demo.js"></script>

## HTML布局


## 完成你的第一个网站
