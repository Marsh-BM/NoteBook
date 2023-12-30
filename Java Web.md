# 1.HTML

## 1.1 HTML介绍

HTML：指的是超文本标记语言 ----决定页面上显示什么内容

## 1.2 HTML的基础标签

```
<html>
    <head>
        <title>Hello</title>
        <meta charset = "UTF-8">
    </head>

    <body>
        Hello World!<br/>你好，HTML！
        <p>这是第一个段落</p>
        <p>这是第二个段落</p>
        <img src="imgs/Catgirl.jpg" width="57" height="73" alt="这里是一张图片"/>
        <h1>标题一</h1>
        <h2>标题一</h2>
        <h3>标题一</h3>
        <h4>标题一</h4>
        <h5>标题一</h5>
        <h6>标题一</h6>

        武林高手排行榜
        <ol type="a" >
            <li>实验体1</li>
            <li>实验体2</li>
            <li>实验体3</li>
            <li>实验体4</li>
            <li>实验体5</li>
        </ol>

        计划表
        <ul type="circle">
            <li>plan1</li>
            <li>plan2</li>
            <li>plan3</li>
            <li>plan4</li>
            <li>plan5</li>
        </ul>

        今天天气<b>正好</b>，是个<I>死</I>去的好日子。<br/>

        水分子的化学式: H<sub>2</sub>O<br/>
        氧气的化学式：O<sup>2</sup><br/>

        <span>什么人能一天离婚两次啊！！！</span><br/>
        <a href="https://www.baidu.com">百度一下</a>




    </body>
</html>
```

```
<!--
1.
    html语言是解释型语言，并非编译性
    浏览器是容错的

2.
    html页面由一组标签组成：<html></html>
    <html>称之为开始标签
    <html>称之为结束标签
3.
    <title> 为网页的标题
4.
    <meta> 表示在标签中设置编码方式
5.
    <br/>表示换行。注意br标签是一个单标签，即开始标签和结束标签是同一个。
6.
    <p></p>表段落标签
7.
    <img> 标签图片标签
      src属性表示图片文件标签
      width和height表示图片的大小
      alt表示图片的提示
8。
    路径问题：
    1.相对路径
    2.决定路径
9.
    <h></h> 用于标题（分为6级）
10.
    ol 有序列表
       start 表示从*开始，type显示的类型：A a I i 1
11.
    ul 无序列表
        type = disc(default), circle, square

12.
字体特效
<b></b>加粗
<i></i>斜体
<u></u>下划线
三者可以随意嵌套

13.
字体下标
<sub></sub> 字体下标
<sup></sup> 字体上标

14.
各种符号（实体符号）
这种符号很多，直接百度搜索html实体符号

15.
进行独立修饰
<span></span>

16.
超链接
<a></a>
    href 连接的地址
    target：_self 在本窗口打开
            _blank 在一个窗口打开
            _parent 在父窗口打开
            _top 在顶层窗口打开
```

```
17.
表格 table
    行   tr
    列   td
    表头  th

    table中有以下属性（虽然已经淘汰，但是还是需要了解一下）
    - width: 表格的宽度
    - cellspacing: 单元格间距
    - cellpadding：单元格填充
    - border：表格边框的粗细

    tr中有一个属性：align -> center, left, right(左对齐，右对齐，居中对齐)
    td中有两个参数 rowspan和columspan 分别用来行合并和列合并如rowspan="2"表示跨两行合并，
    
18.
<hr/> 表示直线
```

```
frameset 表示页面框架，这个标签已经淘汰，仅了解，不需要掌握
frameset表示在框架中的具体页面引用

iframe 在一个页面里嵌入一个子页面
```

#### 1.2.2 html

html页面由一组标签组成：<html></html>

  <html>称之为开始标签

  <html>称之为结束标签

#### 1.2.3 title 

  <title> 为网页的标题

#### 1.2.4 meta

    <meta> 表示在标签中设置编码方式

#### 1.2.5 br

  <br/>表示换行。注意br标签是一个单标签，即开始标签和结束标签是同一个。

#### 1.2.6 P 段落标签

    <p> </p>表段落标签

#### 1.2.7 img 图片标签

​    <img> 标签图片标签

   src属性表示图片文件标签

   width和height表示图片的大小

   alt表示图片的提示

#### 1.2.8路径问题

  路径问题：

  1.相对路径

  2.决定路径

#### 1.2.9 h 段落标签

  <h></h> 用于标题（分为6级）

#### 1.2.10 ol 有序序列

  ol 有序列表

​    start 表示从*开始，type显示的类型：A a I i 1

#### 1.2.11 ul 无序标签

  ul 无序列表

​    type = disc(default), circle, square

#### 1.2.12 字体特效

字体特效

<b></b>加粗

<i></i>斜体

<u></u>下划线

三者可以随意嵌套

 

#### 1.2.13 sup sub字体上下标

字体下标

<sub></sub> 字体下标

<sup></sup> 字体上标

 

#### 1.2.14 实体符号

各种符号（实体符号）

这种符号很多，直接百度搜索html实体符号

 

#### 1.2.15 span独立修饰

进行独立修饰

<span></span>

 

#### 1.2.16 a超链接

超链接

<a></a>

  href 连接的地址

  target：_self 在本窗口打开

​      _blank 在一个窗口打开

​      _parent 在父窗口打开

​      _top 在顶层窗口打开

#### 1.2.17 table 表格

表格 table
  行  tr
  列  td
  表头  th

  table中有以下属性（虽然已经淘汰，但是还是需要了解一下）
  \- width: 表格的宽度
  \- cellspacing: 单元格间距
  \- cellpadding：单元格填充
  \- border：表格边框的粗细

  tr中有一个属性：align -> center, left, right(左对齐，右对齐，居中对齐)
  td中有两个参数 rowspan和columspan 分别用来行合并和列合并如rowspan="2"表示跨两行合并，

#### 1.2.18 hr 直线

< hr / >



#### 1.2.19 form表单
form

#### 1.2.20 input
input type="text" 表示文本框，其中name属性必须要指定，否则这个文本框不会发送给服务器
input type="password" 表示密码框
input type="radio" 表示单选框。需要注意的是，name属性保持一致，这样才会有互斥效果，可以通过checked(checked="checked")属性来设置默认选项中的选项
input type="checkbox"  表示复选框。name属性建议保持一致，这样将来我们服务器端获取值的时候取的是一个数组。
select 表示下拉列表。 每一个选项是option，其中value属性是发送给服务器的值，selected表示默认选中的值
textarea 表示多行文本框
input type="submit" 表示提交按钮
input type="reset" 表示重置按钮
input type="button" 表示普通按钮

#### 1.2.21 Frameset  iframe页面框架

frameset 表示页面框架，这个标签已经淘汰，仅了解，不需要掌握
frameset表示在框架中的具体页面引用

iframe 在一个页面里嵌入一个子页面

# 2. CSS

## 2.1 为什么需要CSS

为了装饰

## 2.2 CSS的基本分类

### 2.2.1 标签类样式

```
/* 标签样式类*/
p{
    color:red;
}
```

在该样式分类下的语句执行以下修饰

```
<p>段落1</p>
<p class="f20">段落2</p>
<p>段落3</p>
<p id="sp4">段落4</p>
<p>段落5</p>
```

### 2.2.2 类样式表

```
/* 类样式 */
 .f20{
    font-size:20px;
 }
```

使用class="f20"对相关语句进行修饰

```
<p class="f20">段落2</p>
```

### 2.2.3 ID样式表

```
/* ID 样式 */
#sp4{
     background-color:pink;
     font-size:24px;
     font-weight:bolder;
     font-style:italic;
     font-family:"华文彩云";
}
```

使用 id="sp4"进行修饰

```
<p id="sp4">段落4</p>
```

### 2.2.4 组合样式

```
/* 组合样式  表示在div内部的p类都按照以下语句进行修饰*/
div p{
     color:blue;
}
/* class32 */
div .f32{
     font-size:32px;
     font-family: "黑体"
}
```

表示在div内部的p类都按照以下语句进行修饰

```
<div>
    <p><span>Hello</span></p>
    <span class="f32">World</span>
    <p>!!!</p>
</div>
```

## 2.2 CSS的位置分类

<font color='red'>内部标签的优先级会更高</font>

### 2.2.1 嵌入式样式表

### 2.2.2 内部样式表

### 2.2.3 外部样式表

### 2.2.4 如何引用外部的样式表

```
<link rel="stylesheet" href="css/demo01.css">
```

![image-20220719191804580](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220719191804580.png)

## 2.3 CSS盒子模型

IE浏览器：实际尺寸=width

Chrome：实际尺寸=width+左右borderwidth+padding

CSS盒子模型：

1.border ：边框

2.margin：间距

3.padding：填充

* 可以使用<font color="blue">body{margin=0 }  来消除div和页面之间的间距 </font>

## 2.4 CSS布局

### 2.4.1 Posistion

absolute：--绝对定位：需要配合left和top

relative：-- 相对定位：一般会和float，margin，padding一起使用。

```
<html>
<head>
    <meta charset="UTF-8">
    <style type="text/css">
        body{
            margin:0;
            padding:0;
        }
    </style>
    <link rel="stylesheet" href="css/demo2.css">

</head>

<body>
    <!--
        <div id="div1">&nbsp;</div>
        <div id="div2">&nbsp;</div>
    -->

    <div id="div3">
        <div id="div4">&nbsp;</div>
        <div id="div5">&nbsp;</div>
    </div>
</body>
</html>
```

```
#div1{
    width:200px;
    height:50px;
    background-color:greenyellow;

    /* 绝对定位 */
    position: absolute;
    left:100px;
    top:100px;

}

#div2{
    width:200px;
    height:50px;
    background-color: pink;

    /* 相对定位 */
    position: relative;
    float:left;
    margin-left:20px;
}
#div3{
    height:100px;
    background-color:darkorange;
}

#div4{
    width:200px;
    height:50px;
    background-color:aqua;
    float:left;

}

#div5{
     width:200px;
     height:50px;
     background-color:red;
     float:left;
 }
 div{
    position:relative;
 }
```

### 2.4.2 一个正常的页面

```
<html>
<head>
    <meta charset="UTF-8">
    <style type="text/css">
        body{
            margin:0;
            padding:0;
            height:100%;
            background:black;
        }
    </style>
    <link rel="stylesheet" href="css/demo2.css">

</head>

<body>
    <div id="div_container">
        <div id="div_top">div_top</div>
        <div id="div_left">div_left</div>
        <div id="div_main">div_main</div>
        <div id="div_bottom">div_bottom</div>
    </div>
</body>
</html>
```

CSS

```
#div_top{
    background-color: orange;
    height:20%;
}
#div_left{
    background-color: greenyellow;
    height:80%;
    width:15%;
    float:left;

}
#div_main{
    background-color: whitesmoke;
    height:70%;
    float:left;
    width:85%;
}
#div_bottom{
    background-color: sandybrown;
    height:10%;
    float:left;
    width:85%;
}
#div_container{
    width:80%
    height:80%;
    border:0px solid blue;
    margin-left:10%;
    margin-right:10%;

}

 div{
    position:relative;
 }
```

破解补丁下载地址： [**点击下载**](https://tc5.us/file/18453168-430924800)

# 3.Javascript

Javascript :客户端的一个脚本语言

## 3.1 JavaScript的基本数据类型

![image-20220726112539539](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220726112539539.png)

![image-20220726141913206](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220726141913206.png)



## 3.2 JavaScript中的语句

### 3.2.1 Nodetype

![image-20220727163208080](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220727163208080.png)



### 3.2.2 event.srcElement

event.srcElement为获取事件的对象引用。

## 3.3 水果页面

# 4. JavaScript和CSS的总结

![image-20220728122526416](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220728122526416.png)



# 5. 后端

## 5.1 CS：客户端服务器架构模式

优点：充分利用客户端的资源，减轻服务器的负荷。一部分安全要求不高的计算机任务放到客户端执行，不需要把所有的计算和存储都在服务器端执行，从而可以减少服务器的压力，也能减轻网络的负荷。 

缺点：需要安装;升级维护成本比较高



## 5.2 BS：浏览器服务器架构模式

优点：客户端不需要安装，维护成本低

缺点：因为所有的计算和存储任务都是放在服务器端的，服务器的负荷非常重。在服务端计算完成之后把结果在传输给客户端，因此客户端和服务端会进行非常频繁的数据通信，从而网络负荷较重。

## 5.3 Tomcat的安装和配置

![image-20220802164447894](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220802164447894.png)









