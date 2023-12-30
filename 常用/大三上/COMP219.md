# COMP219

##  Week3 Lecture5 Safety and Reliability Issues

![image-20221012110935059](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221012110935059.png)

### 1. Safely Concerns

#### 1.1 Generalisation Error

![image-20221012111725284](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221012111725284.png)

## Lecture8 Decision - Tree - Learning 

主要讲的就是自上而下的决策树算法



### 1. The history of Decision Tree Algorithms

* ID3, or Iterative Dichotomizer(ID3 或二分迭代器
  * 在树的每个节点上测试一个属性
  * 最大化信息增益
* CART, or Classification and Regression Trees()
  * 二叉树
  * 通过二分标准选择拆分
* C4.5,改进的ID3版本

​	

### 2. Top-down Decision Tree Learning



### 3. Occam’s razo



## Lab3 Decision-Tree



## Lecture10 Overfitting and K-Nearest Neighbour



### 1. Overfitting

#### 1.1 Overfitting in Decision Tree



##### 1.1.1 由于数据噪声导致的过拟合

##### 1.1.2 overfitting with noise-free data 

不知道噪声是什么的情况

？？？？？？？？？？看录播







### 2. K-NN



# ------------------------------------------------------

## Lecture 3 

![image-20230125170549116](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230125170549116.png)

![image-20230125170613301](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230125170613301.png)



## Lecture4  Probability  Foundation for Machine Learning

## 1. Probaility Foundations 概率论基础

### 1.1 Random Variables

* We have a population of students   我们有一定数量的学生

  * We want to reason about their grades 我们想要推理他们的成绩
  * Random variable: Grade 随机变量 成绩
  * P(Grade) associates a probability with each outcome Val(Grade)={ A, B, C } P(等级)关联每个结果的概率Val(等级)={a, B, C}

* ![image-20221127170428116](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221127170428116.png)

* ![image-20221127170358374](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221127170358374.png)

  * Distribution is referred to as a **multinomial** 
  * 分布式被称为**多项**
  * If **Val{X}={false,true}** then it is a **Bernoullidistribution** 
  * 那么它就是**伯努利分布**
  * P(X) is known as the **marginal distribution** of X       P(X)被称为X的**边界分布**

  

### 1.2 Joint and Conditional Distributions  联合和条件分布

#### 1.2.1 Recap: Marginal, Joint, Conditional Probality

* **Marginal Probability: 边缘概率**  the probability of an event occurring P(A), it may be thought of as an unconditional probability. It is not conditioned on another event.
* 发生P(A)事件的概率,可能被认为是**无条件的概率**。它不受另一个事件的约束。
* 下面的例子以扑克牌举例：

![image-20221127171139068](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221127171139068.png)

* **Joint probability: 联合概率**   P(A and B). The probability of event A and event B occurring. It is the probability of the intersection of two or more events. The probability of the intersection of A and B may be written P(A ∩ B).  
* 事件A和事件B发生的概率。这是两个或多个事件交叉的概率。A和B相交的概率可以写成P(A∩B)。 两件事同时发生的概率。
* 下面的例子以扑克牌举例：

![image-20221127171339883](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221127171339883.png)

* **Conditional probability：条件概率** P(A|B) is the probability of event A occurring, given that event B occurs.  P(A|B)是事件A发生的概率，前提是事件B发生。
* 下面的例子以扑克牌举例：

![image-20221127171520967](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221127171520967.png)



#### 1.2.2 Joint Distribution 联合分布

**联合分布(joint distribution)描述了多个随机变量的概率分布，是对单一随机变量的自然拓展。联合分布的多个随机变量都定义在同一个样本空间中。**

* We are interested in questions involving several random variables   我们对涉及几个随机变量的问题很感兴趣

  ![image-20221127175251733](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221127175251733.png)

* 在成绩A，智力高的情况下，概率为0.18

* **上图是两个随机变量的概率分布，得到的结果之和为1**

* 同时，这也是一个**边缘分布（Marginal Distribution）**的例子

#### 1.2.3 Conditional Probability 条件概率

* P(Intelligence|Grade=A) describes the distribution over events describable by Intelligence given the knowledge that student’s grade 
  is A. P(智力|年级=A)描述了在已知学生成绩为A的情况下，智力所描述的事件的分布情况

![image-20221127180217738](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221127180217738.png)



### 1.3 Independence and Conditional Independence 独立和条件独立



#### 1.3.1 Recap: Chain Rules

**Chain rule** (also called **the general product rule**) permits the calculation of 
any member of the joint distribution of a set of random variables using 
only conditional probabilities.  

**链式法则(也称为一般积法则)允许计算一组随机变量的联合分布的任何成员，只使用条件概率。**

![image-20221127180623996](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221127180623996.png)

使用条件概率计算一组随机变量的联合分布的任何成员。

#### 1.3.2 Independent Random Variables

* We expect P(α|β) to be different from P(α)  我们期望P(α|β)与P(α)不同

  * i.e., β is true changes our probability over α    β 改变了α的概率

  

* Sometimes equality can occur, i.e, P(α|β)=P(α)  有时平等也会发生,例如, P(α|β)=P(α)

  * i.e., learning that β occurs did not change our probability of α 得到β发生并没有改变α的概率
  * We say event α is independent of event β, denoted  我们说事件α独立于事件β，记为
  * ![image-20221127181309864](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221127181309864.png)
  * A distribution P satisfies (α⊥β) if and only if P(α∧β)=P(α)P(β) 
  * 分布P满足(α∧β)当且仅当P(α∧β)=P(α)P(β)

  

#### 1.3.3 Conditional Independence

* While independence is a useful property, we don’t often encounter two independent events  虽然独立性是一个有用的属性，但我们并不经常遇到两个独立事件
* 更常见的情况是,当两个事件独立于另一个事件时
  * Reason about student accepted at Stanford or MIT 
  * ![image-20221127181548072](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221127181548072.png)

![image-20221220133615115](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220133615115.png)

### 1.4 Querying Joint Probability Distributions 查询联合概率分布

#### 1.4.1 Query Type 查询类型

* Probability Queries 概率查询
  * Given evidence (the values of a subset of random variables),
  * 给定证据(随机变量子集的值)，
  * compute distribution of another subset of random variables
  * 计算随机变量的另一个子集的分布
* MAP Queries
  * Maximum a posteriori probability 
  * •最大后验概率
  * Also called MPE (Most Probable Explanation) 
  * •也称为MPE(最可能解释)
  * What is the most likely setting of a subset of random variables
  * •随机变量子集的最可能设置是什么
  * Marginal MAP Queries
  * •边缘MAP查询
  * When some variables are known
  * •当一些变量是已知的



#### 1.4.2 Probability Queries 概率查询

* Most common type of query is a probability query 
* Query has two parts 
  * Evidence: a subset E of variables and their instantiation e 
  * Query Variables: a subset Y of random variables
* Inference Task: P(Y|E=e) 
  * Posterior probability distribution over values y of Y 
  * Conditioned on the fact E=e 
  * Can be viewed as Marginal over Y in distribution we obtain by conditioning on e 

最常见的查询类型是概率查询

•查询分为两部分

•证据:变量的子集E及其实例化E

•查询变量:随机变量的一个子集Y

•推理任务:P(Y|E= E)

•y值的后验概率分布

•以E= E为条件

•可以看作是我们通过条件e得到的分布中的边际除以Y

![image-20221220134412179](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220134412179.png)



#### 1.4.3 Recap： Max and Argmax

![image-20221220134602171](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220134602171.png)

max是最大值

argmax是max对应的索引值

#### 1.4.4 MAP Queries （Most Probable Explanation）

https://www.jianshu.com/p/9c153d82ba2d  关于MAP

为了解释这个，我先补充一些其他知识，比如贝叶斯公式

![image-20221220135824256](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220135824256.png)

![image-20221220142339940](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220142339940.png)

然后看一下关于MAP的更详尽的解释

![image-20221220142456347](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220142456347.png)

<font color='red'>不过我认为这个也就是个定义，相对来说实际使用更重要一点</font>

* Finding a high probability assignment to some subset of variables 

* 寻找变量子集的高概率赋值

* Most likely assignment to all non-evidence variables W = V – E 

* 最有可能赋值给所有非证据变量W = V - E

* <font color='red'>记住公式</font>

  ![image-20221220135007463](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220135007463.png)

* i.e., value of w for which P(w,e) is maximum 

* Difference from probability query 

* 与概率查询的区别

  * Instead of a probability we get the most likely value for all remaining variables 
  * 我们得到的不是概率，而是所有剩余变量的最可能值

![image-20221220142759809](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220142759809.png)

![image-20221220143109428](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220143109428.png)

![image-20221220143119166](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220143119166.png)

记得，这部分用Chain Rules

![image-20221220143159479](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220143159479.png)

![image-20221220143250181](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220143250181.png)

Q3很麻烦，注意点

![image-20221220143624348](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220143624348.png)

![image-20221220143707101](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220143707101.png)

![image-20221220144042625](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220144042625.png)

Exercise1

![image-20221220144852142](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220144852142.png)

Exercise2

![image-20221220144905237](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220144905237.png)



## Lecture5 Safety Problems and Linear-Algebra

### 1. Safety and Reliability Issues

#### 1.1 Safety Concerns

* Despite the success of machine learning in many areas, serious 
  concerns have been raised in applying machine learning to real-world 
  safety-critical systems such as self-driving cars, automatic medical 
  diagnosis, etc.
* 尽管机器学习在许多领域都取得了成功，但在将机器学习应用于现实世界的安全关键系统(如自动驾驶汽车、自动医疗诊断等)时，人们提出了严重的担忧。
* Simply speaking, a learned model    is to approximate a target 
  function   . Therefore, the erroneous behaviour of exists when it is 
  inconsistent with . 
* 简单地说，学习模型就是近似一个目标函数。因此，错误的行为存在于与之不一致的时候。

![image-20221220150310957](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220150310957.png)

##### 1.1.1 Generalisation Error 一般会出现的错误

* Empirical loss:经验损失

![image-20221220150408941](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220150408941.png)

* Expected loss:预期损失

  ![image-20221220150520410](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220150520410.png)

* Generalisation error: 一般化错误 泛化误差

  ![image-20221220150553597](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220150553597.png)

* Generalisation error is closely related to the overfitting problem of 
  machine learning algorithms.
* 泛化误差与机器学习算法的过拟合问题密切相关。
* A machine learning model is overfitted if it performs well on training data samples but badly on test data samples
* 如果一个机器学习模型在训练数据样本上表现良好，但在测试数据样本上表现不佳，那么它就是过拟合的

##### 1.1.2 Adversarial Examples 对抗样本

* Adversarial examples represent another class of erroneous behaviours that also introduce safety implications. 
* 对抗性的例子代表了另一类错误行为，也会带来安全隐患。
* It represents a mis-match of the decisions made by a human and by a neural network, and does not necessarily involve an adversary.
* 它代表了人类和神经网络做出的决策的不匹配，并不一定涉及对立。

![image-20221220153331659](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220153331659.png)

![image-20221220153401032](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220153401032.png)

###### 1.1.2.1 Measurement Of Adversarial Examples

![image-20221220153533301](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220153533301.png)

![image-20221220153618690](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220153618690.png)

<font color='red'>这里涉及到后面的对抗攻击，是个小的引子</font>

##### 1.1.3 Data Poisoning

* Poisoning attack occurs when the adversary injects malicious data 
  into training process, and hence get a machine learning algorithm to 
  learn something it should not. There are two types of poisoning 
  attacks, one for data poisoning attacks and the other for backdoor 
  attacks. 
* 当对手在训练过程中注入恶意数据，从而使机器学习算法学习到它不应该学习的东西时，就会发生投毒攻击。投毒攻击有两种类型，一种是数据投毒攻击，另一种是后门攻击。

##### 1.1.4 Backdoor Attack

后门这个词在传统软件安全中出现的比较多，其为**绕过软件的安全性控制，从比较隐秘的通道获取对程序或系统访问权的黑客方法**。在软件开发时，设置后门可以方便修改和测试程序中的缺陷，但如果后门被其他人知道（可以是泄密或者被探测到后门），或是在发布软件之前没有去除后门，那么它就对软件安全造成了威胁。

![image-20221220154106117](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220154106117.png)

![image-20221220154124826](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220154124826.png)

### 2. Linear Algebra For Machine Learning  线性代数

#### 2.1 Scalar 标量

* Single number 一个独立的数字
* Represented in lower-case italic *x*  用小写斜体x表示

![image-20221220160115314](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220160115314.png)

#### 2.2 Vector 向量

* An array of numbers 
* 一组数字
* Arranged in order 
* 按次序排列
* Each no. identified by an index 
* 每一个都由索引标识
* Vectors are shown in lower-case bold 
* 向量用小写粗体表示
* If each element is in R then x is in Rn
* We think of vectors as points in space 
* 我们认为向量是空间中的点
  * Each element gives coordinate along an axis 
  * 每个元素给出沿轴的坐标

![image-20221220160452039](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220160452039.png)

#### 2.3 Matrix 矩阵

* 2-D array of numbers 二维数组
* Each element identified by two indices  每个元素由两个索引标识
* Denoted by bold typeface A   用粗体A表示
* Elements indicated as Am,n
  •E.g.
* ![image-20221220160710214](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220160710214.png)
* A[i:] is ith row of A, A[:j] is jth column of A 
* If A has shape of height m and width n with real-values then![image-20221220160902896](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220160902896.png)
* 如果A有一个高m宽n的实值形状，那么![image-20221220160905408](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220160905408.png)

![image-20221220160912642](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220160912642.png)

#### 2.4 Tensor 张量

非常像一种多维数组，但是在Python里，Tensor类提供GPU计算和自动求梯度等更多功能。

![image-20221220162737026](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220162737026.png)

![image-20221220162816493](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220162816493.png)

#### 2.5 Transpose of Matrix 矩阵的转至

* Mirror image across principal diagonal  对角线上的进行镜像

![image-20221220163039076](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220163039076.png)

* Vectors are matrices with a single column  向量是只有一列的矩阵
  * Often written in-line using transpose  通常用转置写在行内
  * ![image-20221220163130935](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220163130935.png)

* Since a scalar is a matrix with one element  ![image-20221220163209494](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220163209494.png)
* 因为标量是一个只有一个元素的矩阵![image-20221220163212086](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220163212086.png)

![image-20221220163256660](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220163256660.png)

#### 2.6 Linear Transformation 线性转换

![image-20221220163353856](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220163353856.png)

![image-20221220163439798](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220163439798.png)

#### 2.7 Identity and Inverse Matrices 恒等与逆矩阵

* Matrix inversion is a powerful tool to analytically solve Ax=b  
* 逆矩阵是解决Ax=b的有效工具
* Needs concept of Identity matrix 
* 需要单位矩阵的概念
* Identity matrix does not change value of vector 
* 单位矩阵不改变向量的值
* when we multiply the vector by identity matrix 
* 当我们用单位矩阵乘以这个向量

![image-20221220163925226](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220163925226.png)

##### 2.7.1 Matrix Inverse 逆转矩阵

![image-20221220164037705](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221220164037705.png)

#### 2.8 Norms 模

* Used for measuring the size of a vector 
* 使用测量向量的大小
* Norms map vectors to non-negative values 
* 模将向量映射到非负值
* Norm of vector x is distance from origin to x 
* 向量x的模是从原点到x的距离
  * It is any function f that satisfies:

![image-20221221122203515](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221122203515.png)



#### 2.9 LPNorm（P是上标）

![image-20221221122325166](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221122325166.png)

![image-20221221122602752](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221122602752.png)

![image-20221221122615592](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221122615592.png)

![image-20221221122652789](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221122652789.png)

![image-20221221122726162](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221122726162.png)



#### 2.10 Size of Matrix 矩阵的大小

![image-20221221122912030](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221122912030.png)

![image-20221221122920866](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221122920866.png)



### 3. Introduction to Scientific Python 

**<font color=red>主要是关于Python的相关方法,直接看PPT吧，主要内容从Lecture5到Lecture6的前半段</font>**



#### 3.1 Numpy

* Fundamental package for scientific computing with Python 
* 使用Python进行科学计算的基本包
* N-dimensional array object 
* 一个N维数组的对象
* Linear algebra, Fourier transform, random number capabilities 
* 线性代数，傅里叶变换，随机数能力
* Building block for other packages (e.g. Scipy) 
* 其他包的构建块(例如Scipy)
* Open source
* 开放源码



## Lecture6&7&8&9&10 Decision-Tree-Learning

我先在这里解释一下我自学的决策树，我觉得老师讲的好乱啊

https://blog.csdn.net/jiaoyangwm/article/details/79525237?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522167162688516782388072538%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=167162688516782388072538&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_positive~default-1-79525237-null-null.142

参照上述连接



### 1. The Decision Tree Representation 决策树的表示方法

![image-20230121151214582](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230121151214582.png)

<font color=red size=5>通过不断的决策将事物进行分类，最终得到我们需要的结果</font>

![image-20230121151403135](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230121151403135.png)

### 2. The standard top-down approach to learning a tree  学习树的标准自顶向下方法

![image-20221221164228436](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221164228436.png)

![image-20221221164250369](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221164250369.png)

![image-20221221164357921](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221164357921.png)



![image-20221221164616038](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221164616038.png)

![image-20221221164635236](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221164635236.png)



#### 3.1 Step(1): FindBestSplit寻找分歧

因为决策树是一个分类的方法，所以一开始我们寻找事务中的分歧Split



##### 3.1.1 Candidate splits on numeric features 数字特征上候选类的分歧

* **Given a set of training instances D and a specific feature Xi**
* **给一个训练实例D和一个特定的特征Xi**
  * Sort the values of Xi in D 
  * 对在D中的Xi的值进行排序
  * Evaluate split thresholds in intervals between instances of different classes
  * 评估分割的阈值在不同类实例之间的间隔

![image-20221221170211161](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221170211161.png)

* could use midpoint of each considered interval as the threshold 
* 我们会使用间隔的中点作为阈值threshold
* C4.5 instead picks the largest value of Xiin the entire training set that does not exceed the midpoint 
* C4.5则选择整个训练集中xi的最大值，且不超过中点



![image-20221221171004628](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221171004628.png)

![image-20221221171012513](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221171012513.png)

![image-20221221171152148](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221171152148.png)



#### 3.2 Step(2): DetermineCandidateSplit 决定候选分歧

##### 3.2.1 Find the best split

* How should we select the best feature to split on at each step? 
* 我们应该如何在每一步中选择最好的特征进行分割?
* **Key hypothesis: the simplest tree that classifies the training instances accurately will work well on previously unseen instances** 
* **关键假设:对训练实例进行准确分类的最简单的树在以前未见过的实例上也能很好地工作**

##### 3.2.2 Occam‘s Razor 奥卡姆剃刀

<font color='red'>如无必要，勿增实体</font>

![image-20221221172242569](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221172242569.png)

•短模型(即小树)比长模型少

**•短模型不太可能偶然地很好地拟合训练数据**

**•长模型更有可能巧合地很好地拟合训练数据**

##### 3.2.3 Finding the best splits

 因为可以决定训练数据的最小决策树的寻找是一个NP问题，**所以我们将使用信息理论的启发式来贪婪地选择分割**

* Instead, we’ll use an information-theoretic heuristics to greedily choose splits 

![image-20221221172341197](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221172341197.png)

#### 3.3 Recap: Expected Value(Finite Case) 期望值

* 数学期望

![image-20221221172526992](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221172526992.png)

![image-20221221172533374](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221172533374.png)



### 3.Information theory background 

![image-20230121153705605](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230121153705605.png)

![image-20230121153721207](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230121153721207.png)

![image-20230121153728566](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230121153728566.png)

![image-20230121153742506](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230121153742506.png)

![image-20230121153941598](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230121153941598.png)

* 直观上，如果一个特征具有更好的分类能力，或者说，按照这一特征将训练数据集分割成子集，使得各个子集在当前条件下有最好的分类，那么就更应该选择这个特征。
* **信息增益就能够很好地表示这一直观的准则。**
* 什么是信息增益呢？**<font color=red>在划分数据集之前之后信息发生的变化成为信息增益</font>**，知道如何计算信息增益，我们就可计算每个特征值划分数据集获得的信息增益，获得信息增益最高的特征就是最好的选择。
* **熵定义为信息的期望值**

![image-20230121154338689](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230121154338689.png)







### 4. Entropy and information gain  熵和信息增益

**<font color='red'>这个同样在上述链接有解释</font>**

#### 4.1 Entropy 熵

* **Entropy is a measure of uncertainty associated with a random** 
  **variable**
*  **熵是与随机变量相关的不确定性的度量**
*  **同样也是信息增益的度量**
* **<font color=red>Defined as the expected number of bits required to communicate the value of the variable</font>** 
* **定义为传递变量值所需的预期比特数**

![image-20221221195853302](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221195853302.png)

##### 4.1.2 Conditional Entropy 条件熵

* **Conditional entropy(or equivocation) quantifies the amount of information needed to describe the outcome of a random variable given that the value of another random variable is known.**
* **条件熵(或模棱两可)在已知另一个随机变量值的情况下，量化描述一个随机变量结果所需的信息量。**
* ![image-20221221200135389](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221200135389.png)

![image-20221221201952978](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221201952978.png)

![image-20221221202002119](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221202002119.png)

![image-20221221202018997](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221202018997.png)

#### 4.2 Information Gain 信息熵

* **信息增益**：信息增益是相对于特征而言的。所以，特征A对训练数据集D的信息增益g(D,A)，定义为集合D的经验熵H(D)与特征A给定条件下D的经验条件熵H(D|A)之差，即：
* ![image-20230121180646423](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230121180646423.png)
* **因为我们需要根据特征进行分类，分类往往要选取不同的特征，该怎么评价一个特征选的好不好呢，就用信息增益。在不同的特征下，取信息增益的最大值为最佳特征**

![image-20230121180626616](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230121180626616.png)

* Choosing splits in ID3: select the split S that most reduces the conditional entropy of Y for training set D
* ID3中选择分割:为训练集D选择使Y的条件熵减少最多的分割S
* **将无序数据变得更加有序，但是各种方法都有各自的优缺点，信息论是量化处理信息的分支科学，在划分数据集前后信息发生的变化称为信息增益，获得信息增益最高的特征就是最好的选择**

![image-20221221202249262](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221202249262.png)

![image-20221221202536762](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221202536762.png)

![image-20221221202849584](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221202849584.png)

![image-20221221202856763](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221202856763.png)

![image-20221221202911110](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221202911110.png)

![image-20221221202925632](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221202925632.png)

![image-20221221202933934](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221202933934.png)

**<font color=red size=5>这里就是计算两个不同特征的 information gain来判断选择哪一个特征作为特征值,结果显示Humidity更适合做特征值</font>**

![image-20221221203002165](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221203002165.png)

##### 5.1 One Limitation Of Information Gain 信息熵的一种限制

* **information gain is biased towards tests with many outcomes**
* **信息获取偏向于有多种结果的测试** 
* e.g. consider a feature that uniquely identifies each training instance 
* 考虑一个唯一标识每个训练实例的特征
  * splitting on this feature would result in many branches, each of which is  “pure” (has instances of only one class) 
  * 在这个特性上的分裂将导致许多分支，每个分支都是“纯”的(只有一个类的实例)
  * maximal information gain! 
  * 最大的信息增益!

##### 5.2 Gain Ratio 信息增益比

* **信息增益有时会倾向于有更多取值范围的那个特征（如，是否有工作的取值范围为“是”or“否”；信贷情况的取值范围为“一般”，“好”，“非常好”，此时 3 > 2，有可能会造成 “信贷情况” 的信息增益大于 “是否有工作” 这个特征 ）**

* To address this limitation, C4.5 uses a splitting criterion called gain 
  ratio 
* 为了解决这一限制，C4.5使用了一种称为**增益比**的分裂准则
* Gain ratio normalizes the information gain by the entropy of the split 
  being considered 
* 增益比通过所考虑的分裂的熵将信息增益归一化

![image-20221221203729874](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221203729874.png)

![image-20221221203901264](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221203901264.png)

### 5. Types of decision-tree splits  决策树分割的类型

#### 5.1 (3) Stopping criteria of decision trees 停止标准（就是满足条件停止分类）

* We should form a leaf when 
* 我们应该形成一个叶子结点
  * all of the given subset of instances are of the same class 
  * 所有给定实例的子集都是同一个类
  * we’ve exhausted all of the candidate splits 
  * 我们耗尽了所有的候选人分支
* <font color=red size=5>简单来说，就是确定已经无法分类</font>

### 6. Accuracy of Decision Tree 决策树的准确度

#### 6.1 Definition of Accuracy and Error 准确度和误差的定义

* **Given a set D of samples and a trained model M, the accuracy is the percentage of correctly labeled samples. That is,** 

* 给定一组样本D和一个训练过的模型M，**准确率是正确标记样本的百分比。**

* ![image-20221221210538385](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221210538385.png)

  

  ![image-20221221210721931](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221210721931.png)

* lx是样本x的真实标签，M(x)是预测x的标签

* **Error is a dual concept of accuracy.**

* ![image-20221221210937550](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221210937550.png)



#### 6.2 How can we assess the accuracy of a tree? 如何评价一个树的准确性

* Can we just calculate the fraction of training instances that are correctly classified? 
* 我们能计算出正确分类的训练实例的比例吗?
* Consider a problem domain in which instances are assigned labels at random with P(Y = t) = 0.5 
* 考虑一个问题域，其中实例被随机分配为P(Y = t) = 0.5的标签
  * how accurate would a learned decision tree be on previously unseen instances? 
  * 对于以前未见过的实例，习得的决策树有多准确?
    * Can never reach 1.0. 
  * how accurate would it be on its training set? 
  * 它在训练集上有多准确?
    * Can be arbitrarily close to, or reach, 1.0 if model can be very large. 
    * 如果模型可以很大，可以任意接近或达到1.0。
  
* To get an unbiased estimate of a learned model’s accuracy, we must 
  use a set of instances that are held-aside during learning 
* 为了对学习模型的准确性进行无偏倚的估计，我们必须使用一组在学习期间搁置的实例    <font color='red'>其实就是测试集</font>
* ![image-20221221211957832](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221211957832.png)



### 7. Pruning and Validation Dataset 剪枝和验证数据集

#### 7.1 Stopping criteria 停止标准

* We should form a leaf when 

  * all of the given subset of instances are of the same class 

  * we’ve exhausted all of the candidate splits 
  
  * 我们已经用尽了所有的候选人分裂

 So How to prune back the tree?

#### 7.2 Pruning in C4.5 在C4.5剪枝

* **Split given data into training and validation(tuning) sets** 
* **将给定的数据分割为训练集和验证(调优)集**
* a validation set (a.k.a. tuning set) is a subset of the training set that is held aside 
* 验证集(也称为调优集)是训练集的一个子集，它被放在一边
  * not used for primary training process (e.g. tree growing) 
  * 不用于初级的训练过程
  * but used to select among models (e.g. trees pruned to varying degrees) 
  * 但用于在模型之间进行选择(例如，修剪不同程度的树木)

![image-20221221212811169](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221212811169.png)

* Split given data into training and validation (tuning) sets 
* 将给定的数据分割为训练集和验证(调优)集
* Grow a complete tree
* 长成一棵完整的树
* do until further pruning is harmful 
  * evaluate impact on tuning-set accuracy of pruning each node
  *  评估修剪每个节点对调优集精度的影响
  * greedily remove the one that least reduces tuning-set accuracy
  *  贪婪地删除最小降低调优集精度的一个

**<font color='red'>就是测试集的作用</font>**



### 8. Overfitting

- **过拟合**是指模型在训练集上表现很好，到了验证和测试阶段就很差，即模型的**泛化能力很差**。
- **<font color=blue size=5>arg max function(x)表示在function取最大值时，x对应的值</font>**

![image-20221221213355110](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221213355110.png)

![image-20221221213447803](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221213447803.png)

![image-20221221213459038](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221213459038.png)

![image-20221221213509082](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221213509082.png)

![image-20221221213527471](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221213527471.png)

<font color=red size=5>人们实际上并不清楚正确的模型是什么，但是这里的测试集数据都出现在训练模型和正确模型的交点附近，所以认为是Overfits</font>

![image-20221221220534020](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221220534020.png)

* RMS: root mean square, i.e., the square root of the mean square
* 均方根:均方根，即均方根的平方根

![image-20221221220541688](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221220541688.png)

* **Generalization 泛化 是指训练好的模型在前所未见的数据上的性能好坏。**
* ![image-20230121215840627](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230121215840627.png)

![image-20221221220550522](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221220550522.png)

#### 8.1 Prevent Overfitting

* **cause: training error and expected error are different** 
* **原因:训练误差与预期误差不一致**
  * there may be noise in the training data 
  * 训练数据中可能有噪声
  * training data is of limited size, resulting in difference from the true distribution 
  * 训练数据规模有限，与真实分布存在差异
  * the larger the hypothesis class, the easier to find a hypothesis that fits the difference between the training data and the true distribution 
  * 假设类越大，就越容易找到一个符合训练数据与真实分布之间差异的假设
* prevent overfitting: 
  * cleaner training data help! 
  * 清理训练数据是有帮助的
  * more training data help! 
  * 更多的训练数据好的
  * throwing away unnecessary hypotheses helps! (Occam’s Razor) 
  * 抛弃不必要的假设

#### 8.2 Overfitting in Decision Tree

![image-20221221221128824](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221221128824.png)

在训练集上表现很好，但是在真是情况表现不好

<font size=5>Example1：overfitting with noisy data </font>

![image-20221221221448988](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221221448988.png)

先解释一下这个问题： 1. 我们的目标是求出目标值 ![image-20230121220125930](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230121220125930.png)

* **在correct tree中，我们应该判断特征X1和特征X2，然后停止生成子树，此时正确率为100，得出结果。**
* **在错误的模型中，因为数据错误且模型过于拟合训练数据导致生成了错误模型**
  * **具体的表示是本该在X2处停下的决策树，继续进行生成。**

![image-20221221221717427](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221221717427.png)

因为X2因为有noise导致了存在X1=True,X2=Flase, Y=True的情况，所以存在有多余的树枝

![image-20221221222512312](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221222512312.png)

所以训练集5/6 真实情况100%

![image-20221221222604162](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221222604162.png)

![image-20221221222615103](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221222615103.png)



<font size=5>Example2：overfitting with noise-free data 不知道具体噪声在哪的情况</font>

![image-20221221224248663](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221224248663.png)

![image-20221221224254857](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221224254857.png)

* 在这里我们可以看到一些其他的东西
  * 因为不确定位置的数据错误，导致X3这个特征完美符合结果，从而得出训练集的结果完美符合正确结果，而实际值出错
  * **这里的0.5和0.66上文有给**

![image-20221221224301808](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221224301808.png)

如图，正常来说上述训练模型对X3应该有100%的准确度，但是实际情况是50%



* **下面的是另一种情况，此时的模型如下图所示**

![image-20221221224354515](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221224354515.png)

如图，正常情况该模型对Y应该有60%的正确率，但实际是66%

![image-20221221224503976](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221221224503976.png)

* **得出最后的结果, M1过拟合**
* 因为训练集是有限的样本，可能会有偶然与目标概念相关的特征(组合)

#### 8.3 Avoiding overfitting in DT learning 

* two general strategies to avoid overfitting 
  * early stopping: stop if further splitting not justified by astatistical test 
  * 早期停止:如果进一步的分裂没有被统计测试证明是合理的，就停止
  * **<font color=red size=5>这种方法往往通过限制树的高度来执行</font>**
    * Quinlan’s original approach in ID3 
  * post-pruning: grow a large tree, then prune back some nodes
  * 后修剪:种植一棵大树，然后修剪一些节点
    * more robust to myopia of greedy tree learning 
  * **<font color=red size=5>使用置信度不够的子节点使用叶子节点来代替,进行标记，标记后在后剪枝的过程中删除, 这个更常用，因为精确的估计树应该何时停止增长很难</font>**

## Lecture10 K-NN

https://blog.csdn.net/u010608296/article/details/120640343?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522167171093816800188548770%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=167171093816800188548770&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_click~default-1-120640343-null-null.142

-- K-NN

![image-20221222121030302](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222121030302.png)

### 1. Nearest-Neighbor Classification 最邻近分类法

* learning stage 学习阶段
  * given a training set (x(1), y(1)) ... (x(m) , y(m)), do nothing  什么也不做
    * (it’s sometimes called a lazy learner)
    * (有时也被称为懒惰学习者)
* classification stage 分类阶段
  * given: an instance x(q)to classify 给一个具体实例去分类
  * <font color=red size=5>相当于给一个集合来辅助之后的情况寻找相似点</font>
  * find the training-set instance x(i)that is most similar to x(q)
  * 找到与x(q)最相似的训练集实例x(i)
  * return the class value y(i) 
  * 返回类值y(i)

#### 1.1 Nearest Neighbor 最邻近

* **When to Consider  何时考虑**
  * **Less than 20 attributes per instance 每个实例少于20个属性**
  * **Lots of training data  有很多的训练数据**
* **Advantages** 
  * **Training is very fast 训练速度很快**
  * **Learn complex target functions 学习复杂的目标函数**
  * **Do not lose information 不会丢失信息**
* **Disadvantages**  
  * **Slow at query time 查询缓慢 -- 因此我们在后文使用K-D-Tree来增加速度**
  * **Easily fooled by irrelevant attributes   容易被不相关的属性愚弄**

![image-20221222120834805](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222120834805.png)

**Voronoi图:每个多面体表示在每个训练实例的最近邻域的特征空间区域**



![image-20221222121147885](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222121147885.png)

![image-20230121223126999](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230121223126999.png)

![image-20230121223148396](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230121223148396.png)



#### 1.2 The Defination of K-NN

* Classification task
  * given: an instance x(q)to classify  给一个实例x(q)来进行分类
  * find the k training-set instances (x(1), y(1))... (x(k), y(k)) that are the most similar to x(q)
  * 求k个训练集实例(x(1)， y(1))…(x(k) y(k))和x(q)最相似
  * return the class value 
  * ![image-20221222121449548](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222121449548.png)
  * (i.e. return the class that have the most number of instances in the k training 
    instances
  * 返回k个训练实例中实例数最多的类
  
  ![image-20230121231544822](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230121231544822.png)

##### 1.2.1 How can we determine similarity/distance  如何判断属性之间的距离

* **Suppose all features are categorical  假设所有的特征都是分类的**
  * **Hamming distance (or L0norm)**: count the number of features for which two instances differ
  * **汉明距离：  计算两个实例不同的特征的数量**
  * 实例是一个具体的例子，特征是用于分类的，一个实例可以有多个特征
* Example: X = (Weekday, Happy?, Weather)  Y = AttendLecture? 
  * D : in the table
  * New instance: <Friday, No, Rain>
  * Distances = {2, 3, 1, 2} 
  * For 1-nn, which instances should be selected? 
  * For 2-nn, which instances should be selected? 
  * For 3-nn, which instances should be selected?

![image-20221222124416941](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222124416941.png)



![image-20221222124448472](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222124448472.png)

**Euclidean Distance 欧式距离**

**Manhattan Distance 曼哈顿距离**

![image-20230121232403469](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230121232403469.png) 

![image-20230121232629796](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230121232629796.png)

![image-20221222124654107](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222124654107.png)

![image-20221222124708205](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222124708205.png)

###### 1.2.1.1How can we determine similarity/distance 

* **这种是对于不同的特征使用不同的方法，面对连续特征和间断特征使用不同的值**

![image-20230121232921248](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230121232921248.png)

##### 1.2.2 Standardizing numeric features  标准化数字特征

* 原因：因为不同的特征往往会有不同的规格，这些数据往往是因为用于描述不同种类的数据而差异巨大，比如楼层和距离市中心的距离为两个特征，楼层可以是1-10，市中心距离可能有几千米
* **这样的差别就会影响最终的工作效率. 所以, 我们要提高效率, 特征的标准化就可以帮上忙.我们在机器学习训练之前, 先对数据预先处理一下, 取值跨度大的特征数据, 我们浓缩一下, 跨度小的括展一下, 使得他们的跨度尽量统一.**

* given the training set D, determine the mean and stddev for feature xi
* 给定训练集D，确定特征xi的均值和stddev

![image-20221222125135200](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222125135200.png)

* standardize each value of feature xias follows 
* **标准化特征的每个值，如下所示**
* ![image-20221222125210953](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222125210953.png)
* do the same for test instances, using the same 𝜇and 𝜎derived from the training data 
* 对测试实例做相同的事情

#### 1.3 Speeding up k-NN

<Font size=5>Issues</font>

* Choosing k
  * **Increasing k reduces variance, increases bias** 
  * **增加k减少方差，增加偏差**
* For high-dimensional space, problem that the nearest neighbor may not be very close at all! 
* 对于一些高维空间，相邻的点可能并不是这么多
* Memory-based technique. Must make a pass through the data for each classification. This can be prohibitive for large data sets.
* 基于内存的技术。必须对每个分类的数据进行遍历。这对于大型数据集来说可能是不可取的。

![image-20221222130205278](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222130205278.png)

* Given sample S = ((x1,y1),...,(xm,ym)) and a test point x, 
* 给定样本S = ((x1,y1)，…，(xm,ym))和测试点x，
* it is to find the nearest k neighbours of x
* 就是找到x的k个最近邻居。
* **Note: for the algorithms, dimensionality N, i.e., number of features, is crucial.** 
* **对于算法，维数N，即特征的数量，是至关重要的。**

![image-20230121233755406](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230121233755406.png)

* k-NN is a “lazy” learning algorithm – does virtually nothing at training time 
* k-NN是一种“懒惰”学习算法——在训练时几乎什么都不做
* **but classification/prediction time can be costly when the training set is large** 
* **但是当训练集很大时，分类/预测时间会很昂贵**

![image-20230121233856960](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230121233856960.png)

* two general strategies for alleviating this weakness 
* 缓解这一弱点的两种一般策略
  * **don’t retain every training instance (edited nearest neighbor)** 
  * **不要保留每个训练实例(已编辑的最近邻)**
  * **pre-processing. Use a smart data structure to look up nearest neighbors (e.g. a k-d tree)** 
  * **预处理。使用智能数据结构查找最近的邻居(例如k-d树)**

![image-20230121234310108](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230121234310108.png)

##### 1.4.1 Edited instance-based learning 编辑基于实例的学习

![image-20230121234339436](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230121234339436.png)

##### 1.4.2  K-D-Tree  

https://blog.csdn.net/qq_33143379/article/details/80962326?ops_request_misc=&request_id=&biz_id=102&utm_term=k-d%20tree&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduweb~default-0-80962326.142

  k-d-tree（即k-dimensional tree）是一棵形如二叉树的一种非常重要的空间划分数据结构，尤其在多维数据访问中有重要应用，它能显著降低运算次数、提高运算效率；**主要应用于多维空间关键数据的搜索（如：范围搜索和最近邻搜索）。**

* <font color=red>注意：这是一个对K-NN进行预处理的方法</font>

* a k-d tree is similar to a decision tree except that each internal node 
* 一个k-d tree与决策树非常相像除了每个内部节点不同
  * **stores one instance**  
  * **存储一个实例**
  * **splits on the median value of the feature having the highest variance** 
  * **对具有最高方差的特征的中值进行分割**

![image-20221222163327385](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222163327385.png)

![image-20221222163810670](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222163810670.png)

![image-20221222163824803](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222163824803.png)

![image-20221222163833621](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222163833621.png)

* **这样我们就在一个实例中划分了不同的区域，使得在后续寻找邻近点时更加便捷。**

###### 1.4.2.1 Finding nearest neighbors with a k-d tree

* use branch-and-bound search 
* 使用分支和边界搜索
* priority queue stores 
* 优先队列存储
  * nodes considered
  * 考虑节点
  * lower bound on their distance to query instance 
  * 它们到查询实例距离的下界
* lower bound given by distance using a single feature 
* 下界由使用单一特征的距离给出
* average case: O(log2m) 
* 平均情况:O(log2m)
* worst case: O(m) where m is the size of the training-set
* 最坏情况:O(m)，其中m是训练集的大小

![image-20221222164439045](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222164439045.png)

![image-20221222164705166](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222164705166.png)



* EXAMPLE：这个是老师上课给的例子，讲真每太看懂
* ![image-20230122000651357](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122000651357.png)

![image-20230122000657014](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122000657014.png)

![image-20230122000708043](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122000708043.png)

![image-20230122000714796](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122000714796.png)

![image-20230122000723198](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122000723198.png)

![image-20230122000736930](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122000736930.png)

![image-20230122000820587](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122000820587.png)

![image-20230122000843597](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122000843597.png)

* Example 这个例子更加通俗易懂

![image-20230122001051619](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122001051619.png)

![image-20230122001106664](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122001106664.png)





#### 1.5 Variants of K-NN   K-NN的变体

* learning stage
* 学习阶段 
  *  given a training set (x(1), y(1)) ... (x(m) , y(m)), do nothing 
  *  给定一个训练集(x(1)， y(1))，…(x(m) y(m))什么都不做
    * (it’s sometimes called a lazy learner) 
* classification stage
* 分类阶段
  * given: an instance x(q)to classify
  * 给定:一个实例x(q)进行分类
  * find the k training-set instances (x(1), y(1))... (x(k), y(k)) that are most similar to x(q)
  * 求k个训练集实例(x(1)， y(1))…(x(k) y(k))和x(q)最相似
  * return the value ![image-20221222165537629](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222165537629.png)



![image-20221222165442929](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222165442929.png)

**很明显，相比于Nearest-Neighbor Classification，这里返回的值是周围相似值的平均值**

* find the k training-set instances (x(1), y(1))... (x(k), y(k)) that are most similar to x(q)
* 求k个训练集实例(x(1)， y(1))…(x(k) y(k))和x(q)最相似

##### 1.5.1 Distance-Weighted Nearest Neighbor 最近临近点的距离权重

* We can have instances contribute to a prediction according to their distance from x(q) 
* 通过每个实例到x(q)的距离来预测它对目标值的贡献
* classification: 

![image-20221222170308996](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222170308996.png)

##### 1.5.2 Irrelevant features in instance-based learning  基于实例的学习中不相关的特征

* here’s a case in which there is one relevant feature x1and a 1-NN rule classifies each instance correctly 
* 这里有一个案例，其中有一个相关的特征x1，并且1-NN规则正确地分类了每个实例
* consider the effect of an irrelevant feature x2on distances and nearest neighbors
* 考虑一个不相关的特征x2对距离和最近邻居的影响

![image-20221222172644721](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222172644721.png)

* Can you find a point (a,b) which is red, if classified only according to feature x1, and is green, if classified according to both features? 
* 如果只根据特征x1分类，你能找到一个点(a,b)，它是红色的，如果根据两个特征分类，它是绿色的吗?

##### 1.5.3 Locally weighted regression  局部加权回归

* One way around this limitation is to weight features differently 
* 绕过这种限制的一种方法是对特征进行不同的权重
* locally weighted regression is one nearest-neighbor variant that does this
* 局部加权回归是一种最近邻方法的变种

* prediction task 
  * given: an instance x(q) to make a prediction for 
  * find the k training-set instances (x(1), y(1)) ... (x(k), y(k)) that are most similar to x(q)
  * 求k个训练集实例(x(1)， y(1))…(x(k) y(k))和x(q)最相似
  * return the value ![image-20221222173212414](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222173212414.png)

![image-20221222173130651](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222173130651.png)

![image-20221222173314958](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222173314958.png)

#### 1.6 Discussion  Advantage and Disadvantage of instance-based learning  基于实例的学习

* simple to implement 
* 易于实施
* “training” is very efficient 
* 训练高效
* adapts well to on-line learning 
* 适应在线学习
* robust to noisy training data (when k > 1) 
* 对噪声训练数据的鲁棒性(当k > 1)
* often works well in practice 
* 在练习中工作良好



* sensitive to range of feature values 
* 对特征值范围敏感
* sensitive to irrelevant and correlated features, although ... 
* 对不相关和相关的特征很敏感，尽管…
  * there are variants (such as locally weighted regression) that learn weights for different features
  * 有一些变体(如局部加权回归)可以学习不同特征的权重
* classification/prediction can be inefficient, although ...
* 分类/预测可能效率很低，尽管……
  * edited methods and k-d trees can help alleviate this weakness 
  * 编辑过的方法和k-d树可以帮助缓解这个弱点
* doesn’t provide much insight into problem domain because there is no explicit model 
* 因为没有明确的模型，所以无法深入了解问题领域







## Lecture12 Linear and Logistic Regression

### 1. Recap what we learned

#### 1.1 Inductive Bias 归纳偏差

https://blog.csdn.net/qq_39478403/article/details/121107057?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522167174638116800182166731%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=167174638116800182166731&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_positive~default-1-121107057-null-null.142

**<font color='red'>归纳偏置可以理解为，从现实生活中观察到的现象中归纳出一定的规则 (heuristics)，然后对模型做一定的约束，从而可以起到 “模型选择” 的作用，类似贝叶斯学习中的 “先验”。</font>**

![image-20221222220212870](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222220212870.png)

* **inductive bias is the set of assumptions a learner uses to be able to predict yi for a previously unseen instance xi** 
* **归纳偏差是学习者能够使用的一组假设来预测未见过的实例xi的yi**
* two components 
  * **hypothesis space bias**: determines the models that can be represented 
  * 假设空间偏差:决定可以表示的模型
  * **preference bias**: specifies a preference ordering within the space of models 
  * 偏好偏差:指定模型空间内的偏好顺序
* in order to generalize (i.e. make predictions for previously unseen instances) a learning algorithm must have an inductive bias 
* 为了推广(即对以前未见过的实例进行预测)，学习算法必须具有归纳偏差
* **归纳偏差往往用于泛化**

![image-20221222215726282](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222215726282.png)

![image-20230122100531048](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122100531048.png)

![image-20221222215810913](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222215810913.png)

![image-20221222215923501](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222215923501.png)





### 2. Linear and Logistic Regression

#### 2.1 Recap: dot product in linear algebra

![image-20221222223006477](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222223006477.png)



#### 2.2 Linear Regression 线性回归

https://blog.csdn.net/suotanyu1595/article/details/120362070?ops_request_misc=&request_id=&biz_id=102&utm_term=%E7%BA%BF%E6%80%A7%E5%9B%9E%E5%BD%92&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduweb~default-0-120362070.142

* 关于回归算法和分类算法
* 其实回归算法是相对分类算法而言的，与我们想要预测的目标变量y的值类型有关。如果目标变量y是**分类型变量**，如预测用户的性别（男、女），预测月季花的颜色（红、白、黄……），预测是否患有肺癌（是、否），那我们就需要用分类算法去拟合训练数据并做出预测；如果y是**连续型变量**，如预测用户的收入（4千，2万，10万……），预测员工的通勤距离（500m，1km，2万里……），预测患肺癌的概率（1%，50%，99%……），我们则需要用回归模型。
* 聪明的你一定会发现，有时分类问题也可以转化为回归问题，例如刚刚举例的肺癌预测，我们可以用回归模型先预测出患肺癌的概率，然后再给定一个阈值，例如50%，概率值在50%以下的人划为没有肺癌，50%以上则认为患有肺癌。
* 这种分类型问题的回归算法预测，最常用的就是逻辑回归，后面我们会讲到。
  

![image-20221222223744981](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222223744981.png)

* 线性回归一般分为一维线性回归和多元线性回归
* 具体链接：https://blog.csdn.net/iqdutao/article/details/109402570?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522167174844416800188526203%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=167174844416800188526203&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_positive~default-1-109402570-null-null.142

![image-20221222224052640](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222224052640.png)

* xi的错误率
* 所有训练实例的空间错误率
* 所有训练实例的平均空间错误率
* **<font color=red>上述函数为损失函数</font>**



* **关于错误率，即损失函数，通过上图的公式寻找最小的损失函数**

![image-20221222224206398](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222224206398.png)

#### 2.3 Organise feature data into matrix 在矩阵中组织特征数据

![image-20221222225037801](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222225037801.png)

#### 2.4 Transform input matrix with weight vector 通过权重向量转换输入矩阵

* 给每一个特征设置权重

![image-20221222225836676](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222225836676.png)

 ![image-20221222225850692](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222225850692.png)

#### 2.5 Error Representation 误差表示

![image-20221222230020183](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222230020183.png)

<font color=red size=5>这样我们就把计算**损失函数，即错误率的公式换成了另一个表现形式，两个矩阵相减**</font>

![image-20221222230341898](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222230341898.png)

### 3. Variant: Linear regression 线性回归的变体

#### 3.1 Variant: Linear regression with bias  变体:有偏差的线性回归

![image-20221222230630418](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222230630418.png)

![image-20221222230638587](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222230638587.png)

**这里是通过上述经过权重向量转换后的input，将其加入bias的影响**

#### 3.2 Variant: Linear regression with lasso penalty  变体:线性回归与套索惩罚

https://blog.csdn.net/matrix_studio/article/details/121115119?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522167175057616800182754280%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=167175057616800182754280&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_click~default-1-121115119-null-null.142

![image-20221222231052438](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222231052438.png)

Lasso同样是线性回归的一种变体。而文档中指出，它是一种能让参数ω \omegaω稀疏的模型（作用）。

<font color=red>不懂，但好像不是很重要</font>

#### 3.3 Variant: Evaluation Metrics 变体：评价标准

* Root mean squared error (RMSE) 
* 均方根误差(RMSE)
* Mean absolute error (MAE) – average L1error 
* 平均绝对误差(MAE) -平均l1误差
* R-square (R-squared) 
* r平方(平方)
* Historically all were computed on training data, and possibly adjusted after, but really should cross-validate 
* 从历史上看，所有这些都是根据训练数据计算的，可能在训练后进行调整，但实际上应该进行交叉验证

### 4.Linear classification 线性分类

![image-20221222231805703](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222231805703.png)

* 根据f(x)的线进行分类

![image-20221222231922060](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222231922060.png)

* Piecewise Linear model 𝓗 分段线性模型
* <font color='red'>就是针对wTx的值，对y进行分类</font>

![image-20221222232201226](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222232201226.png)

* **loss = 0, i.e., no loss, when the classification is the same as its label.  loss =1, otherwise.** 
* **如果loss=0，则没有loss，所以分类拥有相同的标签。否则loss=1，标签不同**

![image-20221222232344487](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221222232344487.png)

缺点：1. 对异常值不敏感	2.难以优化



### 5. Logistic Regression 逻辑回归

https://blog.csdn.net/weixin_55073640/article/details/124683459?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522167179893616800213012717%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=167179893616800213012717&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_positive~default-2-124683459-null-null.142

逻辑回归也称作logistic回归分析，是一种广义的线性回归分析模型，属于机器学习中的监督学习。其推导过程与计算方式类似于回归的过程，但实际上主要是用来解决**二分类问题**（也可以解决多分类问题）。通过给定的n组数据（训练集）来训练模型，并在训练结束后对给定的一组或多组数据（测试集）进行**分类**。其中每一组数据都是由p 个指标构成。


![image-20221223123853382](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223123853382.png)

 如上图所示，其中点的个数是样本个数，两种颜色代表两种指标。这个直线可以看成经这些样本训练后得出的划分样本的直线。那么对于之后的样本的p1与p2的值，就可以根据这条直线来判断它属于哪一类了。

**<font color='red'>感觉就是画条线将数据集分成两个类</font>**

#### 5.1.Introduction of Logistic Regression 

* 从本质上来说，逻辑回归训练后的模型是平面的一条直线（p=2),或是平面（p=3)，超平面（p>3)。并且这条线或平面把空间中的散点分成两半，属于同一类的数据大多数分布在曲线或平面的同一侧。
* ![image-20230122111531298](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122111531298.png)

<font size=5>Why logistic regresion?</font>

![image-20230122111624408](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122111624408.png)

* It's tempting to use the linear regression output as probabilities
* 我们很容易将线性回归输出作为概率
* but it's a mistake because the output can be negative and greater than 1, whereas probability can not. 
* 但这是一个错误，因为输出可以是负的并且大于1，而概率不能。

![image-20221223124528006](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223124528006.png)

![image-20221223124539077](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223124539077.png)

**假设以下例子：**

![image-20221223132327710](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223132327710.png)

所以我们得到了以下的公式

![image-20221223124601639](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223124601639.png)

* sigmoid prediction  S形预测
* Squash the output of the linear function 压缩线性函数的输出
* ![image-20221223131610312](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223131610312.png)

* New optimization objective 一种新的优化对象
* ![image-20221223131942394](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223131942394.png)





<font size=5>Linear classification: logistic regression </font>

![image-20221223132007412](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223132007412.png)

![image-20221223132430645](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223132430645.png)

* 关于上述公式的推导过程
* ![image-20230122112124210](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122112124210.png)

#### 5.2 最大似然估计

![image-20221223132836842](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223132836842.png)

![image-20221223132850334](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223132850334.png)

![image-20221223135113584](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223135113584.png)

* 边界Bounded
* 对称Symmetric
* 梯度Gradient

![image-20221223135227018](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223135227018.png)



## Lecture13 Gradient Descent  梯度下降

https://blog.csdn.net/qq_41800366/article/details/86583789?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522167183047716782427420351%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=167183047716782427420351&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_positive~default-1-86583789-null-null.142

-- 梯度下降

梯度下降的基本过程就和下山的场景很类似。

首先，我们有一个可微分的函数。这个函数就代表着一座山。我们的目标就是找到这个函数的最小值，也就是山底。根据之前的场景假设，最快的下山的方式就是找到当前位置最陡峭的方向，然后沿着此方向向下走，**对应到函数中，就是找到给定点的梯度 ，然后朝着梯度相反的方向，就能让函数值下降的最快**！因为梯度的方向就是函数之变化最快的方向(在后面会详细解释)
所以，我们重复利用这个方法，反复求取梯度，最后就能到达**局部的最小值**，这就类似于我们下山的过程。而求取梯度就确定了最陡峭的方向，也就是场景中测量方向的手段。那么为什么梯度的方向就是最陡峭的方向呢？接下来，我们从微分开始讲起：

### 1. Derivative 导数

* Suppose we have function y=f (x), x, y real numbers 
* 假设有函数y=f (x) x, y个实数
  * Derivative of function denoted: f’(x) or as dy/dx 
  * 函数的导数记为f ' (x)或dy/dx
    * Derivative f’(x) gives the slope of f (x) at point x 
    * f ' (x)的导数给出了f (x)在x点的斜率
    * It specifies how to scale a small change in input to obtain a corresponding change in the output: 
    * 它指定了如何缩放输入中的小变化以获得输出中的相应变化:

![image-20221223205053069](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223205053069.png)

* It tells how you make a small change in input to make a small improvement in y 
* 它告诉你如何对输入做一个小的改变来使y有一个小的提高

![image-20221223205330622](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223205330622.png)

#### 1.1 Calculus in optimization 最优化中的微积分

![image-20221223205616018](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223205616018.png)

* Therefore, we can reduce f(x) by moving x in small steps with opposite sign of derivative 
* 因此我们可以通过移动与导数方向想法的极小的x来减少f(x)
* 不就是移动与函数方向相反的x来减少f(x)吗

![image-20221223210122024](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223210122024.png)

#### 1.2 Gradient Descent Illustrated  梯度下降图解

![image-20221223212100803](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223212100803.png)

#### 1.3 Stationary points, Local Optima  静止点， 局部优化

* When  f`(x)=0 derivative provides no information about direction of move 

  当导数f`(x)=0的时候，不提供任何移动方向的信息

* Points where  f`(x)=0 are known as stationary or critical points 

*  **f`(x)=0的点任务是静止点或者关键点**

  * **Local minimum/maximum**: a point where f(x) lower/ higher than all its neighbors
  * 局部最小值/最大值:f(x)低于/高于其所有邻域的点
  * **Saddle Points**: neither maxima nor minima 
  * 鞍点:既不是极大值也不是极小值

![image-20221223212854945](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223212854945.png)

#### 1.4 Presence of multiple minima 存在多个极小值

* Optimization algorithms may fail to find global minimum 
* 优化算法可能无法找到全局最小值
* Generally accept such solutions 
* 一般接受这种解决方法

![image-20221223213059133](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223213059133.png)

### 2. Gradient 梯度

#### 2.1. Minimizing with multiple dimensional inputs 用多维输入最小化

* We often minimize functions with multiple-dimensional inputs
* 我们经常最小化具有多维输入的函数
* ![image-20221223213520745](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223213520745.png)
* For minimization to make sense there must still be only one (scalar) output 
* 为了使最小化有意义，仍然必须只有一个(标量)输出

![image-20221223213641338](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223213641338.png)

#### 2.2 Functions with multiple inputs 多重输入函数

* Partial derivatives  偏导数
* 解释一下，因为往往有多个变量，偏导数是其中一个变量的导数
* ![image-20221223214232406](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223214232406.png)
* measures how f changes as only variable xiincreases at point x 
* 测量f在点x处只有变量xi增加时的变化
* **这不就是高中学的求导吗。。。**
* Gradient generalizes notion of derivative where derivative is wrt a vector
*  **梯度是包含所有偏导数的向量**

![image-20221223214544483](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223214544483.png)

![image-20221223214641319](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223214641319.png)

* **Gradient is vector containing all of the partial derivatives denoted** 
* **梯度是包含所有偏导数的向量**

![image-20221223214738283](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223214738283.png)

* Element iof the gradient is the partial derivative of f wrt xi
* 梯度的元素i是f wrt x的偏导数
* Critical points are where every element of the gradient is equal to zero 
* 临界点是指梯度中的每个元素都等于零

![image-20221223214923078](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223214923078.png)

![image-20221223214930317](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223214930317.png)

![image-20221223214948771](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223214948771.png)



### 3. Directional Derivative 方向导数

https://blog.csdn.net/The_lastest/article/details/77898799?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522167183225716782425684593%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=167183225716782425684593&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_positive~default-1-77898799-null-null.142

- 方向导数是在三维空间中，曲面上某一点沿着任一方向的变化率（坡度）；

![image-20221223215040032](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223215040032.png)

![image-20221223220126162](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223220126162.png)

![image-20221223220352328](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223220352328.png)

* 换句话说，梯度直接指向上坡，负梯度直接指向下坡

### 4. Method of Gradient Descent 梯度下降的方法

* The gradient points directly uphill, and the negative gradient points directly downhill 
* 梯度直接指向上坡，负梯度直接指向下坡
* Thus we can decrease f  by moving in the direction of the negative gradient 
* 因此，我们可以通过向负梯度方向移动来减小f
  * This is known as the method of **steepest descent or gradient descent** 
  * 这被称为这被称为**最陡下降法或梯度下降法**
* Steepest descent proposes a new point 
* 最陡的下降提出了一个新的点
* ![image-20221223220815825](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223220815825.png)
  * ![image-20221223220838717](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223220838717.png)

#### 4.1 选择学习率

![image-20221223220922810](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223220922810.png)

### 5. Example: Gradient Descent on Linear Regression  

![image-20221223221013131](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223221013131.png)

![image-20221223221132301](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223221132301.png)



### 6. Linear Regression: Analytical Solution



#### 6.1 Convergence of Steepest Descent  最陡下降收敛

* Steepest descent converges when every element of the gradient is zero 
* 当梯度的每个元素都为零时，最陡下降收敛
* 就是偏导数为0
  * In practice, very close to zero 
  * 实际上，非常接近于零
* We may be able to avoid iterative algorithm and jump to the critical point by solving the following equation for x
* 我们可以通过求解下面的x方程来避免迭代算法，从而跳到临界点
* ![image-20221223225014815](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223225014815.png)

![image-20221223225110824](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223225110824.png)

* Algebraic view of the minimizer
* 最小化器的代数视图
* If 𝑋is invertible, just solve 𝑋𝑤= 𝑦and get 𝑤= 𝑋−1𝑦
* 如果𝑋is可逆的,只是解决𝑋𝑤=𝑦 and 得到𝑤=𝑋−1𝑦
* But typically 𝑋is a tall matrix 
* 但通常𝑋是一个高大的矩阵

![image-20221223225318506](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223225318506.png)



### 7. Generalization to discrete spaces  推广到离散空间

* Gradient descent is limited to continuous spaces 
* 梯度下降只限于连续空间
* **和求导是在连续函数上求导是一个道理**
* Concept of repeatedly making the best small move can be generalized to discrete spaces 
* 反复做出最佳小动作的概念可以推广到离散空间
* Ascending an objective function of discrete parameters is called hill climbing
* 上升一个离散参数的目标函数称为爬坡

![image-20221223225734130](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221223225734130.png)

## Lecture14 Naive-Bayes

![image-20230122135646717](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122135646717.png)

![image-20230122135656343](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122135656343.png)

### 1. Recall: MAP Queries (Most Probable Explanation) 最可能的解释和最大似然估计

https://www.bilibili.com/video/BV1Hb4y1m7rE/?spm_id_from=333.337.search-card.all.click&vd_source=9d046a6203dde4f5f1794bf980388e63

* Finding a high probability assignment to some subset of variables 
* 寻找变量子集的高概率赋值
* Most likely assignment to all non-evidence variables W
* 最有可能赋值给所有无证据变量W
* ![image-20230122140040841](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122140040841.png)

![image-20230122143212681](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122143212681.png)



### 2. Naïve Bayes Algorithm 贝叶斯算法

https://blog.csdn.net/weixin_45962068/article/details/118148350?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522167439039116782428634527%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=167439039116782428634527&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_positive~default-1-118148350-null-null.142^

![image-20230122143429634](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122143429634.png)

#### 2.1 Reducing the number of parameters to estimate  减少需要估计的参数数量

* 我们有一个P(Y|X), Y是是否富有，特征有两个是 性别 gender和 hours_worked

![image-20230122144202724](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122144202724.png)

![image-20230122144429430](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122144429430.png)

![image-20230122144708572](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122144708572.png)

![image-20230122145444982](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122145444982.png)



#### 2.2 Naïve Bayes 朴素贝叶斯

![image-20230122145855160](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122145855160.png)

![image-20230122150054721](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122150054721.png)

#### 2.3 Recap: Conditional independence 

![image-20230122150259389](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122150259389.png)

* A is conditionally independent of B given C, if the probability distribution governing A is independent of the value of B, given the value of C 
* 如果A的概率分布在给定C的情况下与B的值无关，则A在给定C的情况下与B的值无关

![image-20230122150502883](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122150502883.png)

#### 2.4 AssumpRon for Naïve Bayes

![image-20230122151044388](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122151044388.png)

![image-20230122151547497](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122151547497.png)

![image-20230122151557253](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122151557253.png)



#### 2.5 Naïve Bayes Algorithm

![image-20230122152415626](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122152415626.png)

![image-20230122152421788](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122152421788.png)

![image-20230122152432291](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122152432291.png)





## Lecture15   Deep Learning

### 1. Deep Learning in Different fileds

#### 1.1 ComputerVision

<font size=5>Some Example：</font>

* Object and activity recognition  物体和行动的识别
  * https://www.youtube.com/watch?v=qrzQ_AB1DZk
* Object detection and segmentation 对象的检测和分割
  * https://www.youtube.com/watch?v=CxanE_W46ts
* Image captioning and Q&A  图像字幕和Q&A
  * https://www.youtube.com/watch?v=8BFzu9m52sc

<font size=5>Why should we be impressed? </font>

* Vision is ultra challenging. 视觉是极具挑战的

  ![image-20221114164842854](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221114164842854.png)

* Visual object variations 视觉对象是多变的

  ![image-20221114164950691](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221114164950691.png)

* Semantic object variations 语义对象多变

  ![image-20221114165329787](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221114165329787.png)



#### 1.2  Natural Language Processing (NLP)自然语言处理 and Speech

* Word and sentence representations. 语言和句子代表

  ![image-20221114171135914](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221114171135914.png)

![image-20221114171150134](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221114171150134.png)

* Speech recognition and Machine translation 语音识别与机器翻译

  ![image-20221114171324709](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221114171324709.png)

<font size=5>Why should we be impressed? </font>

* NLP is an extremely complex task. NLP是一个特别复杂的任务
  * synonymy 同义词(“chair”, “stool” or “beautiful”, “handsome”) 
  * ambiguity 模棱两可(“I made her duck”, “Cut to the chase”) 
* NLP is very high dimensional. NLP非常高维
  * assuming 150K english words, we need to learn 150K classifiers  假设有15K个英语单词，我们就需要学习150K个分类器。
* Beating NLP feels the closest to achieving true AI 最接近打败NPL的是真正的AI
  * although true AI probably goes beyond NLP, Vision, Robotics, ... alone. 即使真正的AI已经超过了上述对象

#### 1.3 Robotics and AI

* Self-Driving cars
  * https://www.youtube.com/watch?v=-96BEoXJMs0
* Drones and robots 
  * https://www.youtube.com/watch?v=2hGngG64dNM
* Game AI 
  * https://www.youtube.com/watch?v=V1eYniJ0Rnk

<font size=5>Why should we be impressed? </font>

* Typically robotics are considered in controlled environments 传统的机器人常常在受控制环境中被考虑。

  * Laboratory settings, Predictable positions, Standardized tasks (like in factory robots)  实验室设置，可预测的位置，标准化任务(比如工厂机器人)

* What about real life situations? 什么是真是的生活情况？

  * Environments constantly change, new tasks need to be learnt without guidance, unexpected factors must be dealt with . 环境是持续变化的，新的任务需要在没有指导的情况下被学习，并解决无法预测的因素

* Game AI 游戏AI

  

#### 1.4 Music and the arts

* Imitating famous painters 模仿著名画家

  ![image-20221114173025467](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221114173025467.png)

<font size=5>Why should we be impressed? </font>

* Music, painting, etc. are tasks that are uniquely human. 音乐，绘画等是独属于人类的工作
  * Difficult to model. 难以建模
  * Even more difficult to evaluate (if not impossible)  难以评估
* If machines can generate novel pieces even remotely resembling art, 
  they must have understood something about “beauty”, “harmony”, 
  etc.  如果机器人可以生成新奇的小说作品甚至接近艺术， 那么他们就一定理解美或和谐。
* Have they really learned to generate new art, however?
  * We do not know.



### 2. A brief history of Neural Networks

  ![image-20221114212011036](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221114212011036.png)



#### 2.1 Perceptrons ((感知器)

* Rosenblatt proposed a machine for binary classifications. 

* **Rosenblatt 提出了一种二进制的分类机器**

* Main Idea:

  * One weight 𝑤𝑖 per input 𝑥𝑖  每一个x都有一个权重w
  * Multiply weights with respective inputs and add bias 𝑥0=+1 权重与各自的input相乘在加上偏差值x0
  * If result larger than threshold return 1, otherwise 0 如果结果大于阈值返回1，否则返回0

  ![image-20221114213216540](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221114213216540.png)

##### 2.1.1 Training a perceptron 训练感知器

* Rosenblatt’s innovation was mainly the learning algorithm for 
  perceptrons. 他的创新主要是感知器的学习算法

* Learning algorithm 

  * Initialize weights randomly 随机初始化权重
  * Take one sample 𝑥𝑖and predict 𝑦𝑖 取一个样本xi和预测值yi
  * For erroneous predictions update weights 对于错误的预测值，更新权重。
    * ![image-20221114213714013](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221114213714013.png)
      * ηis learning rate;  set to value << 1
      * <font color='red'>很明显，η大于0小于1，权值取决于u的差值的正负。</font>
    * Repeat until no errors are made 

  ![image-20221114213928488](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221114213928488.png)

##### 2.1.2 Representational power of perceptrons 感知器的表达方式

* in previous example, feature space was 2D so decision boundary was 
  a line.  在之前的例子中，特征空间是2D的，所以决策边界是一条线
* in higher dimensions, decision boundary is a hyperplane.  在更高的维度上，决策边界是一个超平面

![image-20221114214531281](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221114214531281.png)

##### 2.1.3 From a perceptron to a neural network 从感知器到神经网络

* One perceptron = one decision 一个感知器=一个决定

* What about multiple decisions?  有什么需要复数决策

  * Eg：数字分类器

* Stack as many outputs as the possible outcomes into a layer. 将尽可能多的输出叠到同一层中。

  * Neural network 

* Use one layer as input to the next layer. 使用一个图层作为下一个图层的输入

  * Multi-layer perceptron (MLP)  多层感知器

  ![image-20221114215920220](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221114215920220.png)

##### 2.1.4 Some linearly separable functions 一些线性可分函数、

![image-20221114220128815](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221114220128815.png)

<font color='red'>And 和Or是线性可分函数</font>

##### 2.1.5 XOR is not linearly separable XOR（且或非）但不是线性可分

![image-20221114220414572](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221114220414572.png)

不遵守且或非的关系

##### 2.1.6 XOR & Multi-layer Perceptrons  XOR&多层感知器

<font color=red>**However, the exclusive or (XOR) cannot be solved by perceptrons。 然而，排他或XOR不可以使用感知器求解。**</font >

![image-20221114220727728](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221114220727728.png)

如图：

![image-20221114220918961](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221114220918961.png)

根据结果，只有01和10可以被选中。

##### 2.1.7 Minsky & Multi-layer perceptrons

* Interestingly, Minksy（上面提到的人，在图片里） never said XOR cannot be solved by neural networks. 但是他可没有说过话用神经网络不能解决XOR
  * **Only that XOR cannot be solved with 1 layer perceptrons（只是异或不能用一层感知器求解）**
* Multi-layer perceptrons can solve XOR 
  * 9 years earlier Minsky built such a multi-layer perceptron 9年前，明斯基建立了这样一个多层感知器

![image-20221114222250090](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221114222250090.png)

<font color=red>上图中的下面这个图确实可以</font>

那么，新的问题： 如何训练多层感知模型？

* **Rosenblatt’s algorithm not applicable, as it expects to know the desired target.** 
* **Rosenblatt的算法并不适用，因为它期望知道需要的目标**
  * For hidden layers we cannot know the desired target 
  * 对于隐藏值，我们无法知道期待的目标。

![image-20221114222907012](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221114222907012.png)

![image-20221114222916418](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221114222916418.png)



#### 2.2 The “AI winter” despite notable successes 

![image-20221114223110377](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221114223110377.png)



##### 2.2.1  The first “AI winter” 第一次AI寒冬

![image-20230122154231187](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122154231187.png)

![image-20230122154250653](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122154250653.png)

##### 2.2.2 The thaw of the AI Winter AI冬天的解冻

![image-20230122154802642](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122154802642.png)

![image-20230122154856315](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122154856315.png)

##### 2.2.3 Deep Learning

![image-20230122160154120](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122160154120.png)

##### Deep Learning Golden Era

![image-20230122160331743](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122160331743.png)

![image-20230122160411293](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122160411293.png)

![image-20230122160435440](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122160435440.png)





## Leture 16 Deep Learning: Functional View and Features
![image-20230122164650783](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122164650783.png)



### 1. Functional View of DNNS



#### 1.1 What is a nested function?

![image-20230122164802000](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122164802000.png)



#### 1.2 Functional View of DNNs DNNs功能视图

![image-20230122164904178](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122164904178.png)

##### 1.2.1 Illustration of DNN 

![image-20230122165101868](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122165101868.png)

![image-20230122165140278](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122165140278.png)

![image-20230122165223994](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122165223994.png)



### 2. LearningRepresentations & Features

#### 2.1 Raw digital representation --Image and Video

![image-20230122165444815](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122165444815.png)

![image-20230122165450869](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122165450869.png)

#### 2.2 Learning Representations & Features 学习表现与特征

![image-20230122170625605](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122170625605.png)

![image-20230122170709500](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122170709500.png)

![image-20230122170734096](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122170734096.png)

#### 2.3 Good Features 好的特征

![image-20230122170918195](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122170918195.png)



#### 2.4 Data Mainfold 数据流形

![image-20230122171137621](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122171137621.png)

![image-20230122171220072](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122171220072.png)

#### 2.5 The Digits Mainfolds

![image-20230122171403747](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122171403747.png)



#### 2.6 End-to-end learning of feature hierarchies  特征层次结构的端到端学习

![image-20230122171612916](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122171612916.png)

![image-20230122171624170](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122171624170.png)

![image-20230122171646454](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122171646454.png)

![image-20230122171700878](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122171700878.png)



## Lecture17 Adversarial Attack on ML models







## Lecture18 DL-Forward-and-Backward-Computation

### 1. Forward and Backward computation

#### 1.1 Forward Computations 正向计算

* Collect annotated data 

* 收集未注释的数据

* Define model and initialize randomly  

* 定义初始模型并随机化

* Predict based on current model 

* 在现有模型上进行猜测

  * In neural network jargon **“forward propagation”** 
  * 在神经网络术语中被称为**正向传播**

* Evaluate Predictions

  ![image-20221115091433434](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221115091433434.png)

#### 1.2 Backward Computations

* Collect gradient data  收集梯度数据

* Define model and initialize randomly 定义模型并进行随机化

* Predict based on current model 在现有模型上进行猜测

  * In neural network jargon **“backpropagation”** 在神经网络术语中被称为**反向传播**

* Evaluate Predictions

* 评估预测

  ![image-20221115091757492](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221115091757492.png)

  ![image-20221115135026884](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221115135026884.png)

  ![image-20221115135036850](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221115135036850.png)

  ![image-20221115135106052](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221115135106052.png)

  ![image-20221115135127453](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221115135127453.png)

<font color=red>就是一个正推，一个反推</font>

#### 1.3 Recall Training Objective

![image-20221115091910972](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221115091910972.png)

#### 1.4 Forward Computation

Example：

![image-20221115092041556](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221115092041556.png)

* Training Data (a signle sample)

  * given inputs 0.05 and 0.10, we want the neural network to output 0.01 and 0.99.  输入值为0.05和0.1 期望值为0.01和0.99
  * •net be the value before activation function 取激活函数前的值
  * •outbe the value after activation function 输出激活函数后的值
  * •Activation function is sigmoid function 激活函数是sigmoid函数

  ![image-20221115092706145](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221115092706145.png)

  ![image-20221115092720824](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221115092720824.png)

  ![image-20221115092755397](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221115092755397.png)

  ![image-20221115092921826](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221115092921826.png)

* <font color=red>b是偏差值</font>

  

### 2. Back-Propogation and Chain Rule

https://blog.csdn.net/qq_39215715/article/details/108527831?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522166859522316782412582214%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=166859522316782412582214&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduend~default-1-108527831-null-null.142

-- Back-Propogation 算法

#### 2.1 Back-Propogation 反向传播

本质上是通过梯度下降算法求极值的过程。

##### 2.1.1 Recall: Minimizing with multiple dimensional inputs 最小化多维输入

* We often minimize functions with multiple-dimensional inputs. 我们经常性的最小化具有多维输入的函数

  ![image-20221115142037139](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221115142037139.png)

* For minimization to make sense there must still be only one (scalar) output.  **为了使最小化有意义，仍然必须只有一个(标量)输出**



##### 2.1.2 Functions with multiple inputs  多重输入函数

* Partial derivatives 偏导数

  ![image-20221115223833037](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221115223833037.png)

* measures how f changes as only variable xi increases at point x 测量f会如何改变，仅当xi在点x上增加时。

  ![image-20221115224539338](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221115224539338.png)

* **<font color=red>Gradient generalizes notion of derivative where derivative is wrt a vector 梯度一般化导数的导数,导数是wrt向量</font>**

* Gradient is vector containing all of the partial derivatives denoted 梯度是包含了所有偏导数的向量。

  ![image-20221115224907385](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221115224907385.png)



##### 2.1.3 Optimization through Gradient Descent  通过梯度下降进行优化

* As with many model, we optimize our neural network with Gradient Descent. 和很多模型一样，我们用梯度下降优化我们的神经网络算法。

  ![image-20221116101218029](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116101218029.png)

* The most important component in this formulation is the gradient 在这个公式中最重要的组成部分就是梯度。

* Backpropagation to the rescue. 反向传播以进项救援

  * The backward computations of network return the gradients. 网络的反向计算返回梯度

  * How to make the backward computations  如何进行反向运算

    ![image-20221116101758279](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116101758279.png)

##### 2.1.4 Weight Update

![image-20221116102011402](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116102011402.png)

#### 2.2 Chain Rule

* Assume a nested function, 𝑧= 𝑓(𝑦) and y= g(x) 假设一个镶套函数

* Chain Rule for scalars 𝑥, 𝑦, 𝑧 标量x,y,z的标量法则

  ![image-20221115093618957](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221115093618957.png)

* When 𝑥∈R𝑚(上标),𝑦∈R𝑛, 𝑧∈R 

  ![image-20221115093750715](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221115093750715.png)

* ![image-20221115093800168](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221115093800168.png)

* ![image-20221115093816818](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221115093816818.png)

* ![image-20221115093857473](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221115093857473.png)

* ![image-20221115093912480](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221115093912480.png)

##### 2.2.1 Defination of Chain rule

![image-20221115094014836](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221115094014836.png)

* dy/dx 是雅可比矩阵

##### 2.2.2 The Jacobian

![image-20221116102540878](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116102540878.png)

##### 2.2.3 Backpropagation

![image-20221116103108768](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116103108768.png)



#### 2.3 Some Examples

![image-20221116103218640](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116103218640.png)

![image-20221116103258798](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116103258798.png)

![image-20221116103309364](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116103309364.png)

![image-20221116103324192](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116103324192.png)

#### 2.4 General Workflow 一般工作流程

![image-20221116103428496](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116103428496.png)

1. Random Initialization 随机初始化
2. Feed Forward 正向输入
3. Calculate loss function 计算损失函数
4. Calculate the derivative of error. 计算错误的派生
5. Backpropagate 向后传播算法
6. Update the weights 更新权重

### 3. Regularization 正则化

#### 3.1 Recall: what is regularization? 

* **In general: any method to prevent overfitting or help the optimization. 一般来说:任何防止过拟合或有助于优化的方法**
* **Specifically: additional terms in the training optimization objective to prevent overfitting or help the optimization. 具体地说:在训练优化目标中增加防止过拟合或帮助优化的术语**

#### 3.2 Recall: Overfitting 过拟合

* Key: empirical loss and expected loss are different. 经验损失和预期损失是不一样的。
* The smaller the data set, the larger the difference between the two 数据集越小，二者的差别越大
* The larger the hypothesis class, the easier to find a hypothesis that 
  fits the difference between the two 假设类越大，就越容易找到一个符合两者差异的假设
  * Thus has small training error but large test error (overfitting)  因此在一个数据集中，较小的训练集错误可能是极大的测试集错误。也就是过拟合
* Larger data set helps 往往更大的数据集更好
* Throwing away useless hypotheses also helps (regularization) 除非假设有用，否则扔掉（正则化）

#### 3.3 Regularization as hard constraint 带有硬约束的正则化

![image-20221116174653281](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116174653281.png)

![image-20221116174741016](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116174741016.png)

#### 3.4 Regularization as soft constraint 带有软约束的正则化

* 硬约束的优化等于软约束的

![image-20221116174754169](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116174754169.png)

* Showed by Lagrangian multiplier method  拉格朗日乘数法

  ![image-20221116175250280](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116175250280.png)

* Suppose 𝜃∗is the optimal for hard-constraint optimization 假设𝜃*是硬约束优化的最优值

  ![image-20221116175333499](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116175333499.png)

* Suppose 𝜆∗is the corresponding optimal for max  假设𝜆*是max对应的最优值

  ![image-20221116175456974](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116175456974.png)





## Lecture 19 DL-Convolutional-Neural-Networks

### 1. Convolutional Neural Networks(CNN) 卷积神经网络

<font color='red'>一个训练的代码模板, 个人认为蛮关键的</font>

![image-20221115101205728](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221115101205728.png)

#### 1.1 Fully-Connected 全层连接

![image-20221115101539694](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221115101539694.png)



#### 1.2 Convolution 卷积

* Strong empirical application performance. 强大的经验应用性能

* Convolutional networks: neural networks that use convolution in place of general matrix multiplication in at least one of their layers. <font color='red'> **卷积网络:在至少一层中使用卷积代替一般矩阵乘法的神经网络。**</font>

  ![image-20221115101957535](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221115101957535.png)

  for a specific kind of weight matrix 𝑊. 求一种特定的权重矩阵𝑊

![image-20221116175811537](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116175811537.png)

<font size=5>线性</font>

![image-20221116184901769](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116184901769.png)

![image-20221116184912558](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116184912558.png)

![image-20221116184922199](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116184922199.png)

![image-20221116184934991](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116184934991.png)

![image-20221116184943420](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116184943420.png)

![image-20221116184953997](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116184953997.png)

![image-20221116185009984](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116185009984.png)

![image-20221116185027201](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116185027201.png)

<font size=5>二维</font>

![image-20221116185200446](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116185200446.png)

![image-20221116185235537](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116185235537.png)

![image-20221116185244883](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116185244883.png)

##### 1.2.1 A Closer look at spatical dimensions 特殊维度的卷积

* <font size=5>Stride=1</font>

![image-20221116185858655](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116185858655.png)

![image-20221116185911472](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116185911472.png)

![image-20221116190018705](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116190018705.png)

![image-20221116190027653](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116190027653.png)

![image-20221116190036244](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116190036244.png)

可以发现，表格从第一个走到了最后一个，总共走了五次

* <font size=5>Stride=2</font>

![image-20221116190410539](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116190410539.png)

![image-20221116190418958](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116190418958.png)

![image-20221116190428934](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116190428934.png)

* <font size=5>Stride=3</font>

![image-20221116190454847](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116190454847.png)

![image-20221116190511322](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116190511322.png)

##### 1.2.2 Advantage of Convolutional Layer

###### 1.2.2.1 Advantage: sparse interaction 稀疏交互

全联通层

![image-20221116205345950](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116205345950.png)

卷积层

![image-20221116205740662](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116205740662.png)

多重卷积层

![image-20221116205713385](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116205713385.png)



###### 1.2.2.2 Advantage: parameter sharing/weight tying 

![image-20221116231907849](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116231907849.png)

###### 1.2.2.3 Advantage: equivariant representations 等变化表示

* Equivariant: transforming the input = transforming the output 等变量:转换输入=转换输出
* Example: input is an image, transformation is shifting 示例:输入是图像，变换是平移
* Convolution(shift(input)) = shift(Convolution(input)) 卷积(shift(输入))= shift(卷积(输入))
* Useful when care only about the existence of a pattern, rather than 
  the location当只关心模式的存在，而不是位置时，它是有用的





#### 1.3 Zero-Padding 0填充

![image-20221115103717131](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221115103717131.png)

#### 1.4 RELU （整流线性单位）

* rectifieris an activation function defined as the positive part of its argument 整流函数是一种激活函数,它被定义为它的论点的积极部分

  ![image-20221118173546773](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221118173546773.png)

* A smooth approximation to the rectifier is the analytic function 对整流器的平滑逼近是解析函数

  ![image-20221118174322619](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221118174322619.png)

* ![image-20221118174338407](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221118174338407.png)

#### 1.5 Pooling

* **Pooling layer** is frequently used in convolutional neural networks with the purpose to progressively reduce the spatial size of the representation to reduce the amount of features and the computational complexity of the network.  <font color='red'>Pooling Layer</font> 经常用于卷积神经网络,目的是逐步减少表示的空间大小,以减少网络的特征和计算复杂度。、

----

##### 1.5.1 Terminology of Pooling Layer   Pooling Layer的术语

![image-20221118174728571](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221118174728571.png)

----

* Summarizing the input (i.e., output the max of the input) 汇总输入(即输出输入的最大值)

  ![image-20221118175101735](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221118175101735.png)

* Induce invariance 诱导不变性

  ![image-20221118175222350](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221118175222350.png)

![image-20221118175313328](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221118175313328.png)



#### 1.6 Softmax 归一化指数函数

* Recall that logistic regression produces a decimal between 0 and 1.0. For example, a logistic regression output of 0.8 from an email classifier suggests an 80% chance of an email being spam and a 20% chance of it being not spam. Clearly, the sum of the probabilities of an email being either spam or not spam is 1.0.  回想一下，逻辑回归会产生一个0到1.0之间的小数。例如，一个邮件分类器的逻辑回归的输出是0.8，这表明一份邮件有80%的概率是垃圾邮件，20%的概率不是。显然概率之和为1.

* Softmax extends this idea into a multi-class world. That is, Softmax
  assigns decimal probabilities to each class in a multi-class problem. 
  Those decimal probabilities must add up to 1.0. This additional 
  constraint helps training converge more quickly than it otherwise 
  would.   

* softmax将这个想法扩展到一个多类的世界。也就是说，Softmax为多类问题中的每个类分配十进制概率。

  这些十进制概率加起来一定是1.0。这一附加约束有助于训练更快地收敛。

![image-20221118184105093](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221118184105093.png)

#### 1.7 Preprocessing data 预处理数据

![image-20221118184136800](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221118184136800.png)

![image-20221118184313009](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221118184313009.png)

* e.g. consider CIFAR-10 example with [32,32,3] images 
* Subtract the mean image (e.g. AlexNet) (mean image = [32,32,3] array)  减去平均图像(例如AlexNet)(平均图像=[32,32,3]数组)
* Subtract per-channel mean (e.g. VGGNet) (mean along each channel = 3 numbers) 减去每个频道的平均值(例如VGGNet)(每个频道的平均值=3

### 2. Example

* 由Yann LeCun, Leon Bottou, Yoshua Bengio和Patrick Haffner在“基于度的学习应用于文档识别”中提出

  IEEE学报，1998

* Apply convolution on 2D images (MNIST) and use backpropagation 应用卷积在二维图像上并使用反向传播

*  结构:2个卷积层(带池)+ 3个完全连接层

  * Input size: 32x32x1
  * Convolution kernel size: 5x5
  * Pooling: 2x2  

![image-20221118184834581](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221118184834581.png)

![image-20221118184848479](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221118184848479.png)

![image-20221118184855699](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221118184855699.png)

![image-20221118184905083](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221118184905083.png)

![image-20221118184914908](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221118184914908.png)

![image-20221118184927944](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221118184927944.png)

![image-20221118184940283](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221118184940283.png)



## Lecture 20 Model Evaluation

### 1. Test sets revisited 重新访问测试集

* How can we get an unbiased estimate of the accuracy of a learned model?  我们如何得到一个对学习模型的准确性的毫无偏见的估计

  ![image-20221116111333614](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116111333614.png)





### 2. Learn Curve

* How does the accuracy of a learning method change as a function of the training-set size? 
* 学习方法的准确性如何作为训练设置大小的功能变化?
  * this can be assessed by plotting learning curves  
  * 可以用学习曲线表示

![image-20221116111807297](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221116111807297.png)







### 3. Multiple training/test partitions

#### 3.1 Limitations of using a single training/test partition 使用单个训练/测试分区的限制

* we may not have enough data to make sufficiently large training and test sets
  * a larger test set gives us more reliable estimate of accuracy (i.e. a lower variance estimate) 
  * but... a larger training set will be more representative of how much data we actually have for learning process 
* a single training set doesn’t tell us how sensitive accuracy is to a particular training sample 

![image-20230122222019165](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122222019165.png)

![image-20230122222037657](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122222037657.png)





#### 3.2 Using multiple training/test partitions 

![image-20230122222625749](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122222625749.png)

#### 3.4 Random resampling 随机重采样

* We can address the second issue by repeatedly randomly partitioning the available data into training and test sets. 
* 我们可以通过反复随机地将可用数据划分为训练集和测试集来解决第二个问题。

![image-20230122222620541](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122222620541.png)

#### 3.5 Stratified sampling 分层抽样

* When randomly selecting training or validation sets, we may want to ensure that class proportions are maintained in each selected set 
* 当随机选择训练集或验证集时，我们可能希望确保在所选的每个集中保持类的比例

![image-20230122222936636](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122222936636.png)



#### 3.6 Cross Validation 交叉验证

![image-20230122223013820](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122223013820.png)

* 将一个数据集分成合适的5段落，取4个为训练集，1个为测试集。多次重复取样

![image-20230122223209858](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122223209858.png)

* 10-fold cross validation is common, but smaller values of n are often used when learning takes a lot of time 
* 10倍交叉验证是常见的，但当学习需要大量时间时，通常使用较小的n值
* in leave-one-out cross validation, n = # instances 
* 在省略一个交叉验证中，n = #实例
* in stratified cross validation, stratified sampling is used when partitioning the data 
* 在分层交叉验证中，在划分数据时采用分层抽样
* Cross validation makes efficient use of the available data for testing 
* 交叉验证可以有效地利用可用数据进行测试



### 4. Confusion matrices 混淆矩阵

* How can we understand what types of mistakes a learned model makes? 
* 我们如何理解一个学习模型会犯什么类型的错误呢?

![image-20230122223425867](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122223425867.png)

![image-20230122223732930](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122223732930.png)

#### 4.1 Is accuracy an adequate measure of predictive performance? 

![image-20230122223805148](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122223805148.png)

* accuracy may not be a useful measure in cases where 
* 在以下情况下，准确性可能不是一个有用的衡量标准
* we are most interested in a subset of high-confidence predictions 
* 我们对高置信度预测的一个子集最感兴趣

![image-20230122224127604](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122224127604.png)

![image-20230122224153042](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122224153042.png)

![image-20230122224234539](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122224234539.png)



### 5. ROC curves 

* A Receiver Operating Characteristic (ROC) curve plots the TP-rate vs. the FP-rate as a threshold on the confidence of an instance being positive is varied 
* 受试者工作特征(ROC)曲线描绘了TP-rate和FP-rate，作为实例为阳性的置信度的阈值是不同的

![image-20230122224427132](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122224427132.png)

![image-20230122224450594](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122224450594.png)

![image-20230122224459563](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122224459563.png)

![image-20230122224510262](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122224510262.png)

![image-20230122224521166](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122224521166.png)





### 6.PR curves

![image-20230122225128640](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122225128640.png)

![image-20230122225136263](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122225136263.png)

![image-20230122225147458](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122225147458.png)

![image-20230122225158507](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122225158507.png)

![image-20230122225210622](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122225210622.png)

* Both 
  * Allow predictive performance to be assessed at various levels of confidence
  * 允许在不同的置信度水平上评估预测性能
  * Assume binary classification tasks
  * 承担二进制分类任务
  * Sometimes summarized by calculating area under the curve
  * 有时通过计算曲线下的面积来总结
* ROC curves
  * Insensitive to changes in class distribution (ROC does not change if the proportion of positive and negative instances in the test set are varied)
  * 对类分布的变化不敏感(如果测试集中正实例和负实例的比例变化，ROC不变化)
  * Can identify optimal classification thresholds for tasks with differential misclassification costs
  * 能否为具有不同错误分类代价的任务识别最佳分类阈值
* PR curves
  * Show the fraction of predictions that are false positives
  * 显示假阳性预测的比例
  * Well suited for tasks with lots of negative instances
  * 非常适合有很多负面实例的任务









## Lecture 21

### 1.Positioning of Probabilistic Inference

![image-20221122091122238](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221122091122238.png)

#### 1.1 Top 10 Real-world Bayesian Network Applications

•https://data-flair.training/blogs/bayesian-network-applications/

​	•Gene Regulatory Network 基因调控网络
​	•Medicine  医学
​	•Biomonitoring 生物
​	•Document Classification  文件分类
​	•Information Retrieval  信息检索
​	•Semantic Search  语义查找
​	•Image Processing  图像处理
​	•Spam Filter 垃圾邮件过滤
​	•Turbo Code 涡轮码
​	•System Biology 系统生物学

![image-20221123101915161](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221123101915161.png)

![image-20221123101938543](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221123101938543.png)

![image-20221123102046622](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221123102046622.png)

#### 1.2 Fundamental Questions

![image-20221122091949987](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221122091949987.png)

* Representation 表示
  * How to capture/model uncertainties in possible worlds? 如何在可能的世界中捕获不确定性？
  * How to encode our domain knowledge/assumptions/constraints? 如何编码我们范围内的知识



* Inference 

  ![image-20221123102654670](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221123102654670.png)

* Learning

  ![image-20221123102729154](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221123102729154.png)





### 2.Recap: Naïve Bayes 朴素贝叶斯

#### 2.1 Recap of Basic Prob. Concepts

![image-20230122230922425](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122230922425.png)



* Each Xirepresents outcome of tossing coin i
  * Assume coin tosses are marginally independent 
  * 假设抛硬币是边际独立的
  * i.e., ![image-20230122231039173](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122231039173.png) therefore 

![image-20230122231012975](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122231012975.png)

![image-20230122231210002](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122231210002.png)

![image-20230122231329515](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122231329515.png)

![image-20230122231925438](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122231925438.png)

![image-20230122231932510](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122231932510.png)

![image-20230122235832884](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122235832884.png)

* Conditional Parameterization is combined with Conditional Independence assumptions to produce very compact representations of high dimensional probability distributions 
* 条件参数化与条件独立假设相结合可以产生非常紧凑的高维概率分布表示

### 3.Example Bayes Networks

####  3.1 BN for General Naive Bayes Model  BN为一般朴素贝叶斯模型

贝叶斯神经网络为一般朴素贝叶斯模型

![image-20230123000437239](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230123000437239.png)

![image-20230123000452369](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230123000452369.png)

![image-20230123000754849](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230123000754849.png)

* 如果x是条件独立的(如PGM所描述的那样)，联合分布可以分解成一个更简单的乘积，例如:

![image-20230123000826868](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230123000826868.png)



![image-20230123001118957](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230123001118957.png)

![image-20230123001159317](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230123001159317.png)

### 4. Example Probability Query

![image-20230124113137336](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230124113137336.png)

![image-20230124113144520](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230124113144520.png)

![image-20230124113150730](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230124113150730.png)

**<font color=red size=5>!!!!!!</font>**

![image-20230124113208538](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230124113208538.png)

![image-20230124113301689](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230124113301689.png)

![image-20230124113322756](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230124113322756.png)

### 

### 5.Example: Alarm Network 

![image-20230124113422289](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230124113422289.png)

![image-20230124113435226](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230124113435226.png)





## Lecture22 I-Maps: Graphs 

and Distributions

### 1. Recap: COnditional Independence

### 2. Markov Assumption and Definition of I-Maps

### 3. I-Map to Factorization 

### 4. Factorization to I-Map 

### 5. Perfect Map 



![image-20230125225320142](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230125225320142.png)

## Lab 7 

-- Argparse命令模块

https://blog.csdn.net/u011913417/article/details/109047850?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522166877135416800180692349%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=166877135416800180692349&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_positive~default-1-109047850-null-null.142^v65^js_top,201^v3^control_1,213^v2^t3_esquery_v3&utm_term=ArgumentParser&spm=1018.2226.3001.4187





## Lecture24-PGM-D-separation

### 1. Recap

### 2. Independencies in Graphs

* A graph structure G encodes a set of conditional independence assumptions I(G)   图结构G编码了一组条件独立性假设I(G)
* Are there other independencies that we can read-off?  我们是否可以读取其他的独立性
  * i.e., are there other independencies that hold for every distribution that factorizes over G?  对于每一个分解G的分布是否存在其的独立性
* D-separation holds the key   D-separation是关键



### 3. D-separation

#### 3.1 Dependencies and Independencies  独立性和依赖性

* Crucial for understanding network behaviour  理解网络活动非常重要
* Independence properties are important for answering queries  独立属性对于回答查询很重要
  * Exploited to reduce computation of inference  利用推断来减少计算
  * A distribution P that factorizes over G satisfies I(G)  分解G的分布P满足I(G)

#### 3.2 D-separation

#### 3.2.1 Direct Connection between X and Y 

#### 3.2.2 Indirect Connection between X and Y 

#### 3.2.3  I. Indirect Causal Effect: X->Z->Y

##### 3.2.3.1 Causal Chains 

#### 3.2.4  II.  Indirect Evidential Effect: Y->Z->X 

#### 3.2.5  III.  Common Cause: X<-Z->Y

##### 3.2.5.1 Common Cause 

####  3.2.6 IV.  Common Effect (V-structure) X->Z<-Y 

##### 3.2.6.1 Common Effect

