## Lecture 13 Peceptron_0

### 13.1 ANN Learning Rules

* The McCullock-Pitts neuron made a base for a machine (network of units) capable of
* The McCullock-Pitts neuron为机器（单元网络）奠定了基础。
  * **<font color=red>storing information and</font>**
  * **<font color=red>存储信息</font>**
  * **<font color=red>producing logical and arithmetical operations on it</font>**
  * **<font color=red>对其进行逻辑和算术运算</font>**

* 这里先简化一下这个神经元是干嘛用的
* ![  ](D:\笔记\笔记图片\image-20231126000614230.png)

* The next step
  * must be to realise another important function of the brain, which is
    * to acquire new knowledge through experience, i.e. learning.
    * 下一步，是实现大脑的重要功能之一，学习。

![image-20231126000823094](D:\笔记\笔记图片\image-20231126000823094.png)

* ANN learning rule is the rule **how to adjust the weights of connections to get desirable output.**
* ANN 学习规则是如何**调整连接权重以获得理想输出的规则**。



### 13.2 MP Neuron vs. Hebb’s Rule

![image-20231126001045301](D:\笔记\笔记图片\image-20231126001045301.png)



* Given a fixed MP neuron, that is, **all weights of connections** and neuron threshold are set up **in advance.**
* 给定一个固定的 MP 神经元，即事**先设置好所有连接权重**和神经元阈值。

![image-20231126001512586](D:\笔记\笔记图片\image-20231126001512586.png)

![image-20231126001604575](D:\笔记\笔记图片\image-20231126001604575.png)

![image-20231126003249849](D:\笔记\笔记图片\image-20231126003249849.png)



### 13.3 Unsupervised Learning 无监督学习

* Unsupervised learning is a type of machine learning in which **<font color=red size=5>the algorithm is not provided with any pre-assigned labels or scores for the training data.</font>** As a result, unsupervised learning algorithms must first **self-discover any naturally occurring patterns** in that training data set.
* 无监督学习是机器学习的一种类型，在这种类型中，**算法没有为训练数据提供任何预先分配的标签或分数。**因此，无监督学习算法必须首先**自我发现训练数据集中任何自然出现的模式**。

![image-20231126004138235](D:\笔记\笔记图片\image-20231126004138235.png)

* 这个问题是在 20 世纪 40 年代首次提出的、在神经科学实验还很有限的情况下，这些学习规则的经典定义
  这些学习规则的经典定义并非来自生物学，而是心理学



### 13.4 Perceptron 感知器

* Rosenblatt (1958) explicitly considered the problem of pattern recognition, where a “teacher” is essential. (Consider the difference with unsupervised learning)
* 罗森布拉特（Rosenblatt，1958 年）明确考虑了模式识别问题，在这个问题上，"教师 "是必不可少的。(考虑与无监督学习的区别）
* A Perceptron is a neural network that changes with “experience” using an **error-correction rule.**
* 感知器是一种利用纠错规则随 "经验 "变化的神经网络。
* According to the rule, **weight of a neuron changes when it makes error response to the input presented to the network.**
* 根据这一规则，**当神经元对网络输入做出错误响应时，其权重就会发生变化。**

![image-20231126005252762](D:\笔记\笔记图片\image-20231126005252762.png)

![image-20231126004749106](D:\笔记\笔记图片\image-20231126004749106.png)

* The simplest architecture of perceptron comprises **one layer of idealised “neurons”**, which we also sometimes call “units” of the network.
* 最简单的感知器结构包括**一层理想化的 "神经元"**，我们有时也称其为网络的 **"单元"**。

 ![image-20231126004837149](D:\笔记\笔记图片\image-20231126004837149.png)

![image-20231126012104933](D:\笔记\笔记图片\image-20231126012104933.png)

* **输入层（Input Layer）**：由一系列输入单元*a*1,*a*2,...,*a**n* 组成，其中 a0=1*a*0=1 通常表示偏置单元，它的作用是允许输出阈值可调整。
* **输出层（Output Layer）**：包含一个或多个输出神经元 *x* *j*，在这个例子中，只显示了一个输出神经元。

![image-20231126012752329](D:\笔记\笔记图片\image-20231126012752329.png)

* The two layers are fully interconnected, i.e. every input neuron is connected to every output neuron.
* 两层都是充分互联的

![image-20231126012952359](D:\笔记\笔记图片\image-20231126012952359.png)

* Semantically, a perceptron can be considered as a vector-valued function that maps
* 从语义上讲，感知器可被视为 可视为一个向量值函数

**![Uploaded image](D:\笔记\笔记图片\av4RUJF5eUbei8c3WkAVEwhUKvfVOO0JyqW3GDY%3D.png)**

* 尽管每个输出神经元都接收相同的输入，但它们对应的连接权重 *w**ji* 是独立的。这意味着即使对于相同的输入，不同的输出神经元也可能有不同的反应，因为它们通过独立的权重来加权输入信号。
* 幻灯片中提到的“individual connections”表明每个输入和输出之间的连接是唯一的，每个连接都有自己的权重 *w**ji*。由于这些权重是独立的，每个输出神经元可以独立调整，以便在学习过程中进行优化。
* 以 *j*-th 输出神经元为例，它的输出 *X**j* 会由输入的加权和通过激活函数 *f* 确定。权重 0*w**j*0（等于 −−*θ**j*）是偏置权重，用于调节激活阈值。这种结构允许感知机模型对每个输出神经元进行个性化的学习，使其能够识别输入模式并据此做出独立的决策。

![image-20231126014952246](D:\笔记\笔记图片\image-20231126014952246.png)

![image-20231126015104405](D:\笔记\笔记图片\image-20231126015104405.png)

* a0=1是一个偏置单元，往往用于调整激活函数的阙值。这么想，当a0大,wj0为正数，那么就以激活，反之。

![image-20231126015324246](D:\笔记\笔记图片\image-20231126015324246.png)

* With this trick, we have no need to set a threshold manually. Now we can train the threshold like weights.
* 有了这个技巧，我们就不需要 手动设置阈值。现在我们 可以像训练权重一样训练阈值。

![image-20231126015422997](D:\笔记\笔记图片\image-20231126015422997.png)

#### 13.4.1 MP Neuron vs. Perceptron (Syntax and Semantics)

![image-20231126020800637](D:\笔记\笔记图片\image-20231126020800637.png)

![image-20231126020817894](D:\笔记\笔记图片\image-20231126020817894.png)

![image-20231126020846812](D:\笔记\笔记图片\image-20231126020846812.png)

![image-20231126020904287](D:\笔记\笔记图片\image-20231126020904287.png)

![image-20231126021021811](D:\笔记\笔记图片\image-20231126021021811.png)

* - 与Hebb法则类似，我们通过调整两层之间的权重（训练）来学习 知识。
  - 如果数据集是无标记的，我们可以训练感知器网络将输入分组到不同的组中（无监督学习）。

![image-20231126021141199](D:\笔记\笔记图片\image-20231126021141199.png)

* 如果数据集是有标签的，我们就可以训练感知器网络，使其针对特定输入产生所需的输出（监督学习）。

## Lecture 14 Peceptron_1

![image-20231126021505580](D:\笔记\笔记图片\image-20231126021505580.png)

* Rosenblatt (1958) explicitly considered the problem of pattern recognition, where a “teacher” is essential.
* A Perceptron is a neural network that changes with “experience” using an **<font color=red>error-correction rule</font>**. (Supervised learning!)
* According to the rule, **<font color=red>weight of a response unit changes when it makes error response to the input presented to the network.</font>**
* **根据该规则，当响应单元对呈现给网络的输入做出错误响应时，响应单元的权重会发生变化。**



### 14.1.1 Perceptron Training

![image-20231126021748237](D:\笔记\笔记图片\image-20231126021748237.png)

* **<font color=red>Weights 𝑤ji</font>** of connections between two layers are changed according to **<font color=red>perceptron learning rule</font>**, so the network is more likely to produce the desired output in response to certain inputs.
* 两层之间连接的**权重𝑤ji** 会根据**感知器学习规则**发生变化，因此网络更有可能对特定输入产生所需的输出。

![image-20231126023302958](D:\笔记\笔记图片\image-20231126023302958.png)

* The perceptron is trained by using a training set with target outputs (labels).
* 感知器通过使用带有目标输出（标签）的训练集进行训练。
  * **Training set**: a set of input patterns repeatedly presented to the network during training;
  * **训练集**：在训练过程中反复呈现给网络的一组输入模式；
  * **Target/desired output (label)**: the pre-defined correct output of an input pattern in the training set.
  * **目标/预期输出（标签）**：训练集中输入模式的预定义正确输出。

![image-20231126024714824](D:\笔记\笔记图片\image-20231126024714824.png)

* Every input pattern is used multiple times for training
* 每个输入模式都会被多次用于训练

![image-20231126024800195](D:\笔记\笔记图片\image-20231126024800195.png)

* Input pattern in the set is 𝒏-dimensional! Note 𝑎 ! =1
* 集合中的输入模式为 𝒏 维！注意 𝑎 0=1

![image-20231126024903078](D:\笔记\笔记图片\image-20231126024903078.png)

* Note that in unsupervised learning, no label is needed.
* 请注意，在无监督 学习中不需要标签。

![image-20231126025003795](D:\笔记\笔记图片\image-20231126025003795.png)

* The network outputs 𝑿 𝒋 are then **compared to the desired outputs** specified in the training set and obtain the error.
* 然后将网络输出 𝑿 𝒋 与训练集中**指定的期望输出进行比较**，得出误差。
* 这是一个有监督学习，比较输出结果和标准结果得出误差是一个很典型的监督学习特征。

![image-20231126025454546](D:\笔记\笔记图片\image-20231126025454546.png)

* The **error of an output neuron** is the difference between the target output and the instant one.
* **神经元的错误**输出是目标输出与即时输出的差值。

![image-20231126025717617](D:\笔记\笔记图片\image-20231126025717617.png)

* The **errors** are then used to readjust the values of the weights of the connections.
* 然后利用**误差**重新调整连接的权重值。

![image-20231126025840216](D:\笔记\笔记图片\image-20231126025840216.png)

* The weights readjustment is done in such a way that the network is – on the whole – **more likely to give the desired response next time.**
* 权重重新调整的方式是使网络整体上**更有可能在下一次做出预期的响应**。

* The **goal of the training** is to arrive at a single set of weights that allow each input in the training set to be mapped to the correct output by the network.
* 训练的**目的是获得一组权重**，使网络能将训练集中的每个输入映射到正确的输出。



### 14.1.2 Weight Update

![image-20231126030835562](D:\笔记\笔记图片\image-20231126030835562.png)

![image-20231128004732106](D:\笔记\笔记图片\image-20231128004732106.png)

#### 14.1.2.1 Difference with Hebb`s Rule

![image-20231128005158158](D:\笔记\笔记图片\image-20231128005158158.png)



![image-20231128005417818](D:\笔记\笔记图片\image-20231128005417818.png)

* The value of the “learning rate” C is  
  * usually set below 1 and 
  * 经常设置在1以下
  * determines the amount of correction made in a single iteration.
  * 决定了单词迭代的修正量

![image-20231128005349786](D:\笔记\笔记图片\image-20231128005349786.png)

* The overall learning time of the network is affected by the value of the “learning rate” C: slower for small values and faster for larger.
* 越小的学习率意味着越慢的学习时间，反之。

![image-20231128005955579](D:\笔记\笔记图片\image-20231128005955579.png)

* The network performance during training session is measured by a **root-mean-square (RMS)** error value. 
* 训练过程中的网络性能以**均方根误差值**来衡量。

![image-20231128010154312](D:\笔记\笔记图片\image-20231128010154312.png)

* 当RMS=0的时候，停止计算。

![image-20231128010451887](D:\笔记\笔记图片\image-20231128010451887.png)

* The first sum is taken over all patterns in the training set, and the second sum is taken over all output neurons. 
* 第一个总和是训练集中所有模式的总和，第二个总和是所有输出神经元的总和。
* 1. **对所有模式进行求和**：这个步骤累加了整个数据集的误差贡献。
* 2. **对每个模式的所有输出神经元的误差平方进行求和**：这个步骤考虑了单个数据点对所有输出的贡献。

![image-20231128011608524](D:\笔记\笔记图片\image-20231128011608524.png)

* 由于t，r,m,都是固定的值，所以将RMS理解成一个函数，唯一受影响的就是X。

![image-20231128011806010](D:\笔记\笔记图片\image-20231128011806010.png)

* 若是将X也视作一个函数，影响X的值就是各个权重w，因为a是固定的，是一个恒定值

![image-20231128012350584](D:\笔记\笔记图片\image-20231128012350584.png)

* 最终可以获得这个函数

![image-20231128012437939](D:\笔记\笔记图片\image-20231128012437939.png)

* **<font color=red>The best performance of the network</font>** over a given data set D corresponds to **<font color=red>the minimum of the RMS error</font>**, and we adjust the weight of connections w in order to reach the minimum.
* 在给定的数据集 D 上，网络的最佳性能与均方根误差的最小值相对应，我们通过调整连接权重 w 来达到最小值。

![image-20231128013437613](D:\笔记\笔记图片\image-20231128013437613.png)

![image-20231128013458705](D:\笔记\笔记图片\image-20231128013458705.png)

![image-20231128013754599](D:\笔记\笔记图片\image-20231128013754599.png)

* 最终，函数收敛converged。

## Lecture15_Peceptron_2

### 15.1 **A Running Example**

![image-20231128060256517](D:\笔记\笔记图片\image-20231128060256517.png)



![image-20231128061555933](D:\笔记\笔记图片\image-20231128061555933.png)



![image-20231128061607332](D:\笔记\笔记图片\image-20231128061607332.png)

![image-20231128061701216](D:\笔记\笔记图片\image-20231128061701216.png)

![image-20231128061710883](D:\笔记\笔记图片\image-20231128061710883.png)

## Lecture 16 Peceptron_3

### 16.1 Convergence of Perceptron Learning Algorithm

* **<font color=red size=5>The perceptron learning algorithm can converge for the data set that is linearly separable</font>**
* 对于线性可分离的数据集，感知器学习算法可以收敛

![image-20231128064347408](D:\笔记\笔记图片\image-20231128064347408.png)

* Without loss of generality, we consider a simplified case. 
* 在不失一般性的前提下，我们考虑一种简化的情况。
  * There is only one output in the network
  * 我们一般考虑在神经网络只输出一个结果
  * The learning rate C is set as 1.
  * 学习率被设置为1

![image-20231128064533510](D:\笔记\笔记图片\image-20231128064533510.png)

* Recall the following informal definition we mentioned for MP neuron. 
* 回顾一下我们提到的 MP 神经元的非正式定义。
* **<font size=5>Linear separability</font>** (for Boolean functions): There exists a line (plane) such that all inputs which produce a 1 for the function lie on one side of the line (plane) and all inputs which produce a 0 lie on other side of the line (plane).
* 线性可分性（布尔函数）： 存在一条线（一个平面），使得函数产生 1 的所有输入都位于该线（平面）的一边，而产生 0 的所有输入都位于该线（平面）的另一边。

* ![image-20231128065104038](D:\笔记\笔记图片\image-20231128065104038.png)

![image-20231128065236972](D:\笔记\笔记图片\image-20231128065236972.png)

![image-20231128065814800](D:\笔记\笔记图片\image-20231128065814800.png)

#### 16.1.1 Perceptron Learning Algorithm (One output)

![image-20231128070039656](D:\笔记\笔记图片\image-20231128070039656.png)

* Rewriting the general perceptron learning algorithm. 
  * Since we only consider one output, the result becomes a weight vector w=(w0, w1, w2......, wn)  rather than the weight matrix. Here wi represents for the weight of the connection between the i-th input and the output.
  * 由于我们只考虑一个输出，结果就变成了权重向量 w=（w0, w1, w2......, wn），而不是权重矩阵。这里 wi 代表第 i 个输入和输出之间的连接权重。

![image-20231128071912265](D:\笔记\笔记图片\image-20231128071912265.png)

* 由于线性可分，我们将D`分为P和N两个数组，通过这个来对进行划分。

![image-20231128072120081](D:\笔记\笔记图片\image-20231128072120081.png)

* **The convergence of the learning rule means we successfully find a feasible w∗!** 
* **当学习率递归的时候意味着寻找特征w成功**

![image-20231128072347291](D:\笔记\笔记图片\image-20231128072347291.png)

![image-20231128072516169](D:\笔记\笔记图片\image-20231128072516169.png)

![image-20231128072601258](D:\笔记\笔记图片\image-20231128072601258.png)



#### 16.1.2 Geometric Interpretation 几何解读

![image-20231128072736562](D:\笔记\笔记图片\image-20231128072736562.png)

* Red arrows denote the points in P, 
* 红色箭头表示在集合P的点
* Blue arrows denote the points in N, 
* 蓝色的箭头表示在集合N的点
* Thick black line denotes the barrier of w*T a = 0

![image-20231128073740105](D:\笔记\笔记图片\image-20231128073740105.png)

![image-20231128073728493](D:\笔记\笔记图片\image-20231128073728493.png)

*  **<font size=5>Orthogonal 横向</font>**

![image-20231128074227748](D:\笔记\笔记图片\image-20231128074227748.png)



![image-20231128074738388](D:\笔记\笔记图片\image-20231128074738388.png)



![image-20231128074956470](D:\笔记\笔记图片\image-20231128074956470.png)

![image-20231128075011764](D:\笔记\笔记图片\image-20231128075011764.png)

![image-20231128075114948](D:\笔记\笔记图片\image-20231128075114948.png)

![image-20231128080434134](D:\笔记\笔记图片\image-20231128080434134.png)

![image-20231128080817764](D:\笔记\笔记图片\image-20231128080817764.png)

* 这里的权重wk被分配为1

![image-20231128084625011](D:\笔记\笔记图片\image-20231128084625011.png)

![image-20231128084732241](D:\笔记\笔记图片\image-20231128084732241.png)

![image-20231128084802452](D:\笔记\笔记图片\image-20231128084802452.png)

* 我们得到了分母的上限

![image-20231128085329791](D:\笔记\笔记图片\image-20231128085329791.png)

![image-20231128085531575](D:\笔记\笔记图片\image-20231128085531575.png)

* 得到结果

![image-20231128085612816](D:\笔记\笔记图片\image-20231128085612816.png)

![image-20231128085640957](D:\笔记\笔记图片\image-20231128085640957.png)

![image-20231128085650532](D:\笔记\笔记图片\image-20231128085650532.png)

![image-20231128090309275](D:\笔记\笔记图片\image-20231128090309275.png)



## Lecture 17  Multi-Layer Perceptron_0

![image-20231128222745929](D:\笔记\笔记图片\image-20231128222745929.png)

![image-20231128223654328](D:\笔记\笔记图片\image-20231128223654328.png)

* 具体来说，我们关心的是S这个公式的符号。
* w的方向非常重要，而不是长度。比如|w|不中用
* 将学习规则视为在不同情况下改变 w 方向的方法。
* Consider the learning rule as the ways to change the direction of w under different situations.
* 那么，感知器学习规则的收敛性可以认为是，w 最终与存在但未知的最优 w* 具有相似的方向。
* Then the convergence of perceptron learning rule can be considered as that w finally has the similar direction with the optimal w* that exists but is unknown.
* 在证明过程中，我们要做的是证明 w 和 w∗ 之间的夹角会随着w∗数目的增加而变小（不一定是单调的）。和 w∗ 之间的夹角会随着误分类次数的增加而变小（不一定是单调的 的角度会越来越小（不一定是单调的），并且不会小于 0。

![image-20231128224321379](D:\笔记\笔记图片\image-20231128224321379.png)

### 17.1 Beyond Linear Separability

![image-20231128224521993](D:\笔记\笔记图片\image-20231128224521993.png)

* 现在我们知道，对于线性可分离的数据集，感知器学习算法最终可以收敛。收敛。
* **那么，不可线性分离的数据集呢？**
* **最著名的例子就是 "XOR"（排他 "OR"）门、 称为 XOR 问题。**



#### 17.1.1 The XOR Problem （一个典型的非线性问题）

![image-20231128225013099](D:\笔记\笔记图片\image-20231128225013099.png)

![image-20231128230120370](D:\笔记\笔记图片\image-20231128230120370.png)

* 由上面这个式子可以证明XOR不符合线性可分



![image-20231128231233712](D:\笔记\笔记图片\image-20231128231233712.png)

* Minsky and Papert showed that in the case of any non-linearly separable problem, such as XOR, in the network architecture there must be **<font color=red size=5>“hidden neurons”</font>**, i.e. the neurons with output not available to the outside world, in order to help turn the problem into a linearly separable one for the outputs.
* 明斯基和帕帕特指出，在任何非线性可分问题（如 XOR）的情况下，网络结构中必须有 "隐藏神经元"，即对外部世界没有输出的神经元，以帮助将问题转化为输出的线性可分问题。

#### 17.1.2 Hidden Neurons

![image-20231128233328557](D:\笔记\笔记图片\image-20231128233328557.png)

* Minsky and Papert showed that in the case of any non-linearly separable problem, such as XOR, in the network architecture there must be “hidden neurons”, i.e. the neurons with output not available to the outside world, in order to help turn the problem into a linearly separable one for the outputs.

* 明斯基和帕帕特指出，在任何非线性可分问题（如 XOR）的情况下，网络结构中必须有 "隐藏神经元"，即对外部世界没有输出的神经元，以帮助将问题转化为输出的线性可分问题。

![image-20231128234001899](D:\笔记\笔记图片\image-20231128234001899.png)

* The three-layer perceptron below is capable to represent XOR. 
* 下面的三层感知器能够表示 XOR。
* Each hidden neuron separates the input space into a **closed positive** and **open negative half-space**. 
* 每个隐藏神经元将输入空间分为封闭的**正半空间和开放的负半空间**。
* The left bottom figure shows the linear separations defined by each hidden unit, while the positive half-spaces are shaded. 
* 左下图显示了每个隐藏单元定义的线性分隔，而正半空则用阴影表示。



* 这里解释一下这里的hidden neuron, **标注为 −0.5−0.5 的值是两个隐藏层神经元的偏置项。**在神经网络中，每个神经元可以有一个偏置项，这个偏置项是在计算神经元的总输入时加上的一个常数。偏置项的作用是使得神经元激活函数的阈值可以调整，这样即使所有输入都是零，神经元也可以输出一个非零值。
* ![image-20231128234429518](D:\笔记\笔记图片\image-20231128234429518.png)



![image-20231128234448598](D:\笔记\笔记图片\image-20231128234448598.png)



#### 17.1.3 Multilayer Perceptron 多重感知器

![image-20231128234556845](D:\笔记\笔记图片\image-20231128234556845.png)

* A multilayer perceptron (MLP) is a layered architecture of neurons, where 
* 多层感知器（MLP）是一种神经元分层结构，其中
  * all the neurons are divided into - subsets, each set is called a layer; 
  * 所有神经元被分为 - 个子集，每个子集称为一层；
  * There are only connections between two adjacent layers. Usually, the neurons within a layer are not connected to each other, though some neural models make use of this kind of architecture. 
  * 相邻两层之间只有连接。通常情况下，层内的神经元之间没有连接，但有些神经模型会使用这种结构。

![image-20231128234918046](D:\笔记\笔记图片\image-20231128234918046.png)

* The first layer is **the input layer** (We don’t usually count it); 
* 第一层是输入层（我们通常不计算它）；
* The last layer is **the output layer**. 
* 最后一层是输出层。
* All other layers with no direct connections from or to the outside are called **hidden layers**. 
* 所有与外部没有直接联系的其他层都称为隐藏层。



![image-20231128235232325](D:\笔记\笔记图片\image-20231128235232325.png)

* We consider the fully-connected architectures in this module, that is, **every neuron from one layer is connected to all neurons in the following layer.** 
* 我们在本模块中考虑了全连接架构，**即一层的每个 都与下一层的所有神经元相连接**
* Each connection is associated with **a real weight and a real bias**. 
* 每个连接都与**实际权重和实际偏差**相关联。
* Inputs are real. Outputs are real.
* 输入是真实的。输出是真实的。



![image-20231128235451085](D:\笔记\笔记图片\image-20231128235451085.png)

* The input is processed and propagated from one layer to the next, until the final result is computed. 
* 输入经过处理后从一层传播到下一层，直到计算出最终结果。
* This process represents **<font color=red size=5>the forward propagation</font>**. 
* 这个过程就是**前向传播**。
* For simplicity, from now we assume **<font color=red>the biases in the network are all zero.</font>**
* 为简单起见，从现在起我们假设**网络中的偏差均为零。**



![image-20231128235815096](D:\笔记\笔记图片\image-20231128235815096.png)

* The difference of the multilayer perceptron, compared to the single layer one, is that the output value X' of the first layer is not the output value of the multilayer perceptron any more. 
* 多层感知器与单层感知器的区别在于，第一层的输出值 X'不再是多层感知器的输出值。
* The output value X' of the first layer is the input to the next layer.
* 第一层的输出值 X' 是下一层的输入。

![image-20231129000534879](D:\笔记\笔记图片\image-20231129000534879.png)

![image-20231129000651132](D:\笔记\笔记图片\image-20231129000651132.png)

* First of all, we introduce the computation for a single neuron. For instance, consider the first neuron in the first hidden layer.
* 首先，我们介绍单个神经元的计算。例如，考虑第一个隐藏层的第一个神经元。

![image-20231129001549392](D:\笔记\笔记图片\image-20231129001549392.png)

* We start from the first hidden layer. The output of the 3-th neuron in the first layer is
* 我们从第一隐藏层开始。第一层第 3 个神经元的输出为

![image-20231129002048335](D:\笔记\笔记图片\image-20231129002048335.png)

![image-20231129002141982](D:\笔记\笔记图片\image-20231129002141982.png)

* The process of such layer-by-layer calculation to obtain the output of a multilayer perceptron is thus called **forward propagation.**
* 因此，这种逐层计算以获得多层感知器输出的过程被称为**前向传播。**

##### 17.1.3.1 A Running Example

![image-20231129003344268](D:\笔记\笔记图片\image-20231129003344268.png)

![image-20231129003405620](D:\笔记\笔记图片\image-20231129003405620.png)

* 这里需要解释一下ID函数和sigmoid函数
* 在第一层隐藏层中，因为所使用的激活函数是**恒等函数（identity function，通常表示为 *id*）**
* 在第二层隐藏层中，使用的是 **Sigmoid 激活函数**，这是一种常用的非线性激活函数

![image-20231129003414411](D:\笔记\笔记图片\image-20231129003414411.png)

![image-20231129003627641](D:\笔记\笔记图片\image-20231129003627641.png)

* 通过以上计算可以得到各个节点的值，但是注意，第二层的节点的值需要通过sigmoid计算得到X

![image-20231129003821310](D:\笔记\笔记图片\image-20231129003821310.png)

* **Issue: The hidden neurons cannot be trained by making their outputs become closer to the desired values given by the training set.** 
* **问题： 无法通过让隐神经元的输出更接近训练集给出的期望值来训练隐神经元。**



## Lecture 18_Multilayer_Peceptron_1

### 18.1 Gradient Decent and Activation Function Design 梯度修正和激活函数设计

![image-20231129005952810](D:\笔记\笔记图片\image-20231129005952810.png)

* The output error of a multilayer perceptron for the k-th input pattern is a half of the squared error:
* 多层感知器对第 k 个输入模式的输出误差是平方误差的一半

![image-20231129010057432](D:\笔记\笔记图片\image-20231129010057432.png)

* Now we define the performance of multilayer perceptron over a Data set D as a half of the total squared error:

* 现在，我们将多层感知器在数据集 D 上的性能定义为总平方误差的一半：

![image-20231129011113331](D:\笔记\笔记图片\image-20231129011113331.png)

* Now we define the performance of multilayer perceptron over a Data set D as a half of the total squared error:
* 现在，我们将多层感知器在数据集 D 上的性能定义为总平方误差的一半：

![image-20231129011331797](D:\笔记\笔记图片\image-20231129011331797.png)

![image-20231129011646959](D:\笔记\笔记图片\image-20231129011646959.png)

* During the training stage, the input value a to the network are the input vectors of the training set, which are constant parameters for the process. 
* 在训练阶段，网络的输入值 a 是训练集的输入向量，它们是过程的恒定参数。
* Therefore, the MLP error function E is a function of the weights of connections only:
* ![image-20231129011710473](D:\笔记\笔记图片\image-20231129011710473.png)
* 因此，MLP 误差函数 E 只是连接权重的函数：
* The better the MLP performs, the smaller the MLP error function E is.
* MLP 的表现越好，MLP 误差函数 E 就越小。
* Thus MLP learning can be considered as the optimization problem: min wE(w)
* 因此，MLP 学习可视为优化问题： min wE(w)



### 18.2 Gradient Decent 梯度下降

![image-20231129012016382](D:\笔记\笔记图片\image-20231129012016382.png)

* Gradient descent is based on the observation that if the multi-variable function F(x) is defined and differentiable in a neighborhood of a point a, then F(x) decreases fastest if one goes from a in the direction of the negative gradient of F at a, −∇F(a) . It follows that, if
* 梯度下降法的基础是，如果多变量函数 F(x) 在点 a 的邻域内是可定义和可微分的，那么如果从点 a 沿 F 在点 a 的负梯度方向（-∇F(a)）下降，F(x) 下降得最快。由此可见，如果

![image-20231129014559375](D:\笔记\笔记图片\image-20231129014559375.png)

* **<font color=red size>感觉非常像之前高中的求导，目的是寻找最大的值</font>**



![image-20231129015054752](D:\笔记\笔记图片\image-20231129015054752.png)



![image-20231129015020017](D:\笔记\笔记图片\image-20231129015020017.png)

![image-20231129015220388](D:\笔记\笔记图片\image-20231129015220388.png)

* Gradient descent method addresses the issue of how to update weights.
* 梯度下降算法解决了如何更新权重的问题。

![image-20231129015324874](D:\笔记\笔记图片\image-20231129015324874.png)

* One of the most popular techniques is called 
  * **error backpropagation,  （反向传播）**
* where the error of output neurons is propagated back to derive the weight adjustment of a given hidden neuron, based on how much the neuron contributes to the output error.
* 即根据输出神经元对输出误差的贡献程度，将输出神经元的误差反向传播，从而得出给定隐藏神经元的权重调整。
* The backpropagation algorithm updates the weights of connections w computationally efficiently based on the method of gradient descent.
* 反向传播算法基于梯度下降法，以高效的计算方式更新连接权重 w。
* **这里所说的就是通过反向传播来更新hidden layer中的权重。**

![image-20231129020338420](D:\笔记\笔记图片\image-20231129020338420.png)

* Gradient descent method addresses the issue of how to update weights. 
* 梯度下降法解决了如何更新权重的问题。
* The backpropagation algorithm makes the weight updating efficient.
* 反向传播算法使权重更新变得高效。

![image-20231129020551102](D:\笔记\笔记图片\image-20231129020551102.png)



## Lecture21_ Genetic Algorithms

 ### 21.1 Biological Motivation

![image-20231129043542589](D:\笔记\笔记图片\image-20231129043542589.png)

* Species adapt to the environment via **<font color=red>natural selection</font>**.
* 物种通过**自然选择**来适应环境。
* The selection favours those species for survival and further evolution that are best adapted to the environmental condition – **<font color=red>“survival of the fittest”</font>**.
* 选择有利于那些最能适应环境条件的物种生存和进一步进化--**"适者生存"**。
* <font color=red>**Phenotype**</font> is the manner of response and physical embodiment of an individual. There occur small, apparently random and undirected variations between the phenotypes of parents and their offspring.
* **<font color=red>表型</font>**是个体的反应方式和身体体现。亲代和子代的表型之间存在着微小的、明显随机的和非定向的变异。
* These **mutations** prevail through selection, if they prove their worth in the current environment; otherwise they perish.
* 如果这些**变异**在当前环境中证明了它们的价值，它们就会通过选择而获胜；否则，它们就会灭亡。



![image-20231129045600746](D:\笔记\笔记图片\image-20231129045600746.png)

* **<font color=red>Production of offspring</font>** is the basic driving force for selection. 
* **生产后代**是选择的基本动力。
* In a favourable environment, population grows exponentially. This growth is generally limited by **finite resources.** 
* 在有利的环境中，人口呈指数增长。这种增长通常受到**有限资源的限制**。
* When resources are no longer sufficient to support all individuals in a population, **only the fittest, i.e. those most effectively utilizing the resources, survive and produce offspring.** 
* 当资源不再足以支持种群中的所有个体时，**只有那些最适合的个体，即那些最有效地利用资源的个体，才能生存下来并繁衍后代。**
  * **In an unkind environment, organisms in a population are at a selective advantage to utilize resources most effectively.** 
  * **在不友善的环境中，种群中的生物具有选择性优势，能够最有效地利用资源。**

### 21.2 Neo-Darwinism Theory of Evolution (Microscope)

![image-20231129050046861](D:\笔记\笔记图片\image-20231129050046861.png)

* All living organisms consist of **cells**. 
* 所有生物体都由**细胞**组成。
* Each cell in an organism contains the same set of one or more **chromosomes** 
* 生物体中的每个细胞都含有相同的一组或多组**染色体**。
* Chromosomes are strings of **DNA** that serve as a **blueprint** for the organism. 
* 染色体是一串 DNA，是生物体的蓝图。

![image-20231129050510162](D:\笔记\笔记图片\image-20231129050510162.png)

![image-20231129050529652](D:\笔记\笔记图片\image-20231129050529652.png)

#### 21.2.1 DNA Structure DNA结构

![image-20231129050620438](D:\笔记\笔记图片\image-20231129050620438.png)

* A chromosome can be conceptually divided into genes --- **Gene is a functional block of DNA coding a particular protein.** 
* 从概念上讲，染色体可分为基因--基因是 DNA 的一个功能块，**编码一种特定的蛋白质**

#### 21.2.2 DNA Code DNA编码

![image-20231129050813943](D:\笔记\笔记图片\image-20231129050813943.png)

* DNA molecule consists of 
  * two ribbons of phosphate-sugar chains, and 
  * 两条磷酸-糖链，以及 
  * the horizontal rods of the pairs of nitrogenous bases holding the chains together 
  * 将糖链固定在一起的一对含氮碱基的水平杆
* **There exist only four different nitrogenous bases in DNA: <font color=red size=5>adenine, guanine, thymine, cytosine.</font>** 
* **DNA 中只有四种不同的含氮碱基：腺嘌呤、鸟嘌呤、胸腺嘧啶和胞嘧啶。**

![image-20231129051410751](D:\笔记\笔记图片\image-20231129051410751.png)

* The two chains held together by **hydrogen bonds(氢键)** formed between **pairs of bases 碱基对之间的序列** . 
* 通过碱基对之间形成的氢键将两条链固定在一起。
* Pairing is highly specific. It is always that 
* 配对具有高度特异性。总是这样 
  * Adenine pairs with Thymine, A = T; 
  * 腺嘌呤与胸腺嘧啶配对，A = T； 
  * Guanine pairs with Cytosine, G = C. 
  * 鸟嘌呤与胞嘧啶配对，G = C。
* **<font color=red>The precise sequence of bases carries the genetic information.</font>** 
* **<font color=red>碱基的精确序列携带着遗传信息。</font>**

![image-20231129052106058](D:\笔记\笔记图片\image-20231129052106058.png)

* The precise sequence of bases carries the genetic information. 
* 精确的碱基序列携带遗传信息。
* Gene is a functional block of DNA coding a particular protein. 
* 基因是 DNA 的一个功能块，编码一种特定的蛋白质。
* **Problem: there are just 4 letters in the DNA alphabet to code, but 20 amino acids氨基酸 found in proteins.**
* **问题：DNA 字母表中只有 4 个字母可以编码，但蛋白质中却有 20 种氨基酸。**

![image-20231129052540119](D:\笔记\笔记图片\image-20231129052540119.png)

* 首先，肯定不可以一一对应，因为数量上不够

![image-20231129052628237](D:\笔记\笔记图片\image-20231129052628237.png)

* There can not be a two nitrogenous bases to one amino acid match either, as it gives just 4^2 = 16 different pairs of nucleotides < 20
* 也不可能存在两个含氮碱基对一个氨基酸的匹配，因为这样就只有 4^2 = 16 对不同的核苷酸 < 20

![image-20231129053836846](D:\笔记\笔记图片\image-20231129053836846.png)

* **Nitrogenous bases(含氮碱基对)** in combination as a triplet are required to code for each amino acid, as this gives 4^3 = 64 possible combinations.
* 每个氨基酸都需要含氮碱基以三联体的形式组合编码，这样就有 4^3 = 64 种可能的组合。

![image-20231129054611269](D:\笔记\笔记图片\image-20231129054611269.png)

* The genetic code is **<font color=red>universal</font>**, as the codons that code for amino acids are the same in bacteria, plants and animals.
* 遗传密码是**通用**的，因为编码氨基酸的密码子在细菌、植物和动物中都是相同的。



##### 21.2.2.1 DNA Code Crossing-Over

![image-20231129054905132](D:\笔记\笔记图片\image-20231129054905132.png)

* **Organisms with unpaired sets of chromosomes are called haploid.** 
* **染色体不成对的生物称为单倍体。**
* **Organisms, whose chromosomes are arranged in pairs are called diploid.** Most sexually reproducing organisms are diploid.
* **染色体成对排列的生物称为二倍体。**大多数有性生殖的生物都是二倍体。 
* During sexual reproduction, **<font color=red>crossing-over</font>** or **<font color=red>recombination</font>** of genes in parent chromosomes occurs. In each parent cell, a pair of chromosomes first doubles, then the chromosomes exchange genes, and finally produce four gametes, single chromosomes, ready to couple with the other parent gametes to form a new diploid cell.
* 在有性生殖过程中，亲本染色体上的基因会发生**交叉或重组**。在每个亲本细胞中，一对染色体首先加倍，然后染色体交换基因，最后产生四个配子（单条染色体），准备与其他亲本配子结合形成新的二倍体细胞。



##### 21.2.2.2 DNA Code Mutations

![image-20231129060500575](D:\笔记\笔记图片\image-20231129060500575.png)

* **<font color=red>Mutation is a random change of a “letter”, single nucleotide in a chromosome.</font>** 
* **<font color=red>突变是染色体中一个 "字母"（单个核苷酸）的随机变化。</font>**
* Mutations usually result from copying errors in parent chromosomes and then are reproduced in offspring.
* 突变通常是由亲代染色体的复制错误引起的，然后在子代中复制。

##### 21.2.2.3 Neo-Darwinism Theory of Evolution

![image-20231129060659764](D:\笔记\笔记图片\image-20231129060659764.png)

* **Gene is a functional block of DNA coding a particular protein**, see “gene encodes a trait, e.g. eye colour”. 
* **基因是编码特定蛋白质的 DNA 功能块**，见 "基因编码性状，如眼睛颜色"。
* **Different possible settings for a trait**, e.g. blue, brown, black eye colour, are called alleles. 
* **一种性状的不同可能设置**，如蓝色、棕色、黑色的眼睛颜色，称为等位基因。
* Each gene is located at a particular **locus (position)** on the chromosome. 
* 每个基因都位于**染色体上的一个特定位点**（位置）。

![image-20231129061400113](D:\笔记\笔记图片\image-20231129061400113.png)

* **Gene is a functional block of DNA coding a particular protein**, see “gene encodes a trait, e.g. eye colour”. 
* **基因是编码特定蛋白质的 DNA 功能块**，见 "基因编码性状，如眼睛颜色"。
* **<font color=red>The complete collection of all genetic material,</font>** that is all chromosomes taken together, is called the organism’s **<font color=red>genome or genotype</font>**.
* **所有遗传物质的完整集合**，即所有染色体加在一起，称为生物体的**基因组或基因型。**

![image-20231129061648109](D:\笔记\笔记图片\image-20231129061648109.png)

* **<font color=red>Genes are transfer units of heredity.</font>** Genes are occasionally changed by mutations. 
* **基因是遗传的传递单位。**基因偶尔会因突变而改变。
* **Phenotype** expresses complex interaction within the genotype as well as its interaction with environment. 
* **表型**表达了基因型内部复杂的相互作用以及与环境的相互作用。

* Modern biochemistry and genetics explain microscopic mechanisms of heredity. 
* 现代生物化学和遗传学解释了遗传的微观机制。

![image-20231129062317397](D:\笔记\笔记图片\image-20231129062317397.png)

* **种群是不断进化的单位。**种群作为一个单位，限定了一个共同的基因库 包括所有个体的基因型。

![image-20231129062422939](D:\笔记\笔记图片\image-20231129062422939.png)

* **<font color=red size=5>Individual fitness</font>** is measured indirectly as the individual growth rate in comparison to others. 
* **个体适宜性**是通过与其他人相比的个体增长率来间接衡量的。
* **<font color=red>The fitness is the individual propensity to survive and reproduce in a particular environment. </font>**
* 适应性是个体在特定环境中生存和繁殖的倾向。
* Thus, **Natural Selection** according to the individual fitness 
* 因此，根据个体适宜性进行的**自然选择** 
  * is NOT an active driving force, 
  * 不是一种主动的驱动力
  * is differential survival and reproduction within a population.
  * 是种群内部生存和繁殖的差异
* 

![image-20231129070302988](D:\笔记\笔记图片\image-20231129070302988.png)

## Lecture22_Comp_appeal

* 紧接着Lecture21

![image-20231129070448112](D:\笔记\笔记图片\image-20231129070448112.png)

#### 22.1 Natural Evolution. Computational Appeal? **Natural Evolution. Computational Appeal?**

![image-20231129070549895](D:\笔记\笔记图片\image-20231129070549895.png)

* 基因如何映射到表型，然后再反应到适应性上



* map a given genotype into the corresponding phenotype and 
* 将给定的基因型映射到相应的表型中，以及 
* map the phenotype into the individual fitness to survive and reproduce ? 
* 将表型映射到个体的生存和繁殖能力？

![image-20231129071349474](D:\笔记\笔记图片\image-20231129071349474.png)

![image-20231129071533387](D:\笔记\笔记图片\image-20231129071533387.png)

![image-20231129071823271](D:\笔记\笔记图片\image-20231129071823271.png)

![image-20231129071836868](D:\笔记\笔记图片\image-20231129071836868.png)





##### 22.1.1 Parallelism 并行性

![image-20231129071636484](D:\笔记\笔记图片\image-20231129071636484.png)

* **<font color=red size=5>Parallelism 并行性</font>**
  * **Every individual in the population is tested independently in parallel with the others, and that speeds up evolution of the population.**
  * **种群中的每个个体都要与其他个体同时接受独立测试，这就加快了种群的进化速度。**



##### 22.1.2 Adaptation to a changing environment. 适应变化的环境

![image-20231129072121287](D:\笔记\笔记图片\image-20231129072121287.png)

* **<font color=red size=5>Adaptation to a changing environment.  适应不断变化的环境</font>**
  * **Due to the natural selection, only those individuals best fitted for the current environment do survive. The selection results in the population as a whole best adapted to the environment.**
  * **由于自然选择的作用，只有那些最适合当前环境的个体才能生存下来。选择的结果是整个种群最适应环境。**



##### 22.1.3 Optimization 优化

![image-20231129072350203](D:\笔记\笔记图片\image-20231129072350203.png)

* **<font color=red size=5>Optimization 优化</font>**
* Due to the natural selection, only individuals best fitted or “optimal” for the current environment do survive and reproduce. Thus, the selection also performs optimization on an individual level. 
* 在自然选择的作用下，只有最适合或 "最佳 "当前环境的个体才能生存和繁衍。因此，选择也是在个体层面上进行优化。





![image-20231129072533344](D:\笔记\笔记图片\image-20231129072533344.png)

* The listed features of the natural selection are very attractive for many problems in computer science.
* 对于计算机科学中的许多问题来说，自然选择的上述特点非常具有吸引力。
* As these parallelism, adaptation, and optimisation are achieved in nature by very simple manipulation of individual DNA sequences, it is tempting to use the algorithm for non-bio problem solving in engineering, computer science, etc.
* 由于这些并行性、适应性和优化性在自然界中是通过对单个 DNA 序列进行非常简单的操作来实现的，因此将该算法用于解决工程、计算机科学等领域的非生物问题是很有吸引力的。



### 22.2 Genetic Algorithms. Historical Introduction 遗传算法的历史简介

* **By 1950s, it became clear that** 
  * **if a solution of a computational problem might be formulated, i.e., coded, in a form of string of “characters”,** 
  * **如果一个计算问题的解决方案可以用 "字符 "串的形式来表述，即编码**
  * **then the optimal solution to the problem might be searched for using the natural selection technique among a “population”, i.e., set of candidate solutions.**
  * **那么就可以利用自然选择技术，在 "种群"（即一组候选解决方案）中寻找问题的最佳解决方案。**

![image-20231129073449846](D:\笔记\笔记图片\image-20231129073449846.png)

* 1950s-1960s -- several computer scientists independently studied evolutionary systems with the idea to use the algorithm to solve optimisation problems in engineering.
* 20 世纪 50 年代至 60 年代 -- 几位计算机科学家独立研究了进化系统，并萌生了使用该算法解决工程优化问题的想法。



![image-20231129073433085](D:\笔记\笔记图片\image-20231129073433085.png)

![image-20231129073635901](D:\笔记\笔记图片\image-20231129073635901.png)

![image-20231129073717202](D:\笔记\笔记图片\image-20231129073717202.png)

![image-20231129073736544](D:\笔记\笔记图片\image-20231129073736544.png)

* In contrast with Nature, 
  * **there is no universal code in GAs,** 
  * **全球定位系统中没有通用的编码**
  * **every coding is problem dependent.** 
  * **每个编码都取决于问题**
* The art of coding, though left beyond the scope, is very important in Genetic Algorithms, as from the very beginning the approach depends on whether the problem can be coded as a string of characters at all. 
* 编码艺术虽然不在本文讨论范围之内，但在遗传算法中却非常重要，因为从一开始，方法就取决于问题是否能被编码成一串字符。
* The above implies serious restrictions on the class of problems capable of solving by GAs. 
* 上述情况严重限制了全球定位系统所能解决的问题类别

## Lecture_23_Terminology

* 紧接着上一课的内容

### 23.1 GAs by John Holland: Chromosomes 约翰-霍兰的基因算法: 染色体

* **Definition: Genetic Algorithm’s Chromosome is <font color=red>a string of characters</font>**
* **定义 遗传算法的染色体是一串字符**
  * Often the GA chromosome is defined as a
  * 通常，GA 染色体被定义为 
    * Fixed length binary string,
    * **<font color=red>固定长度的二进制字符串</font>**



* 解释一下关于基因算法
* ![image-20231130053906363](D:\笔记\笔记图片\image-20231130053906363.png)

![image-20231130051518727](D:\笔记\笔记图片\image-20231130051518727.png)

* The same as nature blindly operates on real chromosomes and does not know or care what information is actually coded in the chromosomes, Holland had left behind the question of what particular information and in what way was coded in the strings of the Genetic Algorithms chromosomes
* 就像大自然盲目地对真正的染色体进行操作，不知道也不关心染色体中到底编码了什么信息一样，霍兰也抛开了遗传算法染色体串中到底编码了什么特定信息以及以何种方式编码的问题。

![image-20231130054040436](D:\笔记\笔记图片\image-20231130054040436.png)

* Haploid organisms, i.e., the organisms with on-paired chromosomes are considered in the Genetic Algorithms for some operators, e.g., crossover.
* 遗传算法中的某些运算符（如交叉）会考虑单倍体生物，即染色体成对的生物。

![image-20231130054048916](D:\笔记\笔记图片\image-20231130054048916.png)

* 遗传因子染色体与基因型重合，即基因型由单条染色体组成。

![image-20231130054309592](D:\笔记\笔记图片\image-20231130054309592.png)

* For simplicity, there is no phenotype concept in Genetic Algorithms either, and therefore we do not distinguish the following concepts:
  GAs chromosome = GAs genotype = GAs organism
* 为简单起见，遗传算法中也没有表型概念。因此我们不区分以下概念：
  **遗传算法染色体 = 遗传算法基因型 = 遗传算法生物体**

![image-20231130054448487](D:\笔记\笔记图片\image-20231130054448487.png)

* It is also called population of candidate solutions.
* 它也被称为候选方案群。

![image-20231130060319500](D:\笔记\笔记图片\image-20231130060319500.png)

* **In a GAs chromosome, a character represents a gene.**
* **在基因组染色体中，一个字符代表一个基因。**
* **Possible settings for a gene are called <font color=red>alleles</font>**, e.g. in the example above the alleles are 0s and 1s, and if a gene codes a trait then an allele is the trait instance. For binary chromosomes, the alleles “alphabet” consists of just two characters, 0 and 1. There might be bigger “alphabets” to represent bigger number of alleles.
* **基因的可能设置称为等位基因**，例如，在上面的例子中，等位基因是 0 和 1，如果一个基因编码一个性状，那么等位基因就是该性状的实例。对于二进制染色体，等位基因的 "字母表 "只有 0 和 1 两个字符。
* **Position of a gene in the string is called <font color=red>locus of the gene</font>.**
* **基因在字符串中的位置称为基因座。**



### 23.2 GAs by John Holland: Crossover 交叉

![image-20231130060846778](D:\笔记\笔记图片\image-20231130060846778.png)

* In nature, crossover occurs when two parents exchange parts of their corresponding chromosomes
* 在自然界中，当两个亲本交换其相应染色体的一部分时，就会发生交叉现象
* In a genetic algorithm, crossover recombines parts of two parent chromosomes to make two “children”.
* 在遗传算法中，交叉将两个亲代染色体的一部分重组为两个 "子代"。

![image-20231130070032927](D:\笔记\笔记图片\image-20231130070032927.png)

* **The crossover cutting point is chosen randomly.** 
* **交叉切点是随机选择的。**
* **<font color=red size=5>One-point crossover is considered most often.</font>**
* **最常考虑单点交叉。**

### 23.3 GAs by John Holland: Mutation

![image-20231130070248487](D:\笔记\笔记图片\image-20231130070248487.png)

* **<font color=red size=5>Mutation is random of allele of gene at randomly chosen location</font>**
* **突变是随机选择基因等位基因的位置**

![image-20231130070448967](D:\笔记\笔记图片\image-20231130070448967.png)

* **对于二进制染色体来说，这意味着在随机选择的位点上翻转一个比特，例如**
* **For binary chromosomes that means a flip of a bit at random chosen locus, e.g.,**

![image-20231130071124277](D:\笔记\笔记图片\image-20231130071124277.png)

* **For chromosomes with larger alphabet, mutation means replacement of a character at randomly chosen location with randomly chosen new character.** 
* **对于字母较大的染色体，突变意味着用随机选择的新字符替换随机选择位置上的字符。**



### 23.4 GAs by John Holland: Inversion and Translocation 反转和移位

![image-20231130071325249](D:\笔记\笔记图片\image-20231130071325249.png)

* **<font size=5>Inversion</font>** is a mutation when part of a chromosome is cut out, rotates by 180° and then fitted back into the same position
* **<font size=5>倒位</font>**是一种突变，即染色体的一部分被切掉，旋转 180°，然后装回原来的位置。
* ![image-20231130071354734](D:\笔记\笔记图片\image-20231130071354734.png)
* **<font size=5>Translocation</font>** is a mutation when part of a chromosome is cut out and moved to a different location in the chromosome:
* **<font size=5>移位</font>**是指染色体的一部分被切掉并移到染色体的另一个位置的突变：
* ![image-20231130071414187](D:\笔记\笔记图片\image-20231130071414187.png)



### 23.5 GAs by John Holland: Fitness Function 适应度函数

![image-20231130071751005](D:\笔记\笔记图片\image-20231130071751005.png)

* **To evaluate a chromosome fitness**, that is how good the candidate solution solves the problem, **a Genetic Algorithm uses fitness function.** 
* **为了评估染色体的适应度**，即候选方案解决问题的好坏，**遗传算法使用了适应度函数**。
* The fitness function
  *  Takes a chromosome as an input; 
  *  将染色体作为输入
  *  Produces its quantitative fitness evaluation as an output.
  *  将染色体的定量适配性评价作为输出

![image-20231130072141842](D:\笔记\笔记图片\image-20231130072141842.png)

![image-20231130072811565](D:\笔记\笔记图片\image-20231130072811565.png)

* The same as that a particular code to be used for coding a problem solution in a form of GAs chromosomes depends on the problem itself, a particular form of the fitness function also depends on the problem to be solved. 
* 就像在遗传算法染色体形式中编码问题解决方案所使用的特定代码取决于问题本身一样，特定形式的适应度函数也取决于要解决的问题。

![image-20231130072741847](D:\笔记\笔记图片\image-20231130072741847.png)



![image-20231130073014785](D:\笔记\笔记图片\image-20231130073014785.png)

* Two important requirements: 
  * Should **correlate closely with the designer's goal** 
  * 应与**设计者的目标密切相关**
  * Should be **computationally efficient**
  * 应具**有计算效率**

* Precise fitness function but computation is time consuming
* 适合度函数精确，但计算耗时
* Approximate fitness function but very efficient 
* **近似拟合函数，但非常高效（We Chose this way）**

![image-20231130073225398](D:\笔记\笔记图片\image-20231130073225398.png)

* Specifically, we may use approximate fitness function when:
* 具体来说，我们可以在以下情况下使用近似拟合函数
  * Precise fitness function is extremely time consuming;
  * 精确拟合函数非常耗时；
  * Precise fitness function is missing or hardly obtained;
  * 精确拟合函数缺失或难以获得；
  * Precise fitness function model itself contains uncertainties.
  * 精确拟合函数模型本身包含不确定性。

### 23.6 GAs by John Holland: Evolving unit 演化单位

![image-20231130073709107](D:\笔记\笔记图片\image-20231130073709107.png)

* The same as in nature, in **GAs Population** of chromosomes is **the evolving unit**. 
* 自然界相同，在遗传优化中，染色体群是进化单位。
* The GAs population evolves from **one generation** of chromosomes to the next generation and so on.
* 遗传算法的群体从一代染色体进化到下一代染色体，以此类推。

### 23.6 GAs by John Holland: Selection Operator 选择操作

![image-20231130075110302](D:\笔记\笔记图片\image-20231130075110302.png)

*  To simulate natural evolution of population of chromosomes, there must be **a rule how to choose which chromosome is more likely to produce offspring for the next generation.** 
*  要模拟染色体群体的自然进化，**必须有一个规则来选择哪条染色体更有可能为下一代产生后代。**
*  We shall call that rule **<font color=red>a selection operator.</font>** 
*  我们称这种规则为**选择算子。**
*  Usually, a selection operator is defined in a way that better fitted chromosome is selected for reproduction more often and therefore will produce more offspring.
*  通常，选择算子的定义是，更适合的染色体被更频繁地选择用于繁殖，因此会产生更多的后代。



### 23.7 GAs by John Holland: Search Space. 搜索空间

![image-20231130075400661](D:\笔记\笔记图片\image-20231130075400661.png)

* 由于遗传算法的目的是寻找问题的最佳解决方案，因此自然要为算法引入 "搜索空间"（Search Space）的概念。
* **定义：**
  **一个问题所有可能解决方案的集合称为遗传算法搜索空间。**
* 因此，我们要在可能解决方案的搜索空间中寻找问题的最佳解决方案。问题的最佳解决方案。

### 23.8 GAs by John Holland: Fitness Landscape 和适度图

![image-20231130075455752](D:\笔记\笔记图片\image-20231130075455752.png)

* A fitness landscape is a representation of all possible solutions along with their fitness. 
* 适合度景观是所有可能解决方案及其适合度的表示。
* The candidate solutions are represented by points in the coordinate plane, i.e. the search space, and corresponding fitness is measured along an additional dimension.
* 候选方案由坐标平面（即搜索空间）上的点表示，相应的适配度则沿着额外的维度进行测量。

![image-20231130075655203](D:\笔记\笔记图片\image-20231130075655203.png)

- 适合度景观是所有可能解决方案及其适合度的表示。
- 这里会有 "山峰"、"丘陵 "和 "山谷"，就像自然景观一样。景观。
- **<font size=5>进化使种群 向适合度的峰顶移动 景观。</font>**

## Lecture24_Basic_GAs

### 24.1 Basic Genetic Algorithms

![image-20231130214203640](D:\笔记\笔记图片\image-20231130214203640.png)

* a **“population”** of binary strings which he called **“chromosomes”**.
* 他称之为 "染色体 "的二进制字符串 "种群"。
* The **“population”** evolves using kind of **“natural selection”** together with the genetics- inspired operators of **crossover, mutation, and inversion**.
* 种群 "通过 "**自然选择** "与遗传学启发的**交叉、突变和反转**运算符一起进化。
* **Bits in a “chromosome” represent genes, and each “gene” is an instance of a particular “allele”, 0 or 1.**
* 染色体 "中的比特代表基因，每个 "基因 "都是特定 "等位基因"（0 或 1）的实例。
* The **selection operator** chooses those chromosomes in the population that will be allowed to reproduce, and on average the fitter chromosomes produce more offspring than the less fit ones.
* **选择算子**选择种群中可以繁殖的染色体，平均而言，适合的染色体比不适合的染色体产生更多的后代。
* **Crossover** exchange subparts of two chromosomes
* **交叉交换**两个染色体的子部分
* **Mutation** randomly changes the allele values at some locations in the chromosome.
* **突变**随机改变染色体上某些位置的等位基因值。
* **Inversion** reverses the order of a contiguous section of the chromosome rearranging the genes order.
* **倒置**将染色体上连续部分的顺序颠倒过来，重新排列基因顺序。



#### 24.1.1 Basic Structure of a Genetic Algorithm

![image-20231130214911289](D:\笔记\笔记图片\image-20231130214911289.png)

1. Randomly generate initial population of n bit strings (“chromosomes”). 

2. 随机生成由 n 个比特串（"染色体"）组成的初始群体。

3. **<font color=red size=5>Evaluate</font>** the fitness of each string in the population. 

4. 评估种群中每个字符串的适合度。

5. Repeat the following steps until next generation of n individual produced. 

   a. **<font color=red size=5>Select</font>** pair of parent chromosomes from current population according to their fitness, i.e. chromosomes with higher fitness are selected more often. 

   根据适配度从当前种群中选择一对父染色体，即适配度越高的染色体被选择的次数越多。

   b. Apply **<font color=red size=5>crossover</font>** (with probability). 

    应用交叉（概率）。

   c. Apply **<font color=red size=5>mutation</font>** (with probability of occurrence) . 

   应用突变概率

6. a. 根据适配度从当前种群中选择一对父染色体，即适配度越高的染色体被选择的次数越多。 b. 应用交叉（概率）。

7. Apply generational **<font color=red size=5>replacement</font>**. 

8. 应用世代**替换** 

9. Go to 2 or terminate if termination condition is met.

10. 如果满足终止条件，则转到 2 或终止。

##### 24.1.1.1 Example Implementation of a GA

![image-20231130215651741](D:\笔记\笔记图片\image-20231130215651741.png)

* Let length of each chromosome (binary string) l = 8. And the number of chromosomes in the population (population size) n = 4. 
* 假设每条染色体（二进制字符串）的长度为 l = 8，种群中染色体的数量（种群大小）为 n = 4。
* Fitness function f(x) is equal to **the number of ones in the bit string x.** 
* 适合度函数 f(x) **等于比特串 x 中的 1 的个数。**
* Selection operator. Fitness-proportionate selection, that is, the number of times an individual expected to be selected is equal to its fitness fi divided by the average fitness of the population ˉ*f*ˉ(平均值)(also known as **Roulette Wheel Selection**):
* 选择运算符。适合度比例选择，即个体被选中的次数等于其适合度 fi 除以种群的平均适合度 f(平均值)（又称**轮盘选择**）：

![image-20231130220457813](D:\笔记\笔记图片\image-20231130220457813.png)

###### 24.1.1.1.1 The First Generation

![image-20231130220615737](D:\笔记\笔记图片\image-20231130220615737.png)

![image-20231130220630421](D:\笔记\笔记图片\image-20231130220630421.png)

![image-20231130220716036](D:\笔记\笔记图片\image-20231130220716036.png)

![image-20231130221337390](D:\笔记\笔记图片\image-20231130221337390.png)

* chromosome number 1 shall be selected one time, 
* 1 号染色体应选择一次
* chromosome number 2 shall be selected two times, 
* 2号染色体应选择两次
* chromosome number 3 shall not be selected at all, 
* 第 3 号染色体根本不会被选中
* chromosome number 4 shall be selected one time. 
* 第 4 号染色体应选择一次

* ![image-20231130221359023](D:\笔记\笔记图片\image-20231130221359023.png)

![image-20231130221500236](D:\笔记\笔记图片\image-20231130221500236.png)

* **<font color=red>选择N最高的作为父本进行交叉</font>**

![image-20231130222115384](D:\笔记\笔记图片\image-20231130222115384.png)

* **Use a generator producing random numbers in the range between 0 and 1 to get a random number r for each pair of parental chromosomes.** 
* **使用随机数发生器，在 0 和 1 之间产生随机数，为每对亲本染色体获取随机数 r。**
* **If the random number r produced by the generator for the pair of “parents” is less or equal to the crossover probability pc, then apply crossover to the “parents” at randomly chosen locus, otherwise the parents do not crossover.** 
*  **如果生成器为一对 "亲本 "产生的随机数 r 小于或等于交叉概率 pc，则在随机选择的位点上对 "亲本 "进行交叉，否则亲本不进行交叉。**
* **If a pair of parents do not undergo crossover, their offspring are their identical copies**
* **如果一对 "亲本 "不进行交叉，那么它们的后代就是完全相同的拷贝**



![image-20231201000630789](D:\笔记\笔记图片\image-20231201000630789.png)

![image-20231201000723629](D:\笔记\笔记图片\image-20231201000723629.png)

* Use a generator producing random numbers in the range between 0 and 1 to get a random number r for each new chromosome. 
* 使用随机数发生器，在 0 和 1 之间产生随机数，为每条新染色体获取一个随机数 r。
* If the random number r is less or equal to the mutation probability pm(, apply mutation to the chromosome, i.e., flip a bit at randomly chosen locus.
* 如果随机数 r 小于或等于突变概率 pm(，则对染色体进行突变，即在随机选择的位点上翻转一位。

![image-20231201001053466](D:\笔记\笔记图片\image-20231201001053466.png)

![image-20231201001208119](D:\笔记\笔记图片\image-20231201001208119.png)

![image-20231201001718094](D:\笔记\笔记图片\image-20231201001718094.png)



###### 24.1.1.1.2 The Second Generation

**<font size=5>第二个例子</font>**

![image-20231201002511741](D:\笔记\笔记图片\image-20231201002511741.png)

![image-20231201002521589](D:\笔记\笔记图片\image-20231201002521589.png)

![image-20231201002650559](D:\笔记\笔记图片\image-20231201002650559.png)

![image-20231201002840659](D:\笔记\笔记图片\image-20231201002840659.png)



![image-20231201002851329](D:\笔记\笔记图片\image-20231201002851329.png)

![image-20231201002859929](D:\笔记\笔记图片\image-20231201002859929.png)

![image-20231201002911086](D:\笔记\笔记图片\image-20231201002911086.png)

![image-20231201002959902](D:\笔记\笔记图片\image-20231201002959902.png)

![image-20231201003013929](D:\笔记\笔记图片\image-20231201003013929.png)

![image-20231201003032901](D:\笔记\笔记图片\image-20231201003032901.png)

###### 24.1.1.1.3 The Third Generation

<font size=5>第三个例子</font>

![image-20231201004326283](D:\笔记\笔记图片\image-20231201004326283.png)

![image-20231201004410954](D:\笔记\笔记图片\image-20231201004410954.png)

![image-20231201004427316](D:\笔记\笔记图片\image-20231201004427316.png)

![image-20231201004451421](D:\笔记\笔记图片\image-20231201004451421.png)

![image-20231201004502347](D:\笔记\笔记图片\image-20231201004502347.png)

![image-20231201004549032](D:\笔记\笔记图片\image-20231201004549032.png)

![image-20231201004612330](D:\笔记\笔记图片\image-20231201004612330.png)

![image-20231201004912704](D:\笔记\笔记图片\image-20231201004912704.png)

###### 24.1.1.1.4 Evaluate The Fitness

![image-20231201005007720](D:\笔记\笔记图片\image-20231201005007720.png)

![image-20231201005015953](D:\笔记\笔记图片\image-20231201005015953.png)

* **<font color=red>The average fitness in the population of possible solutions increases with every generation. </font>**
* **可能的解决方案群体的平均适合度每一代都在增加**。

![image-20231201005023448](D:\笔记\笔记图片\image-20231201005023448.png)

## Lecture25_Schema_preliminary

![image-20231201012202852](D:\笔记\笔记图片\image-20231201012202852.png)

![image-20231201012303466](D:\笔记\笔记图片\image-20231201012303466.png)

![image-20231201012338912](D:\笔记\笔记图片\image-20231201012338912.png)



![image-20231201012352461](D:\笔记\笔记图片\image-20231201012352461.png)

![image-20231201012403620](D:\笔记\笔记图片\image-20231201012403620.png)

### 25.1 Why do GAs work?

![image-20231201012530542](D:\笔记\笔记图片\image-20231201012530542.png)

* Observation 1: **similar “looking” chromosomes do have similar fitness values.**
* 观察结果 1：**"看起来 "相似的染色体确实具有相似的适应度值。**
* Thus, we can obtain an almost optimal chromosome by searching for a chromosome that “looks” similar to the optimal solution;
* 因此，我们可以通过搜索 "看起来 "与最优解相似的染色体，得到一个几乎最优的染色体；
* Observation 2: A chromosome can be described by a set of “substrings”. Thus, **<font color=red>Similar “looking” chromosomes</font> ⟺ <font color=red>Their “substrings” are similar</font>**
* 观察结果 2：染色体可以用一组 "子串 "来描述。因此，**"看起来 "相似的染色体 ⟺ 它们的 "子串 "相似**

#### 25.1.1 Observation1

![image-20231201013005249](D:\笔记\笔记图片\image-20231201013005249.png)

![image-20231201013120846](D:\笔记\笔记图片\image-20231201013120846.png)

*  similar “looking” chromosomes do have similar fitness values, and therefore are taken for reproduction equally often. 
* 看起来 "相似 "的染色体确实具有相似的适应度值，因此被用于繁殖的次数也相同。

![image-20231201013205403](D:\笔记\笔记图片\image-20231201013205403.png)

* Observation 1 leads to a fact: 
* 观察结果 1 揭示了一个事实
  * **<font color=red>Similarities among highly fit strings guide the search. </font>**
  * **<font color=red>高度匹配的字符串之间的相似性会引导搜索。</font>**
* Combining with Observation 2 (**Similar chromosomes ⟺ Similar Substrings**), we focus on the similar “substrings” of chromosomes.
* 结合观察结果 2（相似的染色体 ⟺ 相似的子串），我们将重点放在染色体的相似 "子串 "上。

#### 25.1.2 Similarity Template = Schema 相似性模板 = 模式

![image-20231201014152993](D:\笔记\笔记图片\image-20231201014152993.png)

* Holland introduced a 
* 荷兰引入了一个 
  * **similarity template = schema = building block** 
  * **相似性模板 = 模式 = 构建模块** 
* **to describe subset of strings with similarities at certain positions.** 
* **来描述在某些位置上具有相似性的字符串子集。**

![image-20231201014451035](D:\笔记\笔记图片\image-20231201014451035.png)

* **A schema is a similarity template describing **
* **模式是一种相似性模板**
* **<font color=red size=5>a subset of strings with similarities at certain string positions.</font>**
* **用于描述在特定字符串位置上具有相似性的字符串子集。**
*  **Other name for a schema is a <font color=red>building block</font> of a chromosome.**
* **模式的另一个名称是染色体的构件。**



![image-20231201015322323](D:\笔记\笔记图片\image-20231201015322323.png)

* To describe building blocks of binary chromosomes, the following three letter alphabet is used.
* 为了描述二进制染色体的构建模块，使用了以下三个字母的字母表。
* ![image-20231201015525809](D:\笔记\笔记图片\image-20231201015525809.png)
* Here ∗ is a wildcard symbol, i.e., is a kind of **placeholder**, which can be interpreted as a number of literal characters.
* 这里的 ∗ 是一个通配符号，即一种**占位符**，可以解释为多个文字字符。
* ![image-20231201015534162](D:\笔记\笔记图片\image-20231201015534162.png)
* Example: 111**0 is a schema of the chromosome 111100
* 例如：111**0 是染色体 111100 的模式

![image-20231201015730102](D:\笔记\笔记图片\image-20231201015730102.png)

* Example: 111**0 is a schema of the chromosome 111100 
* 例如：111**0 是染色体 111100 的模式 
* The meaning of the schema is that it works a **pattern matching device:** 
* 模式的意义在于它是一种**模式匹配装置**： 
  * **a schema matches a particular string ⟺ at every location in the schema a 1 matches 1 in the string, a 0 matches a 0, or a * matches either.** 
  * **模式匹配特定的字符串 ⟺ 在模式中的每个位置，1 与字符串中的 1 匹配，0 与字符串中的 0 匹配，或者 * 与字符串中的任一个匹配。**

![image-20231201023238433](D:\笔记\笔记图片\image-20231201023238433.png)

![image-20231201023328054](D:\笔记\笔记图片\image-20231201023328054.png)

* To match a particular chromosome of a fixed length the schema must 
* 要与固定长度的特定染色体匹配，模式必须 
  * a) be of the same length, 
  * 长度相同
  * b) have either 
    * the same defining symbol as the chromosome does or 
    * 与染色体的定义符号相同，或者
    * an “*“ – placeholder symbol - at any particular locus
    * 在任何特定基因座上有一个 "*"--占位符

![image-20231201023356007](D:\笔记\笔记图片\image-20231201023356007.png)

* Thus, for each of the k placeholder positions, the chromosome that can be matched by the schema can have a 1 or a 0. So there will be 2^k chromosomes.
* 因此，对于 k 个占位符位置中的每个位置，模式可匹配的染色体可以是 1 或 0。



![image-20231201031349842](D:\笔记\笔记图片\image-20231201031349842.png)

![image-20231201031601104](D:\笔记\笔记图片\image-20231201031601104.png)

![image-20231201031629617](D:\笔记\笔记图片\image-20231201031629617.png)

* **How many building blocks are there in a particular chromosome of a fixed length l?** 
* **固定长度为 l 的特定染色体中有多少构件？**
* To match a particular chromosome of a fixed length the schema must 
* 要与固定长度的特定染色体相匹配，模式必须 
  * a) be of the same length, 
  * 长度相同
  * b) have either 
    * the same symbol as the chromosome does or 
    * 与染色体符号相同，或者 
    * an “*“ – placeholder symbol - at any particular locus
    * 在任何特定基因座上有一个 "*"--**占位符**



* Thus, in a binary chromosome of a length l there are 2^l building blocks, as a symbol at a particular locus in the chromosome must correspond to the same or the placeholder symbol in the corresponding locus in the schema. 
* 因此，在长度为 l 的二进制染色体中，有 2^l 个构建模块，因为染色体中特定位点上的符号必须与模式中相应位点上的相同或占位符号相对应。

##### 25.1.2.1 Order

![image-20231201032007881](D:\笔记\笔记图片\image-20231201032007881.png)

* **<font color=red>The Order of a schema H is represented as O(H) , denoting the number of defining symbols (non-* symbols) it contains.</font>**
* **模式 H 的顺序用 O(H)表示，表示它包含的定义符号（非*符号）的数量。**



##### 25.1.2.2 Defining Length

![image-20231201033150312](D:\笔记\笔记图片\image-20231201033150312.png)

![image-20231201033356208](D:\笔记\笔记图片\image-20231201033356208.png)

**定义**：模式的定义长度 *δ*(*H*) 指的是在模式中，两个定义符号（即非“*”符号）之间的最大距离。



![image-20231201033420026](D:\笔记\笔记图片\image-20231201033420026.png)





## Lecture26_Schema_Theorem

![image-20231201033632594](D:\笔记\笔记图片\image-20231201033632594.png)

### 26.1 Schema Theorem

![image-20231201035310343](D:\笔记\笔记图片\image-20231201035310343.png)

![image-20231201035824236](D:\笔记\笔记图片\image-20231201035824236.png)

#### 26.1.1 Schema Theorem: Proof

##### 26.1.1.1 crossover

![image-20231201040528086](D:\笔记\笔记图片\image-20231201040528086.png)

![image-20231201040544213](D:\笔记\笔记图片\image-20231201040544213.png)

![image-20231201042214192](D:\笔记\笔记图片\image-20231201042214192.png)

![image-20231201042200795](D:\笔记\笔记图片\image-20231201042200795.png)



##### 26.1.1.2 mutation

![image-20231201042315681](D:\笔记\笔记图片\image-20231201042315681.png)





















