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
* Program testing is the only validation technique for non-functional requirements
* 程序测试是非功能性需求的唯一验证技术
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

* Defect testing 缺陷测试
  * Tests designed to discover system defects.
  * 设计用于发现系统缺陷的测试。
  * A successful defect test is one which reveals the presence of defects in a system.
  * 一个成功的缺陷测试是揭示系统中存在缺陷的测试。
* Statistical testing 统计检验
  * Tests designed to reflect the frequency of user inputs. Used for reliability estimation.
  * 旨在反映用户输入频率的测试。用于可靠性估计。

#### 1.6 Verification & Validation Goals

* Verification and validation should establish a degree of confidence that the software is fit for purpose
* 验证和确认应该建立一定程度的信心，使软件适合于目的

* This does NOT mean completely free of defects
* 这并不意味着完全没有缺陷
* The degree of confidence required depends upon several different factors as we see on the next slide
* 所需要的自信程度取决于几个不同的因素，我们在下一张幻灯片中看到

![image-20230105171951776](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230105171951776.png)

* **Software function** – A much higher level of confidence that the system is fit for purpose is required for safety critical systems that for prototype systems for example
* **软件功能**——对于安全关键系统(例如原型系统, 重要的系统)，需要对系统是否适合目的有更高的信心
* **User expectations** – Users sometimes have a low expectation of software and are willing to tolerate some system failures (although this is decreasing)
* **用户期望**——用户有时对软件的期望很低，并且愿意容忍一些系统故障(尽管这种情况正在减少)。
* **Marketing environment** – Competing programs must be taken into account and the required schedule for introducing the product to market. Cheaper products may be expected to have more faults.
* **营销环境**-必须考虑到竞争项目和将产品推向市场所需的时间表。更便宜的产品可能会有更多的缺陷。

#### 1.7 Testing and Debugging

* Defect testing and debugging are distinct processes
* 缺陷测试和调试是不同的过程
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

* A syntax error should be caught by the compiler which will (usually) indicate the location the error occurred in and the type of error.
* 语法错误应该被编译器捕获，编译器(通常)会指出错误发生的位置和错误的类型。
* <font color=red>idea上出现红色下划线的部分</font>
* A semantic error (also called a logical error) can occur in a program which compiles and runs, but produces incorrect output on some (or all) input (e.g. An incorrect algorithm or mistake in a formulae etc.)
* 语义错误(也称为逻辑错误)可能发生在编译和运行的程序中，但在某些(或全部)输入上产生不正确的输出。不正确的算法或公式中的错误。)
* <font color='red'>由于逻辑问题产生的不正确的输出</font>
* Semantic errors are often harder to detect since the compiler may not be able to indicate where/what the problem is.
* 语义错误通常更难检测，因为编译器可能无法指出问题在哪里/是什么。

#### 1.8 Testing and Debugging 测试与调试

* Once errors are located, it is necessary to correct the program code and re-test the program
* 一旦发现了错误，就必须纠正程序代码并重新测试程序
* Regression testing – after fixing a defect, it is advisable to retest the program with all previous test data to make sure the “fix” has not introduced new problems
* 回归测试——在修复了一个缺陷之后，建议使用所有之前的测试数据重新测试程序，以确保“修复”没有引入新的问题
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

* Defect testing involves testing programs to establish the presence of system defects
* 缺陷测试包括测试程序来确定系统缺陷的存在

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

* An approach to testing where the program is considered as a ‘black-box’
* 一种测试程序被认为是“黑盒”的方法
* **The program test cases are based on the system specification** 
* **程序测试用例基于系统规范**
* **Test planning can begin early in the software process**
* **测试计划可以在软件过程的早期开始**

![image-20230106151034049](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106151034049.png)

#### 3.1 Equivalence Partitioning 等价类的划分

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

### 4. Structural Testing 结构测试

* Sometime called white-box testing
* 有时被称为白盒测试
* **Derivation of test cases according to program structure. Knowledge of the program is used to identify additional test cases**
* **根据程序结构推导测试用例。程序的知识被用来识别额外的测试用例**
* Objective is to exercise all program statements (not all path combinations)
* 目标是练习所有的程序语句(不是所有的路径组合)

![image-20230106153545444](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106153545444.png)

![image-20230106153553036](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106153553036.png)

![image-20230106153603656](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106153603656.png)

![image-20230106153610497](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106153610497.png)

![image-20230106153617742](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230106153617742.png)



### 5. Path Testing 路径测试

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
* 用于计算环复杂度
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
* As a new module is added, we not only run a new test, we also make sure the addition of the new module does not “break” the previous test cases.
* 当添加一个新模块时，我们不仅要运行一个新的测试，还要确保不添加新模块“打破”之前的测试用例。
*  This can sometimes by done automatically by using a test harness (a program written to automatically generate test data and record their results). [See Junit for Java if you are interested in this.]
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

* Interface misuse  接口误用
  * A calling component calls another component and makes an error in its use of its interface e.g. parameters in the wrong order
  * 一个调用组件调用另一个组件时，在接口的使用上犯了一个错误，例如参数的顺序错误
* Interface misunderstanding 接口误解
  * A calling component embeds assumptions about the behaviour of the called component which are incorrect
  * 调用组件嵌入了关于被调用组件行为的不正确假设
* Timing errors 时间错误
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

#### 3.2 Testing Levels 测试等级

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





















