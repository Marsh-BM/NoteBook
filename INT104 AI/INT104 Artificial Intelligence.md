



# INT104 Artificial Intelligence

## Lecture1

没什么重要的

## Lecture2

### Linear Algebra

#### Application

![image-20220316162240609](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220316162240609.png)

#### Linear Algebra Basics

​	1.Vector/Vector Space:

​	2.Linear Independence（线性独立）：线性独立一般是指向量的线性独立，指一组向量中任意一个向量都不能由其它几个向量线性表示。

* Linear dependence（线性相关）：与线性独立相反，即为任意一个向量都可以用其他的向量表示。

* Linear Combination(线性组合)：在向量空间中的任意的vector都可以用下面表达式表达。λ为常量。

![image-20220317102013893](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220317102013893.png)

![image-20220317102307062](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220317102307062.png)

#### Matrix Decomposition(矩阵分解)

矩阵分解就是将一个矩阵拆解为数个矩阵的乘积。

* Laplace Expansion(拉普拉斯展开式)：

  设A为任意nxn矩阵j是1到n的任意一个值，则A的行列式按第j列展开的拉普拉斯公式是：

  ![img](https://img-blog.csdn.net/20140226164009968)

![image-20220317111312955](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220317111312955.png)

* Eigenvalues and Eignvectors

  如果存在数m和非零n维列向量 x，使得 Ax=mx 成立，则称 m 是A的一个特征值（characteristic value)或本征值（eigenvalue)。x是特征向量。

  例子：

  ![image-20220317113513377](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220317113513377.png)

​				![image-20220317113526792](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220317113526792.png)



#### 数据降维

降维就是一种对高维度特征数据预处理方法。降维是将高维度的数据保留下最重要的一些特征，去除噪声和不重要的特征，从而实现提升数据处理速度的目的。在实际的生产和应用中，降维在一定的信息损失范围内，可以为我们节省大量的时间和成本。降维也成为应用非常广泛的数据预处理方法。

降维具有如下一些优点：

- \1) 使得数据集更易使用。
- \2) 降低算法的计算开销。
- \3) 去除噪声。
- \4) 使得结果容易理解。

降维的算法有很多，比如[奇异值分解(SVD)](https://link.zhihu.com/?target=https%3A//mp.weixin.qq.com/s/Dv51K8JETakIKe5dPBAPVg)、主成分分析([PCA](https://so.csdn.net/so/search?q=PCA&spm=1001.2101.3001.7020))、因子分析(FA)、独立成分分析(ICA)。





#### Singular Value Decomposition（SVD）奇异值分解

1.正交变换

公式：![image-20220317120418557](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220317120418557.png)

X是Y的正交变换 ，其中U是**正交[矩阵](https://so.csdn.net/so/search?q=矩阵&spm=1001.2101.3001.7020)**，X和Y为列向量 。

性质：1. 正交变换不改变向量的模。

			2. 正交变换不改变向量的夹角。

2.奇异值分解

![image-20220317120952741](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220317120952741.png)

![image-20220317121006561](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220317121006561.png)

![image-20220317121429217](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220317121429217.png)

例子

![image-20220317121543808](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220317121543808.png)

![image-20220317121639282](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220317121639282.png)

#### Principle Component Analysis(PCA/主成分分析)

主要思想：将n维的特征映射到k维上，这k维是全新的**正交特征**也被称为主成分，是在原有n维特征基础上重新构造出的k维特征。

PCA的工作就是重新从原始的空间中有顺序寻找一组互相正交的坐标轴，新的坐标轴选择与数据本身是密切相关的。

1. 第一个新坐标轴选择是原始数据中**方差最大**的的方向。
2. 第二个新坐标轴选取是与第一个坐标轴正交的平面中使得**方差最大**的。
3. 第三个轴是与第1,2个轴正交的平面中方差最大的。

* Standard deviation(标准差)![image-20220413213427436](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220413213427436.png)

* Variance (方差)![image-20220413213523067](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220413213523067.png)

* eigenvector(特征向量)![image-20220413220038972](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220413220038972.png)

  x为特征向量。

* eigenvalue(特征值)

  m为特征值。

* covariance(协方差)![image-20220413215910292](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220413215910292.png)

* covariance matrix(协方差矩阵)![image-20220413215934873](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220413215934873.png)

![image-20220413220239920](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220413220239920.png)

#### Independent Component Analysis(ICA)

![image-20220413220526668](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220413220526668.png)













## Lecture3

### Data Collection

#### Data Type

**Structured data(结构化数据)**

结构化数据是数据的数据库，即为行数据，存储在数据库里，可以用二维表结构来逻辑表达实现的数据。

![image-20220309101519615](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220309101519615.png)

**Unstructured Data(非结构化数据)**

非结构化数据,包括所有格式的办公文档、文本、图片、XML、HTML、各类报表、图像和音频/视频信息等等。

![image-20220309101531502](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220309101531502.png)



#### Data Storage And Presentation

* CSV(Comma Separated Values):一般就是我们**从数据库导出数据**的时候应该可以导出为CSV格式的文件。	一般用文本或excel打开，但excel可能会出现数据错误。CSV生成的数据表字段一般用**半角逗号**隔开。

* TSV（Tab Separated Values）tsv文件和[csv](https://so.csdn.net/so/search?q=csv&spm=1001.2101.3001.7020)文件类似。但是tsv是用**制表符**隔开每列数据。

* XML（*Extensible Markup Language*）：xml的作用是**传输和储存数据**，便于不同应用和平台间数据的共享和通信。

* RSS  (Really Simple Syndication)：RSS是一个**能让你在一个地方订阅**各种感兴趣网站的工具。简而言之：资讯聚合。

  ​	来举个例子，

![image-20220309103805205](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220309103805205.png)

* JSON (JavaScript Object Notation):说实话我没太搞懂这个东西是干嘛的，这是一种**传递对象的语法**，而这个对象可以是name/value对，数组和其他的对象。而根据网上的资料显示，这更类似于一个简易的数据库，比起真正的数据库，他更简单和轻量，可以很方便地存储数据供程序调用。

![image-20220309104824533](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220309104824533.png)

#### Data Pre-Processing

在工程实践中，我们得到的数据会存在有缺失值、重复值等，在使用之前需要进行[数据预处理](https://so.csdn.net/so/search?q=数据预处理&spm=1001.2101.3001.7020)。

常用的流程是：去**除唯一属性、处理缺失值、属性编码、数据标准化正则化、特征选择、主成分分析**。（或者是**数据清理、数据集成、数据变换和数据规约**）

在PPT中提到的更多的是数据清理

1.数据清理（Data Cleaning）

 数据清理主要针对数据数值上的各种异常情况的处理，根据数值异常情况的不同，数据清理常见的有以下：缺失值处理、离群和噪声值处理、异常范围及类型值处理。

​	1.1 缺失值处理

![image-20220309110949764](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220309110949764.png)

​	1.2 离群和噪声值处理

![image-20220309112917461](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220309112917461.png)

​	1.3 异常范围以及类型值的处理

![image-20220309113034904](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220309113034904.png) 

完整连接

https://blog.csdn.net/huguozhiengr/article/details/85162268?spm=1001.2101.3001.6650.1&utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ERate-1.pc_relevant_default&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7ECTRLIST%7ERate-1.pc_relevant_default&utm_relevant_index=1

#### Data Analysis VS Data Analytics

![image-20220309113951664](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220309113951664.png)

简单点来说，Analysis更注重分析过去的发生了什么，以及为什么发生。而Analytics 更倾向于为什么会发生以及未来会发生什么。

- Data analysis answers, “**What happened?**” while data analytics answers, “**Why, and What will happen next?**“

#### Data Analysis/Analytics Techniques

#### I.Descriptive Analysis（描述性分析）

- ***\*描述性分析\****是任何模型构建练习的第一部分。我们对历史数据进行分析，以确定因变量和自变量的模式和趋势。这一阶段也有助于假设生成、变量转换和特定行为模式的任何根本原因分析。

![image-20220310165221922](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220310165221922.png)

#### 1.Frequency Distriution（频率分布）

**Histogram（直方图）**

Histogram plot values of observations on the horizontal axis, with a bar showing how many times each value occurred in the dataset.

(直方图观察的值在横轴上绘制，以条形显示每个值在图中出现的次数。) 

* 这种被称为图像直方图。 其计算代价较小，且具有图像[平移](https://baike.baidu.com/item/平移/2376933)、[旋转](https://baike.baidu.com/item/旋转/2516)、[缩放](https://baike.baidu.com/item/缩放/5324343)不变性等众多优点，广泛地应用于图像处理的各个领域，特别是**灰度图像**的阈值分割、基于颜色的[图像检索](https://baike.baidu.com/item/图像检索/1150910)以及图像分类

![image-20220309185622499](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220309185622499.png)

##### 1.1The types of  Histogram

Normal distribution

![image-20220309190549961](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220309190549961.png)

Lack of symmetry (called **skew斜态**)

![image-20220309190844076](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220309190844076.png)

Pointiness(called kurtosis **峰度**)

![image-20220309191006213](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220309191006213.png)

#### 2.Measures of centrality（中心性）

Mean：Measure the central tendency of continous data as well as discrete dataset. (测量连续数据和离散数据的集中趋势)

![image-20220310162332983](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220310162332983.png)

**Median**(中值): The median is the middle score for a dataset that has been sorted according to the values of the data.

**Mode（**数据中最常出现的值，应该就是众数）：The mode is the most frequently occurring value in a dataset.

#### 3. Dispersion (离散度)of a Distribution（分布）

**Range**：The easiest way to look at the **dispersion** is to take the **largest score** and subtract it from the **smallest score**.(离散度用最小的分数减去最大的分数就行。)

**Interquartile（四分位居） Range**. One way around the range’s disadvantage is to calculate it after removing extreme values.(去除极值而计算出的rang值。)

**Variance**(方差). The variance is a measure used to indicate how spread out the data points are.	（x是平均数）

![img](https://bkimg.cdn.bcebos.com/formula/6f45b13ca943244c18d3354f4d386497.svg)

 ![image-20220310164247237](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220310164247237.png)

* 感觉这个减一写错了，以不减一的为准。下面一样。

**Standard Deviation**（标准差）

是离均差平方的算术平均数（即：方差）的算术平方根

![image-20220310164930528](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220310164930528.png)

#### II. Diagnostic analytics(预测分析)

![image-20220310165429396](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220310165429396.png)

利用correlation（相关性）去探究事物为何发生的原因。

***\*预测分析\****是分析的下一个阶段。这里，我们利用已清理和/或转换的数据，并在该数据上拟合一个模型，以预测因变量的未来行为。预测分析解决了可能发生的问题

**Correlation**: Correlation is a statistical analysis that is used to measure and describe the strength and direction of the relationship between two variables.（相关性是一种用于测量和描述两个变量之间的强度和方向的统计分析方法。）

Pearson’s r correlation（皮尔森相关度）:

![image-20220310170444822](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220310170444822.png)

#### III. Prescriptive analytics(规范性分析)

- ***\*规规范性分析\****是最后一个阶段，预测用于规定（或建议）下一组要做的事情。这就是我们奥迪沙政府的例子来源。他们利用气象部门的预测，采取了一系列措施，如安置低洼地区的所有人员，提前安排食物、住所和医疗救助等，以确保损失有限。

![image-20220310171349702](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220310171349702.png)

1. 收集数据
2. 清理误差过大或没有必要的值
3. 确定模式
4. 进行预测

#### IV.Exploratory analysis(探索性分析)

1.An approach to analyzing data sets to find previously unknow relationships.(分析数据集以发现之前没有发现的方法。)

2.Useful when we lack a clear question or a hypothesis （假说）

3.Example: Finding groups of similar genes from a collection of samples

#### V.Mechanistic analysis

1.Involves understanding the exact changes in variables that lead to changes in other variables for individual objects 
 2.Most common (and powerful) technique: regression(线性回归分析)



### Probability Basics(概率的基础知识)

#### 1. Discrete Probabilities(不连续的概率)

![image-20220310173538107](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220310173538107.png)

最后一个是在Y=y的条件下事件x发生的可能。

例子：抛硬币

#### 2.Continuous Probabilities（连续的概率）

![image-20220310173855368](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220310173855368.png)

例子：从1-100种抽出1-10的概率

#### 3. Gaussian Distribution(高斯分布/正态分布)

若随机变量X服从一个[数学期望](https://so.csdn.net/so/search?q=数学期望&spm=1001.2101.3001.7020)为μ、方差为σ^2的高斯分布，记为N（μ，σ^2）。其[概率密度函数](https://so.csdn.net/so/search?q=概率密度函数&spm=1001.2101.3001.7020)为正态分布的期望值μ决定了其位置，其标准差σ决定了分布的幅度。

* 数学期望其实就是加权平均数

![image-20220310175540477](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220310175540477.png)

![image-20220310175659828](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220310175659828.png)

#### 4. Conditional Probability

![image-20220310175822288](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220310175822288.png)

在x发生的条件下，y发生的概率



### Bayes‘ Theorem（贝叶斯定理）

![image-20220310180532578](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220310180532578.png)

![image-20220310181053453](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220310181053453.png)

## Lecture5

### 机器学习

1.Machine Learning: Field of study that gives computers the ability to learn without being explicitly programmed.

在没有明确的编程的的情况下，使机器拥有自主学习的领域

2.

#### 分类

Supervised Learning(监督学习)：

<font size=3 color="red">通过已有的一部分输入数据与输出数据之间的对应关系，生成一个函数，将输入映射到合适的输出，例如分类。</font>

**从给定的训练数据集中学习出一个函数（模型参数），当新的数据到来时，可以根据这个函数预测结果。监督学习的训练集要求包括输入输出，也可以说是特征和目标。**训练集中的目标是由人标注的。监督学习就是最常见的分类（注意和聚类区分）问题，通过已有的训练样本（即已知数据及其对应的输出）去训练得到一个最优模型（这个模型属于某个函数的集合，最优表示某个评价准则下是最佳的），再利用这个模型将所有的输入映射为相应的输出，对输出进行简单的判断从而实现分类的目的。也就具有了对未知数据分类的能力。监督学习的目标往往是让计算机去学习我们已经创建好的分类系统（模型）

Unsupervised Learning(无监督学习):

<font size=3 color="red">直接对输入数据集进行建模，例如聚类。</font>>

输入数据没有被标记，也没有确定的结果。样本数据类别未知，需要根据样本间的相似性对样本集进行分类（聚类，clustering）试图使类内差距最小化，类间差距最大化。通俗点将就是实际应用中，不少情况下无法预先知道样本的标签，也就是说没有训练样本对应的类别，因而只能从原先没有样本标签的样本集开始学习分类器设计。


Semi-supervised Learning(半监督学习/强化学习)

<font size=3 color = "red">综合利用有类标的数据和没有类标的数据，来生成合适的分类函数。</font>>







## Lecture7

### Unsupervised Learning(无监督学习)

1. 什么是无监督学习？
   1. Unsupervised learning wants to learn the underlying structure of the unlabelled data and be able to explain it.对于没有标签的未分类样本进行学习
2. 什么是聚类（Clustering）
   1. Clustering is the assignment of a set of observations into subsets (which is called **clusters**) so that observations in the same cluster are similar in some sense.聚类是将一组观察值分配到子集(称为集群)，以便同一集群中的观察值在某种意义上是相似的。//通过观察来赋给不同的样本不同的标签
3. 如何归纳未被聚类的无标签样本？
   1. Agglomerative clustering （逐次聚合）(bottom-up): hierarchical clustering（系统聚类法）
   2. Divisive clustering（分割聚合） (top-down): k-means

### Cluster（聚类）

什么是聚类（Clustering）

1. Clustering is the assignment of a set of observations into subsets (which is called **clusters**) so that observations in the same cluster are similar in some sense.聚类是将一组观察值分配到子集(称为集群)，以便同一集群中的观察值在某种意义上是相似的。//通过观察来赋给不同的样本不同的标签
2. 如何归纳未被聚类的无标签样本？
   1. Agglomerative clustering （逐次聚合）(bottom-up): hierarchical clustering（系统聚类法）
   2. Divisive clustering（分割聚合） (top-down): k-means

Evaluation(评估)：

The general idea of evaluating the performance of systems is to pursue a smaller intra-cluster distance but a larger inter-cluster distance. 即不同集群间差异最大，集群内部差距最小。

#### Distance Measurements（距离间的测量方法）

There are many ways to measure the distance between samples

1. **Euclidean Distance（欧几里得距离）**

   ![image-20220416195323948](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220416195323948.png)

2. **City Block Distance （曼哈顿距离）** 

   ![image-20220416195340027](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220416195340027.png)

---

1. Mahalanobis Distance （马氏距离）
2. Correlation Distance （相关距离）
3. Cosine Distance （余弦分类器）
4. Hamming Distance （海明距离）
5. Chebyshev Distance （切比雪夫距离）
6. Spearman Distance （斯皮尔曼距离）
7. Jaccard Distance（杰卡德距离）



#### Agglomerative Clustering

The general outline of agglomerative clustering is

![image-20220416195711236](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220416195711236.png)

1. For n objects v1, . . . , vn, assign each to a singleton cluster Ci = {vi} 将n个对象v1，v2，vn, 给它们之间每一个都分配一个单体聚类。

2. Use any computable cluster similarity measure D(Ci , Cj) e.g. Euclidean distance, cosine distance etc.  使用聚类计算方法计算距离，如Euclidean Distance（欧几里得距离），City Block Distance （曼哈顿距离）

3. Repeat{ 

   1. identify the two most similar clusters Cj and Ck (could be ties - choose one pair) 选两个相似的聚类（也可以选一个）

   2. delete Cj and Ck and add (Cj ∪ Ck ) to the set of clusters（删除聚类j和k，添加二者合并的聚类）

       } until just one cluster remains

4. Use a dendrogram diagram to show the sequence of cluster mergers.(使用树状图来显示集群合并的顺序)

![image-20220416195801463](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220416195801463.png)



#### Divisive Clustering

k-means algorithms: an algorithm to classify or to group your objects based on attributes or features into k number of groups, where k is a positive integer. **k-means算法**:一种基于属性或特征对对象进行分类或分组的算法，其中k是一个正整数。

流程

1. In the beginning, we determine the number of clusters (k) that we want and we assume the centroid or centre of these clusters. (决定我们需要k个集群，并确定每个集群的中心)
2. Then repeat the following steps until converge 
   1. Assign each training sample to the cluster with the nearest centroid.（给每一个样本分配到离质心最近的聚类）
   2.  Calculate the new centroid for each cluster（计算新的质心）
3. Stop until no samples changes the cluster belonged after an iteration.(直到迭代后集群没有发生改变为止)

![image-20220416201708099](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220416201708099.png)

具体过程:

 ![image-20220416204732801](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220416204732801.png)

![image-20220416204750117](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220416204750117.png)



### Model based Clustering

![image-20220416204912608](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220416204912608.png)

### Expectation Maximisation

![image-20220416204950720](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220416204950720.png)



## Tutorial7

### Bayes` Rule（贝叶斯定理）

![image-20220416205651799](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220416205651799.png)

### Model Likelihood（似然）

Model likelihood represents how likely a model will be observed according to the given posterior and prior probability hence can be used for model selection. (Model likelihood 根据后验概率和先验概率来预测模型的可能性，用于选择模型)

![image-20220416210110440](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220416210110440.png)

Frequentists choose the model with highest likelihood as the best model, which is known as **Maximum Likelihood Estimation (MLE)**.

### Log-likelihood(对数似然)

The Model likelihood of dataset D for a candidate model whose parameter sets are Θ has a likelihood of

![image-20220416211205958](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220416211205958.png)

For easier calculation, log-likelihood is commonly used which replace multiplications with additions i.e.

![image-20220416211615474](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220416211615474.png)

The base of logarithm does not matter but a base 2 or 16 could lead to a stronger practical meaning in computer-based systems.对数的基数并不重要，但在基于计算机的系统中，以2或16为基数可能具有更强的实际意义

![image-20220416211746461](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220416211746461.png)



### Bayesian Estimation(贝叶斯估计) & Laplacian Correction(拉普拉斯校正)

Considering the fact that if a case never appeared in the training dataset, how the model likelihood will be effected?（当）

This is known as a zero-point problem

A smooth process can be performed by introducing prior probability distribution, which is known as Bayesian Estimation

More commonly, an uniform distribution is used as the prior probability distribution, in which case, it is called Laplacian Correction



## Lecture 8

– Hand-on Practice of Machine Learning

### Load machine learning data

在开始机械学习之前，我们需要先加载数据。在绝大多数情况下，机器学习的数据都是CSV文件。 我们一般可以用以下三种方式用Python语言加载CSV数据。

1. Load CSV Files with the **Python Standard Library**
2. Load CSV Files with **NumPy.**
3. Load CSV Files with **Pandas**.

**Considerations when loading CSV data**(注意事项)

1. **File Header**: 注意数据是否有头文件（File Header）

* Note: A header of the CSV file is an array of values assigned to each of the columns. It acts as a row header for the data.

2. **Comments**：确定文件是否有注释（comments）如果您的文件中有注释，根据用于加载数据的方法，您可能需要指示是否需要注释。
3. **Delimiter(定界符)**:一般默认的分隔符(Delimiter)是     ‘ , ’, 如果要使用其他的符号作为分隔符(如空格或顿号)，需要指明。
4. **Quotes**(引用)：CSV文件中的字段值有时会被引用。默认的引号字符是双引号字符。可以使用其他字符，并且必须指定在文件中使用的引号字符。

#### 代码实例1：Python Standard Library

![image-20220420110345234](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220420110345234.png)

```
filename = 'pima-indians-diabetes.data.csv'
# open的作业是打开一个文件，下面的第一个参数是文件的绝对或相对路径，第二个是打开的模式
raw_data = open(filename,'rb')
# reader方法
reader = csv.reader(raw_data,delimiter=',', quoting = csv.QUOTE_NONE) # QUOTE_NONE表示不引用字段
# 将reader文件格式转换成list
x = list(reader)
# 把x转换成矩阵的形式
data = numpy.array(x).astype('float')
# 打印data的形状.即矩阵大小
print(data.shape)
```

**解释**：

1. quoting = csv.QUOTE_NONE 表示对象不引用字段（即不读取注释）
2. Open方法的相关参数![image-20220424161843182](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220424161843182.png)

3. **最后的(768,9)意味着一个789行，9列的矩阵**

#### 代码实例2：NumPy

![image-20220424163906651](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220424163906651.png)

```
filename = 'pima-indians-diabetes.data.csv'
raw_data = open(filename, 'rb')
# 用于读取文件，常见的用于读取CSV和txt文件
data = loadtxt(raw_data, delimiter=",")

print(data.shape)
```

解释：

1.**关于loadtxt()**

![image-20220424163729934](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220424163729934.png)

#### 代码实例3：Pandas

![image-20220424164251742](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220424164251742.png)

```
from pandas import read_csv
filename = 'pima-indians-diabetes.data.csv'
# 在DataFrame中的各种属性（attribute）名
name = ['preg', 'plas', 'pres', 'skin', 'test', 'mass', 'pedi', 'age', 'class']
# filename为文件名， names=name，指定列名。即按照name确定每一列的名称 
data = read_csv(filename, names=name)
print(data.shape)
```

### Understand your data

#### 1. Descriptive statistics

##### Looking at the raw data

![image-20220424165512335](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220424165512335.png)

```
from pandas import read_csv
filename = 'pima-indians-diabetes.data.csv'
# 在DataFrame中的各种属性（attribute）名
name = ['preg', 'plas', 'pres', 'skin', 'test', 'mass', 'pedi', 'age', 'class']
# filename为文件名， names=name，指定列名。即按照name确定每一列的名称
data = read_csv(filename, names=name)
# 意味读取先20行的数据
peek = data.head(20)
print(data.shape)
print(peek)
```



#### 2.Visualization

##### Data type for each attribute

![image-20220424173449877](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220424173449877.png)

```
from pandas import read_csv
filename = 'pima-indians-diabetes.data.csv'
# 在DataFrame中的各种属性（attribute）名
name = ['preg', 'plas', 'pres', 'skin', 'test', 'mass', 'pedi', 'age', 'class']
# filename为文件名， names=name，指定列名。即按照name确定每一列的名称
data = read_csv(filename, names=name)
# 意味读取先20行的数据
#peek = data.head(20)
# 获得各个列的数据类型
type = data.dtypes
print(type)
```

##### Descriptive statistics

![image-20220424173936860](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220424173936860.png)

![image-20220424173947476](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220424173947476.png)

```
from pandas import read_csv
from pandas import set_option
filename = 'pima-indians-diabetes.data.csv'
# 在DataFrame中的各种属性（attribute）名
name = ['preg', 'plas', 'pres', 'skin', 'test', 'mass', 'pedi', 'age', 'class']
# filename为文件名， names=name，指定列名。即按照name确定每一列的名称
data = read_csv(filename, names=name)
# set_option()主要用于设置DataFrame的显示输出
set_option('display.width', 100) # 表示横向最多显示多少字符
set_option('precision', 3) # 设置数值的精度，即精确到小数点后三位
description = data.describe()
```

**解释：**

1. set_option()这个函数主要用于设置DataFrame的显示输出。

##### Class distribution

![image-20220424175757907](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220424175757907.png)

```
from pandas import read_csv
from pandas import set_option
filename = 'pima-indians-diabetes.data.csv'
# 在DataFrame中的各种属性（attribute）名
name = ['preg', 'plas', 'pres', 'skin', 'test', 'mass', 'pedi', 'age', 'class']
# filename为文件名， names=name，指定列名。即按照name确定每一列的名称
data = read_csv(filename, names=name)
# groupby即为分组，下面所示的就是按照第9列进行分组，并通过size显示其大小
class_counts = data.groupby('class').size()
```

#### 3.Understand your data with descriptive statistics

##### **Correlations between attributes**

相关性是(Correlations)指两个变量之间的关系，以及它们如何可能或不可能一起变化。计算相关性最常用的方法是**皮尔森相关系数**(Pearson`s Correlation Coefficient)，它假定相关属性的正态分布。相关系数为-1或1分别表示完全负相关或完全正相关。而值为0则完全没有相关性。

![image-20220424180412447](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220424180412447.png)

```
from pandas import read_csv
from pandas import set_option
filename = 'pima-indians-diabetes.data.csv'
# 在DataFrame中的各种属性（attribute）名
name = ['preg', 'plas', 'pres', 'skin', 'test', 'mass', 'pedi', 'age', 'class']
# filename为文件名， names=name，指定列名。即按照name确定每一列的名称
data = read_csv(filename, names=name)
set_option('display.width', 100) # 表示横向最多显示多少字符
set_option('precision', 3) # 设置数值的精度，即精确到小数点后三位、
correlations = data.corr(method='pearson')
```

**解释：**

1. DataFrame.corr()的解释

   ![image-20220424181509435](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220424181509435.png)

   ![image-20220424181214044](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220424181214044.png)



##### Skew of Univariate Distributions(单变量分布的偏态)

偏态（Skew）是指假设为高斯分布(正态或钟形曲线)的分布在一个或另一个方向上发生偏移或压缩。

![image-20220424182314296](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220424182314296.png)

mode:峰值

median：中值

mean：平均值

![image-20220424182556319](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220424182556319.png)

```
from pandas import read_csv
from pandas import set_option
filename = 'pima-indians-diabetes.data.csv'
# 在DataFrame中的各种属性（attribute）名
name = ['preg', 'plas', 'pres', 'skin', 'test', 'mass', 'pedi', 'age', 'class']
# filename为文件名， names=name，指定列名。即按照name确定每一列的名称
data = read_csv(filename, names=name)
skew = data.skew()
```

**解释**：

1. Skew

   ![image-20220424182910099](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220424182910099.png)



#### 4. Understand your data with visualization

##### Histograms(直方图)

了解每个属性分布的快速方法是查看直方图。直方图将数据分组到容器中，并为您提供每个容器中观察到的数量的计数。从箱子的形状，您可以快速地了解属性是高斯分布、倾斜分布，甚至是指数分布。它还可以帮助您看到可能的异常值。

![image-20220424220339701](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220424220339701.png)

![image-20220424220503890](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220424220503890.png)

**解释**

1. data.hist()![image-20220424231053072](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220424231053072.png)
2. pyplot.show()显示一个图表



##### Density(密度)

密度图是快速了解每个属性分布的另一种方法。这些图看起来像一个抽象的直方图，通过每个箱子的顶部绘制了一条平滑的曲线，很像您的眼睛试图做的直方图。

![image-20220424230919910](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220424230919910.png)

```
from pandas import read_csv
from matplotlib import pyplot
from pandas import set_option
filename = 'pima-indians-diabetes.data.csv'
# 在DataFrame中的各种属性（attribute）名
name = ['preg', 'plas', 'pres', 'skin', 'test', 'mass', 'pedi', 'age', 'class']
# filename为文件名， names=name，指定列名。即按照name确定每一列的名称
data = read_csv(filename, names=name)
data.plot(kind='density', subplots=True, layout=(3, 3), sharex=False)
pyplot.show()
```

**解释：**

1. data.plot(kind='.....')一个绘图的函数。（plot就是一个绘图的函数。）

![image-20220424225900032](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220424225900032.png)

2. <font size=3 color="red">data.plot()的另外几个参数找不到解释了。。。</font>

#### Box and Whisker(箱线图)

箱线图的查找方法：



![image-20220428212433362](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220428212433362.png)

![image-20220428212459432](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220428212459432.png)

![image-20220428212328369](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220428212328369.png)

#### 5.Multivariate Plots

Normally, we have two ways to visually show the interactions between multiple variables in your dataset.

1. Correlation matrix plot(相关矩阵图)
2. Scatter plot maxtrix（）

##### Correlation matrix plot(相关矩阵图)

用来检验相关属性之间的关联性的方法。

![image-20220428214149404](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220428214149404.png)

![image-20220429112205837](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220429112205837.png)



**解释：**

1. DataFrame.corr()

![image-20220428215321203](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220428215321203.png)

2. add.subplots()# 改变画布的大小，如221就是2*2 1对应1号区等价于2，2，1
3. matshow() # 用于绘制数组或矩阵的函数。其中vmin=-1，和vmax=1是相关值得取值范围。
4. colorbar(), 用来添加颜色条。
5. add_axes([x,y,m,n])创建一块画布，里面得四个参数表示画布得位置和大小。
6. numpy.arange()如：三个参数0，9，1指从0开始到9，间隔为1. ![image-20220429111100367](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220429111100367.png)

​	![image-20220429111303213](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220429111303213.png)

7. set_xticks()和y.set_yticks()表示给x和y上加上刻度。参数如下：

![image-20220429111716206](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220429111716206.png)

![image-20220429111730966](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220429111730966.png)

8. set_xlabel和set_ylabel的作用是给x，y轴的每个刻度命名。

##### Scatter plot matrix(散点矩阵图)

![image-20220429113026244](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220429113026244.png)

![image-20220429113037602](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220429113037602.png)



![image-20220429112905605](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220429112905605.png)

#### 6. Prepare your data for machine learning

Many machine learning algorithms make assumptions about your data. It is often a very good idea to prepare your data in such way to best expose the structure of the problem to the machine learning algorithms that you intend to use.

Normal methods to prepare data: 

1. Rescale data. (调整数据)
2. Standardize data. （规范化数据）
3. Normalize data.（标准化数据）
4. Binarize data.（二值化数据）

##### Rescale data

当您的数据由具有不同规模的属性组成时，许多机器学习算法可以通过将属性重新调整为具有相同规模而受益。这通常被称为规范化，属性通常被重新缩放到0和之间的范围。

常用于：

1.optimization algorithms(最优化算法)

2.alogorithms that weight inputs(权值算法)

3.alogorithms that use distance measures(距离测算法)

![image-20220429122057951](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220429122057951.png)

![image-20220429124651381](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220429124651381.png)

解释：

1. data.values为返回data内所有的值
2. array[]的参数问题

![image-20220429122729517](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220429122729517.png)

![image-20220429122750090](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220429122750090.png)

![image-20220429122816318](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220429122816318.png)

![image-20220429122919047](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220429122919047.png)

![image-20220429122930864](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220429122930864.png)

![image-20220429122945286](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220429122945286.png)

![image-20220429123011149](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220429123011149.png)

3. MinMaxScaler()用于将每个元素（特征，feature）转换为给定范围的值。

![image-20220429123624748](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220429123624748.png)

4. fit_transform(self,X[,y]):**计算**并将数据**放缩**至给定区间，相当于`fit()`+`transform()`

![image-20220429174158545](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220429174158545.png)







![image-20220429124728399](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220429124728399.png)

![image-20220429124747002](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220429124747002.png)

![image-20220429124758273](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220429124758273.png)



#### Feature in machine Learning

在机器学习中，特征是原始数据的数值表示。给定一些数据，特征空间就是从该数据中选择一组特征的所有可能值的集合。

![image-20220429124937058](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220429124937058.png)

特征空间：所有**特征向量**存在的空间。每个具体的输入是一个实例，通常由特征向量表示。

## Lecture10

图像视觉化

k-nn和k-mean方法

基本上纯理论

## Lecture11

### NPL（自然语言处理）

#### Defination

自然语言处理是一种理论驱动的计算技术，用于在语言分析的一个或多个层次上分析和表示自然产生的文本，以便在一系列任务或应用中实现类似人类的语言处理

**难点：**

## Lecture12



# 其他

## CW2

![image-20220430011750910](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220430011750910.png)

一句话概括：random_state是一个**随机种子**，是在**任意带有随机性的类或函数里作为参数来控制随机模式**。当random_state取某一个值时，也就确定了一种规则。

PCA和TSNE的数据初始化模板，（将PCA方法改为TSNE方法就好。）

```
plt.figure()
plt.title('PCA')
pca = PCA(n_components=2)
dataset = np.concatenate([Class_0,Class_1,Class_2,Class_3,Class_4],axis=0)
scaler = StandardScaler()
dataset = scaler.fit_transform(dataset)
afterpca = pca.fit_transform(dataset)
```

![image-20220504111021802](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220504111021802.png)







![image-20220525110656048](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220525110656048.png)
