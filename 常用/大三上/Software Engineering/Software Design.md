## Software Design

<font color='red' size=5>Deriving a solution which satisfies software requirements. </font>

<font color='red' size=5>推导出解决软件需求的方法</font>

## Lecture13  Design Methodology1

### 1. The Design Problems

![image-20221203204115536](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221203204115536.png)



### 2. Software Design 软件设计

* Why
  * Software is produced by many people 软件是由很多人一同设计的
  * Software needs to be
    * Simple 简单
    * Understandable 易于理解
    * Flexible  灵活
    * Portable 便携
    * Re-usable 重复使用
* How
  * Complex to simple  将复杂的东西简化
  * Abstraction 抽象



#### 2.2 Software Design in Reality  现实中设计软件

* Design mixed with implementation 设计往往混合着实现
  * Design step 1
    * Implement and add more design
  * Design step 2
    * Implement and add more design
  * In effect much of software is designed while coded and the 
    design document doesn’t reflect the final product  实**际上，许多软件都是在编码的同时设计的，设计文档并不能反映最终的产品**

#### 2.3 Stages of Design 设计阶段

* **Problem understanding** 理解问题
  * Look at the problem from different angles to discover the 
    design requirements. 从不同的角度看问题,发现设计要求。
* **Identify one or more solutions** 定义一种或多种解决方案
  * Evaluate possible solutions and choose the most appropriate 
    depending on the designer's experience and available 
    resources. 评估可能的解决方案，并根据设计师的经验和可用资源选择最合适的解决方案。
* **Describe solution abstractions** 描述抽象的方法
  * Use graphical, formal or other descriptive notations to 
    describe the components of the design. 使用图形、正式或其他描述性符号来描述设计的组件。
* **Repeat process for each identified abstraction**   对所有的抽象重复以上进程
  * until the design is expressed in primitive terms. 直到设计以原始术语表示。

![image-20221203220358544](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221203220358544.png)

#### 2.4 The Design Process 设计过程

* <font color='red'>Any design may be modeled as a directed graph made up </font>of entities with attributes which participate in relationships.  **任何设计都可以被建模为一个有向图，由具有参与关系的属性的实体组成。**
* The system should be described at several different levels of abstraction.**系统应该在几个不同的抽象级别上进行描述。** 
* <font color='red'>Design takes place in overlapping stages.</font> It is artificial to separate it into distinct phases but some separation is usually necessary. **设计发生在重叠的阶段。把它分为不同的阶段是人为的，但通常需要一些分离。**

![image-20221203220744189](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221203220744189.png)



##### 2.4.1 Phases in the Design Process 设计过程的各个阶段

这是对整个过程的概述

![image-20221203220909395](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221203220909395.png)

#### 2.5 Design Phases 设计阶段

* **Architectural design: Identify sub-systems.  体系结构设计:确定子系统。**

  

* **Abstract specification: Specify sub-systems.  抽象规范:指定子系统。**

  

* **Interface design: Describe sub-system interfaces. 接口设计:描述子系统接口。**

  

* **Component design: Decompose sub-systems into components. 组件设计:将子系统分解为组件。**

  

* **Data structure design: Design data structures to hold problem data. 数据结构设计:设计数据结构来保存问题数据。**

  

* **Algorithm design: Design algorithms for problem functions.  算法设计:问题函数的设计算法。**

### 3. Design （设计中的相关细节）

**相比于前面关于软件设计的大的框架，这里更倾向于一些关于模块的细节**

* Computer systems are not monolithic: they are usually composed of multiple, interacting modules.  计算机系统不是单一的:它们通常由多个相互作用的模块组成。
* **<font color='red'>Modularity</font>** has long been seen as a key to cheap, high quality software. **模块化**一直被视为廉价、高质量软件的关键。
* The goal of system design is to decode:
  *  What the modules are; 模块是什么;
  *  What the modules should do; 模块应该做什么;
  *  How the modules interact with one-another 模块之间如何交互



#### 3.1 Modelar Programming 模块化程序设计

* In the early days, modular programming was taken to mean constructing programs out of small pieces: 
  “subroutines”
* 在早期,模块化编程被认为是在小片段中构建程序:“子例程”
* But modularity cannot bring benefits unless the modules 
  are  除法模块是自治，连贯，稳固的，否则模块化不会带来好处
  * autonomous, 
  * coherent and 
  * robust

![image-20221203224127187](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221203224127187.png)

#### 3.2 Procedural Abstraction 过程抽象

* The most obvious design methods involve **functional decomposition**. 最明显的设计方法涉及功能分解。
* This leads to programs in which **procedures represent distinct logical functions in a program.** 这导致程序中的过程在程序中代表不同的逻辑函数。
* Examples of such functions:
  * “Display menu” 显示菜单
  * “Get user option” “获取用户选项”
* This is called **procedural abstraction** 这被称为过程抽象

![image-20221203224139931](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221203224139931.png)

#### 3.4 Programs as Functions 

* Another view is programs as functions: 有的观点将程序视为一个函数
      input             output
  x ->    f   ->  f (x)    
  the program is viewed as a function from a set I of legal inputs to a set O of outputs.  程序被视为从一组合法输入到一组输出的函数。
* There are programming languages (ML, Miranda, LISP) that directly support this view of programming  有编程语言(ML、Miranda、LISP)直接支持这种编程的观点

![image-20221203224300505](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221203224300505.png)



#### 3.5 Object-Oriented Design 面向对象的设计

*  **The system is viewed as a collection of interacting objects. 系统被看作是相互作用的对象的集合。**
*  The **<font color='red'>system state is decentralized</font>** and each object manages its own state. **系统状态是分散的，每个对象管理自己的状态**。 
*  Note , use of internal state against functional programming 注意，在函数式编程中使用内部状态
*  Objects may be instances of an object class and communicate by exchanging messages. 对象可以是对象类的实例，并通过交换消息进行通信。

![image-20221203225608049](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221203225608049.png)



#### 3.6 Five Criteria for Design Methods 设计方法的五种标准（用于评估模块的设计方法）

* We can identify five criteria to help evaluate modular design methods:  我们可以确定五个标准来帮助评估模块化设计方法:
  * Modular decomposability模块化分解;
  * Modular composability;模块化组合;
  * Modular understandability;模块化的理解能力;
  * Modular continuity;模块化延续;
  * Modular protection.模块化保护

![image-20221204104419941](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204104419941.png)

##### 3.6.1 Modular Decomposability  模块化分解

* <font color='red'>**Modular decomposability**</font> - this criterion is met by a design method if the method supports the decomposition of a problem into smaller sub-problems, which can be solved independently.  
* 如果设计方法支持将问题分解为更小的子问题，那么该设计方法就满足了这一标准。
* In general, this method will be **repetitive**: sub-problems will be divided still further 
* 一般来说，这种方法是重复的:子问题将被进一步划分
* **Top-down design methods** fulfil this criterion; **stepwise refinement** is an example of such a method     
* **自上而下的设计方法**满足这一标准;  逐步细化就是这种方法的一个例子
* ![image-20221204104440627](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204104440627.png)

* EXAMPLE：Hierarchical Design Structure 分层设计结构
* ![image-20221204103843756](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204103843756.png)

###### 3.6.1.1 Top-Down Design 自上而下的设计

* **In principle, top-down design involves starting at the uppermost components in the hierarchy and working down the hierarchy level by level.** 
* **原则上,自上而下的设计包括从层次结构中最上面的组件开始,并按等级水平降低层次结构。**
* In practice, large systems design is never truly top-down. Some branches are designed before others. Designers reuse experience (and sometimes components) during the design process.
* 在实践中,大型系统设计从来没有真正自上而下。有些分支是在其他分支之前设计的。在设计过程中,设计人员重用经验(有时是组件)<font color=blue>就是重复利用某些组件</font>。
* ![image-20221204104801168](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204104801168.png)

* **EXAMPLE：**
* Imagine designing a word processor program from scratch. What subsystems could be initially found at the top level?
* 想象一下从头开始设计一个文字处理器程序。在顶层最初可以找到哪些子系统?
* File I/O, printing, graphical user interface, text processing etc. 文件I/O，打印，图形用户界面，文本处理等。
* For each of these components we can then decompose further, i.e., File I/O comprises of saving documents and opening documents. 对于这些组件，我们可以进一步分解，例如，文件I/O由保存文档和打开文档组成。

![image-20221204105121154](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204105121154.png)

##### 3.6.2 Modular Composability 模块化组合

* **Modular composability** - a method satisfies this criterion if it leads to the production of modules that may be freely combined to produce new systems.
* 模块化组合能力-一种方法满足这个标准,如果它导致模块的生产,可以自由组合以产生新的系统。
* Composability is directly related to the issue of reusability 
* 可组合性直接与可重用性问题有关
* Note that **composability** is often at odds with **decomposability**; top-down design,  注意，可组合性通常与可分解性不一致;   自上向下设计
  * for example, it tends to produce modules that may not be composed in the way desired  例如,它倾向于生成可能不需要的模块 <font color=blue>比如一个库里包含很多函数，并不是的所有的函数都需要是在某一方法中要使用的</font>
* This is because top-down design leads to modules which fulfil a specific function, rather than a general one  这是因为自上向下的设计导致模块完成特定的功能，而不是一般的功能

![image-20221204114628870](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204114628870.png)

* EXAMPLE：
* The Numerical Algorithm Group (NAG) libraries contain a wide range of routines for solving problems in linear algebra, differential equations, etc. 
* 数值算法组(NAG)库包含解决线性代数、微分方程等问题的广泛例程。
* The Unix shell provides a facility called a pipe, written “|”, whereby 
* Unix shell提供了一个叫做管道的工具，写为" | "
  * 一个程序的标准输出可以重定向到另一个程序的标准输入;这种约定有利于可组合性。

![image-20221204114638596](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204114638596.png)

##### 3.6.3 Modular Understandability  模块可理解性

* Abstraction
  *  int A=21
  *  int age_in_years = 21;     print_out_document(Document d)
* **Modular Understandability** - a design method satisfies this criterion if it encourages the development of modules which are easily understandable.
* 模块化的可理解性——设计方法满足这个标准,如果它鼓励模块的开发很容易让人理解的。
* 反例1。使用一千个行程序,不包含任何程序;它只是一个长时间的顺序语句列表。把它分成20个街区,每50个语句长,每一个街区都有一个方法。

![image-20221204115021022](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204115021022.png)

* Related to several component characteristics 与几个部件的特性有关
  * 组件本身可以被理解吗?
  * 是否使用了有意义的名字?
  * 设计是否有良好的文档记录?
  * 是否使用了复杂的算法?
* **Informally, high complexity means many relationships between different parts of the design. 非正式地说，高复杂性意味着设计的不同部分之间有许多关系。**



##### 3.6.4 Modular Continuity 模块可延续性 ？？？

* **Modular continuity** - a method satisfies this criterion if it leads to the production of software such that a small change in the problem specification leads to a change in just one (or a small number of ) modules.
* **模块化连续性**——如果一种方法能够导致软件的生产，使得问题规范中的一个小变化只会导致一个(或少量)模块的变化，那么这种方法就满足了这一标准。
* **感觉更像是添加某个方法后，该模块仍可以正常工作，不会受到影响。**
* EXAMPLE. Some projects enforce the rule that no numerical or textual literal should be used in programs: only symbolic constants should be used
* EXAMPLE: 有些项目强制执行在程序中不应该使用数字或文本文字的规则:只应该使用符号常量
* COUNTER EXAMPLE. Static  arrays (as opposed to dynamic arrays) make this criterion harder to satisfy.
* 反例。静态数组(与动态数组相反)使该标准更难满足。



##### 3.6.5 Modular Protection 模块保护性

* **Modular Protection** - a method satisfied this criterion if it yields architectures in which the effect of an abnormal condition at run-time only effects one (or very few) modules
* **模块化保护**——一种满足这一标准的方法，如果它产生的体系结构中，运行时异常状态的影响只影响一个(或极少数)模块
* EXAMPLE：
* 在源处验证输入可以防止错误在整个程序中传播(契约式设计)
* COUNTER EXAMPLE：
* 在适合子类型或短类型的地方使用int类型。

![image-20221204120345624](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204120345624.png)

![image-20221204120521900](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204120521900.png)

* <font color='red'>组件重用通常是一件好事,但必须注意组件开发的假设仍然有效!</font>

### 4. Repository Models 存储库模型

* Sub systems making up a system must exchange and share data so they can work together effectively.
* 组成一个系统的子系统必须交换和共享数据，这样它们才能有效地一起工作。
* There are two main approaches to this:
  * The repository model – All shared data is held in a central database which may be accessed by all sub-systems
  * **存储库模型——所有共享数据都保存在一个中央数据库中，所有子系统都可以访问该数据库**
  * Each sub-system or component maintains its own database. Data is then exchanged between sub-systems via message passing.
  * 每个子系统或组件维护自己的数据库。然后通过消息传递在子系统之间交换数据。
* There are advantages and disadvantages to each approach as we shall now see. 
* 我们现在看到的每一种方法都有优点和缺点。

![image-20221204121043220](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204121043220.png)

**Advantage:**

1. Databases are an efficient way to share large amounts of data and data does not have to be transformed between different sub-systems (they agree on a single data representation).
2. 数据库是共享大量数据和数据的有效方法,不需要在不同的子系统(它们在单个数据表示上达成一致)之间进行转换。
3. Sub-systems producing data need not be concerned with how that data is used by other sub-systems.
4. 产生数据的子系统不需要关心其他子系统如何使用该数据。
5. Many standard operations such as backup, security, access control, 
   recovery and data integrity are centralised and can be controlled by a single repository manager.
6. 许多标准操作，如备份、安全、访问控制、恢复和数据完整性都是集中的，可以由单个存储库管理器控制。
7. The data model is visible through the repository schema.
8. 数据模型通过存储库模式可见。

**Disadvantage:**

1. Sub-systems must agree on the data model which means compromises must be made, for example with performance.
2. 子系统必须就数据模型达成一致，这意味着必须做出妥协，例如在性能方面。
3. Evolution may be difficult since a large amount of data is generated and translation may be difficult and expensive.
4. 进化可能很难,因为大量的数据产生和翻译可能是困难和昂贵的。<font color=blue>（这里的evolution意思应该是更改，系统更新）</font>
5. Different systems have different requirements for security, recovery and backup policies which may be difficult to enforce in a single database.
6. 不同的系统对安全、恢复和备份策略有不同的要求,这些策略可能很难在单个数据库中执行。
7. It may be difficult to distribute the repository over a number of 
   different machines.
8. 在许多不同的机器上分布存储库可能很困难。

### 5. Lecture Key Points

![image-20221204122052029](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204122052029.png)



## Lecture14 Design Methodology2

### 1. Software Design

*  **In this lecture we shall again be looking at how to derive a software solution which satisfies the software requirements.**
*  **在这一讲中，我们将再次看看如何推导一个软件解决方案，满足软件需求。**
*  We shall be examining ways in which architecture designs and individual components can be said to be “good” in practice.
*  我们将研究如何在实践中说架构设计和单个组件是“好的”。

![image-20230104152052216](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104152052216.png)



* We may remark that a good system has the following properties:  我们一般认为一个好的系统需要有以下属性
  * Useful and usable; 有效的
  * Reliable; 可靠的
  * Flexible; 灵活的
  * Affordable; 可承担的
  * Available. 可用
* During this lecture we will be considering design properties of modules. 
* <font color=red>在这堂课中，我们将讨论模块的设计属性。</font>

![image-20230104163100295](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104163100295.png)

### 1. Module Interfaces 模块接口

* Firstly let us recall what an interface is. 首先让我们回忆一下什么是接口。
  * An interface to a module defines some features of the module upon which other parts of the system may rely. 
  * **模块的接口定义了模块的一些特性系统的其他部分可以依赖的模块。**
  * <font color='blue'>一个模块可以通过接口调用其他模块的方法</font>
* It is thus an abstraction of the module. Encapsulation of the module means that users of the module cannot know more about the module than is given by the interface.
* 因此它是模块的抽象。封装模块意味着模块的用户不能知道更多信息关于模块的信息比接口给出的要多。
* Any assumptions about interfaces should be documented in the interface.  
* 任何关于接口的假设都应该记录在接口。
  * This means that any changes to the internals of a module not causing a change to the interface should not necessitate a change to other parts of the system.
  * 这意味着对模块内部的任何更改都不会导致对接口的更改，不需要对系统的其他部分进行更改。

![image-20221204124219258](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204124219258.png)

**EXAMPLE**

* On the previous slide, do you know how to compute the cross product of two vectors?  
* 在上一张幻灯片中，你们知道如何计算两个向量的外积吗?
  * The point is that due to abstraction, you do not need to know, that information is hidden in the module!
  * 关键的地方由于抽象
* We may choose to replace the code for computing the cross product to be faster or more numerically stable for example, but users of the module (or component) should not need to change their code since the interface has not changed. 
* 我们可能会选择替换计算叉乘的代码，以更快或更稳定的数字为例，但模块(或组件)的用户不需要更改他们的代码，因为接口没有更改。

### 2. Five Principles for Good Design

* From the discussion in the previous lecture, we can derive five principles that should be adhered to:

* 从上节课的讨论中，我们可以得出五个应该坚持的原则:

  * **Linguistic modular units; 语言模块化单元**
  * **Few interfaces; 几个接口**
  * **Small interfaces;小接口**
  * **Explicit interfaces;显式接口**
  * **Information hiding.信息隐藏**

  


![image-20221204125530756](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204125530756.png)

#### 2.1 Linguistic Modular Units 语言模块化单元

* A programming language (or design language) should support the principle of linguistic modular units:
* 编程语言(或设计语言)应该支持语言模块化单元的原则:
  * Modules must correspond to linguistic units in the language used
  * 模块必须与所使用语言中的语言单位相对应
* ![image-20221204125549362](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204125549362.png)

#### 2.2 Few Interfaces 几个接口

* This principle states that the overall number of communication channels between modules should be as small as possible:
* **这个原则指出模块之间的通信通道的总数应该尽可能小:**
  * Every module should communicate with as few others as possible.
  * 每个模块应该尽可能少地与其他模块通信。
* So, in the system with n modules, there may be a minimum of              n(n-1) /2 and a maximumn n(n-1) /2 of links; your system should stay closer to the minimum.
* 因此，在有n个模块的系统中，可能有最小的n-1个和最大的n(n-1) /2链接;  你的系统应该更接近最小值。

![image-20230104160850348](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104160850348.png)

![image-20221204130835867](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204130835867.png)

**外观结果**

![image-20221204130922631](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204130922631.png)



#### 2.3 Small Interfaces(Loose Coupling) 小接口 （松耦合）

* Loose coupling implies that :  松耦合意味着:
  * **If any two modules communicate, they should exchange as little information as possible.**  
  * **如果任何两个模块通信，它们应该交换信息越少越好。**
* An interface to a module defines the features on which a client may rely and the rest of the system can only use the module as permitted by the interface. 
* 模块的接口定义了客户端可能依赖的特性，而系统的其他部分只能在接口允许的情况下使用该模块。
* **COUNTER EXAMPLE.  Declaring all instance variables as public!**
* **反例。声明所有实例变量为公共的!**

### 3. Coupling 耦合

* Coupling is a measure of the strength of the inter-connections between system components.

* **<font color=red>耦合是衡量系统组件之间相互连接强度的指标。</font>**

* Loose coupling means component changes are unlikely to affect other components.

* **松耦合意味着组件更改不太可能影响其他组件。**

  * Shared variables or control information exchange lead to **tight coupling** (usually bad).
  * 共享变量或控制信息交换导致**紧密耦合**(通常是不好的)。
  * Loose coupling can be achieved by state decentralization (as in objects) and component communication via parameters or message passing
  * 松耦合可以通过状态分散(如对象)和通过参数或消息传递的组件通信来实现。

  ![image-20221204131910184](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204131910184.png)



![image-20221204131918790](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204131918790.png)

##### 2.3.2 Coupling and Inheritance 耦合和继承

* Object-oriented systems are loosely coupled because there is no shared state and objects communicate using message passing. 
* 面向对象的系统是松散耦合的，**因为没有共享的状态和使用消息传递的对象通信。**

* However, an object class is coupled to its **super-classes**. Changes made to the attributes or operations in a super-class propagate to all sub-classes.
* 然而，对象类与它的超类是耦合的。**对超类中的属性或操作所做的更改会传播到所有子类**。

![image-20221204132646319](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204132646319.png)

#### 2.5 Reusability 重用性

* A major obstacle to the production of cheap quality software is the intractability of the reusability issue.

* 生产廉价高质量软件的一个主要障碍是难以解决的可重用性问题。
* Why isn’t writing software more like producing hardware?  Why do we start from scratch every time, coding similar problems time after time after time?

* 为什么写软件不更像生产硬件?为什么我们每次都从头开始，一次又一次地编写类似的问题?
* Obstacles: 障碍
  * Economic  经济
  * Organizational  组织
  * Psychological 心理

##### 2.5.1 Stepwise Refinement 逐步求精

* The simplest realistic design method, widely used in practice.  
* 最简单的写实设计方法，在实践中广泛应用。
* Not appropriate for large-scale, distributed systems: mainly applicable to the design of methods. 
* 不适用于大规模、分布式系统:主要适用于设计方法。
* Basic idea is: 基本思想是:
  * Start with a high-level spec of what a method is to achieve; 
  * 从一个方法要实现的高级规范开始；
  * Break this down into a small number of problems (usually no more than 10)
  * 把这个问题分解成几个问题(通常不超过10个)
  * For each of these problems do the same; 
  * 对于每一个这些问题做同样的事情;
  * Repeat until the sub-problems may be solved immediately.
  * 重复执行，直到子问题可能立即得到解决。

![image-20221204160121546](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204160121546.png)



### 4. Explicit Interfaces 显示接口 （2.5）

* **If two modules must communicate, they should do it so that we can see it: 如果两个模块必须通信，它们应该这样做**
  * **If modules A and B communicate, this must be obvious from the documentation of A or B or both.**
  * **如果模块A和模块B通信，这必须从A或B或两者的文档中可以很明显的看出**
* Why? If we change a module, we need to see what other modules may be affected by these changes. A traceability matrix can be used for this purpose.
* 为什么?如果我们更改了一个模块，我们需要查看哪些其他模块可能会受到这些更改的影响。可导性矩阵可用于此目的。

![image-20221204160900434](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204160900434.png)

#### 4.1 Information Hiding (Encapsulation)  信息隐藏(封装)

* This principle states: 该原则指出:

  * All information about a module, (and particularly how the module does what it does) should be private to the module unless it is specifically declared otherwise. 
  * 关于模块的所有信息(特别是模块如何做它所做的事情)都应该是模块私有的，除非特别声明了。

* Thus each module should have an interface, which is how the world sees it anything beyond that interface should behidden.  There is a limit to how much humans canunderstand at any one time. 

* 因此，每个模块都应该有一个接口，这是世界看到它的方式，任何超出该接口的东西都应该在后面。人类在任何时候所能理解的东西都是有限的。

* The default Java rule: 默认的Java规则:

  * Make everything private 让一切都私人化

  ![image-20221204161234182](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204161234182.png)

**<font color='blue'>锐评，private声明</font>**

### 5. Cohesion 内聚性

* **Cohesion - A measure of how well a component “fits together”**
* **内聚性——衡量组件“相互配合”的程度**

* A component should implement a single logical entity or function.
* 组件应该实现单个逻辑实体或功能。
* Cohesion is a desirable design component attribute as when a change has to be made, it is localized in a single cohesive component.
* 内聚是一个理想的设计组件属性，因为当必须进行更改时，它被本地化到单个内聚组件中。
* Various levels of cohesion have been identified.
* 各种层次的凝聚力已被确定。

![image-20221204162705804](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204162705804.png)

#### 5.1 Cohesion Levels 内聚等级

* Coincidental cohesion (weak) 巧合内聚(弱)

  * Parts of a component are simply bundled together.
  * 组件的各个部分简单地捆绑在一起。

* Logical association (weak) 逻辑关联(弱)

  * Components which perform similar functions aregrouped.
  * 执行类似功能的组件被分组。

* Temporal cohesion (weak) 时间内聚(弱)

  * Components which are activated at the same time are grouped.
  * 同时被激活的组件是同一组

* Communicational cohesion (medium) 通信聚合(中)

  * All the elements of a component operate on the same input or produce the same output.
  * 一个组件的所有元素操作相同的输入或产生相同的输出。

* Sequential cohesion (medium) 顺序内聚(中等)

  * The output for one part of a component is the input to another part.
  * 组件一部分的输出是另一部分的输入。

* Functional cohesion (strong) 功能内聚性(强)

  * Each part of a component is necessary for the execution of a single function.
  * 组件的每个部分对于单个函数的执行都是必要的。

* Object cohesion (strong) 对象内聚性(强)

  * Each operation provides functionality which allows object attributes to be modified or inspected.
  * 每个操作都提供了允许修改或检查对象属性的功能。

  

  ![image-20221204163830860](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204163830860.png)

  ![image-20221204163853178](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204163853178.png)

#### 5.2 Cohesion as a Design Attribute 设计结构的内聚

* The concept of cohesion is not well-defined and is often difficult to classify.  内聚的概念没有很好的定义，通常很难分类。
* Inheriting attributes from super-classes weakens cohesion. 从超类继承属性会削弱内聚性。
  * To understand a component, the super-classes as well as the component class must be examined. 要理解一个组件，必须检查超类和组件类。
  * Object class browsers assist with this process.对象类浏览器可以帮助这个过程。

#### 5.3 Cohesion versus Encapsulation 内聚与封装

* **Cohesion** is a measure of abstraction that means developers do not need concern themselves with the internal working of a module.
* 内聚是一种抽象度量，这意味着开发人员不需要关心模块的内部工作。
* **内聚就是指程序内的各个模块之间的关系紧密程度**
* **Encapsulation** means that developers are unable to use hidden information within a module, ensuring that subtle errors cannot be introduced when using connected modules.
* 封装意味着开发人员不能在模块中使用隐藏的信息，从而确保在使用连接的模块时不会引入细微的错误。
* ![image-20230104162910636](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104162910636.png)

![image-20221204164743601](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204164743601.png)

![image-20221204164906551](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204164906551.png)

![image-20221204165054743](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204165054743.png)

![image-20230104162828517](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104162828517.png)



###### 6. Lecture Key Points

![image-20221204165121367](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204165121367.png)



## Lecture15 Distributed System Architectures 1

![image-20221204165833039](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204165833039.png)

### 1. Software Architecture 软件架构

* **The design process for identifying the sub-systems making up a system and the framework for sub-system control and communication is architectural design.**
* **确定构成系统的子系统以及子系统控制和通信框架的设计过程就是架构设计。**
* The output of this design process is a description of **the software architecture**
* 这个设计过程的输出是对以下内容的描述 软件架构

#### 1.1 Architectural Design 架构设计

* **Architectural design should be an early stage of the system design process**
* **架构设计应该是系统设计过程的一个早期阶段**
* Represents the link between specification and design processes
* 代表了规范和设计过程之间的联系
* Often carried out in parallel with some specification activities
* 通常与一些规格活动同时进行
* It involves identifying **major system components** and their **communications**
* 它涉及到识别主要的系统组件和它们的通信

![image-20221204181915341](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204181915341.png)

##### 1.1.1 Architectural Design Process

* **System structuring** 系统结构设计
  *  The system is decomposed into several principal sub- systems and communications between these sub-systems are identified.
  *  该系统被分解成几个主要的子系统，并确定这些子系 统之间的通信。
* **Control modelling**  控制模型
  * A model of the control relationships between the different parts of the system is established.
  * 建立了系统不同部分之间的控制关系模型
* **Modular decomposition**  模块化分解
  * The identified sub-systems are decomposed into modules.
  * 确定的子系统被分解为模块
* **System-> Sub-System -> Module**

###### 1.1.1.1 Sub-systems and Modules 子系统和模块

Sub-System:

* A **sub-system** is a system in its own right whose operation is independent of the services provided by other sub-systems

* 子系统是一个独立的系统，它的操作独立于其他子系统提供的服务。

Module:

* A **module** is a system component that provides services to other components but would not normally be considered as a separate system
* 模块是一个系统组件，为其他组件提 供服务，但通常不会被视为一个独立 的系统。

![image-20230104165925064](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104165925064.png)

![image-20221204182757832](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204182757832.png)

![image-20221204182807170](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204182807170.png)

![image-20221204182834072](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204182834072.png)

![image-20221204182847485](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204182847485.png)

<font color=blue>所谓的拉条线就能让两个子系统互相联系从而实现新的功能, 通过多个子系统组合来生成新的系统。感觉好像可以重复利用同一个子系统</font>

##### 1.1.2 Architectural Models 架构模型

* Different architectural models may be produced during the design process
* 在设计过程中可能会产生不同的建筑模型
* **Each model presents different perspectives on the architecture:**
* **每个模型都提出了关于架构的不同视角**
  * **Static structural model 静态结构模型**
  * **Dynamic process model 动态过程模型**
  * **Interface model 界面模型**
  * **Relationships model 关系模型**

![image-20221204183335420](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204183335420.png)

1. **Static structural models** show the major system components
   1. 静态结构模型显示了系统的主要组成部分
2. **Dynamic process models** show the process structure of the system
   1. 动态过程模型显示系统的过程结构
3. **Interface models** define sub-system interfaces
   1. 接口模型定义子系统接口
4. **Relationships models** such as a data-flow model
   1. 关系模型，如数据流模型



#### 1.2 System Structuring 系统结构化

**Concerned with decomposing the system into interacting****sub-systems**

将系统分解为相互作用的子系统

* The architectural design is normally expressed as a **block diagram** presenting an overview of the system structure
* 架构设计通常以**框图**的形式表达，展示系统结构的 概况
  * (More specific models showing how sub-systems share data, are distributed and interface with each other may also be developed)
  * (也可以开发更多的具体模型，显示子系统如何共享数据 ，如何分布，如何相互连接
* ![image-20221204192356338](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204192356338.png)



##### 1.2.1 The Repository Model  存储库模型

* **Sub-systems must exchange data**. This may be done in two ways:

* 子系统必须交换数据。这可以通过两种方式进行

  * 1.Shared data is held in a central database or repository and may be accessed by all sub-systems
  * 共享数据保存在一个中央数据库或存储库中，所有子 系统都可以访问。
  * 2.Each sub-system maintains its own database and passes data explicitly to other sub-systems
  * 每个子系统维护自己的数据库，并将数据明确地传 递给其他子系统

  

* 当需要共享大量数据时，最常使用的是Repository Model的共享模式

![image-20221204193314780](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204193314780.png)



#### 1.3 Client-Server Architecture 客户端-服务器架构

* **Distributed system model which shows how data and processing is distributed across a range of components:**
* **分布式系统模型，显示数据和处理是如何分布在一 系列组件上的。**
  * **Set of stand-alone servers** which provide specific services such as printing, data management, etc.
  * **一组独立的服务器，提供特定服务**，如打印 、数据管理等。
  * **Set of clients** which call on these services
  * 调用这些服务的一组客户
  * **Network** which allows clients to access servers
  * 允许客户访问服务器的网络

![image-20221204193943946](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204193943946.png)

一个客户端-服务器的系统实例

![image-20221204194047958](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204194047958.png)

![image-20221204194056349](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204194056349.png)

##### 1.3.1 Client-Server Characteristics  客户端-服务器特征

* Advantages

  * Distribution of data is straightforward 数据的分配是直接的
  * Makes effective use of networked systems. May require cheaper hardware 有效地利用了网络系统。可能需要更便宜的硬件
  * Easy to add new servers or upgrade existing servers 易于增加新的服务器或升级现有服务器

* Disadvantages

  * No shared data model so sub-systems use different data organisation. data interchange may be inefficient  没有共享的数据模型，所以子系统使用不同的数据 组织。数据交换可能是低效的。

  * Redundant management in each server  每个服务器的冗余管理

  * No central register of names and services - it may be hard to find out what servers and services are available  没有名称和服务的中央登记册--可能很难发现有哪些 服务器和服务可用




#### 1.4 Control Models 控制模型

**Control Models are concerned with the control flow between sub systems:**

**控制模型关注子系统之间的控制流**

* **Centralised control**  集中控制
  * One sub-system has overall responsibility for control and starts and stops other sub-systems
  * 一个子系统全面负责控制并启动和停止其他子系统
* **Event-based control** 基于事件的控制
  * Each sub-system can respond to externally generated events from other sub-systems or the system’s environment
  * 每个子系统都可以对来自其他子系统或系统环境的外部 产生的事件作出反应

##### 1.4.1  Centralised Control 集中控制

* A control sub-system takes responsibility for managing the execution of other sub-systems. <font color='red'>There are two main types of centralised control models (sequential or parallel)</font>

* 一个控制子系统负责管理其他子系统的执行。**有两种主要的集中控制模式（顺序或平行）**

* **首先是顺序系统**

  * Firstly, there is the **call-return model**   首先，是调用-返回的模式
    * Top-down subroutine model where control starts at the top of a subroutine hierarchy and moves downwards.  Applicable to **sequential systems**
    * 自上而下的子程序模型，控制从子程序层次结构的 顶端开始，然后向下移动。适用于顺序系统
    * Such a model is embedded into familiar programming languages such as C, Java, Pascal etc.
    * 这样的模型被嵌入到熟悉的编程语言中，如C、 Java、Pascal等。

  ![image-20221204200624953](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204200624953.png)

  我附庸的附庸，不是我的附庸

* **其次是平行系统**

  * If the controlled subsystems run **in parallel**, then we may use the manager model of centralised control:
  * 如果被控制的子系统是平行运行的，那么我们可以使 用集中控制的控制模式。
    * Manager Model 管理模式
    * <font color='red'>**Applicable to concurrent systems.** </font>One system component controls the stopping, starting and coordination of other system processes. Can also be implemented in sequential systems as a case statement.
    * 适用于并发系统。一个系统组件控制其他系统进程 的停止、启动和协调。也可以在顺序系统中作为 case语句来实现。

![image-20221204201210795](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204201210795.png)

##### 1.4.2  Event-Driven Systems 事件驱动系统

* **Driven by externally generated events** where the timing of the event is out of the control of the sub-systems which process the event
* 由外部产生的事件驱动，事件发生的时间不受处理该 事件的子系统的控制
* There are two principal event-driven models:
  *  **Broadcast models**. An event is broadcast to all sub-systems.  Any sub-system which can handle the event may do so
  *  **广播模式**。 一个事件被广播给所有的子系统。任何能够 处理该事件的子系统都可以这样做
  *  **Interrupt-driven models**. Used in real-time systems where interrupts are detected by an interrupt handler and passed to some other component for processing
  *  **中断驱动的模型**。在实时系统中使用，中断由中断处 理程序检测，并传递给其他一些组件进行处理。

![image-20221204201840563](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204201840563.png)

###### 1.4.2.1 Broadcast Model 广播系统

* **Effective in integrating sub-systems** on different computers in a network 
* 有效整合网络中不同计算机上的子系统
* **Sub-systems register an interest in specific events. When these occur, control is transferred to the sub- system which can handle the event**
* **子系统注册对特定事件感兴趣。当这些事件发 生时，控制权被转移到能够处理该事件的子系 统中。**
* **Control policy is not embedded in the event** and message handler. Sub-systems decide on events of interest to them
* 控制策略没有嵌入到事件和消息处理程序中。 子系统决定对其感兴趣的事件
* **However**, sub-systems don’t know if or when an event will be handled
* 然而，子系统不知道一个事件是否或何时会被处理

![image-20221204203023712](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204203023712.png)

###### 1.4.2.2 Interrupt-Driven Systems 中断驱动式系统

* **Used in real-time systems** where fast response to an event is essential
* 用于对事件做出快速响应至关重要的实时系统
* There are known interrupt types with a handler defined for each type
* 有已知的中断类型，为每种类型定义了一个处理程序
* Each type is associated with a memory location and a hardware switch causes transfer to its handler
* 每种类型都与一个内存位置相关联，硬件开关会导致传输到其处理程序
* Allows fast response but complex to program and difficult to validate
* 允许快速响应，但编程复杂且难以验证

![image-20221205172821716](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221205172821716.png)



#### 1.5 Modular Decomposition 模块化分解

* Another structural level where sub-systems are decomposed into modules
* 模块化分解
* Two modular decomposition models covered 涵盖两个模块化分解模型
  * An object model where the system is decomposed into interacting objects
  * **将系统分解为交互对象的对象模型**
  * A data-flow model where the system is decomposed into functional modules which transform inputs to outputs. Also known as the pipeline model
  * **一种数据流模型，其中系统被分解为将输入转换为输出的功能模块。也称为管道模型**
* If possible, decisions about concurrency should be delayed until modules are implemented 
* 如果可能的话，关于并发性的决定应该延迟到模块实现之前



##### 1.5.1 Object Model 对象模型

* Structure the system into a set of loosely coupled objects with well-defined interfaces
* 将系统构造成一组松散耦合的对象，这些对象具有定义良好的接口
* **Object-oriented decomposition** is concerned with identifying 
* 面向对象分解涉及识别
  * object classes  对象类
  * their attributes  属性
  * operations 操作
* When implemented, objects are created from these classes and some control model used to coordinate object operations
* 当实现时，对象是从这些类和一些用于协调对象操作的控制模型中创建的

![image-20221205173902320](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221205173902320.png)



##### 1.5.2 Data-Flow Models 数据流

* Functional transformations process their inputs to produce outputs
* 功能转换处理其输入以产生输出
* May be referred to as a pipe and filter model (as in UNIX  shell)
* 可以称为管道和过滤器模型（如UNIXshell）
* Variants of this approach are very common. When transformations are sequential, this is a batch sequential model which is extensively used in data processing systems
* 这种方法的变体非常常见。当转换是顺序的时，这是一种批量顺序模型，广泛用于数据处理系统
* Not really suitable for interactive systems
* 不太适合交互式系统

![image-20221205174225770](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221205174225770.png)





## Lecture 16 Distributed System Architectures 2

**Architectural design for software that executes on more than one processor**

**在多个处理器上执行的软件的体系结构设计**

### 1. Distributed Systems 

* Virtually all large computer-based systems are now distributed systems
* 几乎所有基于计算机的大型系统现在都是分布式系统
* **Information processing** is distributed over several computers rather than confined to a single machine
* 信息处理分布在几台计算机上，而不是局限于一台机器
* **Distributed software engineering** is now very important
* 分布式软件工程现在非常重要



#### 1.1 System Types

* Personal  systems  that  are  not  distributed  and  that  are designed to run on a personal computer or workstation. 
* 个人系统不是分布式系统并且被设计于个人电脑或者工作机上
* Embedded systems that run on a single processor or on an integrated group of processors. 
* 嵌入式系统运行在单个的处理器或者集成的处理器组上
* Distributed systems where the system software runs on a loosely integrated group of cooperating processors linked by a network.  
* 分布式系统的系统软件运行在由网络连接的一组松散集成的协作处理器上。

![image-20230104230726129](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104230726129.png)

#### 1.2 Distributed System Characteristics

![image-20230104230936427](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104230936427.png)

* <font color=red size=5>Advantage</font>
* Resource sharing 资源分享
* Openness 开放式
* Concurrency 并发性
* Scalability 可扩展性
* Fault tolerance 容错能力
* Transparency 透明性 

* <font color=red size=5>Disadvatages</font>
* Complexity 复杂性
* Security 安全性
* Manageability 管理性
* Unpredictability 不可预测性

![image-20230104231635856](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104231635856.png)

#### 1.4 Distributed Systems Architectures

* **Client-server architectures 顾客-服务器结构**
  * Distributed services which are called on by clients. Servers that provide services are treated differently from clients that use services
  * 由客户端调用的分布式服务。提供服务的服务器与使用服务的客户端被区别对待
* **Distributed object architectures 分布式对象体系结构**
  * No distinction between clients and servers. Any object on the system may provide and use services from other objects
  * 客户端和服务器之间没有区别。系统上的任何对象都可以提供和使用来自其他对象的服务

#### 1.5 Middleware

* Software that manages and supports the different components of a distributed system. In essence, it sits in the middle of the system
* 管理和支持分布式系统的不同组件的软件。**本质上，它位于系统的中间**
* Middleware is usually off-the-shelf rather than specially written software
* 中间件通常是现成的，而不是专门编写的软件
* Examples
  * Transaction processing monitors
  * 事务处理监控器
  * Data converters
  *  数据变换器
  * Communication controllers
  * 通信控制器

### 2. Distributed system model

#### 2.1 Multiprocessor Architectures 多处理器架构

* **Simplest distributed system model**
* **最简单的分布式系统模型**
* System composed of multiple processes which may (but need not) execute on different processors
* 由多个进程组成的系统，这些进程可以(但不需要)在不同的处理器上执行
* Architectural model of many large real-time systems
* 是许多大型实时系统的结构模型
* Distribution of process to processor may be pre-ordered or may be under the control of a dispatcher
* 进程到处理器的分配可以是预先安排的，也可以由调度程序控制

![image-20230104234836134](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104234836134.png)

#### 2.2 Client-Server Architectures 客户服务器架构

* **The application is modelled as a set of services** that are provided by servers and a set of clients that use these services
* 应用程序被建模为服务器提供的一组服务和使用这些服务的一组客户端
* **Clients know of servers but servers need not know of clients**
* 客户端知道服务器，但服务器不需要知道客户端
* Clients and servers are logical processes 
* 客户端和服务器是逻辑流程
* The mapping of processors to processes is not necessarily 1 : 1
* 处理器到进程的映射不一定是1:1 （一个处理器可以使用多个进程）

![image-20230104235307736](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104235307736.png)

![image-20230104235338257](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104235338257.png)

##### 2.2.1 Layered Application Architecture 分层应用结构

* **Presentation layer 表示层，显示层**
  * Concerned with presenting the results of a computation to system users and with collecting user inputs
  * 关注系统用户显示计算结果和收集用户输入
* **Application processing layer 应用程序处理层**
  * Concerned with providing application specific functionality e.g., in a banking system, banking functions such as open account, close account, etc.
  * 关注于提供特定于应用程序的功能，例如，在银行系统中，银行功能如开立帐户、关闭帐户等。
* **Data management layer 数据管理层**
  * Concerned with managing the system databases
  * 负责系统数据库的管理

![image-20230104235929329](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104235929329.png)

##### 2.2.2 Thin and Fat Clients 瘦客户机和胖客户机

* Thin-client model 瘦客户机
  * In a thin-client model, all of the application processing and data management is carried out on the server. The client is simply responsible for running the presentation software.
  * 在瘦客户端模型中，所有应用程序处理和数据管理都在服务器上进行。客户端只负责运行演示软件。
* Fat-client model 胖客户机
  * In  this  model,  the  server  is  only  responsible  for  data management.  The software  on  the  client  implements  the application logic and the interactions with the system user.
  * 在这个模型中，服务器只负责数据管理。客户机上的软件实现应用程序逻辑和与系统用户的交互。

![image-20230105001123362](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230105001123362.png)

###### 2.2.2.1 Thin Client Model

* **Used when legacy systems are migrated to client server architectures.** 
* **当遗留系统迁移到客户机服务器体系结构时使用**。
* The legacy system acts as a server in its own right with a graphical interface implemented on a client
* 遗留系统作为自己的服务器，在客户机上实现图形界面
* A major disadvantage is that it places a heavy processing load on both the server and the network
* 一个主要的缺点是它给服务器和网络带来了沉重的处理负载

###### 2.2.2.2 Fat Client Model

* **More processing is delegated to the client** as the application processing is locally executed
* 在本地执行应用程序处理时，**将更多的处理委托给客户机**
* Most suitable for new client-server systems where the capabilities of the client system are known in advance
* 最适合预先知道客户机系统功能的新客户机-服务器系统
* **More complex than a thin client model especially for management.** New versions of the application have to be installed on all clients
* 比瘦客户机模型更复杂，特别是在管理方面。应用程序的新版本必须安装在所有客户端上

![image-20230105002348076](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230105002348076.png)

###### 2.2.2.3 三层架构

* **In a three-tier architecture, each of the application architecture layers may execute on a separate processor**
* **在三层体系结构中，应用程序体系结构的每一层都可以在单独的处理器上执行**
* Allows for better performance than a thin-client approach and is simpler to manage than a fat-client approach
* 允许比瘦客户机方法更好的性能，并且比胖客户机方法更易于管理
* **A more scalable architecture** - as demands increase, extra servers can be added to the data management or application processing layers.
* 更可伸缩的体系结构——随着需求的增加，可以向数据管理或应用程序处理层添加额外的服务器。

![image-20230105002800728](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230105002800728.png)

![image-20230105002840696](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230105002840696.png)

![image-20230105002857710](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230105002857710.png)

#### 2.3 Distributed Object Architectures 分布式对象体系结构

* There is no distinction in a distributed object architectures between clients and servers
* 在分布式对象体系结构中，客户机和服务器之间没有区别
* Each distributable entity is an object that 
  * provides services to other objects and 
  * receives services from other objects
* 每个可分发实体都是一个对象
  * 为其他对象提供服务
  * 接收来自其他对象的服务
* Object communication is through a middleware system called an object request broker **(software bus)**
* 对象通信是通过称为对象请求代理(软件总线)的中间件系统进行的。
* However, they can be more complex to design than client-server systems
* 然而，它们的设计可能比客户机-服务器系统更复杂

![image-20230105003915185](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230105003915185.png)

##### 2.3.1 Advantages of Distributed Object Architecture

* It allows the system designer to delay decisions on where and how services should be provided
* 它允许系统设计人员延迟在何处以及如何提供服务的决策
  * Service-providing objects can execute on any node of the network and thus the distinction between thin/fat-client models becomes irrelevant.
  * 提供服务的对象可以在网络的任何节点上执行，因此瘦客户机模型和胖客户机模型之间的区别变得无关紧要。
* It is a very open system architecture that allows new resources to be added to it as required
* 它是一个非常开放的系统架构，允许根据需要添加新的资源
  * Object communication standards have been developed allowing objects written in different languages to communicate with each other.
  * 对象通信标准已经开发出来，允许用不同语言编写的对象相互通信。

* The system is flexible and scalable

* 该系统具有灵活性和可扩展性

  * New objects can be added as the load on the system increases without disrupting the other system objects. Replicated object can be created to cope with load.
  * 可以在系统负载增加时添加新对象，而不会中断其他系统对象。可以创建复制对象来处理负载。

* It is possible to reconfigure the system dynamically with **objects migrating across the network** as required

* 可以动态地重新配置系统，**使对象根据需要在网络上迁移**

  * This may be important when there is fluctuating patterns of demand on services. A service-providing object can migrate to the same processor as service-requesting objects, thus improving performance.
  * 当服务需求模式波动时，这一点可能很重要。服务提供对象可以迁移到与服务请求对象相同的处理器上，从而提高性能。
  * <font color=blue>当意外出现，将服务对象迁徙到相同类型的处理器</font>

  

## Lecture 17 Concepts of Object Oriented Design 面向对象设计的概念

* Object orientation means to organize the software as a collection of discrete objects that incorporate both data structure and behaviour
* 面向对象意味着将软件组织为包含数据结构和行为的离散对象的集合
* System functionality is expressed in terms of object services
* 系统功能用对象服务表示

* We continue to explore the question “what are good systems like?” by describing the object oriented paradigm.
* 我们继续探索这个问题“好的系统是什么样的?”通过描述面向对象的范式。
* We shall answer these questions:
* What is an object?
* 对象为何物
* How do objects communicate?
* 对象如何通信?
* How is an object’s interface defined?
* 对象的接口是如何定义的?
* What have objects to do with components?
* 对象和组件有什么关系?
* Finally we consider inheritance, polymorphism and dynamic binding.
* 最后我们讨论了继承、多态性和动态绑定。

### 1. Object Concepts

* Don’t think of what an object holds – but what it will do for you
* 不要想一个物品能装什么，而要想它能为你做什么
  * Consequently no public data members
  * 因此没有公共数据成员
  * Think only about the methods (the public interface)
  * 只考虑方法(公共接口)
* **Objects are potentially reusable components.**
* **对象是潜在的可重用组件。**
* **An object may represent something in the real world**
* **一个对象可以代表现实世界中的某些东西**
  * But often not

#### 1.1 What is an Object? 什么是对象

* Conceptually, an object is a thing you can interact with:
* 从概念上讲，对象是你可以与之交互的东西:
  * you can send it various messages and 
  * 你可以向它发送各种信息和
  * it will react
  * 它会发生反应
* How it behaves depends on the current internal state of the object, which may change
* 它的行为取决于对象的当前内部状态，这可能会改变
  *  For example: as part of the object’s reaction to receiving a message.
  * 例如:作为对象对接收消息的反应的一部分
* It matters which object you interact with, an object has an identity which distinguishes it from all other objects. 
* 重要的是你与哪个对象交互，一个对象有一个区别于所有其他对象的身份。

![image-20230105134133426](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230105134133426.png)

##### 1.1.2 Again... What is an Object?

* An object is a thing which has 
  * behaviour,  行为
  * state and  状态
  * identity   身份 [Grady, Booch, 1991] 
* Advantages:
  * Shared data areas are eliminated. Objects communicate by message passing.
  * 共享数据区域被删除。对象通过消息传递进行通信。
  * Objects are independent and encapsulate state and representation information. Their independence can lead to easier maintenance
  * 对象是独立的，并且封装状态和表示信息。它们的独立性可以使维护更容易

###### 1.1.2.1 State 状态

* **The state of the object is all the data which it currently encapsulates**
* **对象的状态是它当前封装的所有数据**
* An object normally has a number of named attributes (or instance variables or data members) each of which has a value
* 对象通常有许多命名属性(或实例变量或数据成员)，每个属性都有一个值
* **Some attributes can be mutable (variable)**
* 有些属性可以是可变的(变量)
  * An attribute ADDRESS 
  * 属性ADDRESS
* **other attributes may be immutable (constant)** 
* 其他属性可能是不可变的(常量)
  * Date of birth 
  * 出生日期
  * Identifying number
  * 识别号码

###### 1.1.2.2 Behaviour 行为

* **The way an object acts and reacts, in terms of its state changes as message passing.**
* **对象的行为和反应方式(就其状态而言)在消息传递时发生变化。**
* An object understands certain messages,
* 对象理解特定的消息，
  * it can receive the message and act on them.
  * 它可以接收信息并采取行动。
* The set of messages that the object understands, like the set of attributes it has, is normally fixed. 
* 对象理解的消息集，就像它拥有的属性集一样，通常是固定的。

###### 1.1.2.3 Identity is more Tricky  身份更棘手

* **The idea is that objects are not defined just by the current values of their attributes**
* **其思想是，对象不仅仅是由其属性的当前值定义的**
* An object has a continuous existence 
* 一个对象具有连续的存在
  * For example the values of the object’s attributes could change, perhaps in response to a message, but it would still be the same object.
  * 例如，对象属性的值可能会改变，可能是响应消息，但它仍然是相同的对象。

![image-20230105140340840](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230105140340840.png)

#### 1.2 Messages 信息

* A message includes a selector; here we’ve seen the selectors 
* 消息包括一个选择器;这里我们已经看到了选择器
  * reportTime and resetTimeTo
* **A message may, but need not, include one or more arguments**
* **消息可以(但不需要)包含一个或多个参数**
* Often, for a given selector there is a single “correct” number of arguments (Recall method overloading however..)
* 通常，对于一个给定的选择器，只有一个“正确”的参数数量(但是回想一下方法重载..)

![image-20230105141113522](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230105141113522.png)

#### 1.3 Interfaces 接口

* The object’s public interface defines which messages it will accept
* 对象的公共接口定义了它将接受哪些消息
*  An object can also send to itself any message which it is capable of understanding (in either its public or private interface)
* 对象还可以向自己发送任何它能够理解的消息(在其公共或私有接口中)。
* So typically an object has two interfaces:
  * **The public interface (any part of the system can use)**
  * **公共接口(系统的任何部分都可以使用)**
  * **The  larger private interface (which the object itself and other privileged parts of the system can use)** 
  * **较大的私有接口(对象本身和系统的其他特权部分可以使用该接口)**



#### 1.4 Classification

![image-20230105141744314](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230105141744314.png)

![image-20230105141803537](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230105141803537.png)

* It depends on the abstraction level and the point of view
* 这取决于抽象级别和观点
*  objects with the same data structure (attributes) and behaviour (operations) are grouped into a class
* 具有相同数据结构(属性)和行为(操作)的对象被分组到一个类中
* each class defines a possibly infinite set of objects
* 每个类都定义了一组可能无限的对象



![image-20230105142405562](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230105142405562.png)

* Each object is an instance of a class
* 每个对象都是一个类的实例
* Each object knows its class
* 每个对象都知道自己的类
* Each instance has its own value for each attribute (state) but shares the attribute names and operations with other instances of the class
* 每个实例对于每个属性(状态)都有自己的值，但与类的其他实例共享属性名和操作
  * also “static” i.e. class variables
* A class encapsulates data and behaviour, hiding the implementation details of an object
* 类封装了数据和行为，隐藏了对象的实现细节

#### 1.5 Object Interface Specification

* Object interfaces have to be specified so that the objects and other components can be designed in parallel.
* 必须指定对象接口，以便对象和其他组件可以并行设计。
* Objects may have several interfaces which are viewpoints on the methods provided.
* 对象可以有几个接口，这些接口是所提供方法的视点。
* Hiding information inside objects means that changes made to an object do not affect other objects in an unpredictable way.
* 在对象中隐藏信息意味着对一个对象所做的更改不会以不可预知的方式影响其他对象。

![image-20230105145718595](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230105145718595.png)

#### 1.6 Classes and Types 类和类型

* Often, people think of classes and types as being the same thing (indeed it is sometimes convenient and not  misleading to do so). It is not strictly correct however.
* 通常，人们认为类和类型是相同的东西(事实上，有时这样做是方便的，不会误导)。然而，它并不严格正确。
* Remember that a class does not only define what messages an object understands! 
* 记住，类不仅仅定义对象所理解的消息!
* **It also defines what the object does in response to the messages.**
* **它还定义了对象对消息的响应。**

![image-20230105150729591](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230105150729591.png)

#### 1.7 Object: Inheritance 类的继承

* **Inheritance is the sharing of attributes and operations among classes based upon a hierarchical relationship**
* **继承是基于层次关系在类之间共享属性和操作**
* A class can be defined broadly and then refined into successively finer subclasses
* 一个类可以被广泛地定义，然后细化成一个个更细的子类
* Each subclass incorporates or inherits all of the properties of its super class and its own unique properties
* 每个子类合并或继承它的父类的所有属性和它自己独特的属性

![image-20230105151102108](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230105151102108.png)

* A subclass is an extended, specialized version of its superclass. 
* 子类是其父类的扩展、专门化版本。
* It includes the operations and attributes of the superclass, and possibly extra ones which extend the class.
* 它包括超类的操作和属性，可能还包括扩展类的额外操作和属性。(指继承)

![image-20230105151420396](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230105151420396.png)

![image-20230105151714127](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230105151714127.png)

![image-20230105153042119](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230105153042119.png)



#### 1.8 Object: Polymorphism 对象的多态

* Polymorphism allows the programmer to use a subclass anywhere that a superclass is expected. E.g., if B is a subclass of type A then if an argument expects a variable of type A, it should also be able to take any variable of type B.

* 多态允许程序员在任何期望的上层使用子类。例句如果B是a类的子类,如果一个参数期望a型的变量,它也应该能够使用B型的任何变量。

* Polymorphism essentially reduces the amount of code duplication required. However, Object-Oriented Programming Languages also usually have a feature called “dynamic binding” which makes this idea even more useful..

* 多态性本质上减少了所需的代码复制量。然而,面向对象

  编程语言通常也有一个叫做“动态绑定”的特性，这使得这个想法更加有用。

#### 1.9 Dynamic Binding 动态绑定

* Dynamic Binding is when an object determines (possibly at run time) which code to execute as the result of a method call on a base type. 
* 动态绑定是指对象确定(可能在运行时)作为基类型上的方法调用的结果执行哪些代码。
* ![image-20230105155438443](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230105155438443.png)
* For example, imagine C is a subclass of B and both have a method named printName(). Then if we write: 
* 例如，假设C是B的一个子类，两者都有一个名为printName()的方法。那么如果我们写:
* ![image-20230105155213074](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230105155213074.png)
  * we would invoke the printName() method of object C, not of object B, even though the type of temp is B.
  * 我们将调用对象C的printName()方法，而不是对象B的printName()方法，即使temp类型是B。
* This is dynamic binding. Let us consider another example..
* 这是动态绑定。让我们考虑另一个例子。

![image-20230105155512639](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230105155512639.png)



### 2. Unified Modelling Language(UML)

* Unify notations
* UML is a language for:
  * Specifying 说明
  * Visualizing  分类 and
  * Documenting 文件
    the parts of a system under development
  * 正在开发的系统的各个部分
* Authors (Booch, Rumbaugh and Jacobsen) agreed on **notation 符号** but not able to agree on a single method
  * This is probably a “good thing”
* UML has been adopted by the Object Management Group (OMG) as an Object-Oriented notation standard
* UML已经被对象管理组采用(OMG)作为面向对象表示法标准

![image-20230105155914510](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230105155914510.png)

#### 2.1 Some Notation

* Object classes are rectangles with the name at the top, attributes in the middle section (“compartment”) and operations in the next compartment.
* 对象类是顶部有名称的矩形，中间部分是属性(“隔间”)，下一个隔间是操作。
* Relationships between object classes (known as associations) are shown as lines linking objects
* 对象类是顶部有名称的矩形，中间部分是属性(“隔间”)，下一个隔间是操作。
* Inheritance is referred to as generalisation.
* 继承一般被称为一般化
  * It uses an open triangular arrow head
  * 一般使用空白的三角箭头

![image-20230105160240495](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230105160240495.png)



### 3. CASE Tools/Workbenches 工作台

* Computer Aided Software Engineering (CASE)
* 计算机辅助软件工程(CASE)
* A coherent set of tools to support a software engineering method
* 支持软件工程方法的一组连贯的工具
* These workbenches may support a specific SE method or may provide support for creating several different types of system model. 
* 这些工作台可以支持特定的SE方法，也可以为创建几种不同类型的系统模型提供支持。
* There are also meta-CASE tools
* A CASE tool to build CASE tools
* 一个用于构建CASE工具的CASE工具

![image-20230105160542157](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230105160542157.png)

![image-20230105160604999](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230105160604999.png)



![image-20230105160617563](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230105160617563.png)

![image-20230105160625814](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230105160625814.png)







## Lecture 18 Introductory Case Study

### 1. Introduction to UML

* During this lecture, we shall see how various features of the Unified Modeling Language (UML) can help to reduce ambiguities and increase understanding of a proposed system
* 在本次讲座中，我们将看到统一建模语言（UML）的各种特性如何帮助减少歧义并提高对所提议系统的理解
* We will be studying an introductory case study based on a health clinic system and giving an introduction to:
* 我们将研究基于健康诊所系统的介绍性案例研究，并介绍:
* **Use case diagrams  用例图**
* **Class diagrams  类图**
* **Sequence diagrams 顺序图**
* **State diagrams  状态图**

#### 1.1 The Problem

* The most difficult part of any design project is understanding the task you are attempting.
* 任何设计项目中最困难的部分是**理解您正在尝试的任务**
* Example: you have been contacted to develop a computer system for a university medical clinic.
* 示例：已联系您为大学医学诊所开发计算机系统。
* The clinic needs the following types of service
* 诊所需要以下类型的服务
  * Staff management 员工管理层
  * Booking appointments 预约
  * Keeping records 保存记录
* You are asked to build an **interactive system** which handles all of these aspects **online.** 
* 您需要构建一个**在线**处理所有这些方面的**交互式系统**

##### 1.1.1 Clarifying the Requirements  明确要求

* Different users will have different, sometimes conflicting, priorities
* 不同的用户会有不同的优先级，有时会有冲突
* Users are not likely to have clear, easily expressed views of what they want
* 用户不太可能对自己想要的东西有清晰、容易表达的观点
* It is hard to imagine working with a system of which you have only seen a description
* 很难想象使用一个你只看到过描述的系统

##### 1.1.2 Facts about the Requirements

![image-20221205182544568](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221205182544568.png)

![image-20221205182554395](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221205182554395.png)

### 2. Use Case Model 用例模型

* If a system is to be seen as having high quality, it must meet the needs of its users.
* 如果一个系统要被视为具有高质量，它必须满足其用户的需求。
* So we take a **user-oriented approach** to systems analysis.
* 因此，我们采用面向用户的方法进行系统分析。
* We identify the users of the system and the tasks they must undertake with the system.
* 我们确定系统的用户及其必须执行的任务。
* We also seek information about which tasks are most important, so that we can plan the development accordingly.
* 我们还寻求关于哪些任务最重要的信息，以便我们能够相应地规划发展。

#### 2.1 What do we Mean by “Users” and “Tasks”?

* UML uses as technical terms “actors” and “use cases”
* UML使用技术术语“参与者”和“用例
* An actor is a user of a system in a particular role (an actor can also be an external system)
* 参与者是处于特定角色的系统的用户（参与者也可以是外部系统）
  * For example. Our system will have an actor Receptionist representing the person who interacts with the system to book an appointment
  * 例如我们的系统将有一名演员接待员，代表与系统交互以预约的人
* A use case is a task which an actor needs to perform with the help of the system, 
* 用例是参与者需要在系统的帮助下执行的任务
  * such as BookAppointment

![image-20221205183520665](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221205183520665.png)

#### 2.2 Scope and Iterations 范围和迭代

* To limit the risk, it is better to aim to get to the ideal system in **several steps** or **iterations.**
* 为了限制风险，最好通过**几个步骤**或**迭代**达到理想的系统
  * The first iteration results in the delivery of a system with only the most basic and essential functionality;
  * 第一次迭代的结果是交付一个只有最基本和最基本功能的系统
  * Later iterations enhance the system
  * 随后的迭代增强了系统
* One of the main purposes of use cases is to help identify suitable dividing lines between interactions:
* 用例的主要目的之一是帮助确定交互之间的适当分界线：
  * An interaction can deliver enough of the system to allow certain use cases to be carried out, but not others  
  * 交互可以提供足够的系统以允许执行某些用例，但不能执行其他用例

#### 2.3 Limiting Requirement 限制要求

* It is important **not to invent new requirements for the system.** After examining use-cases, it is often easy to think of new things the system could or should do, but these must first be discussed with the customer.
* 重要的是不要对系统提出新的要求。在检查用例后，通常很容易想到系统可以或应该做的新事情，但这些必须首先与客户讨论。
  * For example, perhaps it would be good to inform the doctor that a drug is out of stock via their online system? But this may not be what is wanted by the Dr, this may cause an overload of information! 
  * 例如，也许通过他们的在线系统通知医生药物缺货会很好？但这可能不是博士想要的，这可能会导致信息过载！

![image-20221205184635484](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221205184635484.png)

![image-20221205184644500](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221205184644500.png)

#### 2.4 Use Case Advantages

* It may be easier to identify the amount of time required to implement all the required features of the system.
* 可能更容易确定实现系统的所有所需功能所需的时间量。
  * Such details can often be optimistically overlooked.
  * 这些细节常常被乐观地忽视
* We can identify which requirements are important to key strategic (or most influential) personnel in the company.
* 我们可以确定哪些需求对公司的关键战略（或最有影响力的）人员很重要
  * By providing this functionality early, we can show the potential value of the software and avoid the project being cancelled.
  * 通过尽早提供此功能，我们可以显示软件的潜在价值，避免项目被取消。
* We may decide to implement more risky use cases first since we would hopefully still have contingency to tackle problems that arise 
* 我们可能会决定首先实现更高风险的用例，因为我们希望仍然有应急措施来解决出现的问题
  * In other words, early in the development we have more flexibility in terms of time, money, design choices etc.
  * 换句话说，在开发初期，我们在时间、金钱、设计选择等方面具有更大的灵活性。
* Use cases can be used to derive validation checks on the developed system, in order that it provides all required functionality.
* 用例可用于对开发的系统进行验证检查，以便其提供所有所需的功能。

### 3. Class diagrams

#### 3.1 Identifying Classes 识别类别

* In the standard jargon of analysis we often talk about **the key domain abstractions.**
* 在标准的分析术语中，我们经常谈论关键领域抽象
* Identifying the right classes is one of the main skills of OO development.
* 识别正确的类是OO开发的主要技能之一。
* We start the process of identifying the key domain abstractions using the following approach, which is known as the noun identification technique.
* 我们使用以下方法开始识别关键领域抽象的过程，即所谓的名词识别技术。

![image-20221205210017481](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221205210017481.png)

* 对系统的要求进行连贯、简洁的陈述
* 在其名词和名词短语下面划线，即识别表示事物的单词和短语
* 这给出了一个**候选类的列表**，然后我们可以对其进行**精简和修改**，以获得系统的初始类列表

为了对它进行精简和修改，我们一般删除多余的候选人

* In this particular case, we discard:
  * Clinic, because it is outside the scope of our system
  * Urgent appointment redundant covered by appointment
  * Time, because it is a measure, not a thing
  * Free slot, because it is vague (we need to clarify it)
  * System, because it is part of the meta-language of requirements description, not a part of the domain

![image-20221205210444773](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221205210444773.png)

这意味着最终我们会剩下这几个

* Doctor
* Nurse
* Receptionist
* PatientAppointment
* Prescription

接下来，整理类和类之间的关系

#### 3.2 Relations between Classes 类之间的关系

* Next we identify and name important real-world relationships or associations between our classes
* 接下来，我们确定并命名类之间重要的真实世界关系或关联
* We do this for two reasons:
  * To clarify our understanding of the domain, by describing our objects in terms of how they work together;
  * 通过描述我们的对象如何协同工作，阐明我们对领域的理解；
  * To sanity-check the coupling in our system, i.e. make sure that we are following good principles in modularising our design
  * 为了健全地检查系统中的耦合，即确保我们在模块化设计时遵循了良好的原则
  * 得到下图

![image-20221205211135811](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221205211135811.png)

* Finally, we may notice that 
  * Doctor shares all the same associations that Nurse does, and that  医生和护士有着相同的联系
  * this agrees with our intuition that both nurse and doctor are health care staff.  这与我们的直觉一致，即护士和医生都是医护人员。
* Recording this in the class diagram will clarify our understanding of the situation, that there is a generalization relationship between these classes
* 在类图中记录这一点将澄清我们对情况的理解，即这些类之间存在通用关系
* Inheritance, Dr and Nurse are both health care staff and receptionist is also staff
* 继承，医生和护士都是医护人员，接待员也是工作人员
* Notice Staff and HealthCareStaff are additional classes to help with inheritance
* 注意Staff和HealthCareStaff是帮助继承的附加类

![image-20221205211924699](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221205211924699.png)

![image-20221205211934048](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221205211934048.png)

### 4. Sequence Diagram

* A class diagram gives a static view of the system, but we know nothing about the dynamic behaviour
* 类图给出了系统的静态视图，但我们对动态行为一无所知
* In UML we can use **interaction diagrams** to show how messages pass between objects of the system to carry out some task
* 在UML中，我们可以使用**交互图**来显示消息如何在系统的对象之间传递以执行某些任务
  * This will also show how the various classes realize the different use cases we identified in the use case diagram
  * 这也将显示各个类如何实现我们在用例图中确定的不同用例

#### 4.1 An Example Sequence Diagram 序列图示例

* Consider what happens in the appointment booking scenario when a user wishes to make an appointment
* 考虑当用户希望预约时，在预约场景中会发生什么
  * The receptionist must check that the person is a valid patient
  * 接待员必须检查此人是否为有效患者
  * Then the doctor object must be checked to see if there are any available appointments
  * 然后必须检查医生对象以查看是否有可用的预约
  * If there are any suitable slots available, a new appointment should be created and assigned to the doctor.
  * 如果有任何合适的时段，应创建新的预约并分配给医生。
* We now see how this is recorded in a sequence diagram

![image-20221205213715968](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221205213715968.png)

* We shall see more on sequence diagrams later, but note their general structure and that they record which actors and classes are involved in an interaction.
* 稍后我们将看到更多关于序列图的内容，但请注意它们的一般结构，以及它们记录了交互中涉及的参与者和类
* In this example the interaction is very simple, there is a single execution path and nothing occurs in parallel; in more complex scenarios, sequence diagrams can clarify the working of a system to a greater extent
* 在本例中，交互非常简单，只有一个执行路径，没有并行发生；在更复杂的场景中，序列图可以在更大程度上阐明系统的工作



### 5. State Diagrams

// **我觉得状态图应该也是一个交互图interaction diagrams**

* Objects in the system have a state which is all the data which it currently encapsulates
* 系统中的对象具有一个状态，即它当前封装的所有数据
* For example, a Doctor object on the health system can be available or fully booked
* 例如，健康系统上的Doctor对象可以可用或已预订满
* Running methods on the object can cause a change in state, i.e., by booking appointments to the doctor object we change its internal state.
* **在对象上运行方法可能会导致状态改变**，即，通过预约医生对象，我们可以改变其内部状态。
* Changes in object states can be modelled by a **state diagram**..
* 对象状态的变化可以通过状态图进行建模。

![image-20221205214333849](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221205214333849.png)

![image-20221205214340727](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221205214340727.png)

### 6. Lecture Key

![image-20221205214434494](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221205214434494.png)

![image-20221205214443142](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221205214443142.png)



## Lecture19



### 1. On Naming classes

![image-20221206010309788](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206010309788.png)



![image-20221206010319291](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206010319291.png)



### 2. Class Models 类模型

* In this lecture we will be studying Class Models which are a part of **the Unified Modeling Language (UML).**

* 在本课程中，我们将学习作为统一建模语言（UML）一部分的类模型。

* Of the various models in UML, we have the categories:

* 在UML中的各种模型中，我们有以下类别：

  * Use case models – describing a system from the users’ point of view;
  * 用例模型——从用户的角度描述系统
  * Static models – describing the elements of the system and their relationship; class models fall into this category;
  * 静态模型——描述系统元素及其关系；类模型属于这一类
  * Dynamic models – describing the behaviour of the system over time.
  * 动态模型–描述系统随时间的行为

  

#### 2.1 A Very Simple Class Model 一个简单的类模型

* In the Unified Modelling Language (UML), a class is shown in a class diagram as a rectangle giving its name:
* 在统一建模语言（UML）中，类在类图中显示为一个矩形，给出其名称：

![image-20221206010745794](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206010745794.png)

#### 2.2 What Makes a Good Class Model? 什么是好的类模型

* Ultimately, we have two objectives which we aim to meet:
  * Build, as quickly and cheaply as possible, a system which satisfies our current requirements;
  * 尽可能快速、廉价地建立一个满足我们当前需求的系统；
  * Every piece of behaviour required of the system must be provided by the objects we choose
  * 系统所需的每一项行为都必须由我们选择的对象提供
  * Build a system which will be easy to maintain and adapt to future requirements (Evolution)
  * 构建一个易于维护和适应未来需求的系统（进化）
  * Thus build a system composed of encapsulated modules with low coupling and high cohesion.
  * 因此，构建了一个由低耦合和高内聚的封装模块组成的系统。

#### 2.3 In Order to Meet the the Objectives:

* A good class model consists of classes which represent enduring classes domain objects, which don’t depend on the particular functionality required today
* 一个好的类模型由表示持久类域对象的类组成，这些类不依赖于当前所需的特定功能
* Remember that the names of classes are also important; use meaningful names for classes when possible and consider using a data dictionary to avoid conflicts
* 记住类的名称也很重要；尽可能为类使用有意义的名称，并考虑使用数据字典以避免冲突

#### 2.4 Deriving Classes 派生类

* Recall that we previously mentioned the noun identification technique to find potential classes.
* 回想一下我们之前提到的寻找潜在类的名词识别技术
* There are two main (extreme) techniques used to find classes in general:
* 通常有两种主要（极端）技术用于查找类：
  * **Data-driven-design (DDD)** – We identify all the data of the system and divide it into classes. We then assign particular responsibilities (methods) to these classes
  * **数据驱动设计（DDD）**——我们识别系统的所有数据并将其划分为类。然后，我们将特定的职责（方法）分配给这些类
  * **Responsibility-driven-design (RDD)** – We identify all the responsibilities of the system and divide them into classes. We then find the data each class requires.
  * **责任驱动设计（RDD）**——我们确定系统的所有责任，并将其划分为类别。然后我们找到每个类所需的数据。

#### 2.5 Associations 关联

* In the same sense that classes correspond to nouns, associations correspond to verbs.
* 在类对应于名词的相同意义上，关联对应于动词。
* They express the relationship between classes.
* 它们表达了类之间的关系。
* There are instances of associations, just as there are instances of classes
* 有关联的实例，就像有类的实例一样
* Instances of a classes are called objects; 
* 类的实例称为对象；
* Instances of associations are called links in UML   
* 关联的实例在UML中称为链接

**Class A and B are Associated if**

* an object of class A sends a message to an object of class B
* A类对象向B类对象发送消息
* an object of class A creates an object of class B
* 类A的对象创建类B的对象
* an object of class A has an attribute whose values are objects of class B or collections of objects of class B
* A类对象有一个属性，其值是B类对象或B类对象的集合
* an object of class A receives a message with an object of class B as argument
* 类A的对象接收以类B的对象作为参数的消息

**In other words,  if some object of class A has to know about some object of class B**

**换句话说，如果A类的某个对象必须知道B类的某一对象**

##### 2.5.1 Simple Association between Classes  类的简单关联

![image-20221206013134980](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206013134980.png)

* One annotation which is often used early is the multiplicity of an association
* 早期经常使用的一个注释是关联的多重性
* This is so fundamental that we will spend some time thinking about it.
* 这是非常重要的，我们将花一些时间来思考。

![image-20221206013259483](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206013259483.png)



##### 2.5.2 Multiplicity 多重性

We can specify:

* an exact number simply by writing it, e.g. 1
* 简单地写一个精确的数字，例如1
* a range of numbers using two dots between a pair of numbers, e.g., 1..10
* 在一对数字之间使用两个点的数字范围，例如1..10
* an arbitrary, unspecified number using *
* 使用*表示的任意的、未指定的数字
* Loosely, you can think of UML’s * as an infinity sign, so the multiplicity  1 .. *  expresses that number of copies can be anything between 1 and infinity.
* **粗略地说，你可以把UML的 * 看作是一个无限符号，所以多重数1..*表示副本的数量可以是1到无限之间的任何值。**

##### 2.5.3 Attributes and Operations 属性和操作

* The attributes of a class describe the data contained in an object of the class and their type
* 类的属性描述包含在类对象和类型中的数据
* Most important are the operations of a class, which define the ways in which objects may interact.
* 最重要的是类的操作，它们定义了对象交互的方式。

![image-20221206014737726](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206014737726.png)



##### 2.5.4 Operation Signatures 操作系统

* The signature of an operation gives the selector, names and types of all formal parameters (arguments) and the return type. For example:
* 操作的签名给出了选择器、所有形式参数（参数）的名称和类型以及返回类型。例如：

![image-20221206014948747](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206014948747.png)

* Recall that the method called may depend upon a classes position within the inheritance hierarchy. There may be methods with the same name, do you remember the concept of dynamic binding?
* 回想一下，调用的方法可能取决于继承层次结构中的类位置。可能有同名的方法，您还记得动态绑定的概念吗？

###### 2.5.4.1 Dynamic Binding (recap)

![image-20221206015108808](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206015108808.png)



#### 2.6 Generalization 一般化

* Important relationships which may exist between classes are called generalization. Conceptually this means that if class A is a generalization of class B, then the interface of class B must conform to the interface of class A.
* 类之间可能存在的重要关系称为泛化。从概念上讲，这意味着如果类A是类B的泛化，那么类B的接口必须符合类A的接口。
* Every attribute and operation of A will also be supported by B. In addition, B may contain some extra operations and data specific to its class.
* B也支持A的每个属性和操作。此外，B可能包含一些特定于其类的额外操作和数据。
* Let’s see an example of this on the next slide…
* ![image-20221206015653383](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206015653383.png)

![image-20221206020154906](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206020154906.png)

![image-20221206020207064](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206020207064.png)

#### 2.7 Inheritance versus Generalization 继承和泛化

* Generalization is a conceptual relationship between classes whereas inheritance is an implementation relationship.
* 泛化是类之间的概念关系，而继承是实现关系。
* Generalization obviously increases the coupling of a system and if a subclass is changed it usually necessitates a recompilation of the subclass also (this is a pragmatic issue).
* 泛化显然增加了系统的耦合，如果子类发生了变化，通常也需要重新编译子类（这是一个实用问题）。

### 3. CRC Cards

* One common way of checking for a good design and guiding its refinement is to use CRC cards.
* 检查良好设计并指导其改进的一种常见方法是使用CRC卡。
* CRC stands for Classes, Responsibilities, Collaborations.
* CRC代表类别、责任和协作。
* Although CRC is not part of UML, they add some very useful insights throughout a development.
* 虽然CRC不是UML的一部分，但它们在整个开发过程中添加了一些非常有用的见解

#### 3.1 Creating CRC Cards

* The name of a class, at the top
* 类的名称，位于顶部
* The responsibilities of the class, on the left-hand side
* 左边是类的职责
* The collaborators of the class, which help to carry out each responsibility, on the right-hand side of the card.
* 右边是类的合作者，负责帮忙完成每项责任

The responsibilities of the class describe at a high level the purpose of the class’s existence : 类的职责在更高的层次上描述了班级存在的目的

* They are connected with the operations the class provides, but are more general than that might imply – i.e., they can be an abstraction of several operations.
* 它们与类提供的操作相关联，但比这可能暗示的更一般——即，它们可以是几个操作的抽象。

![image-20221206022103111](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206022103111.png)

![image-20221206022109245](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206022109245.png)



![image-20221206022127689](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206022127689.png)



![image-20221206022150563](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206022150563.png)



## Lecture 20 

### 1. Lecture Outline

* Aggregation and composition 聚合和组成
* Roles 角色
* Navigability 适航性
* Qualified association 合格的关联
* Derived association 派生关联
* Constraints 限制条件
* Association classes 关联类
* Interfaces and abstract classes 接口和抽象类



### 2. Aggregation and Composition 聚合和组成



* Aggregation and composition are kinds of association: 聚合和合成是一种关联
  * Instead of just showing that two classes are associated we may choose to show more about what kind of association this is
  * 我们可以选择更多地展示这是什么样的关联，而不是仅仅展示两个类是关联的
* Aggregation and composition are both ways of recording that an object of one class is part of an object of another class.
* 聚合和合成都是记录一个类的对象是另一个类对象的一部分的方法。

![image-20221206113808828](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206113808828.png)

#### 2.1 Aggregation 聚合

https://blog.csdn.net/chengqiuming/article/details/122734159?ops_request_misc=&request_id=&biz_id=102&utm_term=%E8%81%9A%E5%90%88%E4%B8%8E%E7%BB%84%E6%88%90&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduweb~default-0-122734159.nonecase&spm=1018.2226.3001.4187  -- 组合与聚合

* Aggregation is essentially a conceptual notion:

* 聚合本质上是一个概念的概念

  * seeing an aggregation in a class model should help you to understand the relationships between the classes at an informal level
  * 在类的模型中看到聚合应该有助于你理解在非正式类别上类的关系
  * BUT it does not give you any more formal information about how they must be implemented or what you can do with them
  * 但是它没用提供关于如何必须实施或如何使用它们的正式信息
  * Usually we do not name an aggregation association since it is usually “is a part of”.
  * 往往我们并不会命名aggregation association 因为它们通常是一部分

  

  

#### 2.2 Composition 组成

* Composition is a special kind of aggregation which imposes some further restrictions.

* 组成是一种特殊的聚合，它往往施加了进一步的限制   

* In composition association, the whole strongly owns its parts

* 在组成的关系中，整体强烈的拥有自己的部分

  * If the whole object is copied or deleted, its parts are copied or deleted with it
  * 如果复制或删除了某个对象，它的部分也会被删除或复制

* The multiplicity at the whole end of a composition association must be 1 or 0..1

* 组合关联的整个末端的多重数必须为1或0..1

  * A part cannot be part of more than one whole by composition
  * 一个组成部分不能是多个整体的一部分

  ![image-20221206121041844](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206121041844.png)

![image-20221206121051501](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206121051501.png)

![image-20221206121114502](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206121114502.png)



### 3. Roles

* Often you can read an association name in both directions (‘is taking’, ’is taken by’)
* 通常，您可以从两个方向读取关联名称（“istaking”，“istakeby”）
* Sometimes, however, it is more readable to have separate names for the roles that the objects play in the association. 
* 
* 然而，有时，为对象在关联中扮演的角色指定单独的名称更容易理解。![image-20221206122704348](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206122704348.png)

#### 3.1 Association with no Navigability 无适航性的关联

* The diagram records that:
* ![image-20221206165956040](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206165956040.png)
  * For each object of class Student  there are six objects of class Module which are associated with the Student;
  * 对于每个学生类对象，有六个与学生相关的模块类对象
  * For each object of class Module there are some Student objects (the number of students is unspecified) associated with the Module.
  * 对于模块类的每个对象，都有一些与模块相关的学生对象（未指定学生数量）。

#### 3.2 Navigability 适航性

* We can put an arrow on one or both ends of the association line to represent that it is possible for messages to be sent in the direction of the arrow （其实本体是箭头）
* 我们可以在关联行的一端或两端放置一个箭头，表示消息可以按箭头的方向发送

![image-20221206170646244](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206170646244.png)



### 4. Qualified Associations 限定关联

* Occasionally it is helpful to give finer detail about an association than we have so far.
* 有时，提供比目前更详细的关联信息会有所帮助
* Square is identified relative to the board it’s on by attributes raw and column, each taking a value between 1 and 3 

![image-20221206171811668](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206171811668.png)

* In fact we can combine the qualified association notation with the other association notations
* 事实上，我们可以将限定关联表示法与其他关联表示法相结合
* For example, we can add back the information that this particular association is a composition



### 5. Derived Associations 派生的关联

* A derived association exists automatically once we have implemented the main association
* 一旦我们实现了主关联，派生关联就会自动存在
* A derived association as shown using a slash in front of its name
* 派生关联，如在其名称前面使用斜线所示
* The black triangles indicate which direction of the association the name describes.
* 黑色三角形表示名称描述的关联方向。

![image-20221206172637471](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206172637471.png)



### 6. Constraints 限制条件

* **A constraint is a condition that must be satisfied by any correct implementation of a design**
* **约束是设计的任何正确实现都必须满足的条件**
* The formal constraints can be written in **OCL**, the Object Constraint Language (developed by IBM)
* 形式约束可以用OCL，即对象约束语言（由IBM开发）编写
* OCL is intended to be
  * Formal, so that constraints written in it are unambiguous
  * 形式化，因此其中的约束是明确的
  * Easy to use, so that every developer can write constraints
  * 易于使用，因此每个开发人员都可以编写约束



#### 6.1 XOR Constraints

* To get round this problem, we may use an xor constraint which is not written in OCL, but is a specially defined constraint in UML.
* 为了解决这个问题，我们可以使用一个xor约束，它不是用OCL编写的，而是用UML专门定义的约束。
* Xor stands for “exclusive or”.  If we have two possibilities, A and B, then A xor B means either A or B but not both (this is a widely used concept in computer science).
* Xor代表“exclusiveor”。如果我们有两种可能性，A和B，那么AxorB表示A或B，但不是两者（这是计算机科学中广泛使用的概念）。
* It is also sometimes written as :![image-20221206173605392](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206173605392.png)		in logic.

![image-20221206173757699](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206173757699.png)

![image-20221206173811106](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206173811106.png)



### 7. Association Classes 关联类

* Sometimes the association between classes itself may need attributes and operations.
* 有时类之间的关联本身可能需要属性和操作。
* For example, consider the situation that a Student class is associated with a Module class. Where should the students grade for that module be stored? Is it a part of the Student class? The Module Class? 
* 例如，考虑学生类与模块类关联的情况。该模块的学生成绩应存储在哪里？它是学生班的一部分吗？模块类？
* The grade really belongs to the association of these two classes.
* 这个年级真的属于这两个班的学生

![image-20221206174320425](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206174320425.png)

![image-20221206174413543](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206174413543.png)



### 8. Interfaces and Abstract Classes

#### 8.1 Interfaces

* An interface specifies operations of some model element visible outside of the class. In UML2, an interface may specify some attributes and associations.
* 接口指定类外部可见的某些模型元素的操作。在UML2中，接口可以指定一些属性和关联。
* All the elements of such an interface in a class diagram are public. The notation is to use a rectangle just like a class but with a “<<interface>>” string.
* 类图中此类接口的所有元素都是公共的。符号是使用一个矩形，就像一个类，但带有一个“<<interface>>”字符串。

#### 8.2 Abstract Classes

* An interface is similar to the idea of an abstract class, which can be modeled in UML by using the word “abstract” on the class icon as a property.
* 接口类似于抽象类的概念，可以通过使用类图标上的“abstract”一词作为属性，在UML中对抽象类进行建模。
* An abstract class is one in which, for at least one operation, the implementation of that method is not defined. Thus the class cannot be instantiated.
* 抽象类是这样一个类，其中至少有一个操作没有定义该方法的实现。因此，类无法实例化。

说实话，搞不懂





## Lecture 21 

### 1. Outline 

* Use case diagrams 用例图
* Collaborations 协作
* Interaction on collaboration diagrams 协作图中的交互
* Sequence diagrams 序列图
* Messages from an object to itself 从自身到对象的信息
* Suppressing detailed behaviour  抑制详细信息
* Creation and deletion of objects 创建和删除对象
* Timing 计时

### 2. Recap … Use Case Diagrams 复习用例图

* Use case diagrams show the interaction of users of the system with the functionality of the system.
* 用例图显示了系统用户与系统功能的交互
* A use case is a functional component of the system that accomplishes a specific task, and is represented by an ellipse.
* 用例是完成特定任务的系统功能组件，用椭圆表示。
* An actor, depicted as a stickman figure, is a user (human or non-human) of the system performing a specific role.
* 扮演者，被描绘为一个坚守者，是系统中执行特定角色的用户（人类或非人类）
* Use case diagrams are used early in the development process to refine the functional specifications, identify user interface requirements and to define the scope of the project.
* 在开发过程的早期使用用例图来细化功能规范，确定用户界面需求并定义项目范围。

![image-20221206182619366](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206182619366.png)

* Remember that it’s also necessary to describe each use case. To describe a use case, we could use natural language, structured natural language, sequence diagrams, state diagrams etc.
* 记住，描述每个用例也是必要的。为了描述用例，我们可以使用自然语言、结构化自然语言、序列图、状态图等。
* If we use an <<extend>> relation, we should also describe which of the use cases will be chosen.
* 如果我们使用<<extend>>关系，我们还应该描述将选择哪些用例。
* The <<include>> and <<extend>> relations are an advanced feature and should be used with care; remember they add to the complexity of the diagram.
* ＜＜include＞＞和＜＜extend＞＞关系是一个高级特性，应谨慎使用；记住，它们增加了图表的复杂性。



### 3. Recap … Class Diagrams

* A Class diagram shows the static structure of the system.
* 类图显示了系统的静态结构
* It defines model elements such as classes, interfaces, and user-defined data types, their internal structure, and their relationships to each other.
* 它定义了模型元素，例如类、接口和用户定义的数据类型、它们的内部结构以及它们之间的关系。
* Relationships, or associations, are shown as lines connecting elements, and are annotated to describe the relationships and their cardinality (1..1, 1..*, 0..*, etc.).
* 关系或关联显示为连接元素的线，并进行注释以描述关系及其基数（1..1、1..*、0..*等）。
* Inheritance (generalize/specialize), aggregation (comprises), and composition (has) relationships are also captured in this diagram.
* 继承（泛化/专用）、聚合（包含）和组合（具有）关系也在该图中捕获。

![image-20221206184316137](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206184316137.png)



### 5.  Collaborations 协作

* UML provides two sorts of interaction diagram, UML提供了两种交互图
  * sequence diagrams and 
  * 序列图
  * collaboration diagrams.
  * 协作图
* Collectively, the objects which interact to perform some task, together with the links between them, are known as a collaboration
* 总体而言，为执行某项任务而交互的对象以及它们之间的链接被称为协作
  * Objects - Each object is shown as rectangle, which is labelled  objectName: classNameLinks - 
  * 对象-每个对象显示为矩形，标记为objectName:className
  * Links between objects are shown like associations in the class model.Actors - 
  * 链接-对象之间的链接显示为类模型中的关联。
  * Actors can be shown as on a use-case diagram
  * 参与者-参与者可以在用例图上显示

![image-20221206212610517](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206212610517.png)

* 一个没有交互的协作（Collaboration）更像是类模型的一部分实例，他显示对象，连接和参与者

![image-20221206212836425](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206212836425.png)

* Each labelled arrow represents a message sent from the object at the tail of the arrow to the object at the point of the arrow.
* 每个带标签的箭头表示从箭头尾部的对象发送到箭头点的对象的消息
* Furthermore, the target object must understand the message
* 此外，目标对象必须理解消息
* That is, the class of the object at the point of the arrow must provide the appropriate operation 
* 也就是说，箭头点处的对象类必须提供适当的操作

### 6.Sequence diagram 序列图

* A sequence diagram shows the objects and actor which take part in a collaboration at the top of dashed lines.
* 序列图在虚线顶部显示了参与协作的对象和参与者。
* Sequence diagrams are applicable to modeling real-time interactive systems or complex scenarios.
* 序列图适用于建模实时交互系统或复杂场景

![image-20221206214936293](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206214936293.png)

Interaction Shown on a Sequence Diagram 

![image-20221206215046654](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206215046654.png)

* The vertical dimension of a sequence diagram represents time 
* **序列图的垂直维度表示时间**
* The horizontal dimension represents the different objects or roles that participate in the interactive sequence.
* **水平维度表示参与交互序列的不同对象或角色**。

![image-20221206215700676](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206215700676.png)

* Time is assumed to pass as we move from the top to the bottom of the diagram
* **假设时间随着我们从图的顶部移动到底部而流逝。**
* Messages between objects are shown as solid line arrows, and their returns are shown as dashed line arrows.
* **对象之间的消息显示为实线箭头，其返回显示为虚线箭头**

![image-20221206220213373](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206220213373.png)



### 7. Messages from an Object to Itself 从对象到自身的信息

* An object may, and frequently does, send a message to itself (i.e. An object calls another method on itself; Java uses keyword “this”).
* 一个对象可以并且经常向自己发送消息（即，一个对象调用另一个方法；Java使用关键字“this”）
* On a collaboration diagram you show a link from the object to itself, and messages pass along that link in the usual way
* 在协作图上，您显示了从对象到自身的链接，消息以通常的方式沿着该链接传递
* ![image-20221206220839630](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206220839630.png)
* On a sequence diagram, you show a message arrow from the object’s lifeline back to itself.
* 在序列图上，显示了从对象生命线返回到其自身的消息箭头。
* ![image-20221206220854532](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206220854532.png)

* In pure object oriented programming,  在纯粹的面向对象编程中
  * every function invocation is the result of a message, and 
  * 每个函数调用都是消息的结果，并且
  * objects may send messages to themselves so often that an interaction diagram becomes cluttered
  * 对象可能经常向自己发送消息，以至于交互图变得杂乱
* You might choose to omit messages from an object to itself, counting such things as internal computation within the object. This is a type of abstraction.
* 您可以选择忽略从对象到其自身的消息，计算对象内的内部计算等内容。这是一种抽象



### 8. Suppressing Detailed Behavior 抑制详情行为

* It is often sensible to describe interaction at a higher level, rather than showing every message between every pair of objects.

* 在更高层次上描述交互通常是明智的，而不是显示每对对象之间的每个消息。

* To do this we define a (full) sub-collaboration of a collaboration

* 对此我们定义了协作的子协作

  * Collaboration is a collection of objects and links between them
  * 协作是对象和它们之间的连接的集合
  * Sub-collaboration is a subset of the objects, together with the links connecting those objects.
  * 子协作是对象的子集，以及连接这些对象的链接
  * 简单来说就是：子写作是一个由一部分对象和连接这些对象的连接构成的集合

  ![image-20221206222828632](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206222828632.png)



### 9. Creation and Deletion of Objects 创建和删除对象

* The set of objects involved in an interaction is not always static; objects may be created and deleted during an interaction.

* 交互中涉及的对象集合并不总是静态的；可以在交互期间创建和删除对象

* Collaboration diagram 协作图

  * These show which objects are created and destroyed during an interaction by adding the constraints {new} {destroyed}. 
  * 它们通过添加约束｛new｝｛destroyed｝来显示在交互过程中创建和销毁的对象。
  * If the object is both created and destroyed in the same interaction, it can be labelled {transit}
  * 如果对象在同一交互中创建和销毁，则可以将其标记为｛transit｝

  ![image-20221206224456626](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206224456626.png)

* Sequence diagram 顺序图

  * These show an object being created by putting its object box part-way down the page, at the point it is created
  * 这些显示了在创建对象时，通过将其对象框放在页面的一部分来创建对象
  * Destruction of an object is shown by its activation ending with a large X.
  * 物体的破坏表现为其激活以一个大X结尾。

![image-20221206224640051](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206224640051.png)



### 10. Timing 计时

* The major advantage of sequence diagrams over collaboration diagrams is their ability to represent the passage of time graphically.
* 与协作图相比，序列图的主要优势是能够以图形方式**表示时间的流逝**。
* So far we have let the diagram indicate only the relative ordering of messages.
* 到目前为止，我们只让图表指示消息的相对顺序。
* Sometimes, however, the actual times are important.
* 有时候时间很重要
* A system in which actual times are important is called a real-time system. 
* **实际时间很重要的系统称为实时系统**

![image-20221206225104327](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206225104327.png)



### 11. Activity Diagrams 活动图

* Activity diagrams describe how activities are coordinated.
* 活动图描述了如何协调活动。
  * For example, an activity diagram may be used (like an interaction diagram) to show how an operation could be implemented
  * 例如，可以使用活动图（如交互图）来显示如何实现操作
* An activity diagram is particularly useful 
* 活动图特别有用
  * when you know that an operation has to achieve a number of different things, and 
  * 当您知道一个操作必须实现许多不同的事情时，以及
  * you want to model what the essential dependencies between them are, before you decide in what order to do them
  * 在决定按什么顺序执行之前，您需要对它们之间的基本依赖关系进行建模
* 活动图比交互图更能清楚地显示这一点。

![image-20221206235958836](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206235958836.png)

* At the UML semantics level, activity diagrams are state diagrams extended for convenience with some extra notation、
* 在UML语义级别上，活动图是为了方便而扩展的状态图，并使用了一些额外的符号
* Elements of activity diagrams
  * Activity 活动
  * Transition 过渡
  * Synchronization bar 同步栏
  * Decision diamond 决策菱形
  * Start and stop markers 启动和停止标记





* Activity – An activity is recorded like the notation for a state. However, we do not have transitions as a result of event, rather as the finishing of an activity. 
* 活动–活动的记录方式类似于状态的符号。然而，我们并没有将转换作为事件的结果，而是作为活动的结束
* Activity edge – an arrow to indicate where to move in the diagram after an activity finishes. These can be labelled with a guard condition
* 活动边缘–一个箭头，指示活动完成后在图表中移动的位置。这些可标记有防护条件。
* Synchronisation bar – a thick horizontal bar describing the co-ordination of activities which must all be completed before the activity edges leading from the bar are fired.
* 同步条–描述活动协调的粗水平条，所有活动必须在从条开始的活动边缘启动之前完成。
* Decision Diamond – can be used to show decisions as an alternative to guards on separate states leaving the same activity.
* 决策菱形–可用于显示决策，作为对离开同一活动的不同州的警卫的替代。
* Stop/Start markers – are used in the same way as in a state diagram (initial/final states).
* 停止/启动标记–使用方式与状态图（初始/最终状态）相同。

![image-20221207000951288](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221207000951288.png)

![image-20221207001011906](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221207001011906.png)





