# Introduction to Software Engineering

<font color='red' size=5>软件工程学的存在价值：促进软件项目成功</font>

<font color='red' size=5>1、“软件工程” ----Software Engineering是研究和应用如何以系统化的、规范的、可度量的方法去开发、运行和维护软件，即把工程化应用到软件上。</font>

## Lecture1

这个认为将的不错

https://blog.csdn.net/qq_45872668/article/details/125169139?ops_request_misc=&request_id=&biz_id=102&utm_term=%E8%BD%AF%E4%BB%B6%E5%B7%A5%E7%A8%8B&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduweb~default-1-125169139.142^v50^control_1,201^v3^control_1&spm=1018.2226.3001.4187

### 1.Introduction of Software Engineering

#### 1.1 Engineering

没啥好解释的就是工程

![image-20221219162330848](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221219162330848.png)

#### 1.2 Software 

![image-20220928172615970](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220928172615970.png)

* **<font color='red'>程序和文档都是software的一部分</font>**

##### 1.2.1 Classification

首先，software有两种分类

1. **“easy” systems (one developer, one user, experimental use only)** 单人，实验用
2. **“hard” systems  (multiple developers, multiple users, products)**多人，面向社会

二者的关系类似与一条河流的桥与无数河流的桥（大概

![image-20221219162712661](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221219162712661.png)

<font color='red' size=5> **Software engineering is about managing  this** 
**complexity.**</font>

软件工程是管理这种复杂性

##### 1.2.2 Features

1. 因为Software出现问题的后果非常严重，会造成比如隐私泄露，金融问题等。所有Software必须具有安全性。即很低的故障概率
2. 能够自我证明软件有非常低的故障率。

![image-20221219162819646](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221219162819646.png)

### 2. Software engineering tasks

1. 明确要求
   1. 我们需要它来干什么？
2. 设计产品
   1. 设计产品的外观和结构
   2. UI设计，软件模块设计，数据设计
3. 应用和测试
   1. 编码、测试和验证
4. 管理程序
   1. 管理维护软件系统

### 3. What is Software Engineering?

![image-20221219163048753](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221219163048753.png)

<font color='red'>Software Engineering是与软件生成各个方面都有关的工程学。</font>

![image-20220928173724145](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220928173724145.png)

#### 3.1 Software Process

软件过程Software Process是一组活动,其目标是软件的开发或演变。

##### 3.1.1 Software Process 的基本活动

![image-20221219163313308](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221219163313308.png)

1. 规范——系统应该做什么和它的开发限制
2. 开发——软件系统的生产(设计和实现)
3. 验证——检查软件是否是客户想要的
4. 进化——改变软件以响应不断变化的需求

##### 3.1.2 The Attributes Of Software Engineering

![image-20230109100946518](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230109100946518.png)

1. 可维护的
2. 独立的
3. 有效的
4. 可用的

#### 4. Law and Morality

没啥好说的，就看一下关于专业责任的问题：

* Confidentiality 保密
  * Engineers should normally respect the confidentiality of 
    their employers or clients even without a formal 
    confidentiality agreement.
  * 工程师通常应该尊重他们的雇主或客户的机密性，即使没有正式的保密协议。
* Competence 能力
  * Engineers should not misrepresent their level of 
    competence. They should not knowingly accept work 
    which is beyond their competence.
  * 工程师不应歪曲他们的能力水平。他们不应该故意接受超出自己能力范围的工作。

* Intellectual property rights 知识产权
  * Engineers should be careful to ensure that the intellectual 
    property of employers and clients is protected and know 
    the local laws governing IP.
  * 工程师应谨慎确保雇主和客户的知识产权受到保护，并了解管理知识产权的当地法律。
* Computer misuse  计算机滥用
  * Software engineers should not use their technical skills to 
    misuse other people’s computers.
  * 软件工程师不应该使用他们的技术技能来滥用他人的计算机。

#### 5. Lecture Key Points

![image-20221219164009570](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221219164009570.png)

![image-20221219164100753](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221219164100753.png)



##  Coursework1.1

做一个产品的步骤

在这节课上，我们将看到一些软件开发过程的例子，这些例子用于确保软件以一种系统的方式开发，使用经过试验和测试的技术

### 1.Introduction to Coursework 1.1

略

### 2. Use Cases

#### 2.1 Use Cases (用例)

<font color='red'>Use-Cases(用例)</font>：是基于场景的技术统一建模语言(UML)，它识别交互中的参与者，并描述交互本身。

<font color='red'>Use-Cases(用例)</font>是参与者需要在系统的帮助下执行的任务。例如，在书店里找到一本书的详细资料或打印一份收据的复印件。

* 一组用例Use-Cases应该描述与系统的所有可能交互。

![image-20221005154253035](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221005154253035.png)

![image-20221231135354422](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221231135354422.png)

#### 2.2 Sequence Diagrams(序列图)

Sequence Diagrams可以通过显示系统中事件处理的顺序来添加到用例的细节(我们将在以后研究序列图)。

#### 2.3 Use-Case Diagram(用例图)

在用例图中，参与者Actors是系统的用户(例如，系统外部的东西;可以是人类或非人类)扮演特定角色。

#### 2.4 Actors（Players）

系统外部与系统交互的任何东西

![image-20221005153943141](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221005153943141.png)



#### 2.5 The Relation of Use case Diagrams

![image-20221005154325666](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221005154325666.png)

![image-20221005154335548](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221005154335548.png)

##### 2.5.1 **关联**Assaociation

表示参与者与用例之间的通信，任何一方都可发送或接受消息。

【箭头指向】：无箭头，将参与者与用例相连接，指向消息接收方

![image-20221013094221113](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221013094221113.png)

##### 2.5.2 **泛化(Inheritance)**

就是通常理解的继承关系，子用例和父用例相似，但表现出更特别的行为；子用例将继承父用例的所有结构、行为和关系。子用例可以使用父用例的一段行为，也可以重载它。父用例通常是抽象的。在实际应用中很少使用泛化关系，子用例中的特殊行为都可以作为父用例中的备选流存在。

【箭头指向】：指向父用例

![image-20221013094447059](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221013094447059.png)

![image-20221029212100777](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221029212100777.png)



##### 2.5.3 **包含(Include)**

**包含关系用来把一个较复杂用例所表示的功能分解成较小的步骤。**包含关系对典型的应用就是复用，也就是定义中说的情景。但是有时当某用例的事件流过于复杂时，为了简化用例的描述，我们也可以把某一段事件流抽象成为一个被包含的用例；相反，用例划分太细时，也可以抽象出一个基用例，来包含这些细颗粒的用例。这种情况类似于在过程设计语言中，将程序的某一段算法封装成一个子过程，然后再从主程序中调用这一子过程。

　　例如：业务中，总是存在着维护某某信息的功能，如果将它作为一个用例，那添加、修改以及删除都要在用例详述中描述，过于复杂；如果分成添加用例、修改用例和删除用例，则划分太细。这时包含关系可以用来理清关系。

<font color='red'>【箭头指向】：指向分解出来的功能用例</font>

![image-20221013094608529](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221013094608529.png)

##### 2.5.4 **扩展(Extend)**

**扩展关系是指用例功能的延伸，相当于为基础用例提供一个附加功能。**将基用例中一段相对独立并且可选的动作，用扩展（Extension）用例加以封装，再让它从基用例中声明的扩展点（Extension Point）上进行扩展，从而使基用例行为更简练和目标更集中。扩展用例为基用例添加新的行为。扩展用例可以访问基用例的属性，因此它能根据基用例中扩展点的当前状态来判断是否执行自己。但是扩展用例对基用例不可见。

对于一个扩展用例，可以在基用例上有几个扩展点。

【箭头指向】：指向基础用例

![image-20221013094714200](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221013094714200.png)

#### 2.6 对用例的描述

https://www.jianshu.com/p/7ff70e28bb72

## Lecture2

参考

https://blog.csdn.net/weixin_42067279/article/details/104515101?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522166498152316782388095141%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=166498152316782388095141&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduend~default-1-104515101-null-null.142^v51^control_1,201^v3^control_1&utm_term=Software%20Processes%20&spm=1018.2226.3001.4187

#### 1. Progress

- 建房子：不同的房子，虽有不同的建造过程，却有相同的**生命周期（life cycle）。**
- 开发软件：也是一样，**不同开发过程，相同生命周期（5个阶段）：**软件的需求分析、软件设计、软件编码、软件测试、软件维护。<font color='red'>(这里有个小问题，与课件描述不太相符)</font>

简单点来说，**Process是一个软件的生命周期 == 一个软件的开发流程**

其中常规活动有：<font color='red'>**Specifying说明，Designing设计，Implementing应用，Testing测试**</font>

![image-20221219164945307](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221219164945307.png)

* 任何过程都具有以下特征
  * 它规定了所有的主要活动
  * 它使用资源并生产中间产品和最终产品
  * 它可能包括子流程，并具有进入和退出标准
  * 活动是按顺序组织的
  * 约束或控制可以应用于活动(预算限制、可用资源等)

![image-20221219165337479](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221219165337479.png)



#### 2. Software Progress

##### 2.1 Some features Of Software

![image-20221231141805210](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221231141805210.png)

![image-20221005170407182](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221005170407182.png)

![image-20221219165652659](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221219165652659.png)



##### 2.2 Software Process Models

* The Waterfall Model (classic engineering, example bridge 
  building)   
* **瀑布模型(经典工程，例如桥梁建筑)**
  * Separate and distinct phases of specification and development
  * **不同的规范和开发阶段**
* **Evolutionary Development (more like product engineering)**
* 不同的规范和开发阶段
  * Specification and development are interleaved
  * **规范和开发是交错的**
* Agile and Scrum
  * Used widely in industry today

###### 2.2.1 Waterfall Model

![image-20221005171008239](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221005171008239.png)

五个阶段：需求定义Requirements Definition、系统和软件设计System and Software desgin、实现（编码）和单元测试Implementation and unit testing、集成和系统测试Integration and System Testing、运行和维护Operation and Maintenance。

五个阶段有清晰的阶段划分。阶段之间有正向的和反向的箭头连接。

* **正向箭头：**代表这个阶段的工作完成，经过评审以后可以进入下个阶段，像瀑布一样逐级而下。

* **反向箭头：**代表这个阶段的工作存在的问题，要把反馈送回去，再重新进行工作，进行评审。

<font color='blue' size=5>对于各个部分的解释</font>

（1）Requirements analysis and definition：

需求分析和定义，对应 software specification 这样的一个阶段活动。

（2）System and software design：

对应着 系统结构的设计、算法的设计、数据结构的设计。

（3）Implementation and unit testing：

实现和单元测试。实现理解为programming 或 coding；单元测试，一般都是由程序员来承担的，在编码的过程中，通常也要进行单元测试。

（4）Integration and system testing：

经过单元测试，集成起来的子系统，叫做 integration testing

把整个系统集成起来，完成的测试叫做 system testing。

不同测试目标的测试方法 不一样。

（5）Operation and maintenance：

系统投入运行并维护。

<font color='blue' size=5>缺点</font>

**因为这个过程被划分成了数个缺乏柔性的阶段，这使得<font color='red'>它在响应客户需求的变化就变得很困难。</font>所以一但进入的后面的阶段，发现了问题就需要返回重做，这样代价很大。**

**适用范围**

- **适用于：**需求清晰（well understood）、功能明确、变化有限 的系统。
- **适用于：**大型系统（因为大型系统的需求很复杂，通常要做大量的工作，将它完整挖掘，精确描述；大型系统的整体设计不能频繁修改）。
- 比如基于硬件的工程模型，或者广泛使用的航天工业。
- ![image-20221231143004592](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221231143004592.png)

![image-20230109104204540](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230109104204540.png)

###### 2.2.2 Evolutionary Development 演化开发

* Exploratory development  勘探开发
  - Objective is to work with customers and to evolve a final 
    system from an initial outline specification. 
  - 目标是与客户合作，从最初的大纲规范发展出最终的系统。
  - Should start with well-understood requirements. 
  - 应该从很好理解的需求开始。
  - The system evolves by adding new features as they are 
    proposed by customer. 
  - 系统通过添加客户提出的新功能来发展。

![image-20221005172921743](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221005172921743.png)

演化式开发模式可以不需要给出一个清晰的需求描述，而是从一个<font color='red'>outline description</font>开始（也就是说，我大致先知道需要做哪些功能）
一旦有了一个大致的功能和性能要求，就可以通过specification，development，validation。构成一个软件的初始版本，也叫原型**（Initial version）** 。
原型（Initial version）构造好后，交给用户来使用和评价，用户若觉得这个版本不合适，开发人员再进行修改，形成第二个版本。不断重复这些过程，就会形成很多的中间版本**（Intermediate versions），直到形成一个最终版本（Final version）**

**补充**：

**用户参与：**用户是参与在开发过程中的。用户一直和开发团队进行交流，每开发出一个新的版本，用户要进行评价并产生反馈意见，然后由开发者来修订，产生不同的中间版本，最终演化成一个最终版本。
**别名：**演化式开发、原型开发。
**演化式含义：**每个增量，是在上一个版本的基础上，再进行的工作

<font color='blue' size=5>优点：</font>

**对用户需求变化的适应性的代价会比较小**



瀑布模型，有一个清晰的阶段划分，每个阶段都需要有阶段性的成果，包括阶段性的文档用于评审。如果后期发生的变化，前面工作都需要重新来做，代价大。

增量式开发，最后的版本是不断地修改而成，在做中间快速构造原型的过程中，几乎不产生文档，直到最后的版本出现才形成正式的文档。

* 客户值可以通过每个增量交付,因此系统功能可以提前使用
* 早期增量作为一个原型,以帮助引出后续增量的需求
* 较低的整体项目失败风险
* 最高优先级系统服务往往接收到最多的测试

<font color='blue' size=5>缺点：</font>

**过程不可见**

* 可见（visible）指的是：用户查看开发过程中的中间文档来获取信息。缺乏流程可见性

* 追求速度，不会产生大量中间文档，用户就难以系统地获取信息，就不可见。 系统有时结构很差

  

**系统结构可能随增量变多而逐渐退化**

* 起初从outline description开始，意味着这个初始结构就可能存在缺陷（因为没有精确的需求定义），后面一版一版的修改，很可能会造成系统结构不断地退化。
* 除非花钱花时间来重构改善这个软件，否则，经常性的这样的一个改变会导致这个结构的崩溃。（一样东西，若起初就有完整的设计，那么必将呈现一个好的结构；反之，若一开始就糙，再不断修改，就变得更糙，结构就一直存在缺陷

**瀑布模型和增量式开发对比：**

**瀑布模型和增量式开发，两个优缺点几乎是互补的。**
增量式开发：

* 用户全程参与，能得到用户的即时反馈，对于用户需求的变化，响应会比较好。
* 开发快，交付早。中间过程不可见，系统结构可能会逐渐退化。
* 适用于：中小型系统（生命周期较短，对结构和可维护性要求较低）

**瀑布模型：**

用户只参与第一阶段（需求定义），用户的需求发生变化，难以及时反映到开发过程中。

开发慢，交付晚。中间过程可见，系统结构精确且稳定。
适用于：大型系统（生命周期较长，对结构和可维护性要求较高）



###### 2.2.3 Agile Development (敏捷开发)

**换言之，就是把一个大项目分为多个相互联系，但也可独立运行的小项目，并分别完成，在此过程中软件一直处于可使用状态。**

Lightweight approach to software development
Example include Scrum and XP

* 软件开发的轻量级方法
* 例子包括Scrum和XP

轻量级的软件开发工程

![image-20221005175930177](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221005175930177.png)

Agile Development是一种以人为核心、**迭代**、循序渐进的开发方法。在敏捷开发中，软件项目的构建被切分成多个子项目，各个子项目的成果都经过测试，具备集成和可运行的特征。<font color='red'>简言之，就是把一个大项目分为多个相互联系，但也可独立运行的小项目，并分别完成，在此过程中软件一直处于可使用状态。</font>



<font color='blue' size=5>敏捷开发技术的适用范围</font>

1.项目团队的人数不能太多

2.项目经常发生变更

3.高风险的项目实施

4.开发人员可以参与决策

<font color='blue' size=5>敏捷开发技术的几种主要类型</font>

1.XP（Extreme Programming ）－－ 极限编程

2.Cockburn的水晶系列方法

3.开放式源码

4.Highsmith的适应性软件开发方法〔ASD

###### 2.2.4 Incremental Development 增量式开发

**增量开发分成小块的价格。这些被称为增量。每个增量都建立在之前的增量之上。全功能模块会随着时间一点一点地增长。每一次进化都增加了之前的功能。**

![image-20221219172501194](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221219172501194.png)

* **与其将系统作为单个交付交付，不如将开发和交付分解为增量(SCRUM sprint)，每个增量交付所需功能的一部分**
* 用户需求是优先级的，最高优先级的需求包含在早期增量中
* 一旦开始了增量的开发，需求就会被冻结，尽管后续增量的需求可以继续发展
* **<font color='red'>大概的意思是，增量式开发一开始先开发一个小的系统，然后把功能添加到每一个后续增量中直到完成</font>**

优点：

![image-20221219172613870](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221219172613870.png)

客户价值可以随每个增量一起交付，因此系统功能可以更早地可用

早期增量作为一个原型来帮助引出后续增量的需求

降低整体项目失败的风险

最高优先级的系统服务往往接受最多的测试

![image-20221219172727065](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221219172727065.png)

流程依赖于上下文

* 核电站/空中交通管制
* 高度形式化的流程
* 详细测试规范
* 小型网站Web开发
* 原型
* 大型网站的Web开发
* SCRUM开发，故事板

## Week2 Lecture3 Software Processes

![image-20221008104422156](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221008104422156.png)

### 1. Software Specification 软件规范

**Software Specification**: 确定需要什么服务以及对系统操作和开发的约束的过程

* Requirements Engineering Process
  * 可行性分析Feasibility Study
  * 建立和分析需求Requirements elicitation and analysis
  * 需求规范 Requirements specification
  * 需求验证 Requirements validation

![image-20221008110239729](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221008110239729.png)

### 2. Software Design and Implementation

**<font color=red>The process of converting the system specification into 
an executable system. 将系统规范转换成可执行系统的过程</font>**

* Software Design

  * 设计一个可以实现规范的软件结构
  * 任务包括：设计数据库，网站设计，数据结构，通信协议

* Implementation

  * 将上述软件结构转换成可执行的程序

  

**设计和实现的活动是密切相关的，可能是交叉的**

**The activities of design and implementation are closely related and may be inter-leaved**

#### 2.1 Design Process Activities

1. **Architectural Design结构设计** (separate web service modules)
   1. 确定并记录了组成系统的子系统及其关系。
   2. The sub-systems making up the system and their relationships are identified and documented.

2. **Abstract specification 抽象规范**
   1. 对于每一个子系统，都会生成一个操作约束和服务的抽象规范。（每一个子系统都有一个抽象规范）
   2. For each sub-system, an abstract specification of its operational constraints and services is produced.

3. **Interface Design（接口设计）**
   1. 对于每个子系统，都设计了与其他子系统的明确接口并编制了文档
   2. For each sub-system, an unambiguous interface with other sub-systems is designed and documented

4. **Component Design(元件设计)**
   1. 为组件分配服务，并设计这些组件的接口

5. **Data Structure Design** 数据结构设计
   1. 对系统实现中使用的数据结构进行了详细的设计和说明

6. **Algorithm design 算法设计**
7. ．设计并指定了用于提供服务的组件中的算法

<font color='blue' size=5>Example:</font>

![image-20221008132208489](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221008132208489.png)

![image-20221008132219972](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221008132219972.png)

#### 2.2 Design Methods

![image-20221219173415807](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221219173415807.png)

**Design(Structured) Methods设计(结构化)方法：是开发软件设计的系统方法.**

**设计通常被记录为一组图形模型**  The design is usually documented as a set of graphical models

**可能的模型(我们将在后面的课程中详细研究)**

1.数据流模型

2.实体-关系-属性模型(数据库或类设计)

3.结构模型

4.对象模型

5.显示系统状态和触发器的状态转换模型

### 2.3 Programming and Debuging 编程和调试

编程和调试(Programming and Debuging)包括将设计转化为程序并从程序中删除错误.

* 编程通常是个人活动——没有通用的编程过程，但有良好的编程实践和组织标准可以遵循。

* 程序员进行一些程序测试，以发现程序中的错误，并在调试过程中消除这些错误。

#### 2.3.1 The Testing Process

![image-20221008134022423](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221008134022423.png)

原件测试，集成测试，用户测试



![image-20230109121549596](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230109121549596.png)

**Unit testing**

* Individual components are tested对单个组件进行测试

**Module testing**

* 测试依赖组件的相关集合

 **Sub-system testing (merges with system testing)**

* 模块集成到子系统中并进行测试。这里的重点应该放在接口测试上

**System testing**

* 整个系统的测试。紧急特性测试

**Acceptance testing**

* 用客户数据进行测试，以检查其是否可接受

**Example**

**Unit testing  (class/method level)**

* 测试单个类方法

**Module testing  (interleaved with unit testing)**

* 测试与其他类集成的类

**Sub-system  testing**

* 被测试的产生给定服务的许多类(例如信用卡支付服务、短信发送服务)

* 组织为包或JAR库

**System test**

* 测试整个系统

![image-20230106210629054](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106210629054.png)



# Requirements Analysis and Modeling

## Lecture4  Requirement Engineering

![image-20221008135930186](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221008135930186.png)

#### 1. Requirements Engineering要求工程

**Requirements Engineering(需求工程)是在系统运行和开发的约束条件下，建立客户从系统中需要的服务的过程**

![image-20230111131749942](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230111131749942.png)

![image-20221008141746044](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221008141746044.png)

*  Why do we need requiremnet?
   
*  To ensure a software solution correctly solves a  particular problem, we must
   * 充分理解需要解决的问题
   * 发现为什么这个问题需要解决
   * 决定谁应该参与。

*  定义不清的需求会给项目带来重大的财务问题和额外的时间。

**它的范围可能从服务或系统约束的高级抽象语句到详细的数学功能规范**

![image-20221008142239118](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221008142239118.png)

例子(需求迭代)

该系统将支持广泛的最常用的图形文件格式

系统可能支持的文件格式有:png、jpeg、tiff和gif

系统可能支持以下文件格式:png、jpeg、tiff和gif，最大分辨率为1024x1024像素

系统可能支持以下文件格式:png, jpeg, tiff和gif，最大分辨率为1024x1024像素，最大文件大小为20兆字节，这些参数可以很容易地使用插件扩展

![image-20230101101140011](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101101140011.png)

#### 2. Types Of Requirement(不同类型的要求)

**User requirements**

用自然语言编写的语句，加上系统提供的服务及其操作约束的图表。**为客户写的**

**System requirements**

对系统服务进行详细描述的结构化文档。**书面形式为客户和承包商之间的合同。**

**Software specification**

可以作为设计或实现基础的详细软件说明。**为开发人员编写**

![image-20230101101749751](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101101749751.png)

<font color='red'>可以仔细看一下这个例子，很明了</font>



#### 3. Functional And Non-Functional Requirements

**Functional requirements**

系统应该提供的服务、**系统应该如何对特定输入作出反应以及系统在特定情况下应该如何表现的陈述**

**Non-Functional Requirements**

对系统提供的服务或功能的限制，例如时间限制、开发过程的限制、标准等。通常将系统定义为一个整体.

**非功能性需求**是指依一些条件判断系统运作情形或其特性，而不是针对系统特定行为的需求。
包括安全性、可靠性、互操作性、健壮性、易使用性、可维护性、可移植性、可重用性、可扩充性。

<font color=red>这个可以通过Coursework1来看一些例子</font>

**Domain requirements**

来自系统的应用程序领域的需求，反映了该领域的特征

![image-20230101102503132](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101102503132.png)

![image-20221008155105230](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221008155105230.png)

##### 3.1 Requirements Imprecision 需求精确

当需求没有被精确地表述时，问题就出现了

![image-20230111133726046](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230111133726046.png)

##### 3.2 Requirements Completeness and Consistency 需求的完整和一致性

完整的 Complete

**它们应该包括所有所需设施的描述**

一致的 Consistent

系统设施的描述不应有冲突或矛盾

在实践中，产生一个完整且一致的需求文档是非常困难或者不可能的

![image-20230101105233327](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101105233327.png)



##### 3.3 Non-Functional Requirements

<font color='blue'>定义系统属性和约束</font>，例如可靠性、响应时间和存储需求。约束包括I/O设备能力、系统表示等。它们通常是系统的<font color='red'>涌现属性 emergent properties</font>。

<font color=blue>Process Requirement过程需求</font>也可以指定，要求使用特定的CASE系统、编程语言或开发方法

<font color=blue>Non-functional requirements 非功能需求</font>可能比功能需求更关键。如果这些不满足，系统是无用的(例如，加密安全邮件的密钥长度必须是> = 256位)

###### 3.1.1 Non-Functional Classifications(非功能分类)

<font color=blue>Product Requirements</font>

规定所交付产品必须以特定方式运作的要求，例如执行速度、可靠性、安全性等。

<font color=blue>Organisational requirements</font>

由组织政策和程序而产生的要求，例如所采用的过程标准、实施要求等(以Java为编程语言)

<font color=blue>External requirements</font>

来自于系统及其开发过程外部因素的需求，例如互操作性需求、立法需求等(必须符合FIPS

![image-20221008215320651](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221008215320651.png)

<font color=blue size=5>Example</font>

**产品需求** Product requirement

所有加密都应该使用高级加密标准

**组织要求 ** Organisational requirement

系统开发过程和交付成果文件应符合编码和文档标准XYZCo-SP-STAN-95中定义的过程和交付成果

**外部需求** External requirement

除客户的姓名和编号外，系统不会向系统的运营者披露客户的任何个人信息

**性能需求**  性能需求

在“高峰时间”和0.01秒内，系统应在小于0.1秒的时间内响应用户的信息请求

![image-20230101104054035](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101104054035.png)

###### 3.1.2 Goals and Requirements

* Non-functional requirements may be very difficult to state precisely and imprecise requirements may be difficult to verify.
* 非功能性需求可能很难精确地表述，而不精确的需求可能很难验证。
* Verifiable non-functional requirement
* 可验证的非功能需求
  * A statement using some measure that can be objectively tested
  * 一种使用某种可以被客观测试的测量方法的陈述
* Goals are helpful to developers as they convey the intentions of the system users
* 目标对开发人员很有帮助，因为它们传达了系统用户的意图

![image-20230101105623631](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101105623631.png)

![image-20230111135356419](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230111135356419.png)

##### 3.4 Domain Requirement

* Conflicts between different non-functional requirements are common in complex systems

* 来自系统的应用程序领域的需求，反映了该领域的特征

![image-20230101105945883](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101105945883.png)

Conflicts between different non-functional requirements are common in complex systems

在复杂的系统中两个不同的non-functional requirement会产生矛盾是正常的

![image-20230101110111357](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101110111357.png)

![image-20230101110243451](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101110243451.png)



#### 4. User Requirements

**用户需求应该描述功能和非功能需求，以便不具备详细技术知识的系统用户能够理解．使用自然语言、表格和图表来定义用户需求，以便非技术客户能够更好地理解需求并指出潜在的问题。**

<font color=red>傻瓜说明书</font>

* 缺乏清晰
* 要求模糊
* 要求合并

![image-20221008220150732](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221008220150732.png)

![image-20221008220201050](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221008220201050.png)

![image-20230101110508937](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101110508937.png)





## Lecture6 Requirements Engineering Processes

![image-20230101114810456](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101114810456.png)

![image-20230111140434598](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230111140434598.png)

### 1. Requirements Engineering Processes 需求工程进程

* The processes used for requirements engineering vary widely depending on the application domain, the people involved and the organisation developing the requirements.
* 用于需求工程的过程根据应用领域、涉及的人员和开发需求的组织的不同而有很大的不同。
* However, there are a number of generic activities common to all processes which we look at today.
* 然而，我们今天看到的所有流程都有一些通用的活动。
* **The goal of this stage of the software engineering process is to help create and maintain a system requirements document.**
* **软件工程过程的这一阶段的目标是帮助创建和维护系统需求文档。**

#### 1.1 Requirements Engineering Processes

1. Requirements elicitation 需求建立
   1. What services do the end-users require of the system?
   2. 终端用户需要系统提供哪些服务?
2. Requirements analysis 需求分析
   1. How do we classify, prioritise and negotiate requirements?
   2. 我们如何对需求进行分类、确定优先级和协商?
3. Requirements validation 需求验证
   1. Does the proposed system do what the users require?
   2. 所提议的系统是否满足用户的要求?
4. Requirements management 需求管理
   1. How do we manage the (sometimes inevitable) changes to the requirements document?
   2. 我们如何管理需求文档的变更(有时是不可避免的)?

![image-20230101115511410](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101115511410.png)

<font color=red>感觉1和2可以归类成同一个类别</font>

![image-20230101115730588](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101115730588.png)

##### 1.2 Feasibility Studies 可行性分析

* A feasibility study decides whether or not the proposed system is worthwhile.
* 可行性研究决定所建议的系统是否值得。
* A short focused study that checks
  * If the system contributes to organisational objectives;
  * 系统是否有助于实现组织目标;
  * If the system can be engineered using current technology and within budget;
  * 该系统是否可以利用现有技术并在预算范围内设计;
  * If the system can be integrated with other systems that are used.
  * 该系统是否可以与所使用的其他系统集成。
  * Is there a simpler way of doing this (buy in software and customize)
  * 有没有更简单的方法(购买软件并定制)

##### 1.3 Elicitation and Analysis 需求获取与分析

* Sometimes called **requirements elicitation or requirements discovery.**

* 有时称为需求启发或需求发现。

* Involves technical staff working with customers to find out about the **application domain, the services that the system should provide** and **the system’s operational constraints.**

* 涉及技术人员与客户合作，以了解应用程序域、系统应该提供的服务和系统的操作限制。

* May involve end-users, managers, engineers involved in maintenance, domain experts, trade unions, etc. These are called stakeholders.

* 可能涉及最终用户、管理人员、参与维护的工程师、领域专家、工会等。

  这些人被称为利益相关者。

![image-20230101121303792](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101121303792.png)

![image-20230101121805051](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101121805051.png)

##### 1.4 Requirements Specification

在本节课未提及

##### 1.5 Requirements Management

在本节课未提及

### 2.Security for most systems is a core service

#### 2.1 Requirements Discovery

**这个应该属于提纲中的两种分析requirement的方法之一**

<font color=red> 这里的父子标题可能给的有些问题，我没办法清晰确定这一课的逻辑结构</font>

**比如 Requirements Discovery 应该等同于 Elicitation and Analysis**

* Requirements discovery is the process of gathering information about the proposed and existing systems and distilling the user and system requirements from this information.
* 需求发现是收集关于提议的和现有的系统的信息，并从这些信息中提取用户和系统需求的过程。
* Sources of information include documentation, system stakeholders and the specifications of similar systems
* 信息来源包括文档、系统涉众和类似系统的规范

![image-20230101123549699](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101123549699.png)

![image-20230101123607498](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101123607498.png)

![image-20230101123726724](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101123726724.png)

#### 2.2 Vieiyioints 观点

**这个应该属于提纲中的两种分析requirement的方法之一**

* **Viewpoints are a way of structuring the requirements** to represent the perspectives of different stakeholders. Stakeholders may be classified under different viewpoints.

* 视点是构造需求的一种方式，以表示不同涉众的观点。

  涉众可以根据不同的观点进行分类。

* This multi-perspective analysis is important as there is no single correct way to analyse system requirements.

* 这种多角度分析非常重要，因为没有唯一正确的方法来分析系统需求。

![image-20230101124011789](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101124011789.png)

![image-20230101124003452](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101124003452.png)

#### 2.5 Interviewing

![image-20230101150719350](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101150719350.png)

![image-20230101151040310](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101151040310.png)

#### 2.6 Ethnography

？？？我搞不明白这个Ethnography是什么鬼？民族志？

![image-20230101151659914](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101151659914.png)

![image-20230101151631503](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101151631503.png)

##### 2.6.1 Focused Ethnography

![image-20230101152028538](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101152028538.png)

![image-20230101152020592](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101152020592.png)

##### 2.6.2 Scope of Ethnography 民族志的范围

![image-20230101152523639](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101152523639.png)

![image-20230101153415016](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101153415016.png)

![image-20230101153432680](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101153432680.png)

![image-20230101153448399](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101153448399.png)

#### 2.7 Security 安全性

![image-20230101153559042](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101153559042.png)

![image-20230101153608675](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101153608675.png)

![image-20230101153619488](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101153619488.png)·![image-20230101153634635](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101153634635.png)

##### 2.7.1 Confidentiality requirements

![image-20230101153720887](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101153720887.png)

![image-20230101153731757](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101153731757.png)



##### 2.7.2 Integrity Requirements

![image-20230101153844047](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101153844047.png)

![image-20230101153854591](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101153854591.png)

##### 2.7.3 Authentication/Authorization

身份验证

你是谁?

授权

你被允许做什么?

技术

用户名，密码，硬件(卡，加密狗)，

生物识别技术

通常是第一个攻击点

##### 2.7.4 Non-repudiation issue 不可抵赖性问题

![image-20230101154035102](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101154035102.png)

![image-20230101154059117](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101154059117.png)

![image-20230101154204211](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101154204211.png)

##### 2.8 Availability requirements 可用性需求

![image-20230101155220709](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101155220709.png)

![image-20230101155238386](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101155238386.png)

##### 2.9 Security, logs and alerts 安全性和日志

![image-20230101155322778](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101155322778.png)

![image-20230101155405304](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101155405304.png)

###### 2.9.1 Bell-LaPadula Model

https://blog.csdn.net/waqqy/article/details/127803086?ops_request_misc=&request_id=&biz_id=102&utm_term=Bell%E2%80%93LaPadula%20security%20model%20&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduweb~default-3-127803086.142

![image-20230101155442350](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101155442350.png)

**不能向上读，不能向下写**



**同范畴内：上级可读下级，下级不可读上级；下级可写上级，上级不可写下级；**

**同级之间可互读写 不同范畴：上级、下级、同级之间都不可读写**



##### 2.10 Specifying Security 描述安全

![image-20230101155625587](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101155625587.png)

![image-20230111150811743](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230111150811743.png)



##### 2.11 Requirements Checking

![image-20230101155916244](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101155916244.png)

* Validity. Does the system provide the functions which best support the customer’s needs?
* 有效性。系统是否提供了最能支持客户需求的功能?
* Consistency. Are there any requirements conflicts?
* 一致性。是否存在需求冲突?
* Completeness. Are all functions required by the customer included
* 完整性。客户要求的所有功能都包括在内了吗?
* Realism. Can the requirements be implemented given available budget and technology?
* 现实主义。有了可用的预算和技术，这些需求能被实现吗?
* Verifiability. Can the requirements be checked?
* 可验证性。可以检查需求吗?
  * This reduces the potential for disputes between customers and 
    contractors and a set of tests should be possible.
  * 这减少了客户和承包商之间发生纠纷的可能性，并且应该可以进行一套测试。

##### 2.12 Scenarios 脚本

测试是否满足要求

![image-20230101160303468](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101160303468.png)

![image-20230101160338397](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101160338397.png)

#### Cucumber in summary

![image-20230111151253663](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230111151253663.png)

### Lecture7 System Models 1

![image-20230101165337093](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101165337093.png)

还记得我们之前说的system requirement吗？system model是用来描述system requirement

#### 1. System Models

* User requirements must be written in such a way that non-technical experts can understand them, e.g., by using natural language
* 用户需求必须以非技术专家能够理解的方式编写，例如，使用自然语言
* Detailed system requirements may be expressed in a more technical way however
* 然而，详细的系统需求可以用更专业的方式来表达
  * One widely used technique is to document the system specification as a set of system models
  * 一种广泛使用的技术是将系统规范记录为一组系统模型
  * These are graphical representations which describe business processes and the system to be developed
  * 这些图形表示描述了业务流程和要开发的系统
  * They are an important bridge between the analysis and design processes
  * 它们是分析和设计过程之间的重要桥梁



* System modelling helps the analyst to understand the functionality of the system and models are used to communicate with customers
* 系统建模有助于分析人员理解系统的功能，模型用于与客户沟通
* Different models present the system from different perspectives:
* 不同的模型从不同的角度来呈现系统:
  * **External perspective** showing the system’s context or environment
  * 外部视角显示系统的上下文或环境
  * **Behavioural perspective** showing the behaviour of the system
  * 行为视角显示系统的行为
  * **Structural perspective** showing the system or data architecture
  * 结构透视图显示系统或数据架构

![image-20230101170625786](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101170625786.png)

##### 1.1 System Model Advantages

* They can be easier to understand than using a verbose natural language description
* 它们比使用冗长的自然语言描述更容易理解
* System models can leave out unnecessary details of the system so way may focus on what is important
* 系统模型可以省略系统不必要的细节，这样就可以专注于重要的东西
  * A system representation should maintain all the information of a system
  * 系统表示法应该维护系统的所有信息
  * An abstraction deliberately simplifies the system and picks out its most salient characteristics
  * 抽象有意地简化系统并挑出其最显著的特征
* Different models can focus on different approaches to abstraction
* 不同的模型可以关注不同的抽象方法



##### 1.2 System Model Weaknesses

* They do not model non-functional system requirements
* 它们不为非功能性的系统需求建模
* They do not usually include information about whether a method is appropriate for a given problem
* 它们通常不包含关于方法是否适合给定问题的信息
* They may produce too much documentation
* 他们可能会产生太多的文档
* System models are sometimes too detailed and difficult for users to understand
* 系统模型有时过于详细，用户难以理解



##### 1.3 Model Types

* **Data processing model** - showing how the data is processed at different stages
* 数据处理模型-显示数据在不同阶段是如何处理的
* **Composition model** - showing how entities are composed of other entities
* 组合模型-显示实体如何由其他实体组成
* **Architectural model** - showing principal sub-systems
* 体系结构模型-显示主要子系统
* **Classification model** - showing how entities have common characteristics
* 分类模型-显示实体如何具有共同特征
* **Stimulus/response model** - showing the system’s reaction to events
* 刺激/反应模型-显示系统对事件的反应

![image-20230101172024541](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101172024541.png)

#### 2. Context Models 内容模型(上下文模型)

* Context models are used to illustrate the boundaries of a system
* 上下文模型用于说明系统的边界
* Identifying the boundaries of the system to be developed is not always straightforward
* 确定要开发的系统的边界并不总是简单的
* Social and organisational concerns may affect the decision on where to position system boundaries
* 社会和组织的关注可能会影响系统边界定位的决定
* **Architectural models show the system and its relationship with other systems**
* **体系结构模型显示了系统及其与其他系统的关系**

![image-20230101223913035](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101223913035.png)

![image-20230101172702637](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101172702637.png)

#### 3.Process Models 进程模型 流模型

* Process models show the overall process and the processes that are supported by the system
* 流程模型显示了整个流程和系统支持的流程
  * In process models it is implicit 1 process is completed before another process begins
  * 在流程模型中，一个流程在另一个流程开始之前完成
  * Process models are similar to flow charts
  * 流程模型类似于流程图
* **Data flow models** may be used to show the processes and the flow of information from one process to another
* 数据流模型可用于显示流程以及从一个流程到另一个流程的信息流
  * **The data flow models** it is implicit that processes will happen in parallel (concurrent processing)
  * **数据流模型表明流程将以并行方式进行(并发处理)**

![image-20230101223858385](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101223858385.png)

#### 4. Behavioural Model 活动模型

* **Behavioural models are used to describe the overall behaviour of a system**
* **行为模型用于描述系统的整体行为**
* Two types of behavioural model
  *  **Data processing models** that show how data is processed as it moves through the system
  *  数据处理模型，显示了当数据在系统中移动时如何处理数据
  *  **State machine models** that show the systems response to events
  *  显示系统对事件响应的状态机模型
* Both of these models are required for a description of the system’s behaviour
* 这两个模型都是描述系统行为所必需的

![image-20230101223927435](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101223927435.png)

##### 4.1 . Data-Processing Models 数据处理模型

* **Data flow diagrams** are used to model the system’s data processing
* **数据流图**用于对系统的数据处理进行建模
* These show the processing steps as data flows through a system
* 它们显示了数据流经系统时的处理步骤
* IMPORTANT part of many analysis methods
* 许多分析方法是重要的组成成分
* **Simple and intuitive notation**
* 简单直观的符号
* **Show end-to-end processing of data**
* 显示数据的端到端处理

![image-20230101224444147](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101224444147.png)

###### 4.1.1  Data Flow Diagrams 数据流图

* Data Flow Diagrams track and document how the data associated with a process is helpful to develop an overall understanding of the system
* 数据流图跟踪并记录与流程相关的数据如何有助于开发对系统的全面理解
* Data flow diagrams may also be used in showing the data exchange between a system and other systems in its environment
* 数据流图也可以用于显示系统与环境中其他系统之间的数据交换

![image-20230101224846624](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101224846624.png)

* Data Flow Diagrams have an advantage in that they are simple and intuitive and can thus be shown to users who can help in validating the analysis
* 数据流图的优势在于它们简单直观，因此可以显示给能够帮助验证分析的用户
* Developing data flow diagrams is usually a top-down process 
* 开发数据流图通常是一个自顶向下的过程
  * We begin by evaluating the overall process we wish to model before considering sub-processes
  * 在考虑子过程之前，我们首先评估希望建模的整个过程
* Data flow diagrams show a **functional perspective** where each transformation represents a single function or process which is particularly useful during requirements analysis since it shows end-to-end processing.
* 数据流图显示了一个功能视角，其中每个转换代表一个单独的功能或过程，这在需求分析期间特别有用，因为它显示了端到端处理。

![image-20230101225228051](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101225228051.png)

![image-20230101225236305](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101225236305.png)

![image-20230101225244229](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101225244229.png)

##### 4.2 . Statechart Diagrams 状态图

* **Statechart Diagrams (or State machine models )** show the behaviour of the system in response to external and internal events
* **状态图(或状态机模型)显示了系统响应外部和内部事件的行为**
* They show the system’s responses to stimuli (the event-action paradigm) so are often used for modelling real-time systems
* 它们显示了系统对刺激的反应(事件-动作范式)，因此经常用于实时系统建模
* Statechart diagrams show system states as nodes and events as arcs between these nodes. When an event occurs, the system moves from one state to another
* 状态图将系统状态显示为节点，事件显示为这些节点之间的弧。当一个事件发生时，系统从一种状态转移到另一种状态
* Statecharts are an integral part of the Unified Modeling Language (UML)
* 状态图是统一建模不可分割的一部分语言(UML)



画法：

* An initial state is denoted by a solid circle and is optional (sometimes the system will start in different places and thus the initial state should be omitted). 
* 初始状态用实心圆表示，是可选的(有时系统会在不同的地方开始，因此初始状态应该省略)。
* If required, a final state can also be used; this is denoted by a solid circle with a ring around it.
* 如果需要，也可以使用最终状态;这是用一个实心圆和一个环来表示的。
* We use a level of abstraction so that we can observe the essential behaviour of the system we want to model. 
* 我们使用一个抽象级别，这样我们就可以观察到我们想要建模的系统的基本行为。
* Rounded rectangles are used for states. Each state contains two components, the state name and a brief description of the action performed in that state (see next slide).
* 圆角矩形用于表示状态。每个状态包含两个组件，状态名称和在该状态下执行的操作的简要描述(见下一张幻灯片)。

![image-20230101230150253](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101230150253.png)

![image-20230101230209764](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101230209764.png)

![image-20230101230224886](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101230224886.png)

* Statecharts also allow the decomposition of a model into sub-models (see figure on next slide).
* 状态图还允许将模型分解为子模型(参见下一张幻灯片中的图)。
* A brief description of the actions is included following the ‘do’ in each state (the word “do” is optional).
* 在每个状态的“do”后面都包含了对操作的简要描述(“do”是可选的)。
* Can be complemented by tables describing the states and the stimuli.
* 可以通过描述状态和刺激的表格来补充。？？？大概就是添加表格进行说明吧



对于图的详细解释

* The label on an arc can denote the method called to move from one state to the next (the event).
* 弧线上的标签可以表示从一个状态移动到下一个状态(事件)所调用的方法。
* A guard is used to ensure that the system only moves from one state to the other if the expression is satisfied.
* 保护用于确保只有在表达式满足时，系统才从一个状态移动到另一个状态。
* A state can contain a subdiagram within it (also called a composite state). This is useful for example when we wish to model a subsystem or substates.
* 状态中可以包含子图(也称为复合状态)。例如，当我们希望为子系统或子状态建模时，这是有用的。
* On the next slide, we can see all these elements of a UML statechart diagram

![image-20230101230928560](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101230928560.png)

#### 8. Actions

![image-20230101231008185](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101231008185.png)

![image-20230101231051876](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101231051876.png)

经常有一个空闲状态ldle state，进程不活跃

所有状态都需要一些出口(没有死锁，即使在错误条件下)

使用多个状态图来保持设计简单

不需要有一个状态图作为其他状态图的子状态

系统可以由多个状态机并发运行来描述

![image-20230101231244454](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101231244454.png)

#### 9. Finite State Machine 有限状态机

* Finite  State  Machines  (FSM),  also  known  as  Finite State Automata  (FSA)  are models  of the  behaviours 
  of  a  system  or  a  complex  object,  with  a  limited number  of  defined  conditions  or  modes,  where mode transitions change with circumstance.
* 有限状态机(FSM)，也称为有限状态自动机(FSA)是系统或复杂对象的行为模型，具有有限数量的已定义条件或模式，其中模式转换随环境而变化。

![image-20230101231521547](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101231521547.png)

![image-20230101231531019](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101231531019.png)

![image-20230101231542731](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101231542731.png)

## Lecture 8 System Model 2

![image-20230102104141726](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230102104141726.png)

### 1. Variants of FSMs (Finite State Machines )

* There are many variants, for instance, 
  * machines having actions (outputs) associated with transitions **(Mealymachine)** or states **(Moore** 
    **machine)**, 
  * 具有与**转换(Mealy机**)或**状态(Moore机)**相关联的动作(输出)的机器
* multiple start states, 
* 多重开始状态，
* transitions conditioned on no input symbol (a null) or more than one transition for a given symbol and state (**nondeterministic finite state machine**), 
* 转换以不输入符号(null)或给定符号和状态的多个转换为条件**(非确定性有限状态机**)，
* one or more states designated as accepting states (recognizer), etc.
* 一个或多个被指定为接受州的州**(识别器**)等。

![image-20230102100512628](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230102100512628.png)

![image-20230102100554056](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230102100554056.png)

#### 1.1 Moore Machine 摩尔机

https://blog.csdn.net/m0_61703043/article/details/125853828?ops_request_misc=&request_id=&biz_id=102&utm_term=%20Moore%20Machine&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduweb~default-0-125853828.142^

* Basically a Moore machine is just a FSA with two extra attributes. 
* Moore Machine 是一个FSA有两个额外属性
* \1. It has TWO alphabets, an input and output alphabet. 
* 它有两个字母，一个输入字母和输出字母。
* \2. It has an output letter associated with each state. The machine writes the appropriate output letter as it enters each state. 
* 它有一个输出字母与每个州相关联。机器在进入每一种状态时都写出相应的输出字母。

![image-20230112111236193](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230112111236193.png)

**<font color=red>上面这个图有点问题，四个输入应该有五个输出才对（这个是依照老师的课件，因为考试，所以我们参考老师的课件为准）</font>**

![image-20230102101335747](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230102101335747.png)

**Moore Machine的下一个状态取决于当前状态和当前输出，但其输出只取决于当前状态**

只能输出一个固定的值

![image-20230112111354766](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230112111354766.png)

![image-20230102101505275](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230102101505275.png)

#### 1.2 Mealy Machine 米利机

* Mealy machines are computationally equivalent to Moore machines 
  * (we can implement any Mealy machine using a Moore machine, and vice versa). 
  * 我们可以用摩尔机实现任何米利机，反之亦然
* However, Mealy machines move the output function from the state to the transition. This turns out to be easier to deal with in practice, making Mealy machines more practical. 
* 然而，Mealy机器将输出函数从状态移动到转换。这在实践中更容易处理，使Mealy机器更实用。

![image-20230102103850624](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230102103850624.png)

**<font color=red>Mealy Machine的输出与当前状态和输入都有关。</font>**

![image-20230102103914507](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230102103914507.png)

![image-20230102103921804](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230102103921804.png)

* Mealy machines are complete in the sense that there is a transition for each character in the input alphabet leaving every state. 
* Mealy机器是完整的，因为输入字母表中的每个字符离开每种状态都有一个过渡。
* There are no accept states in a Mealy machine because it is not a language recogniser, it is an output producer. **Its output will be the same length as its input.** 
* 在Mealy机器中没有接受状态，因为它不是语言识别器，而是输出生产者。**它的输出和输入的长度是一样的。**
* **可以注意到，Moore Machine的输入和输出长度不一样**

<font color='red'>这个和218要学的PDG很像</font>



### 2. Other System models

<font color=red>上面的两个也是系统模型</font>

#### 2.1 Petri Net Models petri网模型

* Petri Nets were developed originally by Carl Adam Petri (when he was 12), and were the subject of his dissertation in 1962. 
* 皮氏网最初是由卡尔·亚当·佩特里(当时他12岁)开发的，是他1962年论文的主题。
* Originally to model chemical reactions
* 最初是为了模拟化学反应
* Since then, Petri Nets and their concepts have been extended, developed, and applied in a variety of areas.
* 从那时起，Petri网及其概念得到了扩展、发展并应用于各种领域。
* While the mathematical properties of Petri Nets are interesting and useful, the beginner will find that a good approach is to learn to model systems by constructing them graphically.
* 虽然Petri网的数学特性是有趣和有用的，初学者会发现一个很好的方法是通过图形化构造系统来学习建模。



自己理解的方式

https://www.bilibili.com/video/BV18L411K7Sv/?spm_id_from=333.337.search-card.all.click&vd_source=9d046a6203dde4f5f1794bf980388e63

##### 2.1.1 Petri Net Models 构成元素



上课的PPT

![image-20230102104534739](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230102104534739.png)

![image-20230102105027525](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230102105027525.png)

1. **Arcs have capacity 1 by default;  弧的容量默认为1;**
2. **Places have infinite capacity by default.  默认情况下，地方的容量是无限的。**
3. **Transitions have no capacity 转换没有容量**

![image-20230102110128183](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230102110128183.png)

* 箭头只能连接places 和 transition 反之亦然
* 我们还将根据需要添加一些其他特性和注意事项。

##### 2.1.2 Enabled Transitions and Firing

![image-20230102105034985](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230102105034985.png)

<font color=red size=5>一个Transition是enabled的当每个input上的token的数量至少等于arc从place到transition的权重</font>

无论是上述图还是我所知道的图，**发现token可以在transition的过程中有所损失或者增加**，上图token由2-3，下图由2-1

![image-20230109084527778](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230109084527778.png)

<font color=red>这种情况被称为抑制 Inhibition, 这里的意思是当P1里有一个token时，这条路会被堵住</font>

![image-20230102105059528](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230102105059528.png)

![image-20230102105107110](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230102105107110.png)

![image-20230102105115600](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230102105115600.png)

![image-20230102111949404](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230102111949404.png)

* **Petri网是不确定的，因此可以用来模拟离散分布式系统。**

#### 2.2 Semantic Data Models 语义数据模型

* **Used to describe the logical structure of data** processed by the system
* 用于描述系统处理的数据的逻辑结构
* **Entity-relation-attribute  model** sets out the entities in the system, the relationships between these entities and the entity attributes
* 实体-关系-属性模型描述了系统中的实体，以及这些实体之间的关系和实体属性
* Widely used in database design. Can readily be implemented using relational databases
* 广泛应用于数据库设计。可以很容易地使用关系数据库实现
* No specific notation provided in the UML but objects and associations can be used
* UML中没有提供特定的符号，但是可以使用对象和关联
  * Class diagrams show some of the same ideas
  * 类图显示了一些相同的思想

![image-20230102112403734](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230102112403734.png)

**数据字典是系统模型中使用的所有名称的列表。**

![image-20230102112416786](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230102112416786.png)



#### 2.3 Object Models 物件模型

* **Object models describe the system in terms of object classes**
* **对象模型用对象类来描述系统**
* An object class is an abstraction over a set of objects with common attributes and the services (operations) provided by each object
* 对象类是一组具有公共属性的对象和每个对象提供的服务(操作)的抽象
* Various object models may be produced
  * Inheritance models 继承模型
  * Aggregation models 聚合模型
  * Interaction models 相互作用模型



* **Natural ways of reflecting the real-world entities manipulated by the system**
* **反映由系统操纵的现实世界实体的自然方式**
* **More abstract entities are more difficult to model using this approach**
* **更抽象的实体更难以使用这种方法建模**
* Object class identification is recognised as a difficult process requiring a deep understanding of the application domain
* 对象类识别被认为是一个困难的过程，需要对应用程序领域有深刻的理解
* Object classes reflecting domain entities are reusable across systems
* 反映域实体的对象类可以跨系统重用



#### 2.4 The Unified Modelling Language

* Devised by the developers of widely used object-oriented analysis and design methods
* 由开发人员设计并广泛使用的面向对象的分析和设计方法
* Has become an effective standard for **object-oriented modelling**
* 已成为面向对象建模的有效标准

![image-20230102113738312](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230102113738312.png)

![image-20230102113812047](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230102113812047.png)

* Notation for UML Class Diagrams:
  * Object classes are rectangles with the name at the top, attributes in the middle section and operations in the bottom section
  * 对象类是顶部有名称的矩形，中间部分有属性，底部部分有操作
  * Relationships between object classes (known as associations) are shown as lines linking objects
  * 对象类之间的关系(称为关联)显示为连接对象的行
  * Inheritance is referred to as generalisation and is shown ‘upwards’ rather than ‘downwards’ in a hierarchy
  * 继承被称为泛化，在层次结构中显示为“向上”而不是“向下”

## Lecture 9&10  Modelling Based on Petri Nets



### 1. High-Level Petri Nets

* High-level Petri nets are Petri nets extended with
  * **colour** (for the modelling of attributes)
  * **time** (for performance analysis)
  * **hierarchy** (for the structuring of models, DFD's) 

![image-20230102123323613](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230102123323613.png)

### 2. The Petri Nets

* Petri Nets can be used to rigorously define a system (reducing ambiguity, making the operations of a system clear, allowing us to prove properties of a system etc.)
* Petri网可以用来严格定义一个系统(减少歧义，使系统的操作清晰，允许我们证明系统的属性等)
* They are often used for **distributed systems** (with several subsystems acting independently) and for systems with resource sharing.
* 它们通常用于分布式系统(几个子系统独立工作)和资源共享的系统。
* Since there may be more than one transition in the Petri Net active at the same time (and we do not know which will ‘fire’ first), they are non-deterministic.
* 因为在Petri中可能有不止一个transition同时网络活跃(我们不知道哪个会先“开火”)，它们是不确定的。

![image-20230102123620762](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230102123620762.png)



* Another (equivalent) notation is to use a solid bar for the transitions:
* 也可以使用实心长方形代替transition
* We may use either notation since they are equivalent, sometimes one makes the diagram easier to read than the other..
* 我们可以使用任何一种符号，因为它们是等效的，有时一种比另一种更容易阅读图表。
* **The state of a Petri net is determined by the distribution of tokens over the places (we could represent the above state as (1,2,1,1) for (p1,p2,p3,p4))**
* **Petri网的状态是由标记在位置上的分布决定的(我们可以将上面的状态表示为(1,2,1,1)(p1, p2, p3, p4))**



#### 2.1 Transitions with Multiple Inputs and Outputs

![image-20230102124210113](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230102124210113.png)

#### 2.2 Enabling Condition

* Transitions are the active components and places and tokens are passive components.
* Transition是主动组件，places和token是被动组件。
* A transition is enabled if each of the input places contains tokens.
* 如果每个输入位置都包含token，则启用transition。

![image-20230102173842511](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230102173842511.png)

<font color='red'>只有当每一个作为input的Places都有一个token，Transition才被认为是enabling的（在箭头没有特别标注要求token的数量的时候，如果标注，则要达到要求的数量）</font>

#### 2.3 Firing

* An enabled transition may fire.
* 一个enabled 的transition可能是fire的
* **Firing corresponds to consuming tokens from the input places and producing tokens for the output places.**
* **Firing对应于从输入位置消费令牌并为输出位置产生令牌。**

![image-20230103080712654](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103080712654.png)

**Firing is atomic (only one transition fires at a time, even if more than one is enabled)**

**触发是原子的(一次只触发一个转换，即使启用了多个转换) 一次只能转换一个token**

![image-20230103080821054](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103080821054.png)

#### 2.4 Creating/Consuming Tokens

* **A transition without any input can fire at any time and produces tokens in the connected places:**
* **没有任何input的transition在任何时候都可以fire and 产生tokens 在与之连接的places上**

![image-20230103082510414](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103082510414.png)



* A transition without any output must be enabled to fire and deletes (or consumes) the incoming token(s):
* 没有任何输出的transition必须启用，以触发和删除(或消耗)传入token:

![image-20230103082706700](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103082706700.png)

#### 2.5 Non-Determinism in Petri Nets

![image-20230103082846141](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103082846141.png)

* Two transitions fight for the same token: conflict.
* 两个转换争夺同一个标记:冲突。
* Even if there are two tokens, there is still a conflict.
* 即使有两个令牌，仍然存在冲突。
* The next transition to fire (t1 or t2) is arbitrary (non-deterministic).
* 下一个转换到发射(t1或t2)是任意的(不确定的)。



### 3. Petri Net Modelling

* States of a process can be modelled by tokens in places and state transitions leading from one state to another are modelled by transitions.
* 流程的状态可以通过位置上的标记来建模，而从一个状态到另一个状态的状态转换可以通过转换来建模。



* Tokens can represent resources (humans, goods, machines), information, conditions or states of objects.
* Tokens可以表示资源(人、商品、机器)、信息、条件或对象的状态。
* Places represent buffers, channels, geographical locations, conditions or states.
* Places代表缓冲区、通道、地理位置、条件或状态。
* Transitions represent events, transformations or transportations.
* Transitions表示事件、转换或传输。

![image-20230103083541341](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103083541341.png)

![image-20230103083637998](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103083637998.png)

Example:

![image-20230103084748875](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103084748875.png)

![image-20230103084729923](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103084729923.png)

![image-20230103084814655](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103084814655.png)

<font color='red'>这个就是需要其他类型的资源safe才能进行转换</font>

![image-20230103085106802](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103085106802.png)



<font color='red'>为了保证公平，不让二者产生冲突，所以要如图所示，safe相当于锁的资源，red相当于亮起资源</font>

#### 3.1 Arcs in Petri Nets

![image-20230103090452629](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103090452629.png)

* The number of arcs between two objects specifies the number of tokens to be produced/consumed (we can alternatively represent this by writing a number next to a single arc).
* 两个对象之间的弧线数量指定了要产生/消费的令牌数量(**我们也可以通过在单个弧线旁边写一个数字来表示**)。
* This can be used to model (dis)assembly processes.
* 这可以用来建模(分解)组装过程。

![image-20230103090929563](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103090929563.png)

* **Current state** (also called current marking) - The configuration of tokens over the places.
* 当前状态(也称为当前标记)-位置上标记的配置。
* **Reachable state** - A state reachable form the current state by firing a sequence of enabled transitions.
* 可达状态——可达状态通过触发一系列已启用的转换形成当前状态。
* **Deadlock state - A state where no transition is enabled.**
* **死锁状态——没有启用转换的状态。**

![image-20230103091111359](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103091111359.png)

*  If we write the places in some fixed order (red, black say), then we can use a tuple: (n,m) to denote the number of tokens in each corresponding place (n tokens in “red” and m tokens in “black”).
*  如果我们以某种固定的顺序(比如红色，黑色)来写位置，那么我们可以使用元组:(n,m)来表示每个对应位置上的标记的数量(n个标记在“红色”中，m个标记在“黑色”中)。
*  The example below is thus in state (3,2). After firing transition “rr”, it will move to state (1,3) etc..
*  因此，下面的示例的状态为(3,2)。点火后转换“rr”，它将移动到状态(1,3)等。

![image-20230103091728797](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103091728797.png)

**注意，观察是以transition为基准， 比如br就是从red 和 black抽调两个，然后送一个到red里**

![image-20230103091812860](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103091812860.png)

#### 3.2 Example: The Four Seasons

![image-20230103092616843](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103092616843.png)



![image-20230103092631287](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103092631287.png)

![image-20230103092645816](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103092645816.png)



### 4. High-Level Petri Nets 高级Petri网络

* In practice, classical Petri nets have some modelling problems: 
* 在实践中，经典的Petri网存在一些建模问题: 
  * The Petri net becomes too large and too complex.
  * Petri网变得太大太复杂。
  * It takes too much time to model a given situation.
  * 建模一个给定的情况需要太多的时间
  * It is not possible to handle time and data.
  * 它不可能处理时间和数据。

Therefore, we use high-level Petri nets, i.e. Petri nets extended with:

* colour 颜色
* time 时间
* hierarchy 体系

 EXAMPLE：

![image-20230103140602968](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103140602968.png)

#### 4.1 The Extension with Colour

* A token often represents an object having all kinds of attributes.
* 一个token代表着一个具有各种属性的对象。
* Therefore, each token has a value (colour) with refers to specific features of the object modelled by the token.
* 因此，每个token都有一个值(颜色)，它指向由token建模的对象的特定特征。

![image-20230103141152212](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103141152212.png)

* Each transition has an (in)formal specification which specifies:
* 每个transition都有一个正式的规范，它指定
  * the number of tokens to be produced,  
  * 要生产的代币数量，
  * the values of these tokens,
  * 代币的价值
  * and (optionally) a precondition.
  * 还有(可选的)一个前提条件。
* The complexity is divided over the network and the values of tokens.
* 复杂度被分为高于神经网络和token的值
* This results in a compact, manageable and natural process description.
* 这就产生了一个紧凑的、可管理的和自然的过程描述。

![image-20230103142621062](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103142621062.png)



#### 4.2 The Extension with Time

![image-20230103142751001](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103142751001.png)

* To analyse performance, we must model durations, delays, etc.
* 为了分析性能，我们必须对持续时间、延迟
* A timed Petri net associates a pair tmin and tmax with each transition (there are other possible definitions for timed Petri net, but we shall only consider this one).
* 一个定时Petri网将一对tmin和tmax与每个转换关联起来(对于定时，还有其他可能的定义Petri网，但我们只考虑这一个)。
* <font color='red'>使用时间将每一个Transition连接起来</font>

![image-20230103143205492](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103143205492.png)

* The values tmin and tmax, tell us the minimum and maximum time that a transition will take to fire once enabled.
* tmin和tmax值告诉我们，一旦启用转换，触发转换所需的最小和最大时间。
* This allows us to model performance properties of the system, although the analysis of such systems may be more difficult.
* 这允许我们对系统的性能属性建模，尽管这样的系统的分析可能更加困难。

![image-20230103143727204](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103143727204.png)

最短用时是客户2，画个时间图就可以解。



#### 4.3 The Extension with Hierarchy

* A hierarchy is a mechanism to structure complex Petri nets comparable to Data Flow Diagrams.
* 层次结构是一种结构,结构复杂的Petri nets ,可与数据流程图相比较。
* A subnet is a net composed out of places, transitions and other subnets.
* 子网是由位置、过渡和其他子网组成的网络。
* This allows us to model a system at different levels of abstraction and can reduce the complexity of the model.
* 这允许我们在不同的抽象级别上对系统建模，并且可以降低模型的复杂性。
* We shall see an example of this on the next slide..
* 我们将在下一张幻灯片中看到一个例子。

![image-20230103170536196](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103170536196.png)

![image-20230103170556353](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103170556353.png)

**将复杂的流程简写，并且每一个流程存储到h中**



### 5. Another Example 

* Recall the following example of an informal specification from a critical system [1] :
* 回想一下从一个关键系统中一个非正式规范的示例
  * The message must be triplicated. The three copies must be forwarded through three different physical channels. The receiver accepts the message on the basis of a two-out-of-three voting policy.
  * 消息必须有三份。三份副本必须通过三个不同的物理通道转发。接收方根据三选二的投票策略接受消息。
* Questions: Can you identify any ambiguities in this specification?
* How could we model this system with a Petri net?

![image-20230103171059024](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103171059024.png)

P是接收方，在此进行投票选择，有三种可能。

![image-20230103171221308](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103171221308.png)

### 6. A Final Note on Petri Nets

* We can see from the previous example that the ambiguity (or impreciseness) in the informal specification for the message triplication protocol is clearly highlighted by the more formal Petri net model.
* 从前面的例子中可以看出,在更正式的皿化模式中明确地强调了信息三叠协议的非正式规范的模糊性(或不精确)。
* We can also perform some analysis on the model itself, for example to see if certain “bad” states ever occur or if deadlock/livelock is possible in the model.
* 我们还可以对模型本身进行一些分析,例如,看看是否有特定的“坏”状态发生,或者在模型中是否可能出现死锁/ livelock。
* Finally we can represent timing constraints (to encode even more constraints on the system) and use hierarchical models to show different levels of abstration.
* 最后,我们可以表示时间约束(对系统进行更多的约束),并使用层次模型来显示不同层次的抽象。

![image-20230103171917805](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103171917805.png)

![image-20230103171923921](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103171923921.png)





## Lecture 11 Formal Specifications



**Formal Specification - Techniques for the Unambiguous Specification of Software**

**明确软件规范的技术**

![image-20230103172858403](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103172858403.png)



### 1. Formal Methods 形式化方法



* **Formal specification** is part of a more general collection of techniques that are known as ‘formal methods’ 
* **形式化规范**是被称为“形式化方法”的更通用的技术集合的一部分。
* ![image-20230103173536249](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103173536249.png)
* Formal methods include 形式化方法
  * **Formal specification 正式规范**
  * **Specification analysis and proof 规范分析和证明**
  * **Transformational development  转换的发展**
  * **Program verification 程序验证**

#### 1.1 Formal Methods in reality 实际上的正式方法

* When software was first developed
  * It was done using assembly language 
  * 使用汇编语言书写
  * No OO, no high level languages
  * 没有高级语言
  * Limited understanding of software testing and testing tools
  * 对软件测试和测试工具了解有限
* Modern software development
  * Many ways to make high quality software
  * So 
    * Mostly formal methods not used
    * 很多formal没啥用了
    * The most acceptable techniques are approaches like programming by contract (e.g. Eiffel)
    * 最可接受的技术是契约式编程

![image-20230103175412871](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103175412871.png)

#### 1.2 Acceptance of Formal Methods 正式方法的接受

* Formal methods have not become mainstream software development techniques as was once predicted
* 形式化方法并没有像曾经预测的那样成为主流软件开发技术

![image-20230103175622317](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103175622317.png)

* **Other software engineering techniques have been successful at increasing system quality.** Hence the need for formal methods has been reduced
* 其他软件工程技术已经成功地提高了系统质量。因此，对形式化方法的需求已经减少
* Market changes have made time-to-market rather than software with a low error count the key factor. Formal methods do not reduce time to market
* 市场变化使得上市时间成为关键因素，而不是出错率低的软件。**形式化方法并不会缩短上市时间**
* **The scope of formal methods is limited.** They are not well-suited to specifying and analysing user interfaces and user interaction for example**
* 形式化方法的范围是有限的。例如，它们不适用于指定和分析用户界面和用户交互
* Formal methods are **hard to scale up to large systems**
* 形式化方法很难扩展到大型系统

#### 1.3 Use of Formal Methods 使用规范方法

* **Their principal benefits are in reducing the number of errors in systems so their main area of applicability is critical systems:**
* **它们的主要好处是减少系统中的错误数量，因此主要适用于关键系统:**
  * Air traffic control information systems,
  * 空中交通管制信息系统，
  * Railway signalling systems
  * 铁路信号系统
  * Spacecraft systems
  * 飞船系统
  * Medical control systems
  * 医疗控制系统
* In this area, the use of formal methods is most likely to be cost-effective
* 在这方面，使用形式化方法最有可能具有成本效益





### 2. Specification in the Software Process 软件过程中的规范

* **Specification and design are inextricably mixed.**
* **规格和设计不可分割地混合在一起。**
* **Architectural design** is essential to structure a specification.
* 建筑设计是结构规范的基础。
* **Formal specifications** are expressed in a mathematical notation with precisely defined vocabulary, syntax and semantics.
* 形式化规范用精确定义的词汇、语法和语义的数学符号表示。

#### 2.1 Specification Techniques

* **Algebraic approach 代数方法**
* The system is specified in terms of its operations and their relationships
* 系统是根据其**操作**及其**关系**来指定的
* **Model-based approach 基于模型的方法**
  * The system is specified in terms of a state model that is constructed using mathematical constructs such as sets and sequences. 
  * 系统是根据使用诸如**集合和序列等数学构造构造的状态模型**来指定的。
  * Operations are defined by **modifications to the system’s state**
  * 操作是通过修改系统状态来定义的

![image-20230103235247577](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103235247577.png)

#### 2.2 Use of Formal Specification

* Formal specification involves investing more effort in the early phases of software development 
* 正式的规范要求在软件开发的早期阶段投入更多的精力
  * This reduces requirements errors as it forces a detailed analysis of the requirements 
  * 这减少了需求错误，因为它迫使对需求进行详细的分析
* Incompleteness and inconsistencies can be discovered and resolved.
* 不完整和不一致可以被发现和解决
* Hence, savings are made as the amount of rework due to requirements problems is reduced
* 由于需求问题导致的返工量减少，从而节省了成本

![image-20230103235545033](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103235545033.png)

#### 2.3 Formal Specification 形式规范

* Critical systems development usually follows a software process based on the waterfall model.
* 关键系统开发通常遵循基于瀑布模型的软件过程。
* The system requirements and design are expressed in detail, reducing ambiguity, and carefully analysed and refined before implementation begins
* 系统需求和设计被详细地表达，减少了歧义，并在开始实施之前仔细分析和细化
* A large benefit of formal specification is its ability to uncover potential problems and ambiguities in the requirements.
* 形式化规范的一大好处是它能够发现需求中潜在的问题和不明确之处。

![image-20230103235842518](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103235842518.png)

#### 2.4 Interface Specification 接口规范

* Large systems are decomposed into subsystems with well-defined interfaces between these subsystems
* 大型系统被分解为子系统，这些子系统之间有良好定义的接口
* Specification of subsystem interfaces allows independent development of the different subsystems
* 子系统接口的规范允许不同子系统的独立开发
* Interfaces may be defined as abstract data types or object classes
* 接口可以定义为抽象数据类型或对象类

* **The algebraic approach to formal specification is particularly well-suited to interface specification**
* **形式化规范的代数方法特别适合于接口规范**



##### 2.4.1 Sub-System Interface Specification 子系统的接口规范

* Clear and unambiguous sub-system interface specifications reduce the chance of misunderstandings between a provider and user of a sub-system.
* 清晰明确的子系统接口规范可以减少子系统提供者和用户之间产生误解的机会。
* The algebraic approach to specification was originally developed for the definition of abstract data types.
* 用于规范的代数方法最初是为定义抽象数据类型而开发的。
* This idea was then extended to model complete system specifications.
* 这一思想随后被扩展到建模完整的系统规范。

![image-20230104000806436](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104000806436.png)



### 3. Algebraic Specification 代数规范

#### 3.1 The Structure of an Algebraic Specification

![image-20230104001215542](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104001215542.png)

* **Introduction** – Declares the sort (the type name) of the entity being specified, i.e., a set of objects with common characteristics. It also imports other specifications to use.
* 介绍--声明所指定实体的排序(类型名)，即具有共同特征的一组对象。它还导入其他规范来使用。
* **Description** – An informal description of the operations to aid understanding.
* 描述——对操作的非正式描述，以帮助理解。
* **Signature** – Defines the syntax of the interface to the abstract data type (object), including their names, parameter list and return types.
* 定义抽象数据类型(对象)的接口语法，包括它们的名称、参数列表和返回类型。
* **Axioms** – Defines the semantics of the operations by defining axioms characterising the behaviour.
* 通过定义表征行为的公理来定义操作的语义。

#### 3.2 Systematic Algebraic Specification

* Algebraic specifications of a system may be developed in a systematic way:
* 系统的代数规范可以以系统的方式发展
  * Specification structuring;  
  * Specification naming;
  * Operation selection; 
  * Informal operation specification;
  * Syntax definition;
  * Axiom definition.

![image-20230104001855183](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104001855183.png)



### 4. Specification Operations 规范操作

* **Constructor operations.** Operations which create entities of the type being specified.
* **构造函数的操作。**创建指定类型的实体的操作。
* **Inspection operations.** Operations which evaluate entities of the type being specified.
* 检查操作。对指定类型的实体求值的操作。
* To specify behaviour, define the inspector operations for each constructor operation.
* 要指定行为，请为每个构造函数操作定义检查器操作。

![image-20230104002200577](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104002200577.png)

![image-20230104002218473](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104002218473.png)

![image-20230104002226098](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104002226098.png)

![image-20230104002242060](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104002242060.png)

#### 4.1 A Sector Object

* Critical operations on an object representing a controlled sector are
* 对代表受控扇区的对象的关键操作为
  * Enter - Add an aircraft to the controlled airspace;
  * Leave - Remove an aircraft from the controlled airspace;
  * Move - Move an aircraft from one height to another;
  * Lookup - Given an aircraft identifier, return its current height;

![image-20230104002519419](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104002519419.png)

![image-20230104002539921](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104002539921.png)

![image-20230104002547860](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104002547860.png)

![image-20230104002554769](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104002554769.png)

![image-20230104002613548](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104002613548.png)



## Lecture 12 Formal Specifications 2

![image-20230104110851722](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104110851722.png)

### 1. Behavior Specification

* **Algebraic specification** can be cumbersome when the object operations are not independent of the object state
* 当对象操作不独立于对象状态时，代数规范可能很麻烦
* **Model-based specification** exposes the system state and defines the operations in terms of changes to that state
* 基于模型的规范公开了系统状态，并根据对该状态的更改定义了操作



### 2. Abstract State Machine Language (AsmL) 抽象状态机语言

* **AsmL is a language for modelling the structure and behaviour of digital systems. We will see a basic introduction to ASML and how someconcepts can be encoded formally.** 
* **AsmL是一种为数字系统的结构和行为建模的语言。**我们将了解ASML的基本介绍，以及如何对一些概念进行正式编码。
  *  (We will not go into too many details but just see the overall format ASML uses).
* AsmL can be used to faithfully capture the abstract structure and step wise behaviour of any discrete systems, including very complex ones such as:
* **AsmL可用于忠实地捕获任何离散系统的抽象结构和逐级行为，包括非常复杂的系统**，例如:
  * Integrated circuits  集成电路
  * Software components  软件组成
  * Devices that combine both hardware and software 结合硬件和软件的设备

![image-20230104113407618](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104113407618.png)

* An AsmL model is said to be abstract because it encodes only those aspects of the system’s structure that affect the behaviour being modelled
* **AsmL模型之所以被认为是抽象的，是因为它只对那些影响被建模行为的系统结构方面进行编码**
* The goal is to use the minimum amount of detail that accurately reproduces (or predicts) the behaviour of the system that we wish to model
* 目标是使用**最少的细节来精确地再现(或预测)我们希望建模的系统的行为**
* This means we may obtain an overview of the system without becoming bogged down in irrelevant implementation details and concentrate on important concerns such as concurrency.
* 这意味着我们可以获得系统的概述，而不会陷入不相关的实现细节，并将注意力集中在重要的问题上，如并发性。

![image-20230104114622931](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104114622931.png)



* Abstraction helps us reduce complex problems into manageable units and prevents us from getting lost in a sea of details
* 抽象有助于我们将复杂的问题简化为可管理的单元，并防止我们迷失在细节的海洋中
* AsmL provides a variety of features that allows us to describe the relevant state of a system in a very economical and high-level way 
* AsmL提供了多种特性，允许我们以一种非常经济和高级的方式描述系统的相关状态

![image-20230104114810247](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104114810247.png)

#### 2.1 Abstract State Machine and Turing Machines

* An abstract state machine is a particular kind of mathematical machine, like a Turing machine (TM)
* 抽象状态机是一种特殊的数学机器，就像图灵机(TM)。
* But unlike a TM, abstract state machines may be defined by a very high level of abstraction
* 但与TM不同的是，抽象状态机可以由非常高的抽象级别定义
* An easy way to understand ASMs is to see them as defining a succession of states that may follow an initial state
* 理解ASM的一种简单方法是将它们视为定义了初始状态之后的一系列状态

关于抽象的级别

![image-20230104115205116](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104115205116.png)

#### 2.2 Sets Described Algorithmically 集合描述算法

![image-20230104115340446](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104115340446.png)



### 3. Sequences

* A Sequence is a collection of elements of the same type, just as a set is but they differ from sets in two ways:
* Sequence是相同类型元素的集合，就像set一样，但它们与set有两个不同之处:
  * A sequence is ordered while a set is not.
  * 序列是有序的，而集合不是。
  * A sequence can contain duplicate elements while a set does not.
  * 序列可以包含重复的元素，而集合则不可以。

![image-20230104115718961](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104115718961.png)

![image-20230104115727007](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104115727007.png)

![image-20230104115814515](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104115814515.png)

![image-20230104115821658](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104115821658.png)

![image-20230104115835596](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104115835596.png)

![image-20230104115845901](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104115845901.png)



#### 3.1 快速排序

![image-20230104120005724](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104120005724.png)

![image-20230104120011299](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104120011299.png)

![image-20230104120018117](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104120018117.png)



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
  * In effect much of software is designed while coded and the design document doesn’t reflect the final product  实**际上，许多软件都是在编码的同时设计的，设计文档并不能反映最终的产品**

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
* **Repeat process for each identified abstraction**   对每个确定的抽象重复该过程
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
  * **autonomous,** 
  * **coherent and** 
  * **robust**

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

https://blog.csdn.net/elevenXL/article/details/2567861?ops_request_misc=&request_id=&biz_id=102&utm_term=Modular%20Continuity%20&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduweb~default-6-2567861.142^

* We can identify five criteria to help evaluate modular design methods:  我们可以确定五个标准来帮助评估模块化设计方法:
  * Modular decomposability模块化分解;
  * Modular composability;模块化组合;
  * Modular understandability;模块化的理解能力;
  * Modular continuity;模块化延续;
  * Modular protection.模块化保护

![image-20221204104419941](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204104419941.png)

![image-20230112174029450](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230112174029450.png)

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
* **The Numerical Algorithm Group (NAG)** libraries contain a wide range of routines for solving problems in linear algebra, differential equations, etc. 
* 数值算法组(NAG)库包含解决线性代数、微分方程等问题的广泛例程。
* **The Unix shell provides a facility called a pipe,** written “|”, whereby 
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



##### 3.6.4 Modular Continuity 模块可延续性 

* **Modular continuity** - a method satisfies this criterion if it leads to the production of software such that a small change in the problem specification leads to a change in just one (or a small number of ) modules.
* **模块化连续性**——如果一种方法，在由它得到的软件架构中，功能规格上的微小改动只会引起一个（或少量）模块的变化，那么该方法就满足模块连续性。
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
5. Many standard operations such as backup, security, access control, recovery and data integrity are centralised and can be controlled by a single repository manager.
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



## Lecture14 Design Methodology 2

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

* **A programming language (or design language) should support the principle of linguistic modular units:**
* **编程语言(或设计语言)应该支持语言模块化单元的原则:**
  * Modules must correspond to linguistic units in the language used
  * 模块必须与所使用语言中的语言单位相对应
* ![image-20221204125549362](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204125549362.png)

#### 2.2 Few Interfaces 几个接口

* This principle states that the overall number of communication channels between modules should be as small as possible:
* **这个原则指出模块之间的通信通道的总数应该尽可能小:**
  * Every module should communicate with as few others as possible.
  * 每个模块应该尽可能少地与其他模块通信。
* So, in the system with n modules, there may be a minimum of n(n-1) /2 and a maximumn n(n-1) /2 of links; your system should stay closer to the minimum.
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

### 5. Information Hiding (Encapsulation)  信息隐藏(封装)

* This principle states: 该原则指出:

  * **All information about a module, (and particularly how the module does what it does) should be private to the module unless it is specifically declared otherwise.** 
  * **关于模块的所有信息(特别是模块如何做它所做的事情)都应该是模块私有的，除非特别声明了。**

* Thus each module should have an interface, which is how the world sees it anything beyond that interface should behidden.  There is a limit to how much humans canunderstand at any one time. 

* 因此，每个模块都应该有一个接口，这是世界看到它的方式，任何超出该接口的东西都应该在后面。人类在任何时候所能理解的东西都是有限的。

* The default Java rule: 默认的Java规则:

  * Make everything private 让一切都私人化

  ![image-20221204161234182](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221204161234182.png)

**<font color='blue'>锐评，private声明</font>**

### 6. Cohesion 内聚性

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

### 7. Lecture Key Points

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

* **Personal  systems**  that  are  not  distributed  and  that  are designed to run on a personal computer or workstation. 
* **个人系统**不是分布式系统并且被设计于个人电脑或者工作机上
* **Embedded systems** that run on a single processor or on an integrated group of processors. 
* **嵌入式系统**运行在单个的处理器或者集成的处理器组上
* **Distributed systems** where the system software runs on a loosely integrated group of cooperating processors linked by a network.  
* **分布式系统**的系统软件运行在由网络连接的一组松散集成的协作处理器上。

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

#### 1.5 Middleware 中间件

* Software that manages and supports the different components of a distributed system. In essence, it sits in the middle of the system
* 管理和支持分布式系统的不同组件的软件。**本质上，它位于系统的中间**
*  Middleware is usually off-the-shelf rather than specially written software
* 中间件通常是现成的，而不是专门编写的软件
* Examples
  * Transaction processing monitors
  * 事务处理监控器
  * Data converters
  * 数据变换器
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

* **There is no distinction in a distributed object architectures between clients and servers**
* **在分布式对象体系结构中，客户机和服务器之间没有区别**
* Each distributable entity is an object that 
  * provides services to other objects and 
  * receives services from other objects
* **每个可分发实体都是一个对象**
  * **为其他对象提供服务**
  * **接收来自其他对象的服务**
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
  *  例如:作为对象对接收消息的反应的一部分
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
* An object can also send to itself any message which it is capable of understanding (in either its public or private interface)
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
* objects with the same data structure (attributes) and behaviour (operations) are grouped into a class
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

  * **Use case models** – describing a system from the users’ point of view;
  * 用例模型——从用户的角度描述系统
  * **Static models** – describing the elements of the system and their relationship; class models fall into this category;
  * 静态模型——描述系统元素及其关系；类模型属于这一类
  * **Dynamic models** – describing the behaviour of the system over time.
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
* Aggregation and **composition** are both ways of recording that an object of one class is part of an object of another class.
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

* **A Class diagram shows the static structure of the system.**
* **类图显示了系统的静态结构**
* It defines model elements such as classes, interfaces, and user-defined data types, their internal structure, and their relationships to each other.
* 它定义了模型元素，例如类、接口和用户定义的数据类型、它们的内部结构以及它们之间的关系。
* Relationships, or associations, are shown as lines connecting elements, and are annotated to describe the relationships and their cardinality (1..1, 1..*, 0..*, etc.).
* 关系或关联显示为连接元素的线，并进行注释以描述关系及其基数（1..1、1..*、0..*等）。
* Inheritance (generalize/specialize), aggregation (comprises), and composition (has) relationships are also captured in this diagram.
* 继承（泛化/专用）、聚合（包含）和组合（具有）关系也在该图中捕获。

![image-20221206184316137](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221206184316137.png)



### 5.  Collaborations 协作

* **UML provides two sorts of interaction diagram, UML提供了两种交互图**
  * **sequence diagrams and** 
  * **序列图**
  * **collaboration diagrams.**
  * **协作图**
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
  * **Activity 活动**
  * **Transition 过渡**
  * **Synchronization bar 同步栏**
  * **Decision diamond 决策菱形**
  * **Start and stop markers 启动和停止标记**

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



# **Validation and testing**

## Lecture 22 Verification and Validation

Ensuring that a software system meets a user's needs

确保软件系统满足用户的需求

![image-20230105165416643](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230105165416643.png)



### 1. Verification vs Validation

* **Verification should check the program meets its specification as written in the requirements document for example.**
* **Verification应该检查程序是否符合需求文档中所写的规范。**
  * This may involve checking that it meets it functional and non-functional requirements
  * 这可能涉及检查它是否满足其功能性和非功能性需求
* **Validation ensures that the product meets the customers expectations**
* **Validation确保产品满足顾客的期望**
  * This goes beyond checking it meets its specification; as we have seen, system specifications don’t always accurately reflect the real needs of users
  * 这不仅仅是检查它是否符合规格;正如我们所看到的，系统规格并不总是准确地反映用户的真实需求

#### 1.1 The Verification & Validation Process

* As a whole life-cycle process - V & V must be applied at each stage in the software process.
* 作为一个完整的生命周期过程- V & V必须应用于软件过程的每个阶段。
* Has two principal objectives
  * **The discovery of defects in a system**
  * **发现现在的缺陷**
  * **The assessment of whether or not the system is usable in an operational situation.**
  * **评估系统是否可用**

#### 1.2 Static(Software inspections) and Dynamic Verification（**Software testing** ）

* **Software inspections**  Concerned with analysis of the static system representation to discover problems  **(static verification)**
* **软件检查**涉及对静态系统表示的分析，以发现问题**(静态验证)**
  * May be supplement by tool-based document and code analysis
  * 可以通过基于工具的文档和代码分析来补充
* **Software testing**  Concerned with exercising and observing product behaviour (dynamic verification)
* **Software testing 关注执行和观察产品行为(动态验证)**
  * The system is executed with test data and its operational behaviour is observed
  * 使用测试数据执行系统，并观察其运行行为

![image-20230105170346018](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230105170346018.png)

* **System testing** is only possible when an executable version of the program is available
* 只有当程序的可执行版本可用时，才可能进行**系统测试**
* This is therefore an advantage of incremental development since a testable version of the system is available at a fairly early stage
* 因此，这是增量开发的一个优势，因为系统的可测试版本在相当早的阶段就可用了
* New functionality can be checked as it is added to the system and we can perform regression testing (we will talk about this in a few slides time)
* 新功能可以在添加到系统时进行检查，我们可以执行回归测试(我们将在几张幻灯片中讨论这个问题)
* **Real data** can be used as input to the system and we try to observe any anomalies in the output
* **实际数据**可以作为系统的输入,我们试图观察输出中的任何异常

![image-20230105170636346](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230105170636346.png)



#### 1.3 Program Testing 程序测试

* **Can reveal the presence of errors NOT their absence !!!**
* **可以揭示错误的存在，而不是他们的缺席!!**
* A successful test is a test which discovers one or more errors
* 成功的测试是发现一个或多个错误的测试
* **Program testing is the only validation technique for non-functional requirements**
* **程序测试是非功能性需求的唯一验证技术**
* Should be used in conjunction with static verification to provide full V&V coverage
* 是否应与静态验证一起使用以提供完整的V&V覆盖



#### 1.4 Testing with Agile (XP and SCRUM) 敏捷测试

* Development is test driven
* 开发是测试驱动的
* Test developed before target code
* 在目标代码之前进行测试开发
* Target code developed to pass test
* 开发目标代码以通过测试
* **Benefits**
  * **Test is more valid, based purely on specification**
  * **测试更有效，纯粹基于规范**
  * **Code is always tested**
  * **代码总是经过测试的**
  * **Code is often simpler and closer to specification**
  * **代码通常更简单，更接近规范**
* TDD see comp220 comp285 for more details...

#### 1.5 Types Of Testing

* **Defect testing 缺陷测试**
  * Tests designed to discover system defects.
  * 设计用于发现系统缺陷的测试。
  * A successful defect test is one which reveals the presence of defects in a system.
  * 一个成功的缺陷测试是揭示系统中存在缺陷的测试。
* **Statistical testing 统计检验**
  * Tests designed to reflect the frequency of user inputs. Used for reliability estimation.
  * 旨在反映用户输入频率的测试。用于可靠性估计。

#### 1.6 Verification & Validation Goals

* **Verification and validation should establish a degree of confidence that the software is fit for purpose**
* **验证和确认应该建立一定程度的信心，使软件适合于目的**

* **This does NOT mean completely free of defects**
* **这并不意味着完全没有缺陷**
* The degree of confidence required depends upon several different factors as we see on the next slide
* 所需要的自信程度取决于几个不同的因素，我们在下一张幻灯片中看到

![image-20230105171951776](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230105171951776.png)

* Verification & Validation Goals
* **Software function** – A much higher level of confidence that the system is fit for purpose is required for safety critical systems that for prototype systems for example
* **软件功能**——对于安全关键系统(例如原型系统, 重要的系统)，需要对系统是否适合目的有更高的信心
* **User expectations** – Users sometimes have a low expectation of software and are willing to tolerate some system failures (although this is decreasing)
* **用户期望**——用户有时对软件的期望很低，并且愿意容忍一些系统故障(尽管这种情况正在减少)。
* **Marketing environment** – Competing programs must be taken into account and the required schedule for introducing the product to market. Cheaper products may be expected to have more faults.
* **营销环境**-必须考虑到竞争项目和将产品推向市场所需的时间表。更便宜的产品可能会有更多的缺陷。

#### 1.7 Testing and Debugging

* **Defect testing and debugging are distinct processes**
* **缺陷测试和调试是不同的过程**
* (!) Verification and validation is concerned with establishing the existence of defects in a program
* 验证和确认所涉及的是确定程序中缺陷的存在![image-20230105172442411](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230105172442411.png)
* (!!) Debugging involves  调试包括
  * formulating a hypothesis about program behaviour 
  * 制定一个关于程序行为的假设
  * then testing these hypotheses to find the system error
  * 然后对这些假设进行检验，找出系统误差



#### 1.8 Testing and Debugging 测试与调试

* There is no simple process for debugging and it often involves looking for patterns in test outputs with defects and using a programmers skill to locate the error

* 调试没有简单的过程，它经常涉及到在带有缺陷的测试输出中寻找模式，并使用程序员的技能来定位错误

* Question: Recall the programs you have written in Java for example so far. Were there errors in early versions? How did you discover them and fix them? Were they syntactic or semantic errors?

* 问:回想一下你写过的程序

  以Java为例。早期版本有错误吗?你是如何发现并修复它们的?

  是句法错误还是语义错误?

* Interactive debuggers provide a special run-time environment with access to the symbol table and program variables to aid error location. You can also “step-through” the program line by line

* 交互式调试器提供了一个特殊的运行时环境，可以访问符号表和程序变量，以帮助定位错误。你也可以逐行执行程序

![image-20230106001500524](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106001500524.png)

##### 1.9 Syntax and Semantic Errors 语法和语义错误

* **A syntax error** should be caught by the compiler which will (usually) indicate the location the error occurred in and the type of error.
* **语法错误应该被编译器捕获**，编译器(通常)会指出错误发生的位置和错误的类型。
* <font color=red>idea上出现红色下划线的部分</font>
* **A semantic error** (also called a logical error) can occur in a program which compiles and runs, but produces incorrect output on some (or all) input (e.g. An incorrect algorithm or mistake in a formulae etc.)
* **语义错误(也称为逻辑错误)**可能
* 发生在编译和运行的程序中，但在某些(或全部)输入上产生不正确的输出。不正确的算法或公式中的错误。)
* <font color='red'>由于逻辑问题产生的不正确的输出</font>
* Semantic errors are often harder to detect since the compiler may not be able to indicate where/what the problem is.
* 语义错误通常更难检测，因为编译器可能无法指出问题在哪里/是什么。

#### 1.8 Testing and Debugging 测试与调试

* Once errors are located, it is necessary to correct the program code and re-test the program
* 一旦发现了错误，就必须纠正程序代码并重新测试程序
* **Regression testing** – after fixing a defect, it is advisable to retest the program with all previous test data to make sure the “fix” has not introduced new problems
* **回归测试——在修复了一个缺陷之后，建议使用所有之前的测试数据重新测试程序，以确保“修复”没有引入新的问题**
  * This is not always feasible due to costs
* Experience has shown that a large proportion of fault repairs introduce new errors or are incomplete
* 经验表明，很大比例的故障修复引入了新的错误或不完整

![image-20230106003512870](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106003512870.png)



#### 1.10 Verification and Validation Planning

* **Careful planning is required to get the most out of testing and inspection processes**
* **为了充分利用测试和检查过程，需要进行仔细的计划**
* Planning should start early in the development process
* 计划应该在开发过程的早期开始
* **The plan should identify the balance between static verification and testing**
* **该计划应该确定静态验证和测试之间的平衡**
* Test planning is about defining standards for the testing process rather than describing product tests\
* 测试计划是定义测试过程的标准，而不是描述产品测试

![image-20230106004110929](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106004110929.png)

**<font color=red>写的时候一步步测，写完实际用再一步步测</font>**

#### 1.11 The Structure of a Software Test Plan

* **Test recording procedures** – The results of tests must be systematically recorded, it is not enough to simply run the tests. This allows an audit of the testing process to check it has been carried out correctly (imagine a safety critical system; procedures for auditing the tests are often necessary)
* **测试记录程序**——必须系统地记录测试结果，仅仅运行测试是不够的。这允许对测试过程进行审计，以检查它是否正确执行(想象一个安全关键系统;审计测试的程序通常是必要的)
* **Hardware and software requirements** – This part of the document sets out a list of software tools required and the estimated hardware utilisation
* **硬件和软件要求**-这部分文件列出所需的软件工具清单，以及估计的硬件使用率
* **Constraints** – Any constraints affecting the testing process should be anticipated in this section
* **约束**——任何影响测试过程的约束都应该在本节中预测到

#### 1.12 Software Inspections 软件检查

* **Involve people examining the source representation with the aim of discovering anomalies and defects**
* **让人们检查源代码表示，目的是发现异常和缺陷**
* Does not require execution of a system so it may be used before the implementation phase
* 不需要执行一个系统，所以它可以在实现阶段之前使用
* May be applied to any representation of the system (requirements, design, test data, etc.)
* 可适用于任何系统的表示(需求、设计、测试数据等)
* Very effective technique for discovering errors
* 非常有效的发现错误的技术

![image-20230106005537808](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106005537808.png)

* Incomplete versions of the system can be inspected without additional costs – specialised test harnesses that work on only a part of the program are not required
* 不完整版本的系统可以检查，而不需要额外的费用-专门的测试工具，只工作在程序的一部分
* As well as program defects, inspections can consider broader quality attributes such as compliance with standards, portability and maintainability
* 除了程序缺陷，检查还可以考虑更广泛的质量属性，如符合标准、可移植性和可维护性
* Poor programming style and inefficiencies can be found which could make the system difficult to maintain and update
* 糟糕的编程风格和低效率可能会使系统难以维护和更新



#### 1.13 Inspection Success 检查成功

* **Many different defects** may be discovered in a single inspection, there is no “interaction” between errors to be concerned with. In testing, one defect, may mask another, so several executions are required
* 在一次检查中可以发现许多不同的缺陷，错误之间没有相互作用需要考虑。在测试中，一个缺陷可能会掩盖另一个缺陷，因此需要多次执行
* **They reuse domain and programming knowledge** so reviewers are likely to have seen the types of error that commonly arise
* 它们重用领域和编程知识，因此审查人员很可能已经看到了常见的错误类型



* Inspections and testing are complementary and not opposing verification techniques
* 检查和测试是互补的，而不是对立的验证技术
* Both should be used during the V & V process
* 在V & V过程中两者都应使用
* Inspections can check conformance with a specification but not conformance with the customer’s real requirements
* 检验可以检查是否符合规格，但不符合客户的实际要求
* Also inspections cannot check non-functional characteristics such as performance, usability, etc. (Emergent properties).
* 此外，检查不能检查非功能特征，如性能、可用性等。(紧急属性)。

![image-20230106010313144](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106010313144.png)

![image-20230106010407704](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106010407704.png)



## Lecture 23 Software Testing 1

 Defect Testing

* **Defect testing involves testing programs to establish the presence of system defects**
* **缺陷测试包括测试程序来确定系统缺陷的存在**

![image-20230106144324841](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106144324841.png)

![image-20230106144406410](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106144406410.png)

### 1. The Test Process 测试过程

* Component testing 
* 元件测试
  * Testing of individual program components
  * 独立程序原件的测试
  * Usually the responsibility of the component developer (except sometimes for critical systems)
  * 通常是组件开发人员的责任(有时关键系统除外)
  * Tests are derived from the developer’s experience
  * 测试源自开发人员的经验
* Integration testing
* 集成测试
  * Testing of groups of components integrated to create a system or sub-system
  * 为创建系统或子系统而集成的组件组的测试
  * The responsibility of an independent testing team
  * 测试团队的责任
  * Tests are based on a system specification
  * 测试基于系统规范

### 2. Defect Testing 缺陷测试

* The goal of defect testing is to discover defects in programs
* 缺陷测试的目标是发现程序中的缺陷
* A successful defect test is a test which causes a program to behave in an anomalous way
* 一个成功的缺陷测试是一个导致程序以一种异常的方式行事的测试
* Tests show the presence not the absence of defects
* 测试显示缺陷的存在，而不是没有



#### 2.1 Testing Priorities 测试的优先级

* Only exhaustive testing can show a program is free from defects. However, exhaustive testing is impossible
* 只有详尽的测试才能显示程序没有缺陷。然而，**彻底的测试是不可能的**
* Tests should exercise a system's capabilities rather than its components
* 测试应该测试系统的功能，而不是它的组件
* Testing old capabilities is more important than testing new capabilities
* 测试旧功能比测试新功能更重要
* Testing typical situations is more important than boundary value cases
* 测试典型情况比测试边界值情况更重要

#### 2.2 Test Data and Test Cases 测试数据和测试情况

* Test data  Inputs which have been devised to test the system
* 测试数据用于测试系统的输入
* Test cases  Inputs to test the system and the predicted outputs from these inputs if the system operates according to its specification
* 测试用例的输入是为了测试系统，如果系统按照其规范运行，则测试这些输入的预测输出

![image-20230106150021870](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106150021870.png)

![image-20230106150037748](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106150037748.png)



### 3. Black-Box Testing 黑箱测试

https://blog.csdn.net/weixin_43950588/article/details/108550652?ops_request_misc=&request_id=&biz_id=102&utm_term=%E9%BB%91%E7%AE%B1%E6%B5%8B%E8%AF%95&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduweb~default-1-108550652.142^

![image-20230106151541432](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106151541432.png)

* 
* **The program test cases are based on the system specification** 
* **程序测试用例基于系统规范**
* **Test planning can begin early in the software process**
* **测试计划可以在软件过程的早期开始**

![image-20230106151034049](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106151034049.png)

#### 3.1 Equivalence Partitioning 等价的划分

* Input data and output results often fall into different classes where all members of a class are related
* 输入数据和输出结果通常属于不同的类，类的所有成员都是相关的
* **Each of these classes is an equivalence partition where the program behaves in an equivalent way for each class member**
* **这些类中的每一个都是一个等价分区，其中程序对每个类成员的行为都是等价的**
* Test cases should be chosen from each partition
* 应该从每个分区中选择测试用例
* An approach to testing where the program is considered as a ‘black-box’
* 一种测试程序被认为是“黑盒”的方法

* Partition system inputs and outputs into ‘equivalence sets’ 

* 划分系统输入和输出的“等效集”

  * If input is a 5-digit integer between 10,000 and 99,999, equivalence partitions are <10,000, 10,000-99, 999 and > 10, 000

  * 如果输入的是10000 ~ 99999之间的5位整数，则等价分区分别为小于10000,10000 ~ 99999和大于

    10000

* Choose test cases at the boundary of these sets

* 在这些集合的边界处选择测试用例

  * 00000, 09999, 10000, 99999, 10001

* These are more likely to display erroneous behaviour than choosing random values

* 这比选择随机值更容易显示错误行为

* <font color='red'> 因为边界值更容易出现错误情况</font>

![image-20230106151952803](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106151952803.png)

![image-20230106152009441](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106152009441.png)

![image-20230106152212629](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106152212629.png)

**IPUT可能出现的各种情况**

##### 3.2.1 Boudary Test and Partition Testing 边界测试和等价划分测试

<font color='red' size=5> 感觉这方面有点问题，关于等价类的划分</font>

强行解释一下的话，就是一个是取极端值来针对边界情况，一个是使用等价划分来寻找代表值减少成本。

![image-20230108111243124](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230108111243124.png)

![image-20230108111306941](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230108111306941.png)

#### 3.2 Testing Guidelines (Sequences) 测试指引

* Test software with sequences which have only a single value
* 用只有一个值的序列测试软件
* Use sequences of different sizes in different tests
* 在不同的测试中使用不同大小的序列
* Derive tests so that the first, middle and last elements of the sequence are accessed
* 派生测试,以便访问序列的第一个、中和最后一个元素
* Test with sequences of zero length  
* 用零长度的序列进行测试

**<font color='red'>根据经验的一些容易出现问题的测试情况</font>**

![image-20230106152515300](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106152515300.png)

### 4. Structural Testing 结构测试 white-box testing 白箱测试

* Sometime called white-box testing
* 有时被称为白盒测试
* **Derivation of test cases according to program structure. Knowledge of the program is used to identify additional test cases**
* **根据程序结构推导测试用例。程序的知识被用来识别额外的测试用例**
* Objective is to exercise all program statements (not all path combinations)
* 目标是练习所有的程序语句(不是所有的路径组合)

![image-20230115105107347](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230115105107347.png)

![image-20230106153545444](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106153545444.png)

![image-20230106153553036](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106153553036.png)

![image-20230106153603656](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106153603656.png)

![image-20230106153610497](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106153610497.png)

![image-20230106153617742](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106153617742.png)

#### 4.1 Path Testing 路径测试

* **The objective of path testing is to ensure that the set of test cases is such that each path through the program is executed at least once**
* **路径测试的目标是确保测试用例的集合是这样的,通过程序的每一条路径至少执行一次**
* The starting point for path testing is a program flow graph that shows nodes representing program decisions and arcs representing the flow of control
* 路径测试的起点是一个程序流图,它显示表示程序决定的节点和表示控制流的arcs
* Statements with conditions are therefore nodes in the flow graph
* 因此,条件中的语句是流图中的节点

![image-20230106153801636](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106153801636.png)

* Describes the program control flow. Each branch is shown as a separate path and loops are shown by arrows looping back to the loop condition node
* 描述了程序的控制流程。每个分支都显示为单独的路径，循环由循环回循环条件节点的箭头显示
* Used as a basis for computing the cyclomatic complexity
* 用于计算圈复杂度
* **<font color=red>Cyclomatic complexity</font> = “Number of edges - Number of nodes + 2” in the program control flow graph**
* **程序控制流图中的圈复杂度=“边数-节点数+ 2”**

#### 5.1 Cyclomatic Complexity 圈复杂度

* The number of tests to test all control statements equals the cyclomatic complexity
* 测试所有控制语句的测试数等于圈复杂度
* **Cyclomatic complexity equals the number of conditions in a program plus one.**
* **圈复杂度等于程序中的条件数加一。**
* Useful if used with care. Does not imply adequacy of testing. 
* 小心使用很有用。并不意味着测试足够。
* Although all paths are executed, all combinations of paths are not executed
* 虽然执行了所有路径，但并不执行所有路径的组合

![image-20230106154144370](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106154144370.png)



## Lecture24  Software Testing 2

https://blog.csdn.net/huangjinjin520/article/details/121112719?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522167302817716800186523250%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=167302817716800186523250&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_positive~default-1-121112719-null-null.142

### 1. Cyclomatic Complexity

* **The number of tests to test all control statements equals the cyclomatic complexity**
* **测试所有控制语句的测试次数等于圈复杂度**
* **Cyclomatic complexity** equals number of conditions in a program plus one  (or equivalently, in the program flow graph it is the “Number of edges - Number of nodes +2”)
* 圈的复杂度等于程序中的条件数+ 1(或等价),在程序流图中是“边数-节点+ 2”)
* **Conditions** are any type of branching operation such as each “if” statement or any types of loop (for, while etc.)
* 条件是任何类型的分支操作，如每个“if”语句或任何类型的循环(for, while等)。
* Useful if used with care. Does not imply adequacy of testing. Although all paths are executed, all combinations of paths are not executed
* 小心使用很有用。并不意味着测试足够。虽然执行了所有路径，但并不执行所有路径的组合

![image-20230106180115553](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106180115553.png)

![image-20230106180227696](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106180227696.png)



#### 1.1 Independent Paths 独立路径

* Independent paths introduce new nodes into test...
* 独立路径将新节点引入测试…
* 1,2,8,9 // new nodes 1,2,8,9
* 1, 2, 3, 8, 9 // new nodes 3
* 1, 2, 3, 4, 5, 7, 2,8,9 // new nodes 4,5,7
* 1, 2, 3, 4, 6, 7, 2,8,9 // new nodes 6
* Test cases should be derived so that all of these paths are executed
* 应该导出测试用例，以便执行所有这些路径
* A dynamic program analyser may be used to check that paths have been executed
* 动态程序分析器可用于检查路径是否已执行

#### 1.2 Integration Testing 集成测试

* Integration testing - tests complete systems or subsystems composed of integrated components
* **集成测试——测试由集成组件组成的完整系统或子系统**
* Integration testing should be black-box testing with tests derived from the specification
* 集成测试应该是使用来自规范的测试的黑盒测试
* Main difficulty is localising errors
* 主要困难在于定位错误
* Incremental integration testing reduces this problem
* 增量集成测试减少了这个问题

![image-20230106200024991](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106200024991.png)

#### 1.3 Incremental Integration Testing 增量集成测试

* Note that incremental integration as on the previous slide uses the idea of regression testing, i.e., future tests also test previous test cases again.
* 请注意，前面幻灯片上的增量集成使用了回归测试的思想，即，未来的测试也会再次测试之前的测试用例。
* **As a new module is added, we not only run a new test, we also make sure the addition of the new module does not “break” the previous test cases.**
* **当添加一个新模块时，我们不仅要运行一个新的测试，还要确保不添加新模块“打破”之前的测试用例。**
* This can sometimes by done automatically by using a test harness (a program written to automatically generate test data and record their results). [See Junit for Java if you are interested in this.]
* 这有时可以通过使用测试工具(自动生成测试数据并记录测试结果的程序)自动完成。[如果您对此感兴趣，请参阅Junit for Java。]

![image-20230106201004749](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106201004749.png)



#### 1.4 Approaches to Integration Testing 集成测试方法

* Top-down testing 自上而下的测试
  * Start with high-level system and integrate from the top-down replacing individual components by stubs where appropriate
  * 从高级系统开始，从上到下集成，在适当的地方用存根替换单个组件
* Bottom-up testing 自下而上测试
  * Integrate individual components in levels until the complete system is created
  * 在关卡中整合各个组件，直到创建完整的系统
* In practice, most integration involves a combination of these strategies
* 在实践中，大多数集成涉及这些策略的组合

![image-20230106201359853](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106201359853.png)

![image-20230106201419709](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106201419709.png)

##### 1.4.1 For which types of system is bottom-up testing appropriate, and why?自底向上测试适合于哪种类型的系统，为什么?

* **Object-oriented systems** – because these have a neat decomposition into classes and methods – makes testing easy
* **面向对象的系统**——因为这些系统对类和方法进行了简洁的分解——使得测试变得很容易
* **real-time systems** – because we can identify slow bits of code more quickly
* **实时系统**——因为我们可以更快地识别慢代码
* **systems with strict performance requirements** – because we can measure the performance of individual methods early in the testing process
* **具有严格性能要求的系统**——因为我们可以在测试过程的早期测量单个方法的性能

![image-20230106201700391](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106201700391.png)

#### 1.5 Testing Approaches

* Architectural validation 架构的确认
  * Top-down integration testing is better at discovering errors in the system architecture
  * 自顶向下集成测试更善于发现系统架构中的错误
* System demonstration 系统论证
  * Top-down integration testing allows a limited demonstration at an early stage in the development
  * 自顶向下集成测试允许在开发的早期阶段进行有限的演示
* Test implementation
  * Often easier with bottom-up integration testing
  * 自底向上的集成测试通常更容易
* Test observation
  * Problems with both approaches. Extra code may be required to observe tests
  * 两种方法都存在问题。观察测试可能需要额外的代码

### 2.Interface Testing 接口测试

* Takes place when modules or sub-systems are integrated to create larger systems
* 当模块或子系统被集成以创建更大的系统时发生
* Objectives are to detect faults due to interface errors or invalid assumptions about interfaces
* 目标是检测由于接口错误或对接口的无效假设而导致的故障
* Particularly important for object-oriented development as objects are defined by their interfaces
* 对于面向对象的开发尤其重要，因为对象是由它们的接口定义的

![image-20230106202803199](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106202803199.png)

![image-20230106202846242](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106202846242.png)

#### 2.1 Interfaces Types 接口类型

* Parameter interfaces 参数接口
  * Data passed from one procedure to another
  * 从一个过程传递到另一个过程的数据
* Shared memory interfaces 共享内存接口
  * Block of memory is shared between procedures
  * 内存块在过程之间共享
* Procedural interfaces 过程接口
  * Sub-system encapsulates a set of procedures to be called by other sub-systems
  * 子系统封装了一组由其他子系统调用的过程
* Message passing interfaces 消息传送接口
  * Sub-systems request services from other sub-systems

![image-20230106203335152](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106203335152.png)

#### 2.2 Interface Errors 接口错误

* **Interface misuse  接口误用**
  * A calling component calls another component and makes an error in its use of its interface e.g. parameters in the wrong order
  * 一个调用组件调用另一个组件时，在接口的使用上犯了一个错误，例如参数的顺序错误
* **Interface misunderstanding 接口误解**
  * A calling component embeds assumptions about the behaviour of the called component which are incorrect
  * 调用组件嵌入了关于被调用组件行为的不正确假设
* **Timing errors 时间错误**
  * The called and the calling component operate at different speeds and out-of-date information is accessed
  * 被调用组件和调用组件以不同的速度运行，并且会访问过时的信息



#### 2.3 Interface Testing Guidelines 接口测试指导

* Design tests so that parameters to a called procedure are at the extreme ends of their ranges
* 设计测试，使被调用过程的参数处于其范围的极端
* Always test pointer parameters with null pointers
* 总是用空指针测试指针参数
* Design tests which cause the component to fail
* 设计导致组件失败的测试
* Use stress testing in message passing systems
* 在消息传递系统中使用压力测试
* In shared memory systems, vary the order in which components are activated
* 在共享内存系统中，改变激活组件的顺序

![image-20230106204014629](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106204014629.png)

### 3. Stress Testing 压力测试

* Exercises the system beyond its maximum design load. Stressing the system often causes defects to come to light
* 使系统超出其最大设计负载。强调系统往往会导致缺陷暴露出来
* **Stressing the system test failure behaviour.**Systems should not fail catastrophically. Stress testing checks for unacceptable loss of service or data
* **强调系统测试失败行为。**系统不应该出现灾难性的故障。压力测试检查不可接受的服务或数据丢失
* Particularly relevant to distributed systems which can exhibit severe degradation as a network becomes overloaded
* 特别是与分布式系统相关，当网络变得过载时，分布式系统会表现出严重的退化

#### 3.1 Object-Oriented Testing 面向对象测试

* The components to be tested are object classes that are instantiated as objects
* 要测试的组件是实例化为对象的对象类
* Larger grain than individual functions so approaches to white-box testing have to be extended
* 粒度大于单个函数，因此必须扩展白盒测试方法
* No obvious ‘top’ to the system for top-down integration and testing
* 对于自上而下的集成和测试，系统没有明显的“顶部”

#### 3.1.1 Testing Levels 测试等级

* **Testing operations associated with objects**
* **测试与对象关联的操作**
* **Testing object classes**
* **测试对象类**
* **Testing clusters of cooperating objects**
* **测试协作对象的集群**
* **Testing the complete OO system**
* **测试完整的OO系统**

![image-20230106205214210](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106205214210.png)



### 4. Object Class Testing 对象类的测试

* Complete test coverage of a class involves
* 类的完整测试覆盖包括
  * **Testing all operations associated with an object**
  * **测试与对象相关的所有操作**
  * **Setting and interrogating all object attributes**
  * **设置和查询所有对象属性**
  * **Exercising the object in all possible states**
  * **在所有可能的状态下执行对象**
* Inheritance makes it more difficult to design object class tests as the information to be tested is not localised
* 继承使得设计对象类测试更加困难，因为要测试的信息不是本地化的

![image-20230106205815033](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106205815033.png)

#### 4.1 Object Integration  对象集成

* Levels of integration are less distinct in object-oriented systems
* 在面向对象的系统中，集成的级别不那么明显
* **Cluster testing** is concerned with integrating and testing clusters of cooperating objects
* <font color='red'>集群测试Cluster testing涉及集成和测试协作对象的集群</font>
* Identify clusters using knowledge of the operation of objects and the system features that are implemented by these clusters
* 使用对象操作的知识和由这些集群实现的系统特性来识别集群

#### 4.2 Approaches to Cluster Testing 集群测试的方法

* Use-case or scenario testing 用例或场景测试
  * Testing is based on a user interactions with the system
  * 测试基于用户与系统的交互
  * Has the advantage that it tests system features as experienced by users
  * 它是否具有测试用户所体验的系统特性的优势
* Thread testing 线程测试
  * Tests the systems response to events as processing threads through the system
  * 在系统中处理线程时测试系统对事件的响应
* Object interaction testing 对象交互测试
  * Tests sequences of object interactions that stop when an object operation does not call on services from another object
  * 测试当对象操作不调用来自另一个对象的服务时停止的对象交互序列

#### 4.3 Scenario-Based Testing 基于场景的测试

* **Identify scenarios from use-cases and supplement these with interaction diagrams that show the objects involved in the scenario**
* **从用例中识别场景，并用显示场景中涉及的对象的交互图补充这些场景**
* Consider the scenario in the weather station system where a report is generated
* 考虑在气象站系统中生成报告的场景

![image-20230106211134734](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106211134734.png)

![image-20230106211142889](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106211142889.png)

![image-20230106211155788](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106211155788.png)

![image-20230106211201554](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106211201554.png)



# Project Mangement

## Lecture 25 Project Management

<font size=5 color=red>Organising, planning and scheduling software projects</font>

组织、计划和安排软件项目

![image-20230106211537785](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106211537785.png)

* To introduce software project management and to describe its distinctive characteristics
* 介绍软件项目管理，并描述其特点
* To discuss project planning and the planning process
* 讨论项目规划和规划过程
* To show how graphical schedule representations are used by project management
* 展示项目管理如何使用图形进度表示
* To discuss the notion of risks and the risk management process
* 讨论风险的概念和风险管理过程

![image-20230106213336098](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106213336098.png)



### 1. Management Activities 管理活动

#### 1.1 Software Project Management 

* Concerned with activities involved in ensuring that software is delivered on time and on schedule and in accordance with the requirements of the organisations developing and procuring the software
* 参与确保软件按照开发和采购软件的组织的要求按时、按期交付的活动
* Project management is needed because software development is always subject to budget and schedule constraints that are set by the organisation developing the software
* 项目管理是必要的，因为软件开发总是受制于由开发软件的组织设定的预算和进度限制

#### 1.2 Software Management Distinctions 软件管理的区别

* The product is intangible 
* 产品是无形的
  * (cannot be seen or touched)
* Software engineering is not recognized as an engineering discipline with the same status as mechanical, electrical engineering, etc.
* 软件工程不被认为是一门与机械、电气工程等具有相同地位的工程学科。
* The software development process is not standardised
* 软件开发过程没有标准化
* Many software projects are 'one-off' projects
* 许多软件项目都是“一次性的”项目

#### 1.3 Management Activities

![image-20230106214448990](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106214448990.png)

![image-20230106214545117](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106214545117.png)

#### 1.5 Management Commonalities 管理的共性

* These activities are not peculiar to software management
* 这些活动并不是软件管理所特有的
* Many techniques of engineering project management are equally applicable to software project management
* 工程项目管理的许多技术同样适用于软件项目管理
* Technically complex engineering systems tend to suffer from the same problems as software systems
* 技术上复杂的工程系统往往会遇到与软件系统相同的问题

##### 1.5.1 Project Staffing 项目资源安排

* May not be possible to appoint the ideal people to work on a project
* 可能无法任命合适的人为一个项目工作
  * Project budget may not allow for the use of highly-paid staff
  * 项目预算可能不允许使用高薪人员
  * Staff with the appropriate experience may not be available
  * 可能找不到有适当经验的工作人员
  * An organisation may wish to develop employee skills on a software project
  * 一个组织可能希望在软件项目中培养员工的技能
* Managers have to work within these constraints especially when (as is currently the case) there is an international shortage of skilled IT staff
* 管理人员必须在这些限制条件下工作，特别是当国际上缺乏熟练的IT人员时(就像目前的情况一样)

### 2. Project Planning 项目计划

* Probably the most time-consuming  project management activity
* Project Planning可能是最耗时的项目管理活动
* Continuous activity from initial concept through to system delivery. Plans must be regularly revised as new information becomes available
* 从最初的概念到系统交付的持续活动。计划必须在获得新信息时定期修订
* Various different types of plan may be developed to support the main software project plan that is concerned with schedule and budget 
* 可以开发各种不同类型的计划来支持与进度和预算有关的主要软件项目计划

![image-20230106215449469](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106215449469.png)

![image-20230106215501662](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106215501662.png)

#### 2.1 Project Plan Structure 项目计划结构

![image-20230106215601134](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106215601134.png)

![image-20230106215551119](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106215551119.png)

#### 2.2 Activity Organization 活动组织

* Activities in a project should be organised to produce tangible outputs for management to judge progress
* 项目活动的组织应产生有形的产出，以供管理层判断进度
* **Milestones** are the end-point of a process activity
* **里程碑**是流程活动的终点
* **Deliverables** are project results delivered to customers
* **交付成果**是指交付给客户的项目成果
* The waterfall process allows for the straightforward definition of progress milestones
* 瀑布式流程允许对进度里程碑进行直接的定义

![image-20230106215909995](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106215909995.png)

**<font color='red'>The RE Process是前序处理工作</font>**

### 3. Project Scheduling 项目调度

* **Split project into tasks and estimate time and resources required to complete each task**
* **将项目分成任务，并估计完成每个任务所需的时间和资源**
* Organize tasks concurrently to make optimal use of workforce
* 同时组织任务，充分利用人力资源
* **Minimize task dependencies** to avoid delays caused by one task waiting for another to complete
* **最小化任务依赖关系**，以避免由于一个任务等待另一个任务完成而造成的延迟
* Dependent on project managers intuition and experience
* 依靠项目经理的直觉和经验

![image-20230106220329541](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106220329541.png)

#### 3.1 Scheduling Problems 调度问题

* **Estimating** the difficulty of problems and hence the cost of developing a solution is hard
* **估算**问题的难度以及开发解决方案的成本是困难的
* Productivity is not proportional to the number of people working on a task
* 工作效率与完成一项任务的人数不成正比
* Adding people to a late project can make it even later because of communication overheads
* 将人员添加到一个较晚的项目中可能会因为沟通开销而使项目变得更晚
* The unexpected always happens. Always allow for contingency in planning
* 意外总是会发生。在制定计划时要考虑到偶然性

#### 3.2 Bar Charts and Activity Networks 柱状图和活动网络

* Graphical notations used to illustrate the project schedule
* 用于说明项目进度表的图形符号
* Show project breakdown into tasks. Tasks should not be too small. They should take about a week or two
* 将项目分解为任务。任务不应该太小。大概需要一两个星期
* **Activity charts show task dependencies and the critical path**
* **活动图表显示任务依赖关系和关键路径**
  * **关键路径是一条穿过所有预期完成时间最长的节点的线。**

* 
* **Bar charts show schedule against calendar time**
* **柱状图显示日程安排与日历时间的对比**

![image-20230106220940288](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106220940288.png)

![image-20230106220946885](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106220946885.png)

![image-20230115094311203](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230115094311203.png)

![image-20230106220953299](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106220953299.png)

![image-20230106221000409](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106221000409.png)

### 4. Risk Management 风险管理

* **Risk management is concerned with identifying risks and drawing up plans to minimise their effect on a project.**

* **风险管理涉及识别风险并制定计划，以尽量减少风险对项目的影响**。

* A risk is a probability that some adverse circumstance will occur. 

* 风险是某些不利情况发生的概率。

  * Project risks affect schedule or resources
  * 项目风险影响进度或资源
  * Product risks affect the quality or performance of the software being developed
  * 产品风险影响正在开发的软件的质量或性能
  * Business risks affect the organisation developing or procuring the software
  * 业务风险影响开发或采购软件的组织

  ![image-20230106221529824](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106221529824.png)

#### 4.1 Pert Charts Pert图

![image-20230106221708074](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106221708074.png)

![image-20230106221701571](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106221701571.png)

![image-20230106221747753](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106221747753.png)

#### 4.2 The Risk Management Process 风险管理过程

* Risk identification 风险辨认
  * Identify project, product and business risks
  * 识别项目、产品和业务风险
* Risk analysis 风险分析
  * Assess the likelihood and consequences of these risks
  * 评估这些风险的可能性和后果
* Risk planning 风险计划
  * Draw up plans to avoid or minimise the effects of the risk
  * 拟定计划以避免或尽量减少风险的影响
* Risk monitoring 风险监测
  * Monitor the risks throughout the project
  * 监控整个项目的风险

![image-20230106222116166](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106222116166.png)

#### 4.3 Risk Identification 风险识别

![image-20230106222201293](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106222201293.png)

![image-20230106222208166](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106222208166.png)



#### 4.4 Risk Analysis 风险分析

* Assess probability and seriousness of each risk
* 评估每个风险的可能性和严重性
* **Probability** may be very low, low, moderate, high or very high
* 概率可能很低、低、中等、高或很高
* **Risk effects** might be catastrophic, serious, tolerable or insignificant
* 风险影响可能是灾难性的、严重的、可容忍的或微不足道的

![image-20230106222349914](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106222349914.png)

#### 4.5 Risk Planning

* **Consider each risk and develop a strategy to manage that risk**
* **考虑每一种风险并制定管理风险的策略**
* **Avoidance strategies **回避策略
  * The probability that the risk will arise is reduced
  * 风险发生的概率降低了
* **Minimisation strategies** 最小化策略
  * The impact of the risk on the project or product will be reduced
  * 风险对项目或产品的影响将会降低
* **Contingency plans** 应急计划
  * If the risk arises, contingency plans are plans to deal with that risk
  * 如果风险出现，应急计划是处理风险的计划

![image-20230106222647021](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106222647021.png)

#### 4.6 Project management Tools 项目管理工具

![image-20230106222725443](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106222725443.png)

![image-20230106222730755](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106222730755.png)



![image-20230106222739822](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106222739822.png)

![image-20230106222745188](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106222745188.png)





## Lecture 26 Software Cost Estimation



### 1. Software Cost Estimation 软件成本估算

* Software cost estimation involves predicting the resources required for a software development process
* 软件成本估算包括预测软件开发过程所需的资源

![image-20230106230333149](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106230333149.png)

#### 1.1 Software Cost Components 软件成本部件

* Hardware and software costs
* 硬件和软件成本
* Travel and training costs
* 差旅及培训费用
* Effort costs  (the dominant factor in most projects)
* 工作成本(大多数项目中的主要因素)
  * salaries of engineers involved in the project
  * 参与该项目的工程师的工资
  * Social and insurance costs
  * 社会及保险费用
* Effort costs must take overheads into account
* 工作成本必须考虑到管理费用
  * costs of building, heating, lighting
  * 建筑、取暖、照明的成本
  * costs of networking and communications
  * 网络和通讯费用
  * costs of shared facilities (e.g library, staff restaurant, etc.)
  * 共用设施的费用(例如图书馆、员工餐厅等)

![image-20230106230821730](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106230821730.png)

##### 1.11 Costing and Pricing

* Estimates are made to discover the cost, to the developer, of producing a software system
* 估算是为了发现开发人员生产软件系统的成本
* There is not a simple relationship between the development cost and the price charged to the customer
* 开发成本和向客户收取的价格之间并不是简单的关系
* Broader organisational, economic, political and business considerations influence the price charged
* 更广泛的组织、经济、政治和商业因素会影响定价

![image-20230106231023882](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106231023882.png)

#### 1.2 Programmer Productivity 程序员的效率

* **A measure of the rate at which individual engineers involved in software development produce software and associated documentation**
* **对参与软件开发的工程师个人生产软件和相关文档的速度的度量**
* Not quality-oriented although quality assurance is a factor in productivity assessment
* 不以质量为导向，尽管质量保证是生产力评估的一个因素
* Essentially, we want to measure useful functionality produced per time unit
* 从本质上讲，我们希望衡量每个时间单位产生的有用功能



##### 1.2.1 Productivity Measures

* Size-related measures based on some output from the software process. This may be lines of delivered source code, object code instructions, etc.
* 基于软件过程输出的与大小相关的度量。这可能是交付的源代码、目标代码指令等行。
* Function-related measures based on an estimate of the functionality of the delivered software. Function-points are the best known of this type of measure
* 基于对所交付软件功能的估计的功能相关度量。功能点是这类度量中最著名的

##### 1.2.2 Measurement Problems 测量问题

![image-20230107000657636](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230107000657636.png)

**![image-20230107000705361](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230107000705361.png)**

##### 1.2.3 Lines of Code 代码的行

* What's  a line of code?
* 一行代码是什么?
  * The measure was first proposed when programs were typed on cards with one line per card
  * 这种方法最初是在每张卡片上输入一行程序时提出的
  * How does this correspond to statements as in Java which can span several lines or where there can be several statements on one line
  * 这与Java中的语句是如何对应的呢? Java中的语句可以跨越几行，或者在一行中可以有几条语句
* What programs should be counted as part of the system?
* 哪些程序应该算作系统的一部分?
* Assumes linear relationship between system size and volume of documentation
* 假设系统大小和文档量之间存在线性关系

#### 1.3 Productivity Comparisons 效率的比较

* **The lower level the language, the more productive the programmer**
* **语言级别越低，程序员的工作效率就越高**
  * The same functionality takes more code to implement in a lower-level language than in a high-level language
  * 相同的功能在低级语言中实现比在高级语言中实现需要更多的代码

![image-20230107001131079](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230107001131079.png)



#### 1.4 Function Points 功能点

* **Based on a combination of program characteristics**
* **基于组合程序的特点**
  * external inputs and outputs
  * 外部输入和输出
  * user interactions
  * 用户交互
  * external interfaces
  * 外部接口
  * files used by the system
  * 系统使用的文件
* A weight is associated with each of these
* 权重与每一个相关
* **The function point count is computed by multiplying each raw count by the weight and summing all values**
* **功能点计数是通过将每个原始计数乘以权重并将所有值相加来计算的**

![image-20230107001517850](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230107001517850.png)



#### 1.5 Object Points  对象点

* **Object points are an alternative function-related measure to function points**
* **对象点是功能点以外的一种与功能相关的度量方法**
* Object points are NOT the same as object classes
* 对象点与对象类不同
* The number of object points in a program is a weighted estimate of
* 程序中对象点的数量是对的加权估计
  * The number of separate screens that are displayed
  * 显示的独立屏幕的数量
  * The number of reports that are produced by the system
  * 系统生成的报表数量
  * The number of modules that must be developed
  * 必须开发的模块数量

#### 1.6 Productivity Estimates  生产率估计

![image-20230107001911704](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230107001911704.png)

![image-20230107001918315](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230107001918315.png)

#### 1.7 Quality and Productivity  质量和生产率

* It could be argued that all metrics based on volume/unit time are flawed because they do not take quality into account
* 可以说，所有基于体积/单位时间的指标都是有缺陷的，因为它们没有考虑质量
* Productivity may generally be increased at the cost of quality
* 生产率的提高通常是以质量为代价的
* It is not clear how productivity/quality metrics are related
* 目前还不清楚生产率/质量指标是如何相关的
* **If change is constant (simplifying and improving code for example) then an approach based on counting lines of code is not meaningful**
* **如果变化是持续的(例如简化和改进代码)，那么基于计算代码行数的方法是没有意义的**

#### 1.8  Estimation Techniques 评估方法

* There is no simple way to make an accurate estimate of the effort required to develop a software system
* 没有一种简单的方法可以准确地估计开发软件系统所需的工作量
  * Initial estimates are based on inadequate information in a user requirements definition
  * 最初的估计是基于用户需求定义中的不充分信息
  * The software may run on unfamiliar computers or use new technology
  * 该软件可以在不熟悉的计算机上运行或使用新技术
  * The people in the project may be unknown
  * 项目中的人可能是未知的
* Project cost estimates may be self-fulfilling
* 项目成本估算可能是自我实现的
  * The estimate defines the budget and the product is adjusted to meet the budget 
  * 估算定义预算，并调整产品以满足预算

![image-20230107002433034](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230107002433034.png)

![image-20230107002450231](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230107002450231.png)



#### 1.9 Algorithmic Code Modelling 算法代码建模

![image-20230107002544765](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230107002544765.png)

![image-20230107002559217](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230107002559217.png)

![image-20230107003736966](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230107003736966.png)





#### 1.10 Expert Judgement 专家评估

* One or more experts in both software development and the application domain use their experience to predict software costs. Process iterates until some consensus is reached.
* 软件开发和应用程序领域的一个或多个专家使用他们的经验来预测软件成本。过程不断迭代，直到达成某种共识。
* **Advantages:  Relatively cheap estimation method. Can be accurate if experts have direct experience of similar systems**
* **优点:相对便宜的估算方法。如果专家有类似系统的直接经验，是否可以准确**
* **Disadvantages:  Very inaccurate if there are no experts!**
* **缺点:如果没有专家，非常不准确!**



#### 1.11 Estimation by Analogy 类比估计

![image-20230107002819740](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230107002819740.png)

* The cost of a project is computed by comparing the project to a similar project in the same application domain

* 项目的成本是通过将该项目与同一应用程序域中的类似项目进行比较来计算的

  * Advantages:  Accurate if project data available
  * 优点:如果有项目数据，准确无误
  * Disadvantages: Impossible if no comparable project has been tackled. Needs systematically maintained cost database
  * 缺点:如果没有处理过类似的项目，则不可能。需要系统维护成本数据库

  

#### 1.12 Parkinson's Law 帕金森定律

* **The project costs whatever resources are available** 
* **这个项目的成本取决于可用的资源**
  * Advantages:  No overspend 没有超支
  * Disadvantages: System is usually unfinished 系统通常未完成

![image-20230107003201083](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230107003201083.png)

![image-20230107003207089](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230107003207089.png)

**因为是根据成本决定进度，所以有时候会被用在未知的新领域**

#### 1.13 Pricing to Win 定价制胜

* The project costs whatever the customer has to spend on it
  * Advantages: You get the contract
  * Disadvantages: The probability that the customer gets the system he or she wants is small. Costs do not accurately reflect the work required

![image-20230107003324571](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230107003324571.png)

![image-20230107003708450](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230107003708450.png)

#### 1.14 Top-Down and Bottom-Up Estimation

* Any of these approaches may be used top-down or bottom-up
* 这些方法中的任何一种都可以自顶向下或自底向上使用
  * Top-down 
    * Start at the system level and assess the overall system functionality and how this is delivered through sub systems
    * 从系统级别开始，评估整个系统功能，以及如何通过子系统交付功能
  * Bottom-up
    * Start at the component level and estimate the effort required for each component. Add these efforts to reach a final estimate
    * 从组件级别开始，并估计每个组件所需的工作量。把这些努力加起来，得出最终的估计

#### 1.15 Estimation Methods

![image-20230107003530390](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230107003530390.png)

![image-20230107003546878](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230107003546878.png)

#### 1.16 Experience-Based Estimates 经验估计

![image-20230107003638117](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230107003638117.png)



#### 1.17 Estimation Accuracy 估计精度

* The size of a software system can only be known accurately when it is finished
* 软件系统的大小只有在完成时才能准确地知道
* Several factors influence the final size
* 影响最终尺寸的因素有几个
  * Use of COTS and components
  * COTS和组件的使用
  * Programming language 
  * 编程语言
  * Distribution of system
  * 系统的分布
* As the development process progresses then the size estimate becomes more accurate
* 随着开发过程的进展，大小估计变得更加准确











































