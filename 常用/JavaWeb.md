# JavaWeb

![image-20230212105153408](D:\笔记\笔记图片\image-20230212105153408.png)

## 1.HTML

![image-20230212105553500](D:\笔记\笔记图片\image-20230212105553500.png)

* 浏览器通过http协议向Server发送请求，请求某个静态页面
* Server将某个静态页面以代码(HTML, CSS, JavaScript)的形式发送回去。
* ![image-20230212105900487](D:\笔记\笔记图片\image-20230212105900487.png)

### 1.1 前端的基础标签

文件test1.html

1. <img src="D:\笔记\笔记图片\image-20230212113748369.png" alt="image-20230212113748369" style="zoom:150%;" />

2. <img src="D:\笔记\笔记图片\image-20230212113814855.png" alt="image-20230212113814855" style="zoom:150%;" />

3. ![image-20230212113850150](D:\笔记\笔记图片\image-20230212113850150.png)



4. <img src="D:\笔记\笔记图片\image-20230212113913632.png" alt="image-20230212113913632" style="zoom:150%;" />



5. <img src="D:\笔记\笔记图片\image-20230212113924556.png" alt="image-20230212113924556" style="zoom:150%;" />



6. <img src="D:\笔记\笔记图片\image-20230212113950910.png" alt="image-20230212113950910" style="zoom:150%;" />



7.  ![image-20230212114458538](D:\笔记\笔记图片\image-20230212114458538.png)



8. ![image-20230212114600442](D:\笔记\笔记图片\image-20230212114600442.png)



9. ![image-20230212114726618](D:\笔记\笔记图片\image-20230212114726618.png)

### 1.2 表格标签

1. 表格创建![image-20230212114959437](D:\笔记\笔记图片\image-20230212114959437.png)

   一些参数

![image-20230212115236578](D:\笔记\笔记图片\image-20230212115236578.png)

![image-20230212115440104](D:\笔记\笔记图片\image-20230212115440104.png)

* 行合并和列合并

![image-20230212115941510](D:\笔记\笔记图片\image-20230212115941510.png)



![image-20230212120006786](D:\笔记\笔记图片\image-20230212120006786.png)

### 1.3 表单标签

* 输入框，用于承载数据发送个服务器

![image-20230212152545208](D:\笔记\笔记图片\image-20230212152545208.png)

![image-20230212152909588](D:\笔记\笔记图片\image-20230212152909588.png)



### 1.4 Farmeset标签

* frame
* ![image-20230212155622414](D:\笔记\笔记图片\image-20230212155622414.png)

* iframe 在一个页面中嵌入另一个子页面，效果类似





### 1.5 阶段总结 ：html标签

![image-20230212160006331](D:\笔记\笔记图片\image-20230212160006331.png)

## 2. CSS



### 2.1 CSS的布局 Position

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Demo03</title>
  <style type="text/css">

    #div1{
        width: 200px;
        height:50px;
        background-color: coral;
        position: absolute; /* 表示绝对的定位 */
        left: 100px;
        top: 100px;
    }
    #div2{
        width: 200px;
        height:50px;
        background-color: red;
        /*position: absolute;*/
        margin-left: 20px;
    }
    #div3{
        height: 50px;
        background-color: darkorange;
        /* 默认是相对位置，相对位置指的是与父容器的位置 */
    }
    #div4{
         width: 200px;
         height: 50px;
         background-color: olivedrab;
        float: left;
    }
    #div5{
        width: 200px;
        height: 50px;
        background-color: red;
        float: left;
    }
    div{
        position: relative;
    }
  </style>
</head>
<body>
<!--    <div id="div1">&nbsp;</div>-->
<!--    <div id="div2">&nbsp;</div>-->
    <div id="div3">
        <div id="div4"> &nbsp; </div>
        <div id="div5"> &nbsp; </div>
    </div>
</body>
</html>
```

 ![image-20230215185023669](D:\笔记\笔记图片\image-20230215185023669.png)

position：relative

```
<!--<!DOCTYPE html>-->
<!-- 上面这个是html5的意思，以内容决定占比-->
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Demo03</title>
  <style type="text/css">
    body{
      margin: 0px;
      padding: 0px;
    }
    #div_top{
      background-color: orange;
      height: 20%;
      width: 85%;
      float: right;
    }
    #div_left{
      background-color: gray;
      height: 100%;
      width: 15%;
      float: left;
    }
    #div_main{
      background-color: wheat;
      height: 70%;
      width: 85%;
      float: right;
    }
    #div_bottom{
      background-color: sandybrown;
      height: 15%;
      width: 85%;
      float: right; /*如果不加float，就代表的是剩下部分的85%*/
    }
    #div_container{
      width: 80%;
      height: 100%;
      border: 1px solid blue;
      margin-left: 10%;

      float:left;
    }
    div{
      position: relative;
    }
  </style>
</head>
<body>
  <div id="div_container">
    <div id="div_top">div_top</div>
    <div id="div_left">div_left</div>
    <div id="div_main">&nbsp;</div>
    <div id="div_bottom">&nbsp;</div>
  </div>

</body>
</html>
```





## 3 JavaScript















