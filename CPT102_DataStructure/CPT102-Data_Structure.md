



# CPT102-Data_Structure

## Lecture1 概述及指引 软件设计

### 1. Data Structure

 #### 1.1 The Definition of Data Structure

数据结构是组织数据集合以实现高效访问的系统方法

#### 1.2 数据结构的三个研究方向

——属性

——组织

——操作

#### 1.3 数据结构的类型

• Arrays 

• Lists 

• Stacks 

• Queues 

• Maps 

• Trees 

• Graphs

#### 1.4 数据结构的目的

仔细设计软件系统中使用的数据结构有助于设计出好的软件。

### 2. Abstraction抽象

#### 2.1 The Defination of Abstraction

<font color='red'>作为一个过程，抽象表示提取一个项目或一组项目的基本细节，同时忽略非基本细节。</font>

<font color='red'>作为一个实体，抽象表示一个模型、一个视图或一个实际项目的一些表示，而忽略了项目的一些细节。</font>

#### 2.2 抽象的种类

##### 2.2.1 数据抽象 data abstraction

数据抽象的目的是确定存储和操作<font color='red'>数据</font>的哪些细节是重要的，哪些是不重要的

##### 2.2.2 过程抽象 procedural abstraction

过程抽象的目的是确定<font color='red'>任务</font>如何完成的哪些细节是重要的，哪些是不重要的

#### 2.3 The key to Abstraction

* 提取组件的共性，隐藏其细节

* 抽象通常关注于一个对象/概念的外部视图

#### 2.4 Abstraction Example - Huffman Coding（霍夫曼编码）

##### 2.4.1 The Definition of 霍夫曼编码

  霍夫曼编码(Huffman Coding)是一种编码方法，霍夫曼编码是可变字长编码(VLC)的一种。

霍夫曼编码使用变长编码表对源符号（如文件中的一个字母）进行编码，其中变长编码表是通过一种评估来源符号出现机率的方法得到的，出现机率高的字母使用较短的编码，反之出现机率低的则使用较长的编码，这便使编码之后的字符串的平均长度、期望值降低，从而达到无损压缩数据的目的。

##### 2.4.2 霍夫曼编码的具体步骤与实例

1）将信源符号的概率按减小的顺序排队。

2）把两个最小的概率相加，并继续这一步骤，始终将较高的概率分支放在右边，直到最后变成概率１。

3）画出由概率１处到每个信源符号的路径，顺序记下沿路径的０和１，所得就是该符号的霍夫曼码字。   

4）将每对组合的左边一个指定为0，右边一个指定为1（或相反）。

**<font size=5>实例：</font>**

![image-20220605113831041](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220605113831041.png)

![image-20220605114345168](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220605114345168.png)

![image-20220605114405705](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220605114405705.png)

![image-20220605114424828](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220605114424828.png)

### 3. Information Hiding

#### 3.1 信息隐藏的定义

<font color='red'>信息隐藏是一个模块的用户只需要知道该模块的基本细节的原则(通过抽象来标识)</font>因此，抽象引导我们识别模块的细节，哪些对用户是重要的，哪些是不重要的信息隐藏告诉我们，我们应该积极地对用户保守所有不重要的细节，并试图阻止他使用任何不重要的细节用户需要从模块的规范中了解模块的重要细节因此，信息隐藏意味着模块是通过它们来规范而不是它们来实现来使用的。

#### 3.2 信息隐藏在O-O world中的应用

* O-O面向对象

在一个设计良好的面向对象应用程序中，对象会公开它可以做什么——也就是它能够提供的服务，或者它的方法头在一个设计良好的面向对象应用程序中，对象会公开它可以做什么——也就是它能够提供的服务，或者它的方法头

隐藏了如何执行这些服务和数据的内部细节(属性&amp;结构)，以支持这些服务。



### 4. Encapsulation(封装)

#### 4.1 封装的定义

<font color='red'>作为一个过程，封装意味着将一个或多个项(数据/函数)封装在(物理或逻辑)容器中。</font>

<font color='red'>作为一个实体，封装是指包含(包含，封装)一个或多个项(数据/函数)的包或外壳。</font>

这种封闭物内部和外部之间的分隔物有时被称为墙或屏障。

#### 4.2 在面向对象的编程中封装的作用

* 在面向对象编程中，封装是在对象中包含该对象运行所需的所有资源——即方法和数据。
* 这个想法是:不要告诉我你是怎么做的;告诉我你能做什么!

#### 4.3 沟通中的封装

* 在通信中，封装是将一个数据结构包含在另一个结构中，从而隐藏第一个数据结构。

#### 4.4 封装的例子

![image-20220605124134429](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220605124134429.png)



### 5. 抽象，信息隐藏，封装的对比



抽象是一种技术，它帮助我们识别哪些特定信息对模块的用户是重要的，哪些信息是不重要的

信息隐藏是指对用户隐藏所有不重要的信息

封装是一种对信息进行包装的技术，以隐藏应该隐藏的内容，并使希望显示的内容可见。

### 6. 静态数据结构和动态数据结构

除了时间和空间效率之外，选择数据结构的另一个重要标准是它能够存储的数据项的数量是否可以根据我们的需要进行调整或有限制。这种区别导致了动态数据结构与静态数据结构的区别。

#### 6.1 动态数据结构

动态数据结构在运行时增长或收缩以适应当前的需求，例如用于交通流建模的结构。<font color='red'>在运行中可以动态变化</font>

* <font color='red'>在Java中，数组总是动态分配的。</font>

##### 6.1.1 动态数据结构的优缺点

<font size=4>**优点:**</font>

**1.不需要知道数据项的确切数量.**

因为动态数据结构可以收缩或增长以完全适应正确的数据项数量，不需要知道我们需要存储多少数据项.

**2.有效利用内存空间**

扩展动态数据结构的大小, 每当我们需要添加的数据项,否则不可能存储在结构和收缩时动态数据结构有未使用的空间,那么这个结构总是没有正确的大小和内存空间被浪费了

<font size=4>**缺点:**</font>

•内存分配/回收开销

•当一个动态数据结构增长或收缩时，分配给该数据结构的内存空间必须增加或删除(这需要时间)





#### 6.2 静态数据结构

静态数据结构在创建时是<font color='red'>固定的</font>。例如，用于存储邮政编码或信用卡号码的结构(具有固定格式)

##### 6.2.1 静态数据结构的优缺点

**<font size=4>优点:</font>**

**1.易于规范**

编程语言通常提供一种简单的方法来创建几乎任意大小的静态数据结构

**2.没有内存分配开销**

由于静态数据结构的大小是固定的，

没有任何操作可以用来扩展静态结构;

这样的操作将需要为结构分配额外的内存(这需要时间)

**<font size=4>缺点：</font>**

**1.必须确保有足够的容量**

由于我们可以存储在静态数据结构中的数据项的数量是固定的，一旦创建了它，我们必须确保这个数量足够大，以满足我们的所有需求

**2.更多的元素?(错误),更少的元素?(浪费)**

然而，当我们的程序试图在静态数据结构中存储比它允许的更多的数据项时，这将导致错误(例如ArrayIndexOutOfBoundsException)。另一方面，如果存储的数据项更少，那么静态数据结构的一部分仍然是空的，但是内存已经被分配，不能用于存储其他数据

## Lecture1 Q&A

1. 空间效率和时间效率都是用于评估算法(和数据结构)性能的指标。(T、F ?)

T

2. 一般来说，动态数据结构的空间效率更高。(T、F ?)

T

3. 一般来说，静态数据结构的时间效率更高。

T

4. 信息隐藏的原则是软件组件的用户只需要知道如何初始化和访问组件的基本细节，而不需要知道实现的细节(T或F?)

F



## Lecture2 Java Collection Libraries(Collection 类)



### 1. Overview of Data Structure Programming in Collection

#### 1.1 Linear Collection(线性集合类)

Programming with Linear collections

##### 1.1.1 线性集合类的种类

• Lists, Sets, Bags, Maps, Stacks, Queues, Priority Queues(优先队列)

##### 1.1.2 线性集合类的作用

Using Linear collections

* Programming with collections 编程与集合

* Searching & Sorting Data 搜索和整理数据

* Implementing linear collections 实现线性的集合

* Implementing sorting algorithms 实现排序算法

* Linked data structures and “pointers” 链接的数据结构和“指针”

#### 1.2 Hierarchical collections(分层集合类)

Programming with Hierarchical collections

##### 1.2.1 分层集合类的种类

Trees, binary trees, general trees

##### 1.2.2 分层集合的作用

•使用树结构的集合

​	•建造树形结构

​	•搜索树结构

​	•遍历树结构

•实现树形结构的集合

•实现线性集合

•用二叉搜索树



### 2. Programming with Libraries（编程与库）

因为现代编程太大了，无法一个人完成，需要调用其他人写的包Libraries。

![image-20220605164535255](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220605164535255.png)

![image-20220605164731077](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220605164731077.png)

![image-20220605164740489](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220605164740489.png)

![image-20220605164754122](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220605164754122.png)

![image-20220605164804030](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220605164804030.png)



## Lecture2 Q&A

1. 列出3种可以在下面实现的集合类型，使用线性集合的Java编程

Integer, String, Floating

2. 说出三个常见数据集合中常见的典型结构。

list, queue, stack

3. 请说出常见数据收集中常见的三种典型操作

get, add, delete

4. 命名2种可以在下面实现的集合类型，使用分层集合的Java编程

Trees, binary trees, general trees



5. 什么是软件“库”?

软件库是一套数据和编程代码，用于开发软件程序和应用程序。它被设计用来协助程序员和编程语言编译器构建和执行软件。

A software library is a suite of data and programming code that is used to develop software programs and applications. It is designed to assist both the programmer and the programming language compiler in building and executing software.

6. Define Java “Package”. 

java包[类库](https://baike.baidu.com/item/类库/3351433)由一组支持程序开发的类组成。一个编译器或开发环境以一个类库为基础。

7. • Name Java’s IO library.

*Java的*核心*库java*.*io*提供了全面*的IO*接口。包括：文件读写、标准设备输出等。Java中IO是以流为基础进行输入输出的，所有数据被串行化写入输出流，或者从输入流读入。

8. Name Java’s GUI library.

![image-20220605171656826](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220605171656826.png)

9. What is the Java statement to include package or class into your program?

import 

## Lecture3 1-dimensional data structure(一维数据结构)



#### 1. Collection Types

![image-20220605172838261](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220605172838261.png)

#### 1.1 Methods of Collection and List(集合和列表的类和方法)

![image-20220605173008908](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220605173008908.png)

#### 1.2 Using a collection type(集合类)

声明为接口类型的变量或字段：

* 指定集合的类型

* 指定值的类型

![image-20220605173305210](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220605173305210.png)

创建实现该类型的类的对象:

* 指定类

* 指定值的类型

![image-20220605173500004](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220605173500004.png)



## Lecture3 Q&A

![image-20220605183431620](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220605183431620.png)

1. What does it store inside?

数组

2. How does it keep track of the size?

![image-20220605183536005](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220605183536005.png)

3. How does it grow when necessary?

![image-20220605183738665](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220605183738665.png)

4. 它的迭代器是如何工作的?

“迭代器(Iterator)是一个对象,它的工作是遍历并选择序列中的对象,它提供了一种访问一个容器(container)对象中的各个元素,而不必暴露该对象内部细节的方法。通过迭代器,开发人员不需要了解容器底层的结构,就可以实现对容器的遍历。”

## Lecture 4 Bags, Sets, Stacks, Maps

![image-20220605183952249](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220605183952249.png)

### 1. Bags(包)

![image-20220605184056749](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220605184056749.png)

#### 1.1 Bag Applications

什么时候使用Bag？

当不需要订购集合，并且副本是可能的:

当前登录用户的集合(可以有dups吗?)

藏书中的书(会有dups吗?)

### 2. Set ADT

![image-20220605184335491](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220605184335491.png)

### 3. Stack(栈)

![image-20220605184512352](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220605184512352.png)

#### 3.1 Method of Stack(栈的方法)

![image-20220605184553079](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220605184553079.png)

#### 3.2 Applications Of Stacks(栈的应用)

![image-20220605184640449](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220605184640449.png)

### 4. HTML & XML的例子

![image-20220605185113565](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220605185113565.png)



### 5. Maps

hashmap，存储键和值两个部分

## Lecture5 

### 1. Map of Example

![image-20220606171609032](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220606171609032.png)

![image-20220606171622078](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220606171622078.png)

![image-20220606171638696](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220606171638696.png)

![image-20220606171649003](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220606171649003.png)

![image-20220606171701512](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220606171701512.png)

### 2. Queues

一边进，一边出

#### 2.1 Ordinary queues

只在后面加

![image-20220606172508721](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220606172508721.png)

#### 2.2 Priority queues

以给定的优先级添加或删除

![image-20220606172542600](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220606172542600.png)

#### 2.3 队列的作用

![image-20220606172622587](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220606172622587.png)

#### 2.4 队列的方法

![image-20220606172646192](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220606172646192.png)

### 3. Iterators 迭代器

用于遍历集合类

![image-20220606173121394](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220606173121394.png)

#### 3.1 迭代器的格式

![image-20220606173216121](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220606173216121.png)

![image-20220606173145311](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220606173145311.png)



### Lecture5 Q&A

1. Java has specified a “Queue” interface. (T or F)

T

2. Java没有任何类支持“优先队列”。(T、F)

F

3. 如果队列为空，则Queue接口下的peek()操作将抛出异常。(T、F)

F

4. Queue接口下的poll()操作将在队列为空时抛出异常。(T、F)

F

5. 在Queue接口下有一个element()方法。(T、F)

T

6. Iterable是一个带有Iterator的类的接口规范。

T

7. Iterator是可以生成迭代元素的类的接口规范。

T

### Lecture6

### 1. Iterators and Iterables

![image-20220606180002409](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220606180002409.png)



###   2. Sorting a Collection（组的排序）

没啥好说的，就组的排序

### 3. Comparators（比较）

![image-20220606180405585](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220606180405585.png)

![image-20220606180426166](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220606180426166.png)



## Lecture6 Q&A

1. 在可比类下定义的对象将具有“自然排序”。(T、F)

T

2. Objects declared under a comparable class can be compared using which method?

**compareTo()**

3. compareTo方法的签名是什么?

![image-20220606180757266](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220606180757266.png)

4. 哪种方法可以用来对可比对象列表进行排序?

**Collections.sort() and Arrays.sort()**

5. Comparator是一个可以比较其他对象的对象。(T)或

   F)

T

6. compare()方法的签名是什么?

![image-20220606180915454](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220606180915454.png)

7. 一个可比类可以实现多个比较器。(T、F)

T

## Lecture7 

### 1. Comparators

![image-20220606223048562](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220606223048562.png)

![image-20220606223059499](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220606223059499.png)

![image-20220606223152431](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220606223152431.png)

![image-20220606223200825](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220606223200825.png)



### 2. Exceptions(异常)

![image-20220606223258506](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220606223258506.png)

![image-20220606223314066](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220606223314066.png)

#### 2.1 异常的种类

![image-20220606223337347](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220606223337347.png)



## Lecture7 Q&A

1. 列举3种常见的Java异常。

RuntimeExpections，IOException，ArrayIndexOutOfBoundsException

2. RuntimeExceptions don’t have to be handled. (T or F) 

   IOException doesn’t have to be handled. (T or F)

T T

3. Which Java statement can cause an exception? 

<font color='red'>不知道Throw</font>

4. 当我们尝试向不可变列表中添加元素时会发生什么?

报错，出现异常

5. Java接口是否提供了一个“构造函数”?

没有

6. ArrayList实现了哪个接口?

List

7. public interface List extends which Java Interface?

Collection 

8. **A method will do what when something goes wrong?**

- Throwing exceptions
- Handling (catching) exceptions

9. 当发生错误时，异常提供了一个本地出口【T或F】

F An Exception is a non-local exit

10. 列出3种可能引发异常的情况

- F  The file doesn't exist
- Divided by 0
- Call a method on the null object
- Call an undefined method

11. 我们如何处理异常?

- Throwing exceptions
- Handling (catching) exceptions

12. 异常可以使用什么Java语句?

- try{}catch{}

13. **Does exception have a type?**

Yes

14. 异常处理程序完成它的工作后，程序下一步将做什么

    异常处理程序执行后继续执行

15. 异常处理程序可以使用异常对象中的信息吗?

    是的

16. 当e是一个异常对象时，“e. getmessage()”做什么?

    打印错误类型

## Lecture8 ArrayList

### 1. ArrayList

#### 1.1 Definitiontion of ArrayList

![image-20220606230116117](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220606230116117.png)

#### 1.2 ArrayList 的方法

![image-20220606230244162](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220606230244162.png)

![image-20220606230302794](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220606230302794.png)

![image-20220606230316668](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220606230316668.png)

![image-20220606230323677](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220606230323677.png)

![image-20220606230336603](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220606230336603.png)

![image-20220606230343702](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220606230343702.png)

![image-20220606230402645](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220606230402645.png)

## Lecture8 Q&A

1. 抽象类的关键特性是什么?

类定义中必须有一个抽象关键字

抽象类可以有抽象方法和非抽象方法。

如果一个类有一个抽象方法，那么它必须被定义为一个抽象类。

它可以有默认构造函数或参数化构造函数。

不允许为抽象类创建对象

它还允许定义最终方法和静态方法

我们只能通过使用extends关键字来通过继承访问抽象类。

扩展抽象类的类必须实现所有抽象方法。

抽象类也可以包含变量

2. 抽象类可以实例化吗?

NO

3. 抽象方法可以在类中定义，以节省实现工作【T或F】

F

4. 当我们从数组列表中移除一个元素时，实现的关键问题是什么?

将空槽位设置为空

5. 当我们从数组列表中添加元素时，实现的关键问题是什么?

建立空槽

## Lecture9 

### ArrayList: iterator(Arraylist 迭代器)



## Lecture9 Q&A

1. remove() is compulsory in Iterator implementation. (T or F)

F 	Must be declared, but not have to implement

2. ArrayList在其实现中如何使用“类型参数”?

3. 哪个元素将被ArrayList.remove()删除?

Most recent called by next ()

4. 在返回列表中的下一个元素之前，ArrayList.next()检查什么?

nextIndex >= list.count

5. 如何ArrayList.remove()确保只有一个元素可以删除后，每个调用next()?

**by the flag -->canRemove**

6. 如果两个或多个迭代器同时运行在同一个数组列表下会发生什么?

可以删除最后返回的项

这个实现并不聪明，如果对它所遍历的ArrayList进行任何更改，就可能会损坏

## Lecture 10 Cost

### 1. Analysing Costs

#### 1.1 Time

•运行程序并计算毫秒/分钟/天。

•计算算法将执行的步骤/操作的数量。

#### 1.2 Space

•测量程序占用的内存数量

•计算算法存储的基本数据项的数量

#### 1.3 Big O

![image-20220607104304379](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607104304379.png)

![image-20220607105232837](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607105232837.png)

![image-20220607105212007](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607105212007.png)



## Lecture10 Q&A

1. O(log(n)) < O(sqrt(n)) (T or F)

T		 *sqrt（N）的* 增长将比 *log 2（N）_大得多*

2.  O(n^n) < O(n!) (T or F) 

F

3. O(2^n) < O(n^n) (T or F) 

T

4. 在分析一个算法的代价时，循环通常是重点。(T、F)

T

5. 下面哪个操作更昂贵?

   •从文件中读取一行

   •从用户处读取一行（T）

6. 最坏情况的成本分析通常比平均成本分析更困难。(T、F)

F

## Lecture11 Recursion



### 1. Recursive Functions 

递归函数是直接或间接调用自身的函数

### 2. Factorial Function阶乘函数

![image-20220607112701465](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607112701465.png)

![image-20220607112712561](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607112712561.png)

### 3. Fibonacci Function（斐波那契函数）

![image-20220607112831671](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607112831671.png)

### 4. Recursion VS iteration

![image-20220607113141650](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607113141650.png)



## Lecture11 Q&A

1. 设计递归函数的关键步骤是什么?

需要一个递归步骤将问题划分为子问题

2. 每一个递归函数都可以被重写为一个迭代函数。(T、F)

T

## Lecture12 Linked Structures

![image-20220607114424273](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607114424273.png)



## Lecture12 Q&A

1. d什么时候为“黑盒”测试编写测试用例?实施前还是实施后?

实施后（<font color='blue'>不确定</font>）

2. 解释为什么队列的数组实现比较慢。

<font color='red'>不知道</font>

3. 内存管理中垃圾收集的目的是什么?

垃圾回收系统的目的是清除不再使用的空间。腾出新的空间。

## Lecture13 &14 Linked Structure



### 1. Linked Structure

![image-20220607160150763](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607160150763.png)

### 2. Linked List的一些方法

![image-20220607160213180](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607160213180.png)

![image-20220607160225324](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607160225324.png)

![image-20220607160233463](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607160233463.png)

![image-20220607160241009](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607160241009.png)

![image-20220607160253030](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607160253030.png)



## Lecture15 Linked Stacks and Queues

### 1.  A Stack using a Linked List with a header

![image-20220607160454335](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607160454335.png)



### 2. A Queue using a Linked List with a header

![image-20220607161654747](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607161654747.png)

![image-20220607161716824](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607161716824.png)



## Lecture16 ArraySet and Binary Search

### 1. ArraySet 

![image-20220607165148104](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607165148104.png)

![image-20220607165222420](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607165222420.png)

![image-20220607165241396](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607165241396.png)

![image-20220607165255164](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607165255164.png)



###  2. Binary Search

 ![image-20220607172738382](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607172738382.png)

![image-20220607172746718](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607172746718.png)

![image-20220607172938383](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607172938383.png)

### 3. ArraySet With Binary Search

![image-20220607173012338](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607173012338.png)

![image-20220607173031078](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607173031078.png)



## Lecture16 Binary Search and Sorting

### 1. Binary Search



### 2. Sort

![image-20220607173531582](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607173531582.png)

![image-20220607173557952](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607173557952.png)

#### 2.1 Inserting Sorts（选择排序）

![image-20220607173649169](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607173649169.png)

![image-20220607173705227](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607173705227.png)

#### 2. 2 Bubble Sort（冒泡排序）

![image-20220607173802043](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607173802043.png)





 ##  Lecture18 Sort



### 1. Merge Sort（归并排序）

![image-20220607174533849](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607174533849.png)

![image-20220607174549771](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607174549771.png)

### 2. QuickSort

![image-20220607180337558](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607180337558.png)

![image-20220607180256048](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607180256048.png)

![image-20220607180314773](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607180314773.png)



## Lecture20 Trees

 

### 1. Trees

![image-20220607182210871](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607182210871.png)

### 2. Binary Trees

![image-20220607182248807](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607182248807.png)

## Lecture20 Q&A

1. 树表示一种高效的一维数据结构。

   (T、F ?)

T

2. 树中的叶子节点没有子节点。(T、F ?)

T

3. 二叉树对它的兄弟节点没有排序。(T)或

   F ?)

T

4. Name 3 applications for tree.

Binary Tree, General Tree (n-ary tree), AVL Tree

5. 递归调用之间的关系可以用什么类型的树来表示?

Recursion tree

## Lecture21 树的搜索方法

### 1. 树的搜索方法

#### 1.1 前序

#### 1.2 后序

#### 1.3 中序

### 2. 二叉平衡搜索树（AVL Tree）

![image-20220607192921158](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607192921158.png)

![image-20220607193107226](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607193107226.png)



## Lecture23 Hashing and Hash Tables

### 1. HashTables

![image-20220607193917446](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607193917446.png)

### 2. Table Size

![image-20220607215851977](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607215851977.png)



### 3. Hash Function哈希函数

 哈希函数是任何定义良好的过程或数学函数，用于将数据转换为数组的索引。

#### 3.1 Hash函数的性质

•避免碰撞

•在数组中均匀分布键

•计算成本低-必须为O(1)

#### 3.2 Hash函数的例子

##### 3.2.1 Mid-Square Method

![image-20220607221842897](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607221842897.png)

### 4. Collisions(冲突)

#### 4.1 Dealing with Collisions(处理冲突)

##### 4.1.1 Open Addressing开地址法

key/value pairs are stored in array slots

##### 4.1.2 Linear Probing线性探测

![image-20220607222524605](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607222524605.png)

##### 4.1.3 Quadratic Probing二次探测

![image-20220607223023394](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607223023394.png)

##### 4.1.4 Double Hashing 双倍hash

![image-20220607223110803](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607223110803.png)

#### 4.2 处理冲突的其他方法

* 分离链接法
* 每个数组槽是一个SearchList
* ![image-20220607223321936](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607223321936.png)

* deletions are not a problem

#### 4.3 Dealing with A Full Table

![image-20220607223454268](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607223454268.png)



## Lecture24 Introduction to Graph Theory

### 1. Basic Definitions Of Graph Theory

图G包括:

* 顶点V(G)的有限集合，不能为空
* 以及连接顶点对的有限边集E(G)。

**G中的顶点数称为G的阶数，用|V|表示。**

![image-20220607224548288](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607224548288.png)



### 2.关联Incidence，邻接adjacency和邻居neighbors

* 如果两个顶点由一条边连接，则它们是相邻adjacency的。
* 相邻的顶点称为相邻neighbors顶点。
* 连接顶点的边称为与顶点关联的边。

### 3. Multiple edges重边, loops循环 and simple graphs线连通简单图

* 连接同一对顶点的两条或多条边称为多条边。
* 将一个顶点与自身连接起来的边称为环。
* 一个不包含多个边或环的图称为简单图

### 4. Weighted Graphs(权重图)

![image-20220607230540580](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607230540580.png)

### 5. Digraphs(有向图)

![image-20220607230838776](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607230838776.png)



### 6. Degree（度）

边与顶点V关联的次数称为顶点度，用d(V)表示。

## Lecture25 

![image-20220607232905209](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607232905209.png)

### 关于adjacency and incidence matrices的相关例题

adjacency matrices 邻接矩阵

两个点之间是否存在线，有1条就是1，没有0，多条就是相应的数字

incidence matrices 关联矩阵

点与线段之间的关系，这个点有这条线就是1，没有就是0.

![image-20220607232944962](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607232944962.png)

![image-20220607233010299](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607233010299.png)



![image-20220607234125122](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607234125122.png)

![image-20220607234143368](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607234143368.png)



![image-20220607234200262](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607234200262.png)

![image-20220607234213146](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607234213146.png)



## Lecture26 Introduction to Graph Theory 

### 1. Trees

![image-20220607234702488](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607234702488.png)

![image-20220607235252069](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607235252069.png)



#### 1.1 Minimum spanning tree（最小生成树）

![image-20220607235339703](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607235339703.png)



#### 1.2 The shortest path problem

![image-20220607235411127](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220607235411127.png)







