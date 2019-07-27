[TOC]
# 一、Web前端介绍
## 1. 什么是网页
网页是基于浏览器的应用程序，是数据展示的载体.
##  2. 网页的组成
1. 浏览器
	- 向服务器发送用户请求指令
	- 接收并解析数据展示给用户
2. 服务器
    - 存储数据
    - 处理并响应请求
3. 协议
    - 规范数据在传输过程中的打包方式
## 3. 网页的优势

1. 即时响应
   - 更新服务端页面即完成更新
   - 客户端重新加载即兑现内容
2. 无需安装和更新
   - 无需安装任何应用软件
   - 只需要一个浏览器执行即可

## 4. 开发前的准备

1. 运行环境：浏览器，设置chrome为默认浏览器，作为网页文件的运行环境。
2. 调试工具：浏览器自带的调试工具，使用快捷键"F12"或右键"检查"打开。
3. 开发工具：不限，选用个人习惯的即可。（Sublime、VSCode、EditPlus、Webstrom等）

# 二、 HTML语法介绍
## 1. HTML介绍
超文本标记语言浏览器能够识别和解析的语言，通过标签的形式构建页面结构和填充内容
## 2. 标签
标签也称为标记或元素，用于在网页中标记内容
1. 语法：标签使用< >为标志，标签名不区分大小写，推荐小写表示
2. 分类：
    - 双标签：成对出现，包含开始标签和结束标签。例：

    ```html
    <html></html>
    ```

    - 单标签：只有开始标签，没有结束标签，可以手动添加“/”表示闭合。例：

    ```html
    <br>
    <br/>
    ```
3. 标签属性：
	- 标签属性书写在开始标签中，使用空格与标签名隔开，用于设置当前标签的显示内容或者修饰显示效果。由属性名和属性值组成，属性值使用双引号表示。例：

    ```HTML
    <img src="imgs/img01.jpg">
    ```

	- 同一个标签中可以添加若干组标签属性，使用空格间隔。例：

    ```html
    <img src="imgs/img01.jpg" width="200px" height="200px">
    ```
## 3. 使用
1. 创建网页文件，使用.html或.htm作为文件后缀。
2. 添加网页的基本结构：
    ```html 
    <!doctype html>
    <html>
    	<head>
    		<title>网页标题</title>
    		<meta charset="utf-8">
    	</head>
    	<body>
             网页主体内容
    	</body>
    </html>
    ```
3. 标签嵌套
    在双标签中书写其他标签，称为标签嵌套
    
    - 嵌套结构中，外层元素称为父元素，内层元素称为子元素。
    - 多层嵌套结构中，所有外层元素统称为祖先元素，内层元素统称为后代元素。
    - 平级结构互为兄弟元素。
4. HTML语法规范
	- 标签名不区分大小写，建议使用小写。
	- 注释语法：
	```html
	<!-- 此处为注释 -->
	```
# 三、常用标签介绍
## 1. 基本结构解析
 ```html
<!-- 文档类型声明，便于浏览器正确解析标签及渲染样式 -->
<!doctype html> 
<!-- HTML文档开始的标志 -->
<html> 
   <!-- 头部设置，可在head中设置网页标题，引入外部的资源文件 -->
   <head>
       <!-- 设置网页标题，显示在网页选项卡上方 -->
       <title>网页标题</title>
       <!-- 设置网页字符编码 -->
       <meta charset="utf-8"> 
   </head>
   <!-- 网页主体部分，显示网页主要内容 -->
   <body> 
       网页主体内容
   </body>
</html><!-- 文档结束-->
 ```

## 2. body中常用标签
  - 文本标签
    - 标题标签：自带加粗效果，从h1到h6字体大小逐级递减
    ```html
     <h1>一级标题</h1>
     <h2>二级标题</h2>
     <h3>三级标题</h3>
     <h4>四级标题</h4>
     <h5>五级标题</h5>
     <h6>六级标题</h6>
    ```
    - 段落标签：
     ```html
     <p>段落文本</p>
     ```
    - 普通文本标签：
     ```html
     <b>加粗标签</b>
     <strong>强调标签，效果同b标签</strong>
     <i>斜体标签</i>
     <u>删除线标签</u>
     <span>行分区标签，用于对特殊文本特殊处理</span>
     <label>普通文本标签，常与表单控件结合实现文本与控件的绑定</label>
     ```
    - 换行标签：
     浏览器会忽略代码中的换行和空格，只显示为一个空格。想要实现页面中的换行，需要借助于换行标签。
     ```html
     <br>
     ```
    - 水平线标签，在页面中插入一条水平分割线
     ```html
     <hr>
     ```
    - 字符实体：
     某些情况下，浏览器会将一些特殊字符按照 HTML 的方式解析，影响显示结果。此时需要将这类字符转换为其他的形式书写。
    例：
    
    ```
     使用 &lt; 在页面中呈现 "<"
     使用 &gt; 在页面中呈现 ">"
     使用 &nbsp; 在页面中呈现一个空格
     使用 &copy; 在页面中呈现版权符号"©"
     使用 &yen; 在页面中呈现人民币符号"￥"
    ```
  - 容器标签
    常用于页面结构划分，结合CSS实现网页布局
    
       ```html
       <div id="top">页面顶部区域</div>
       <div id="main">页面主体区域</div>
       <div id="bottom">页面底部区域</div>
       ```
  - 图片与超链接标签
    - 图片标签 <img src="">：用于在网页中插入一张图片。
      1. 属性 src 用于给出图片的URL，必填。
      2. 属性 width/height 用于设置图片尺寸，取像素值，默认按照图片的原始尺寸显示。
      3. 属性 title 用于设置图片标题，鼠标悬停在图片上时显示
      4. 属性 alt 用于设置图片加载失败后的提示文本

      语法：
    ```html
    <img src="" width="" height="" title="" alt="">
    ```
    - 超链接标签：用户可以点击超链接实现跳转至其他页面
      1. 属性 href 用于设置目标文件的URL，必填。
      2. 属性 target用于设置目标文件的打开方式，默认在当前窗口打开。可以设置新建窗口打开目标文本(取"_blank")
      3. 属性href也可以指向某个id号属性的元素
    ```html
    <a href="http://www.taobao.com" target="_self">淘宝</a>
    <a href="http://www.baidu.com" target="_blank">百度</a>
    ```
## 3. 常用结构标签
  - 列表标签 
    - 无序列表
    默认用实心圆点标识列表项
     ```html
    <ul>
    	<li>list item 列表项</li> 
    	<li>list item 列表项</li>
    	<li>list item 列表项</li>
    </ul>
     ```
    - 有序列表
      默认使使用阿拉伯数字标识每条数据，可以使用start属性设置起始的值，默认为1
     ```html
     <ol>
      	<li>list item 列表项</li> 
      	<li>list item 列表项</li>
      	<li>list item 列表项</li>
      </ol>
     ```
    - 列表嵌套
    	在已有列表中嵌套添加另一个列表，常见于下拉菜单
     ```html
    <ol>
    	<li>
    		西游记
    		<ul>
    			<li>孙悟空</li>
    			<li>孙悟空</li>
    			<li>孙悟空</li>
    		</ul>
    	</li>
    </ol>
     ```

  - 表格标签
    - 表格由行和单元格组成，常用于直接的数据展示或辅助排版，基本结构如下：
    ```html
    <!-- 创建表格标签 -->
    <table>
    	 <!-- 创建行标签 -->
    	<tr>
    		<!-- 行中创建单元格以显示数据 -->
    		<td>姓名</td>
    		<td>年龄</td>
    		<td>班级</td>
    	</tr>
    	<tr>
    		<td>张三</td>
    		<td>20</td>
    		<td>一(1)班</td>
    	</tr>
    </table>
    ```
    - 单元格合并：用于调整表格结构，分为跨行合并和跨列合并，合并之后需要删除被合并的单元格，保证表格结构完整。
    
      | 单元格属性 | 作用           | 取值       |
      | ---------- | -------------- | ---------- |
      | colspan    | 跨列合并单元格 | 无单位数值 |
      | rowspan    | 跨行合并单元格 | 无单位数值 |
    
    - 合并示例代码：
    ```html
    <table border="1">
        <tr>
            <th>姓名</th>
            <td>李小明</td>
        </tr>
        <tr>
            <th rowspan="2">电话</th>
            <td>010-1234567</td>
        </tr>
        <tr>
            <td>13912321213</td>
        </tr>
    </table>
    
    <table border="1">
        <tr>
            <th>姓名</th>
            <th colspan="2">电话</th>
        </tr>
        <tr>
            <td>李小明</td>
            <td>010-1234567</td>
            <td>13912321213</td>
        </tr>
    </table>
    ```
  - 表单标签
    表单用于采集用户的信息并提交给服务器，由表单元素和表单控件组成。表单元素form负责提交数据给服务器，表单控件负责收集数据。
    
     - 表单使用<form></form>
    | 属性名   | 取值                                                         |
    | -------- | ------------------------------------------------------------ |
    | action   | 设置数据的提交地址                                           |
    | method   | 设置数据的提交方式，默认为get方式，可以设置为post            |
    | onsubmit | 设置表单数据提交时的触发事件的执行函数（事件绑定中详细介绍） |
    例如：
    ```html
    <form action="" method="" onsubmit="">
    	<!--此处为表单控件-->
    </form>
    ```
     - 表单控件使用（重点）
 表单控件用于采集用户信息，可设置以下标签属性
    
    |  属性名   |   取值  |
    | ---- | ---- |
    | type | 设置控件类型 |
    | name | 设置控件名称，最终与值一并发送给服务器 |
    | value | 设置控件的值 |
    | placeholder | 设置输入框中的提示文本 |
    | maxlength | 设置输入框中可输入的最大字符数 |
    | checked | 设置单选按钮或复选按钮的默认选中 |
    | selected | 设置下拉菜单的默认选中 |















































