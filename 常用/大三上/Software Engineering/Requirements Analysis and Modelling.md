# Requirements Analysis and Modeling



### Lecture4  Requirement Engineering

![image-20221008135930186](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221008135930186.png)

#### 1. Requirements Engineering要求工程

**Requirements Engineering(需求工程)是在系统运行和开发的约束条件下，建立客户从系统中需要的服务的过程**

![image-20221008141746044](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221008141746044.png)

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

##### 3.2 Requirements Completeness and Consistency

完整的 Complete

它们应该包括所有所需设施的描述

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

**产品需求**

所有加密都应该使用高级加密标准

**组织要求**

系统开发过程和交付成果文件应符合编码和文档标准XYZCo-SP-STAN-95中定义的过程和交付成果

**外部需求**

除客户的姓名和编号外，系统不会向系统的运营者披露客户的任何个人信息

**性能需求**

在“高峰时间”和0.01秒内，系统应在小于0.1秒的时间内响应用户的信息请求

![image-20230101104054035](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101104054035.png)

###### 3.1.2 Goals and Requirements

* Non-functional requirements may be very difficult to state precisely and imprecise requirements may be difficult to verify.
* 非功能性需求可能很难精确地表述，而不精确的需求可能很难验证。
* Verifiable non-functional requirement
* 可验证的非功能需求
  * A statement using some measure that can be objectively tested
  *  一种使用某种可以被客观测试的测量方法的陈述
* Goals are helpful to developers as they convey the intentions of the system users
* 目标对开发人员很有帮助，因为它们传达了系统用户的意图

![image-20230101105623631](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101105623631.png)

##### 3.4 Domain Requirement

来自系统的应用程序领域的需求，反映了该领域的特征

![image-20230101105945883](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101105945883.png)

Conflicts between different non-functional requirements are common in complex systems

在复杂的系统中两个不同的non-functional requirement会产生矛盾是正常的

![image-20230101110111357](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101110111357.png)

![image-20230101110243451](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101110243451.png)



#### 4. User Requirements

**用户需求应该描述功能和非功能需求，以便不具备详细技术知识的系统用户能够理解．使用自然语言、表格和图表来定义用户需求，以便非技术客户能够更好地理解需求并指出潜在的问题。**

<font color=red>傻瓜说明书</font>

![image-20221008220150732](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221008220150732.png)

![image-20221008220201050](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221008220201050.png)

![image-20230101110508937](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101110508937.png)





## Lecture6 Requirements Engineering Processes

![image-20230101114810456](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101114810456.png)

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

* Requirements discovery is the process of gathering information about the proposed and existing systems and distilling the user and system requirements from this information.
* 需求发现是收集关于提议的和现有的系统的信息，并从这些信息中提取用户和系统需求的过程。
* Sources of information include documentation, system stakeholders and the specifications of similar systems
* 信息来源包括文档、系统涉众和类似系统的规范

![image-20230101123549699](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101123549699.png)

![image-20230101123607498](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101123607498.png)

![image-20230101123726724](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101123726724.png)

#### 2.2 Viewpoints 观点

* Viewpoints are a way of structuring the requirements to represent the perspectives of different stakeholders. Stakeholders may be classified under different viewpoints.

* 视点是构造需求的一种方式，以表示不同涉众的观点。

  涉众可以根据不同的观点进行分类。

*  This multi-perspective analysis is important as there is no single correct way to analyse system requirements.

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

##### 2.8 Availability requirements

![image-20230101155220709](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101155220709.png)

![image-20230101155238386](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101155238386.png)

##### 2.9 Security, logs and alerts 安全性和日志

![image-20230101155322778](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101155322778.png)

![image-20230101155405304](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101155405304.png)

![image-20230101155442350](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101155442350.png)

##### 2.10 Specifying Security

![image-20230101155625587](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101155625587.png)

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

![image-20230101160303468](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101160303468.png)

![image-20230101160338397](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101160338397.png)



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

* Data processing model - showing how the data is processed at different stages
* 数据处理模型-显示数据在不同阶段是如何处理的
* Composition model - showing how entities are composed of other entities
* 组合模型-显示实体如何由其他实体组成
* Architectural model - showing principal sub-systems
* 体系结构模型-显示主要子系统
* Classification model - showing how entities have common characteristics
* 分类模型-显示实体如何具有共同特征
* Stimulus/response model - showing the system’s reaction to events
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

* Behavioural models are used to describe the overall behaviour of a system
* 行为模型用于描述系统的整体行为
* Two types of behavioural model
  *  **Data processing models** that show how data is processed as it moves through the system
  * 数据处理模型，显示了当数据在系统中移动时如何处理数据
  * **State machine models** that show the systems response to events
  * 显示系统对事件响应的状态机模型
* Both of these models are required for a description of the system’s behaviour
* 这两个模型都是描述系统行为所必需的

![image-20230101223927435](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101223927435.png)

#### 5. Data-Processing Models 数据处理模型

* **Data flow diagrams** are used to model the system’s data processing
* 数据流图用于对系统的数据处理进行建模
* These show the processing steps as data flows through a system
* 它们显示了数据流经系统时的处理步骤
* IMPORTANT part of many analysis methods
* 许多分析方法是重要的组成成分
* **Simple and intuitive notation**
* 简单直观的符号
* **Show end-to-end processing of data**
* 显示数据的端到端处理

![image-20230101224444147](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230101224444147.png)



#### 6. Data Flow Diagrams 数据流图

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





#### 7. Statechart Diagrams 状态图

* Statechart Diagrams (or State machine models ) show the behaviour of the system in response to external and internal events
* 状态图(或状态机模型)显示了系统响应外部和内部事件的行为
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

### 1. Variants of FSMs

* There are many variants, for instance, 
  * machines having actions (outputs) associated with transitions **(Mealymachine)** or states **(Moore** 
    **machine)**, 
  * 具有与转换(Mealy机)或状态(Moore机)相关联的动作(输出)的机器
* multiple start states, 
* 多重开始状态，
* transitions conditioned on no input symbol (a null) or more than one transition for a given symbol and state (nondeterministic finite state machine), 
* 转换以不输入符号(null)或给定符号和状态的多个转换为条件**(非确定性有限状态机**)，
* one or more states designated as accepting states (recognizer), etc.
* 一个或多个被指定为接受州的州**(识别器**)等。

![image-20230102100512628](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230102100512628.png)

![image-20230102100554056](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230102100554056.png)

#### 1.1 Moore Machine 摩尔机

* 
* Basically a Moore machine is just a FSA with two extra 
  attributes. 
  \1. It has TWO alphabets, an input and output alphabet. 
  \2. It has an output letter associated with each state. The 
  machine writes the appropriate output letter as it enters each 
  state. 
* Basically a Moore machine is just a FSA with two extra 
  attributes. 
  \1. It has TWO alphabets, an input and output alphabet. 
  \2. It has an output letter associated with each state. The 
  machine writes the appropriate output letter as it enters each 
  state. 
*  Basically a Moore machine is just a FSA with two extra 
  attributes. 
  \1. It has TWO alphabets, an input and output alphabet. 
  \2. It has an output letter associated with each state. The 
  machine writes the appropriate output letter as it enters each 
  state. 
*  Basically a Moore machine is just a FSA with two extra 
  attributes. 
  \1. It has TWO alphabets, an input and output alphabet. 
  \2. It has an output letter associated with each state. The 
  machine writes the appropriate output letter as it enters each 
  state. 



* Basically a Moore machine is just a FSA with two extra attributes. 
* Moore Machine 是一个FSA有两个额外属性
* \1. It has TWO alphabets, an input and output alphabet. 
* 它有两个字母，一个输入字母和输出字母。
* \2. It has an output letter associated with each state. The machine writes the appropriate output letter as it enters each state. 

![image-20230102101335747](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230102101335747.png)

**Moore Machine的下一个状态取决于当前状态和当前输出，但其输出只取决于当前状态**

只能输出一个固定的值

![image-20230102101505275](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230102101505275.png)

#### 1.2 Mealy Machine 米利机

* Mealy machines are computationally equivalent to Moore machines 
  * (we can implement any Mealy machine using a Moore machine, and vice versa). 
  * 我们可以用摩尔机实现任何米利机，反之亦然
* However, Mealy machines move the output function from the state to the transition. This turns out to be easier to deal with in practice, making Mealy machines more practical. 
* 然而，Mealy机器将输出函数从状态移动到转换。这在实践中更容易处理，使Mealy机器更实用。

![image-20230102103850624](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230102103850624.png)

![image-20230102103914507](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230102103914507.png)

![image-20230102103921804](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230102103921804.png)

* Mealy machines are complete in the sense that there is a transition for each character in the input alphabet leaving every state. 
* Mealy机器是完整的，因为输入字母表中的每个字符离开每种状态都有一个过渡。
* There are no accept states in a Mealy machine because it is not a language recogniser, it is an output producer. Its output will be the same length as its input. 
* 在Mealy机器中没有接受状态，因为它不是语言识别器，而是输出生产者。它的输出和输入的长度是一样的。

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

![image-20230102110128183](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230102110128183.png)

* 箭头只能连接places 和 transition 反之亦然
* 我们还将根据需要添加一些其他特性和注意事项。

##### 2.1.2 Enabled Transitions and Firing

![image-20230102105034985](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230102105034985.png)

![image-20230102105059528](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230102105059528.png)

![image-20230102105107110](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230102105107110.png)

![image-20230102105115600](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230102105115600.png)

![image-20230102111949404](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230102111949404.png)



#### 2.2 Semantic Data Models

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

* Object models describe the system in terms of object classes
* 对象模型用对象类来描述系统
* An object class is an abstraction over a set of objects with common attributes and the services (operations) provided by each object
* 对象类是一组具有公共属性的对象和每个对象提供的服务(操作)的抽象
* Various object models may be produced
  * Inheritance models 继承模型
  * Aggregation models 聚合模型
  * Interaction models 相互作用模型



* Natural ways of reflecting the real-world entities manipulated by the system
* 反映由系统操纵的现实世界实体的自然方式
* More abstract entities are more difficult to model using this approach
* 更抽象的实体更难以使用这种方法建模
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
  * colour (for the modelling of attributes)
  * time (for performance analysis)
  * hierarchy (for the structuring of models, DFD's) 

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
*  A transition is enabled if each of the input places contains tokens.
* 如果每个输入位置都包含token，则启用transition。

![image-20230102173842511](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230102173842511.png)

<font color='red'>只有当每一个作为input的Places都有一个token，Transition才被认为是enabling的</font>

#### 2.3 Firing

* An enabled transition may fire.
* 一个enabled 的transition可能是fire的
* Firing corresponds to consuming tokens from the input places and producing tokens for the output places.
* 触发对应于从输入位置消费令牌并为输出位置产生令牌。

![image-20230103080712654](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103080712654.png)

Firing is atomic (only one transition fires at a time, even if more than one is enabled)

触发是原子的(一次只触发一个转换，即使启用了多个转换) **一次只能转换一个token**

![image-20230103080821054](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103080821054.png)

#### 2.4 Creating/Consuming Tokens

* A transition without any input can fire at any time and produces tokens in the connected places:
* 没有任何input的transition在任何时候都可以fire and 产生tokens 在与之连接的places上

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
* 两个对象之间的弧线数量指定了要产生/消费的令牌数量(我们也可以通过在单个弧线旁边写一个数字来表示)。
* This can be used to model (dis)assembly processes.
* 这可以用来建模(分解)组装过程。

![image-20230103090929563](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103090929563.png)

* Current state (also called current marking) - The configuration of tokens over the places.
* 当前状态(也称为当前标记)-位置上标记的配置。
* Reachable state - A state reachable form the current state by firing a sequence of enabled transitions.
* 可达状态——可达状态通过触发一系列已启用的转换形成当前状态。
* Deadlock state - A state where no transition is enabled.
* 死锁状态——没有启用转换的状态。

![image-20230103091111359](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103091111359.png)

*  If we write the places in some fixed order (red, black say), then we can use a tuple: (n,m) to denote the number of tokens in each corresponding place (n tokens in “red” and m tokens in “black”).
* 如果我们以某种固定的顺序(比如红色，黑色)来写位置，那么我们可以使用元组:(n,m)来表示每个对应位置上的标记的数量(n个标记在“红色”中，m个标记在“黑色”中)。
* The example below is thus in state (3,2). After firing transition “rr”, it will move to state (1,3) etc..
* 因此，下面的示例的状态为(3,2)。点火后转换“rr”，它将移动到状态(1,3)等。

![image-20230103091728797](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103091728797.png)

bb/br意思是bb和br同时使用

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

将复杂的流程简写，并且每一个流程存储到h中



### 5. Another Example ？？？？

* Recall the following example of an informal specification from a critical system [1] :
* 回想一下从一个关键系统中一个非正式规范的示例
  * The message must be triplicated. The three copies must be forwarded through three different physical channels. The receiver accepts the message on the basis of a two-out-of-three voting policy.
  * 消息必须有三份。三份副本必须通过三个不同的物理通道转发。接收方根据三选二的投票策略接受消息。
*  Questions: Can you identify any ambiguities in this specification?
* How could we model this system with a Petri net?

![image-20230103171059024](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103171059024.png)

![image-20230103171221308](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103171221308.png)

### 6. A Final Note on Petri Nets

![image-20230103171917805](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103171917805.png)

![image-20230103171923921](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103171923921.png)





## Lecture 11 Formal Specifications



**Formal Specification - Techniques for the Unambiguous Specification of Software**

**明确软件规范的技术**

![image-20230103172858403](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103172858403.png)



### 1. Formal Methods 正式方法



* **Formal specification** is part of a more general collection of techniques that are known as ‘formal methods’ 
* **形式化规范**是被称为“形式化方法”的更通用的技术集合的一部分。
* ![image-20230103173536249](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103173536249.png)
* Formal methods include 形式化方法
  * Formal specification 正式规范
  * Specification analysis and proof 规范分析和证明
  * Transformational development  转换的发展
  * Program verification 程序验证

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
  *  So 
    * Mostly formal methods not used
    * 很多formal没啥用了
    * The most acceptable techniques are approaches like programming by contract (e.g. Eiffel)
    * 最可接受的技术是契约式编程

![image-20230103175412871](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230103175412871.png)

#### 1.2 Acceptance of Formal Methods 正式方法的接受

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

* The algebraic approach to formal specification is particularly well-suited to interface specification
* 形式化规范的代数方法特别适合于接口规范



##### 2.4.1 Sub-System Interface Specification 子系统的接口规范

* Clear and unambiguous sub-system interface specifications reduce the chance of misunderstandings between a provider and user of a sub-system.
* 清晰明确的子系统接口规范可以减少子系统提供者和用户之间产生误解的机会。
* The algebraic approach to specification was originally developed for the definition of abstract data types.
* 用于规范的代数方法最初是为定义抽象数据类型而开发的。
* This idea was then extended to model complete system specifications.
* 这一思想随后被扩展到建模完整的系统规范。

![image-20230104000806436](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230104000806436.png)



### 3. Algebraic Specification 代数规范

**注意：代数规范是规范方法的一种**

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

* AsmL is a language for modelling the structure and behaviour of digital systems. We will see a basic introduction to ASML and how someconcepts can be encoded formally. 
* **AsmL是一种为数字系统的结构和行为建模的语言。**我们将了解ASML的基本介绍，以及如何对一些概念进行正式编码。
  *  (We will not go into too many details but just see the overall format ASML uses).
* AsmL can be used to faithfully capture the abstract structure and step wise behaviour of any discrete systems, including very complex ones such as:
* **AsmL可用于忠实地捕获任何离散系统的抽象结构和逐级行为，包括非常复杂的系统**，例如:
  * Integrated circuits  集成电路
  *  Software components  软件组成
  *  Devices that combine both hardware and software 结合硬件和软件的设备

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







