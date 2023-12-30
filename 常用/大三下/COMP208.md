# COMP208

## 1. 网址导航网站

### 1.0 基础目标

![image-20230208215830274](D:\笔记\笔记图片\image-20230208215830274.png)

* 登录注册系统（暂缓）
* **番茄钟**
* 天气
* 视差滚动页面（未定）
* 记事本
* **网页书签**
* **App栏（添加和删除）**
* 主页（白天和黑夜模式，布局调整，壁纸更换，页面布局）
* **搜索框**
* 桌面宠物(暂定)







### 1.1 类似的例子：

MyHome网站地址：https://s.paul.ren/ 

https://www.bilibili.com/video/BV11f4y1y7tU/?spm_id_from=333.337.search-card.all.click&vd_source=9d046a6203dde4f5f1794bf980388e63

奇趣导航网站地址：https://www.myhomeabc.com/

https://blog.csdn.net/fclworking/article/details/118309592?ops_request_misc=&request_id=&biz_id=102&utm_term=%E7%BD%91%E5%9D%80%E5%AF%BC%E8%88%AA%E7%BD%91%E7%AB%99&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduweb~default-2-118309592.142

果汁导航网站地址：http://guozhivip.com/



极光导航：https://www.jigdh.com

https://www.bilibili.com/video/BV1n94y1D7P3/?spm_id_from=333.337.search-card.all.click&vd_source=9d046a6203dde4f5f1794bf980388e63



鱼皮导航：https://home.code-nav.cn/ （开放了源代码）

https://github.com/liyupi/code-nav



### 1.2 教程

1. 将自己的网站上传到云端，然后为公众提供服务，推荐使用宝塔

https://www.bilibili.com/video/BV1rU4y1J785/?spm_id_from=333.788.recommend_more_video.0&vd_source=9d046a6203dde4f5f1794bf980388e63

2. 桌面宠物制作

https://www.bilibili.com/video/BV1EB4y1v7B4/?spm_id_from=333.788.recommend_more_video.-1&vd_source=9d046a6203dde4f5f1794bf980388e63

3. JS+CSS+HTML95集合集

https://www.bilibili.com/video/BV1Er4y1V7KA/?spm_id_from=333.337.search-card.all.click&vd_source=9d046a6203dde4f5f1794bf980388e63

4. 尚硅谷JavaWeb教程(全新技术栈,全程实战) 42小时课程

https://www.bilibili.com/video/BV1AS4y177xJ/?spm_id_from=333.337.search-card.all.click&vd_source=9d046a6203dde4f5f1794bf980388e63

5. 黑马程序员前端JavaScript入门到精通全套视频教程 44小时课程

https://www.bilibili.com/video/BV1Y84y1L7Nn/?spm_id_from=333.337.search-card.all.click

6. 一节课彻底搞懂前端后端的关系

https://www.bilibili.com/video/BV1UV411h7Mv/?spm_id_from=trigger_reload&vd_source=9d046a6203dde4f5f1794bf980388e63







### 1.3 基础知识

![image-20230208221129874](D:\笔记\笔记图片\image-20230208221129874.png)

![image-20230208210744922](D:\笔记\笔记图片\image-20230208210744922.png)

### 1.4 Requirement Analysis



#### 1.4.1 Projection Description 项目描述

* 在日常生活中，我们发现很多浏览器默认的起始页，要么广告太多，要么呆板无趣，都满足不了我们对美观和实用兼顾的需求，于是我们觉得趁这次小组的机会自己动手设计一个简洁，明朗，大方的导航网页界面。

* 该项目致力于完成一个响应式的导航式网站系统。项目主体分为

  * 菜单栏：显示网站的主要类别的页眉栏，并提供访问子页面的途径。（就是搜索框下面的一堆APP的那个）<font color=blue>这个或许可以写成下拉式</font>
  * 搜索功能：允许访问者在网站内搜索特定内容的搜索框。（Chrome，github）
  * Breadcrumb Trail:访问者在网站中的位置的可视化表示，允许他们看到他们在哪里以及如何返回到以前的页面。
  * Sitemap（页面布局）:一个列出网站和他们的层次结构的页面,让访问者很容易看到网站的整体结构。
  * 页脚:显示有用信息的页脚,如联系信息、社交媒体链接和链接到重要页面。
  * 登录和注册页面：让用户拥有自己的独立账户。
  

技术:导航系统将使用HTML、CSS和JavaScript构建。团队还可以考虑使用Bootstrap之类的前端框架，以确保在不同设备之间具有一致的外观和感觉。

时间:根据网站的复杂性和团队的可用性，项目的估计时间为1-2个月。

交付物:在项目结束时，团队将交付一个功能齐全的导航系统，该系统已集成到网站中，可供访问者使用。该小组还将提供文件和培训材料



#### 1.4.2 Aims and Objectives 目的与目标

* **这个项目的目标是通过提供一个直观有效的导航系统来改善网站的用户体验。通过集成菜单栏、搜索功能、面包屑导航、站点地图、页脚和响应式设计等组件，导航系统将帮助访问者更快速、更容易地找到他们需要的信息。-- Aim**

* 这不仅将改善访问者的整体体验，而且还将有助于增加网站的可用性和可访问性，使访问者更容易参与其内容和完成任务，如购买或提交表单。通过简化导航过程，网站也将变得更加友好，这可以提高参与度、更高的转化率和更高的客户满意度

* The aims and objectives of this project can be summarized as follows:

  1. To improve the usability and accessibility of the website: By providing a navigation system that is intuitive and easy to use, visitors will be able to find the information they need more quickly and easily, improving their overall experience on the website.
  2. To increase engagement: A well-designed navigation system can help visitors engage with the website's content more effectively, leading to increased engagement and a higher likelihood of visitors returning to the site.
  3. To enhance the user experience: By providing a responsive design and integrating useful components such as a search function and site map, the navigation system will enhance the overall user experience, making it more enjoyable and satisfying for visitors.
  4. To increase conversions: By streamlining the navigation process and making it easier for visitors to complete tasks such as making purchases or submitting forms, the website's conversion rates are likely to increase, which can result in a higher return on investment for the website owner.
  5. To meet accessibility standards: By ensuring the navigation system is designed with accessibility in mind, the website will meet or exceed industry standards for accessibility, improving the experience for users with disabilities and helping to create a more inclusive online environment.

  These are the main aims and objectives of the project, and by achieving them, the website will become more user-friendly, engaging, and successful.

![image-20230210144817919](D:\笔记\笔记图片\image-20230210144817919.png)



#### 1.4.3 Description of Key Literature & Background 关键文献与背景描述

* Background

* The background of the website navigation project refers to the context and history of website navigation and design, including information on the evolution of website navigation systems, the current state of the field, and the latest trends and developments.

  This background information can include:

  1. Evolution of website navigation: This could include a brief history of how website navigation systems have evolved over time, from early navigation systems based on simple text links to more complex systems incorporating advanced features such as search functions and drop-down menus.
  2. The importance of website navigation: This could include information on why website navigation is critical to the success of a website, including its impact on the user experience, engagement, and conversions.
  3. Current trends and developments in website navigation: This could include information on the latest trends and innovations in website navigation, such as the rise of mobile-responsive navigation systems, the increased use of artificial intelligence and machine learning in navigation, and the trend towards more personalized navigation experiences.

  By understanding the background of website navigation, the project team can gain a deeper understanding of the context and history of the field, as well as the current state of the art, which can inform the design and development of the navigation system. This background information will provide the context for the project and help ensure that the final product is up-to-date, innovative, and in line with the latest trends and developments in the field.

* ![image-20230210145235493](D:\笔记\笔记图片\image-20230210145235493.png)



#### 1.4.4 Development and Implementation Summary 开发及开发及实施总结

* *HTML*是*什么HTML*是目前网络上应用最为广泛的*语言*，也是构成网页文档的主要*语言*。
* 数据库使用Cookie
* 开发环境：jetBrain，使用



#### 1.4.5 Data Sources 数据源

网址



#### 1.4.6 Testing and Evaluation 测量和评估

* 使用web网页测试用例
* 黑盒测试
* 



#### 1.4.7 Ethical Considerations 道德条件





#### 1.4.8 BCS Project Criteria BCS项目标准



#### 1.4.9 UI/UX Mockup UI / UX模型

**注释表示图片**



#### 1.4.10 Project Plan 项目计划

Here is a high-level project plan for a website navigation project:

1. Project initiation: In this phase, the project team will identify the goals and objectives of the project, gather requirements and constraints, and establish a project timeline and budget.
2. Key literature and background review: In this phase, the project team will conduct research and analysis of existing literature and information related to website navigation and design. This will inform the design and development of the navigation system.
3. Requirements gathering and analysis: In this phase, the project team will gather requirements from stakeholders, including website owners and users, and perform a thorough analysis to ensure that the requirements are feasible and aligned with the goals of the project.
4. Design and development: In this phase, the project team will design and develop the navigation system, incorporating best practices and guidelines, user experience research, and accessibility standards. The team will also test the navigation system to ensure that it meets the requirements and goals of the project.
5. Deployment: In this phase, the project team will deploy the navigation system to the website, perform any necessary training and support, and monitor the system to ensure that it is functioning as expected.
6. Evaluation and continuous improvement: In this phase, the project team will evaluate the performance of the navigation system, gather feedback from stakeholders and users, and make any necessary improvements to the system to ensure that it continues to meet the goals and requirements of the project.

This is a high-level project plan, and the specific details and activities involved in each phase will vary depending on the specific requirements and constraints of the project. However, this plan provides a general outline of the key steps involved in a website navigation project and can be adapted to meet the specific needs of the project.

![image-20230210145514954](D:\笔记\笔记图片\image-20230210145514954.png)



#### 1.4.11 Risks & Contingency Plans 风险和应急计划



![image-20230210150457021](D:\笔记\笔记图片\image-20230210150457021.png)

Here is a more specific contingency plan for a website navigation project:

1. Requirements gathering and analysis:

- Contingency plan: If the requirements gathered from stakeholders are found to be incomplete or misaligned with the goals of the project, the project team will revisit the requirements gathering and analysis process and conduct additional user research and testing to ensure that all relevant requirements have been captured. The project timeline and budget may need to be revised to accommodate this additional work.

1. Design and development:

- Contingency plan: If the navigation system is found to be non-compliant with the requirements and goals of the project, the project team will revise the design and development plan and allocate additional resources, as needed, to ensure that the system meets the required standards. The project timeline and budget may need to be revised to accommodate this additional work.

1. Deployment:

- Contingency plan: If the deployment of the navigation system causes problems with other parts of the website, the project team will roll back the deployment, investigate the issue, and implement a fix as quickly as possible. The project team will also revise the deployment plan to address the root cause of the issue and prevent it from happening again in the future.

1. User acceptance:

- Contingency plan: If the navigation system is not well-received by the target audience, the project team will gather feedback from stakeholders and users, revise the design and development plan, and allocate additional resources, as needed, to address any issues and ensure that the navigation system meets the needs and expectations of the target audience. The project timeline and budget may need to be revised to accommodate this additional work.

This is a sample contingency plan for a website navigation project, and the specific activities involved in each contingency plan will vary depending on the specific requirements and constraints of the project. However, this plan provides a general outline of the key steps involved in a contingency plan for a website navigation project and can be adapted to meet the specific needs of the project.

![image-20230210151218925](D:\笔记\笔记图片\image-20230210151218925.png)

#### 1.4.12 References 参考



# javaWeb杂记

## Servlet

* 什么是servlet？

*   Servlet（Server Applet），全称Java Servlet，未有中文译文。是用Java编写的服务器端程序。**其主要功能在于交互式地浏览和修改数据，生成动态Web内容。**狭义的Servlet是指Java语言实现的一个接口，广义的Servlet是指任何实现了这个Servlet接口的类，一般情况下，人们将Servlet理解为后者。

      Servlet运行于支持Java的应用服务器中。从实现上讲，Servlet可以响应任何类型的请求，但绝大多数情况下Servlet只用来扩展基于HTTP协议的Web服务器。

```
1.设置编码
        // super.doPost(req, resp);
        // post方式下使用下面方法解决乱码问题 request.setCharacterEncoding("UFT-8");
        // get请求目前不需要编码(基于tomcat8之后，之前有特殊的编码方式，不过很少用了 )
        注意，设置编码必须在所有获取参数之前
2.servlet的继承关系
    2.1 javax.servlet.Servlet接口
        2.1.1 javax.servlet.GenericsServlet抽象类
             2.1.1.1 javax.servlet.HttpsServlet

     2.2 相关方法
        javax.servlet.Servlet接口
            void init(config) -初始化方法
            void service(request, response) -服务方法
            void destroy() -销毁方法

        javax.servlet.GenericServlet 接口 抽象类
            void service(request,response)-仍然是抽象的

        javax。servlet.https.HttpServlet 抽象子类
            void service(request, response) -不抽象的
            1. String method = req.getMethod() 获取请求的方法
            2. 各种if判断，根据请求方式的不同，决定去调用不同的do方法
            3. 在HttpServlet这个抽象类中，do方法都差不多




3.servlet的生命周期
    1.从出生到死亡的过程就是生命周期，对应着init(),service(),destroy()的三种方法
    2.默认情况下：
        在第一次接受请求时，这个Servlet会进行实例化（调用构造方法），初始化（调用init），然后
        服务（调用service）从第二次请求开始，每一次都是服务
        当容器关闭时，其中所有的servlet实例都会被销毁，调用销毁的方法。
    3. 通过以上实例我们发现：
        - Servlet实例tomcat只会创建一个，所有的请求实际上是去让这个实例去相应
            - 因为发现刷新网页也不会新建一个servlet
        - 默认情况下，只有在第一次请求时，tomcat才会去实例化，初始化，
            然后再去相应服务。这样的好处是：提高系统的启动速度
            缺点是第一次启动相对来说更慢
        - 因此得出结论：如果需要提高系统的启动速度，当前默认情况就是这样。
            如果需要提高相应速度，我们应该设置servlet的初始化时机。
    4.servlet的启动时机
        - 默认在第一次接受请求时，实例化并初始化
        - 我们可以通过<load-on-startup>1</load-on-startup>来设置servlet启动的先后顺序
            如果有多个servlet需要启动的话。
     5.Servlet在容器当中是：单例的，线程不安全的
        单例的：从上述可知servlet只会创建一个实例，即使有多个访问
        线程不安全的：当多个客户端访问一个Service的时候，
        比如线程1和线程2，那么线程1调用service的方法经过判断语句1执行
        如果此时线程2同时请求，可能会改变判断语句1的参数导致线程1出错。
        （比如num=1是判断语句的条件，线程2的执行语句可能会导致num->2进而导致线程出错）
            - 所以尽量不要在servlet中定义成员变量
              如果必须定义，那么不要根据成员变量的值做一些逻辑判断
```



## HTTP协议

* **HTTP（Hyper Text Transfer Protocol）：** 全称超文本传输协议，是用于从万维网（WWW:World Wide Web ）服务器传输超文本到本地浏览器的传送协议。

### 请求报文

* 请求行

  * 一般是包含三个信息：
    * 1.请求的方式
    * 2.请求的URL
    * 3.请求的主体

* 请求头

  * 作用：通过具体的参数对本次请求进行详细的说明
  * 格式：键值对，键和值之间使用冒号隔开
  * 相对来说比较重要的消息头
  * ![image-20230222142307136](D:\笔记\笔记图片\image-20230222142307136.png)

* 请求体

  * 请求主题：三种情况
    * 1.get方式，没有请求体，有一个叫queryString
    * 2.post方式，有请求体，form data
    * 3.json格式，有请求体，request payload

  



### 响应报文

* 1.响应行 2.响应头 3.响应体
  * 响应行：1.协议 2.响应状态码 3.响应状态
  * 响应头 ：包含了服务器的信息，服务器发送给浏览器的信息（内容的媒体类型，编码，内容长度）
  * 响应体：响应的实际内容（比如请求add.html界面时，响应的内容就死<html>.....巴拉巴拉）



## Thymeleaf



![image-20230222181622376](D:\笔记\笔记图片\image-20230222181622376.png)







## 保存作用域

* 保存作用域：
* 在原始情况下，保存作用域我们可以认为有四个：Page(页面级别)，Request(一次请求相应范围), Session（一次会话范围）, Application（整个应用请求范围）
* request：一次响应请求范围
* ![image-20230223110804291](D:\笔记\笔记图片\image-20230223110804291.png)
  * 请求2不能调用请求1中的值

* Session：一次会话范围有效

![image-20230223115920241](D:\笔记\笔记图片\image-20230223115920241.png)

* Application: 整个应用请求范围

 ![image-20230223120258493](D:\笔记\笔记图片\image-20230223120258493.png)







## JDBC

### JDBC驱动载入



### JDBC插入数据

![image-20230224210518408](D:\笔记\笔记图片\image-20230224210518408.png)

```
package com.atguigu.jdbc;

import java.sql.Connection;
import java.sql.DriverManager;
import java.sql.PreparedStatement;
import java.sql.SQLException;
// 使用JDBC来添加数据
public class Demo02 {
    public static void main(String[] args) throws ClassNotFoundException, SQLException {
        //1.加载驱动
        Class.forName("com.mysql.jdbc.Driver");
        //2.通过驱动管理器获取连接对象
        //url 表示 和 数据库通信的地址
        //如果url中需要带参数，则需要使用?进行连接
        //如果需要带多个参数，则从第二个参数开始使用&连接
        Connection conn = DriverManager.getConnection("jdbc:mysql://localhost:3306/fruitdb?useSSL=false&useUnicode=true&characterEncoding=utf-8","root","gzk2280802");
        //3.编写SQL语句
        //id , fname , price , fcount , remark
        String sql = "insert into t_fruit values(0,?,?,?,?)";// ?表示占位符，表示之后要有一个参数把这个填充掉
        //4.创建预处理命令对象
        PreparedStatement psmt = conn.prepareStatement(sql); //java和Database之间的连接桥
        //5.填充参数
        psmt.setString(1,"榴莲");
        psmt.setInt(2,15);
        psmt.setInt(3,100);
        psmt.setString(4,"榴莲是一种神奇的水果");
        //6.执行更新(增删改），返回影响行数
        int count = psmt.executeUpdate();
        System.out.println(count > 0 ? "添加成功！" : "添加失败！");
        //7.释放资源（关闭连接 , 先关闭psmt，后关闭conn）
        psmt.close();
        conn.close();
    }
}
```































































