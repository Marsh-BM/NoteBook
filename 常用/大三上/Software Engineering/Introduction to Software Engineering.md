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

![image-20221219163333396](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221219163333396.png)

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
*  **瀑布模型(经典工程，例如桥梁建筑)**
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

增量式开发模式可以不需要给出一个清晰的需求描述，而是从一个<font color='red'>outline description</font>开始（也就是说，我大致先知道需要做哪些功能）
一旦有了一个大致的功能和性能要求，就可以通过specification，development，validation。构成一个软件的初始版本，也叫原型**（Initial version）** 。
原型（Initial version）构造好后，交给用户来使用和评价，用户若觉得这个版本不合适，开发人员再进行修改，形成第二个版本。不断重复这些过程，就会形成很多的中间版本**（Intermediate versions），直到形成一个最终版本（Final version）**

**补充**：

**用户参与：**用户是参与在开发过程中的。用户一直和开发团队进行交流，每开发出一个新的版本，用户要进行评价并产生反馈意见，然后由开发者来修订，产生不同的中间版本，最终演化成一个最终版本。
**别名：**演化式开发、原型开发。
**增量式含义：**每个增量，是在上一个版本的基础上，再进行的工作

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

* 增量式开发，追求速度，不会产生大量中间文档，用户就难以系统地获取信息，就不可见。 系统有时结构很差

  

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

Lightweight approach to software development
Example include Scrum and XP

* 软件开发的轻量级方法
* 例子包括Scrum和XP

轻量级的软件开发工程

![image-20221005175930177](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221005175930177.png)

Agile Development是一种以人为核心、迭代、循序渐进的开发方法。在敏捷开发中，软件项目的构建被切分成多个子项目，各个子项目的成果都经过测试，具备集成和可运行的特征。<font color='red'>简言之，就是把一个大项目分为多个相互联系，但也可独立运行的小项目，并分别完成，在此过程中软件一直处于可使用状态。</font>



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

![image-20221219172501194](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221219172501194.png)

* 与其将系统作为单个交付交付，不如将开发和交付分解为增量(SCRUM sprint)，每个增量交付所需功能的一部分
* 用户需求是优先级的，最高优先级的需求包含在早期增量中
* 一旦开始了增量的开发，需求就会被冻结，尽管后续增量的需求可以继续发展

优点：

![image-20221219172613870](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221219172613870.png)

客户价值可以随每个增量一起交付，因此系统功能可以更早地可用

早期增量作为一个原型来帮助引出后续增量的需求

降低整体项目失败的风险

最高优先级的系统服务往往接受最多的测试

![image-20221219172727065](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221219172727065.png)

流程依赖于上下文

核电站/空中交通管制

高度形式化的流程

详细测试规范

小型网站Web开发

原型

大型网站的Web开发

SCRUM开发，故事板

## Week2 Lecture3

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
   2.  For each sub-system, an abstract specification of its operational constraints and services is produced.
   
3. **Interface Design（接口设计）**
   1. 对于每个子系统，都设计了与其他子系统的明确接口并编制了文档
   2.  For each sub-system, an unambiguous interface with other sub-systems is designed and documented
   
4. **Component Design(元件设计)**
   1. 为组件分配服务，并设计这些组件的接口
   
5. **Data Structure Design**
   1. 对系统实现中使用的数据结构进行了详细的设计和说明
   
6. **Algorithm design 算法设计**
1. ．设计并指定了用于提供服务的组件中的算法

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

#### 2.3 Programming and Debuging 编程和调试

编程和调试(Programming and Debuging)包括将设计转化为程序并从程序中删除错误.

* 编程通常是个人活动——没有通用的编程过程，但有良好的编程实践和组织标准可以遵循。

* 程序员进行一些程序测试，以发现程序中的错误，并在调试过程中消除这些错误。

#### 2.4 The Testing Process

![image-20221008134022423](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221008134022423.png)

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
