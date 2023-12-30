# COMP226

## 1. R语言 (1.1)

* R是用于统计分析、绘图的语言和操作环境。R是属于GNU系统的一个自由、免费、开源的软件，它是一个用于统计计算和统计制图的优秀工具
* R is a statistical computing platform, and complete programming language
* R是一个统计计算平台，也是一个完整的编程语言
* It is cross-platform, free, and open-source, so you can use it on your own or department computers
* 它是跨平台、免费和开源的，因此您可以在自己或部门的计算机上使用它
* R is one of the leading tools for statistics, data analysis, and machine learning; proficiency in R is a valuable skill
* R是统计、数据分析和机器学习的主要工具之一;精通R语言是一项宝贵的技能
* Lots of flexibility to develop and test trading strategies
* 开发和测试交易策略的灵活性很大
* Hundreds of user-contributed packages on CRAN, so many things have already been implemented for you
* CRAN上有数百个用户贡献的包，很多东西已经为您实现了
* R is very widely used and there is a lot of freely available information about it
* R被广泛使用，并且有很多关于它的免费信息

![image-20230523150509897](D:\笔记\笔记图片\image-20230523150509897.png)

![image-20230523150534376](D:\笔记\笔记图片\image-20230523150534376.png)



### 	1.1 Simple Arithmetic 简单的算法

![image-20230202195325752](D:\笔记\笔记图片\image-20230202195325752.png)

* 简单的+-*/

![image-20230523150846851](D:\笔记\笔记图片\image-20230523150846851.png)

* **<font size=5>source('文件名.R', echo=TRUE):这个函数的作用是加载loaded某个文件，注意需要将echo这个参数设置为Ture，该参数用于控制在运行脚本时是否可以显示代码的输出，当`echo=TRUE`时，运行脚本时会同时显示代码和输出结果，可以看到代码的执行过程。当`echo=FALSE`时，只会显示输出结果而不显示代码本身。</font>**



![image-20230523151514164](D:\笔记\笔记图片\image-20230523151514164.png)

* **<font size=5> '' * ''的作用是乘法</font>****
* **<font size=5>^的作用是乘方</font>**
* **<font size=5>sqrt的作用是开方</font>**







### 1.2 Variable Assignment (1.2)

* **<font size=5><- or with = 来对某个变量进行赋值</font>**

![image-20230202195308526](D:\笔记\笔记图片\image-20230202195308526.png)

### 1.3 Basic data types in R 基础的数据类型



![image-20230202194626082](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230202194626082.png)

* **<font size=5>character (strings)</font>**
* **<font size=5>logical (booleans - TRUE/FALSE)</font>**
* **<font size=5>numeric (numbers)</font>**
* **<font size=5>factors  (categories  -  used  a  lot  in  statistics;  we  won't  use them much)</font>**



### 1.4 Checking the data type with "is"

* **<font size=5>"<font color=red>is.某个数据类型(判断数据)</font>" 该函数用于检查数据类型，数据类型正确返回true，错误返回false</font>**
* ![image-20230202195224316](D:\笔记\笔记图片\image-20230202195224316.png)

* is.logical()可以用来判断正，如图所示



### 1.5 Converting types with "as"

* **<font size=5>"<font color=red>as.某个数据类型(目标数据)</font>"用于类型之间的相互转换。将一个数据从一个类型转换成另一个类型</font>**

![image-20230202200722600](D:\笔记\笔记图片\image-20230202200722600.png)

### 1.6 Vectors

* **<font size=5>在R语言中，Vector（向量）是一种基本的数据结构，用于存储一组相同类型的元素。它是R中最常用的数据结构之一，用于存储数字、字符、逻辑值等。Vector可以是一维的，即包含一个维度。它可以是以下类型之一：</font>**
* ![image-20230523152822754](D:\笔记\笔记图片\image-20230523152822754.png)

![image-20230202200824663](D:\笔记\笔记图片\image-20230202200824663.png)

### 1.7 Creating vectors: combine

* **<font size=5><font color=red>c </font>stands for combine and creates vectors from shorter vectors:</font>**

**![image-20230202200909664](D:\笔记\笔记图片\image-20230202200909664.png)**

* **Combine可以镶套, 在一个combine中可以调用多个其他的combine**



### 1.8 Creating vectors: seq

* **<font size=5><font color=red>seq</font> is used to generate regular sequences</font>**
* **<font size=5>Seq用于生成规则序列</font>**

![image-20230202201311262](D:\笔记\笔记图片\image-20230202201311262.png)

* **<font size=5>seq的参数</font>**
* seq的其他用法，from表示开始的数字，to表示结束的数字，**（也可以使用length.out=4来表示一个长度为4的vector）**，by表示每个数字的间隔
* ![image-20230523155434634](D:\笔记\笔记图片\image-20230523155434634.png)

* **length_out: 用于指定输出长度**
* ![image-20230523155356733](D:\笔记\笔记图片\image-20230523155356733.png)
* 

![image-20230202201719626](D:\笔记\笔记图片\image-20230202201719626.png)

![image-20230202201726602](D:\笔记\笔记图片\image-20230202201726602.png)



### 1.9 Lists

*  **<font size=5>在R语言中，List（列表）是一种复合数据结构，用于存储不同类型的对象（元素）的有序集合。</font>**
*  A list is an important and simple construct in R
* 列表是R语言中一个重要而简单的结构
*  Vector  elements  must  be  the  same  type;  list  element  types may differ
* 向量元素必须是相同的类型;列表元素类型可能不同

![image-20230202205939556](D:\笔记\笔记图片\image-20230202205939556.png)

* 通过这个图片，我们可以看出c(1,'hello')会将数据结构转换为对应类型。 list却可以存储多个不同类型的对象的有序集合。

![image-20230202210244113](D:\笔记\笔记图片\image-20230202210244113.png)

* **一个列表拥有不同的节点，每个节点可以存储不同类型的数据，甚至你可以给每一个节点取个名字**



* **Elements can be accessed by name, but are also ordered and can be accessed by index**
* **元素可以按名称访问，也可以按顺序访问，也可以按索引访问**

![image-20230202210557755](D:\笔记\笔记图片\image-20230202210557755.png)



### 1.10 Setting the working directory（1.3）

* **<font size=5>getwd(): 用于获得当前的工作路径</font>**
* **<font size=5>list.files(): 用于列出指定目录中的所有文件和文件夹，返回一个字符向量，每个元素表示一个文件或文件夹的名称。</font>**
* **<font size=5>`list.dirs()`函数用于列出指定目录下的所有子目录（包括子目录的子目录），返回一个字符向量，每个元素表示一个子目录的路径。</font>**
* **<font size=5>setwd("/private/tmp/R"):用于设定指定的工作路径</font>**

![image-20230202210826498](D:\笔记\笔记图片\image-20230202210826498.png)

![image-20230202210901913](D:\笔记\笔记图片\image-20230202210901913.png)

### 1.11 查看帮助文档 Searching for information in R

* **<font size=5>Within R, use a question mark before a method name to find out what something does, e.g.</font>**
* **<font size=5>在R中，在方法名前使用问号来找出它是做什么的，例如:</font>**
* **<font size=5>The question mark is actually shorthand for the help function. So we could also write</font>**
* **<font size=5>问号实际上是帮助函数的简写。我们也可以这样写</font>**
* 

![image-20230202211244079](D:\笔记\笔记图片\image-20230202211244079.png)



![image-20230202211302567](D:\笔记\笔记图片\image-20230202211302567.png)

* **<font size=5>对package使用help函数</font>**

![image-20230202211326057](D:\笔记\笔记图片\image-20230202211326057.png)



#### 1.11.1 Help when you don't knoyou'reat your looking for

* **<font size=5>查看某一确定关键字内容的文档，使用两个??</font>**
* 比如下面的“moving average”

![image-20230202214216158](D:\笔记\笔记图片\image-20230202214216158.png)



![image-20230202214232434](D:\笔记\笔记图片\image-20230202214232434.png)

### 1.12 Functions

* The following is an example of a function that computes the mean of the components of a vector (or list)
* 下面是一个函数的示例，用于计算向量(或列表)各分量的平均值)

![image-20230202214614298](D:\笔记\笔记图片\image-20230202214614298.png)

![image-20230202214621605](D:\笔记\笔记图片\image-20230202214621605.png)

* <font size=5>**给函数设置默认参数**</font>

![image-20230202214645023](D:\笔记\笔记图片\image-20230202214645023.png)

* 提供所有参数的数据
* We can specify multiple arguments with defaults, and override any number of them when calling the function
* 我们可以用默认值指定多个参数，并在调用函数时覆盖任意数量的参数
* **If arguments are not named in the call, the order matters, as this example demonstrates:**
* **如果参数在调用中没有被命名，顺序很重要，如下例所示:**

![image-20230202214740811](D:\笔记\笔记图片\image-20230202214740811.png)

* <font color=red>观察上面的例子，你可以发现最后一个将参数顺序调换了，重载了override，所以你可以发现完全可以重载某些函数。</font>

* No explicit return statement
* 没有显式的返回语句
* **<font size=5>If no explicit return statement is given in a function, then the last variable assignment is returned</font>**
* **如果函数中没有给出显式的返回语句，则返回最后一个变量赋值**
* E.g., the following functions will always return the same thing
* 例如，下面的函数总是返回相同的东西

![image-20230202214936667](D:\笔记\笔记图片\image-20230202214936667.png)

![image-20230202214945208](D:\笔记\笔记图片\image-20230202214945208.png)

### 1.13 Matrices 矩阵（1.6）

* **<font size=5>Matrices are the two-dimensional analog of vectors, in particular containing only one data type</font>**
* **<font size=5>矩阵是向量的二维模拟，特别是只包含一种数据类型</font>**
* 矩阵存储的数据类型必须相同
* 矩阵可以用于存储和处理具有相同维度和数据类型的数据。

![image-20230208165601971](D:\笔记\笔记图片\image-20230208165601971.png)

* **我们可以通过m[1,2]来通过索引得到对应的值**

### 1.14 Data Frames 数据框架

* **<font size=5>A data.frame shares the properties of matrices and lists; unlike a matrix a data.frame can have columns with different types of data</font>**
* data.frame共享矩阵和列表的属性;与矩阵不同，**data.frame可以包含不同类型数据的列**

![image-20230208170619132](D:\笔记\笔记图片\image-20230208170619132.png)

* **<font color=blue>需要保证每一列的行数相等</font>**

* <font color=blue>**paste（）：**从多个向量中获取多个元素，并将它们连接为一个元素。</font>

* ![image-20230523180031039](D:\笔记\笔记图片\image-20230523180031039.png)



### 1.15 Recyling 回收

* **<font size=5>在R语言中，Recycling（循环复用）是指在进行二元操作（如加法、减法、乘法等）时，当两个向量的长度不匹配时，R会自动复制较短的向量使其长度与较长的向量相等，以便进行元素之间的对应操作。</font>**
* ![image-20230523180417236](D:\笔记\笔记图片\image-20230523180417236.png)

* **<font color=red>在这个例子中，`vec1`和`vec2`的长度不匹配。根据Recycling的规则，R会将较短的向量`vec2`复制并重复使其长度与较长的向量`vec1`相等。然后，进行元素级别的相加操作，得到结果向量`result`。在这个例子中，`vec2`被复制成`4, 5, 4`，然后与`vec1`相加得到`5, 7, 7`。</font>**
* R  is  vectorized  and  recycles  elements  (e.g.,  for  creating  the  x column in the previous slide); another example we already saw:
* R是向量化的，并循环使用元素(例如，用于创建上一张幻灯片中的x列);我们已经看到的另一个例子:

![image-20230208172406248](D:\笔记\笔记图片\image-20230208172406248.png)

![image-20230208172521120](D:\笔记\笔记图片\image-20230208172521120.png)

![image-20230208172543540](D:\笔记\笔记图片\image-20230208172543540.png)

![image-20230523180901572](D:\笔记\笔记图片\image-20230523180901572.png)

![image-20230523180911701](D:\笔记\笔记图片\image-20230523180911701.png)

### 1.17 The Apply Family(1.7)

* **<font size=5>`apply()`函数是一个高级函数，用于对矩阵、数组或数据框的行或列进行迭代操作。</font>**
* The apply family serve as an alternatives  to  loops (similar to list comprehension in python; and map in functional programming)
* apply族可以作为循环的替代品(类似于python中的列表理解;函数式编程中的映射)
* The apply family, each member applies a function to the elements of a data structure:
* apply族，每个成员对数据结构的元素应用一个函数:
  * lapply (for lists/vectors)
  * Lapply(用于列表/向量)
  * sapply (simplified version of lapply)
  * Sapply (lapply的简化版本)
  * apply (for matrices/data.frames)
  * 应用(适用于矩阵/data.frames)
  * mapply (for multiple lists/vectors/matrices etc.)
  * Mapply(用于多个列表/向量/矩阵等)


![image-20230208192324443](D:\笔记\笔记图片\image-20230208192324443.png)



#### 1.17.1 Example：lapply/sapply

* The s in sapply stands for simple; sapply simplifies the output as much as possible, now returning a vector, not a list:
* sapply中的s代表简单;spapply尽可能地简化输出，现在返回一个向量，而不是一个列表:
* lapply函数正好相反，lapply函数 对列表、数据框按列进行循环，输入必须为列表(list)，返回值为列表(list)。**lapply(X, FUN, …)**

![image-20230208192536403](D:\笔记\笔记图片\image-20230208192536403.png)



#### 1.17.2 Example: apply

* ![image-20230524133819098](D:\笔记\笔记图片\image-20230524133819098.png)
* `X`：要操作的矩阵、数组或数据框。
* `MARGIN`：**指定操作的维度，取值为1表示按行操作，取值为2表示按列操作**。
* `FUN`：要应用的函数，可以是自定义的函数或内置函数。
* `...`：可选的额外参数，传递给应用的函数。

![image-20230208192909282](D:\笔记\笔记图片\image-20230208192909282.png)

#### 1.17.3 Example: mapply

* **在R语言中，`mapply()`函数是一个多元化的`apply()`函数，用于同时迭代多个对象，并将每个对象的对应元素传递给指定的函数进行处理。它可以方便地在多个对象之间进行操作，并将结果整合成一个向量、矩阵或数据框。**

![image-20230208193353086](D:\笔记\笔记图片\image-20230208193353086.png)

* **mapply is multivariate apply**
* **mapply对多个矩阵进行迭代操作**

![image-20230208193346727](D:\笔记\笔记图片\image-20230208193346727.png)

![](D:\笔记\笔记图片\image-20230208193430570.png)



![image-20230208193441704](D:\笔记\笔记图片\image-20230208193441704.png)

![image-20230208193447942](D:\笔记\笔记图片\image-20230208193447942.png)



* **<font color=red>小知识，<-表示赋值于局部范围，<<-表示赋值于全局范围</font>**

### 1.18 Financial time series and quantmod 金融时间序列和量子模型

* **<font size=5>A time series is a sequence of measurements indexed by time. The measurements can be</font>**
* **时间序列是以时间为索引的一系列测量值。测量可以是**
  * **at regular intervals\**
  * **定期间隔**
  * **or unevenly spaced (e.g., trade times)**
  * **或不均匀间隔(例如，交易时间)**
* Any trading strategies we develop will be based **on historical data that is indexed by time**
* 我们开发的任何交易策略都将基于按时间索引的历史数据
* It could be **daily price** and **volume data** or **tick data** (trades or orders that can happen at any time)
* 它可以是每日价格和成交量数据，也可以是波动数据(随时可能发生的交易或订单)。

#### 1.18.1 The quantmod package

![image-20230524140636169](D:\笔记\笔记图片\image-20230524140636169.png)

![image-20230524140816967](D:\笔记\笔记图片\image-20230524140816967.png)

![image-20230524141044348](D:\笔记\笔记图片\image-20230524141044348.png)

* Warning
  * Quantmod's **getSymbols** used to be able to source its data from Yahoo or Google finance.
  * Quantmod的getSymbols过去可以从雅虎(Yahoo)或谷歌财经(Google finance)获取数据。
  * Google stoppped their service some years ago now, and, unfortunately, **now Yahoo finance daily data is unreliable.**
  * **谷歌几年前就停止了这项服务，不幸的是，现在雅虎财经的每日数据是不可靠的**。
  * This does not really affect the usefulness of the relatedCOMP226 materials for educational purposes, but:
  * 这并不真正影响相关的comp226材料的实用性为教育目的，但是:
* Do not rely on Yahoo finance data for investment or trading decisions in real life.

![image-20230524144205040](D:\笔记\笔记图片\image-20230524144205040.png)

![image-20230524144213002](D:\笔记\笔记图片\image-20230524144213002.png)

![image-20230524144227943](D:\笔记\笔记图片\image-20230524144227943.png)

### 1.19 The xts package

#### 1.19.1 Times and dates in R

* There are many time and date classes in R, e.g.
* 在R中有许多时间和日期类，例如
  * POSIXct, POSIXlt, Date, chron, timeData, yearmon, yearqtr
* We will use mainly
  * **<font color=red>Date (date)</font>**
  * `Date`是一种表示日期的数据类型，它仅存储年、月和日的信息，不包括具体的时间。`Date`对象在R中以整数格式存储，可以通过格式化函数进行转换和显示。
  * **<font color=red>POSIXct (date-time)</font>**
  * `POSIXct`是一种表示日期和时间的数据类型，它存储日期和时间的具体时间戳，包括年、月、日、时、分、秒以及可能的时区信息。它基于UNIX时间戳，以从1970年1月1日起的秒数表示时间。`POSIXct`对象在R中以数字格式存储，但可以通过格式化函数进行转换和显示。

![image-20230524144834310](D:\笔记\笔记图片\image-20230524144834310.png)

![image-20230524144847054](D:\笔记\笔记图片\image-20230524144847054.png)

![image-20230524145046780](D:\笔记\笔记图片\image-20230524145046780.png)

* <font size=5>What is zoo?</font>
* class of indexed totally ordered observations
* 一类有索引的全有序观测值
* particularly aimed at irregular time series
* 特别针对不规则时间序列
* must contain data of one type (numeric/logical/character)
* 必须包含一种类型的数据(数字/逻辑/字符)
* zoo's key design goals are
* Zoo的主要设计目标是
  * independence from particular index/date/time class;
  * 独立于特定的索引/日期/时间类;
  * consistency with ts and base R by providing methods to extend standard generics (e.g. plot)
  * 通过提供扩展标准泛型(例如plot)的方法，与ts和base R保持一致。

* <font size=5>What is xts?</font>

* time-based extension of zoo which is popular and robust
* 基于时间的zoo扩展是流行的和鲁棒性的
* Requires indexing bases on recognised time-based class, e.g. POSIXct, Date, chron, timeData, yearmon, yearqtr
* 需要基于公认的基于时间的类的索引，例如POSIXct, Date, chron, timeData, yearmon, yearqtr
* time-based subsetting
* 基于时间的构造子集
* hidden attributes (accessed with xtsAttributes())
* 隐藏属性(通过xtsAttributes()访问)
* smart conversion tools
* 智能转换工具
* time-based tools like fast aggregation
* 基于时间的工具，比如快速聚合
* ![image-20230524154831736](D:\笔记\笔记图片\image-20230524154831736.png)
* 例子1：这里可以发现通过xts函数将prices和dates联系在了一起

![image-20230524154703231](D:\笔记\笔记图片\image-20230524154703231.png)

* 

![image-20230524155101221](D:\笔记\笔记图片\image-20230524155101221.png)

* 

* ![image-20230524160119124](D:\笔记\笔记图片\image-20230524160119124.png)

![image-20230524160141928](D:\笔记\笔记图片\image-20230524160141928.png)

* ![image-20230524160342352](D:\笔记\笔记图片\image-20230524160342352.png)
* ![image-20230524160358590](D:\笔记\笔记图片\image-20230524160358590.png)

* ![image-20230524160413089](D:\笔记\笔记图片\image-20230524160413089.png)

* ![image-20230524160427617](D:\笔记\笔记图片\image-20230524160427617.png)





## 2.Finacial Markets and Automated Trading

### 2.1 Finacial Markets （2.1）

* A **<font size=5 color=red>security</font>** is a tradable financial asset; **financial markets** are where securities are traded. A simple breakdown of markets by type of **security** is:
* **证券**是一种可交易的金融资产;金融市场是证券交易的场所。按证券类型划分市场的简单分类如下:

* • Capital markets (equities and fixed income) 
* 资本市场(股票和固定收益)
* • Foreign exchange markets
* 海外交易市场
*  • Money markets 
* 货币市场
* • Derivative markets (e.g. futures and options)
* 衍生品市场(例如期货和期权)



* Broadly speaking:
* For **equities** and **futures** trading, **exchanges** have been prominent (our focus); whereas for many other markets **over the counter (OTC)** trading has predominated, but this is changing
* 对于**股票**和**期货**交易，**交易所**一直是突出的(我们的重点);而在许多其他市场，**场外交易(OTC)**占主导地位，但这种情况正在改变

### 2.2 Buy side versus sell side

* **<font color=red>Buy Side</font>:** the side of the market that buys large amounts of securities for money or fund management (examples include asset managers, private equity funds, mutual funds, life insurance companies, unit trusts, hedge funds, and pension funds)
* **买方**:市场上为货币或基金管理购买大量证券的一方(例如资产管理公司、私募股权基金、共同基金、人寿保险公司、单位信托基金、对冲基金和养老基金)
* **<font color=red>Sell Side</font>**: the other side of the financial market, including prime brokers and broker-dealers (often investment banks), which deals with the creation, promotion, and selling of traded securities to the buy side
* **卖方**:金融市场的另一方，包括主要经纪人和经纪交易商(通常是投资银行)，负责创建、推广和向买方出售交易证券
* ![image-20230214102808345](D:\笔记\笔记图片\image-20230214102808345.png)

### 2.3 Active versus passive investment 主动投资和被动投资

*  **Passive investments track the market** (e.g., an index fund that tracks the S&P500)
* **被动投资**跟踪市场(例如，跟踪标准普尔500指数的指数基金)
* **Active strategies** make trading decisions to **try and beat passive investment benchmarks**
* **主动策略**做出交易决策，试图击败被动投资基准

![image-20230214103051874](D:\笔记\笔记图片\image-20230214103051874.png)

### 2.4 Automated Trading 自动化交易

* Automated/algorithmic trading: trading decisions are made by computer programs (as opposed to humans)

* 自动/算法交易:交易决策是由计算机程序(而不是人类)做出的。

* We will **focus on equities and futures markets** because of the prevelance of automated trading in those markets
  Many innovations in automated trading started in equities and futures markets, though automated trading is becoming ever more present in all markets

* 我们将重点关注股票和期货市场，因为这些市场中自动化交易的盛行

  自动交易的许多创新始于股票和期货市场，尽管自动交易在所有市场都越来越普遍



* <font size=5>什么是股票Equities？</font>
  * 股票是一种代表对公司所有权的金融工具。当你购买一家公司的股票时，你成为了该公司的股东之一，也就意味着你分享了公司的利润和风险。
  * 购买股票的主要目的是通过股票价格上涨和股息收入获得投资回报。当股票价格上涨时，你可以通过出售股票获得利润。此外，一些公司会向股东支付股息，作为对股东投资的回报。
* <font size=5>什么是期货Futures？</font>
  * 期货是一种金融衍生品，代表着双方就特定资产（如商品、货币、股票指数等）在未来的某个时间点以约定的价格进行交割的合约。
  * 在期货合约中，买方同意在合约到期时购买特定资产，而卖方同意在合约到期时出售特定资产。合约中约定了交割的标的物、数量、交割日期和价格等细节。这种交易方式允许投资者根据对市场未来走势的预测进行投机或对冲风险。
  * 期货市场的参与者包括投机者（如交易商、基金经理和个人投资者）和实物交易者（如农民、生产商和进口商）。投机者试图通过市场价格的波动来获取利润，而实物交易者则通过期货市场锁定价格，规避价格风险。
  * <font color=red>这里插一嘴，期货就相当于将未来的东西拿到现在卖，买方认为该物品会在未来升值，卖方通过此举规避价格风险。</font>

![image-20230214103202994](D:\笔记\笔记图片\image-20230214103202994.png)

## 3. Equity Markets 股票市场

* **Shares** allow firms to finance themselves via public ownership
* 股份允许公司通过公共所有制为自己融资
*  A share represents a portion of firm's inherent value or equity
* 股票代表公司固有价值或权益的一部分 
* The number of shares at a given time is known. But 
* 给定时间内的股份数量是已知的。但
  * Firms may issue or buy back shares, or 
  * 公司可以发行或回购股票，或者
  * make periodic dividend payments to shareholders 
  * 定期向股东支付股息
* **These corporate actions are important when valuing equities and evaluating trading strategies** 
* **在评估股票价值和评估交易策略时，这些公司行为非常重要**
* **• These actions are represented via <font color=red size=5>adjusted prices</font> for equities**
* **这些行为通过调整后的股票价格表现出来**

![image-20230214104036324](D:\笔记\笔记图片\image-20230214104036324.png)

* 2-for-1 stock split 2换1股票分割

![image-20230214104248298](D:\笔记\笔记图片\image-20230214104248298.png)

![image-20230214104317989](D:\笔记\笔记图片\image-20230214104317989.png)

### 3.1 Adjustment formulas 调整公式

* **<font size=5>Cash dividends: dividend value deducted from close price</font>**
* **现金股利:从收盘价中扣除的股息价值**
* <font color=blue>**Cash dividends**指的是公司向股东以现金形式支付的利润分配。当一家公司盈利并决定向股东分配部分利润时，它可以选择以现金形式向股东支付股息，这被称为现金股息或现金红利。</font>
* ![image-20230214104700157](D:\笔记\笔记图片\image-20230214104700157.png)
* <font size=5>**Stock dividends/stock splits**: close price divided by factor by which number of shares has increased</font>
* **股票分红/股票分割:收盘价除以股票数量增加的因素**
* <font color=blue>**股票红利（Stock dividends）**：**股票红利指的是公司向股东分配额外股票的方式来进行利润分配。当公司决定发放股票红利时，股东将获得额外的股票，而不是现金。**这意味着公司将现有股份分割成更多的股份，并将这些新的股份分配给股东。股票红利通常以一定比例的方式进行，例如1股股票红利对应每持有X股的股东获得1/X股的额外股票。通过发放股票红利，公司可以向股东分享利润并增加股东的持股数量，但每股股价会相应调整。</font>
* <font color=blue>**股票拆分（Stock splits）：股票拆分是指公司将现有的股票按照一定比例进行拆分，以增加股份的数量，同时降低每股的价格。**例如，公司可以进行2：1的拆分，意味着每持有1股股票的股东将获得2股股票。拆分后的每股股价将降低，但股东总体持有的股票数量不变。股票拆分旨在使股票价格更具吸引力，提高流动性，并吸引更多的投资者参与股票交易。</font>

![image-20230214104821455](D:\笔记\笔记图片\image-20230214104821455.png)

![image-20230524175738334](D:\笔记\笔记图片\image-20230524175738334.png)

![image-20230214104829604](D:\笔记\笔记图片\image-20230214104829604.png)

![image-20230524175752140](D:\笔记\笔记图片\image-20230524175752140.png)

![image-20230214104841511](D:\笔记\笔记图片\image-20230214104841511.png)

![image-20230524175909528](D:\笔记\笔记图片\image-20230524175909528.png)

![image-20230524175925159](D:\笔记\笔记图片\image-20230524175925159.png)

* 这三次上涨(5月、8月和11月)约为3.05美元，与股息支付相对应

![image-20230216101534125](D:\笔记\笔记图片\image-20230216101534125.png)

* Sometimes we will not pay proper care and attention to adjustments (we do not have money on the line).
* 有时我们不会对调整给予适当的关心和关注（我们没有钱）
* However, you need to be aware of how important corporate actions are when using historial data for real trading in equities and corporate bond markets.
* 然而，在使用历史数据进行股票和公司债券市场的真实交易时，你需要意识到公司行为是多么重要。
* This is an example of a general point: it is crucial to understand the correct interpretation of financial data. Data cleaning, pre-processing is an important part of developing trading strategies.
* 这是一个普遍观点的例子：了解金融数据的正确解释是至关重要的。数据清洗、预处理是制定交易策略的重要部分。

![image-20230524180649013](D:\笔记\笔记图片\image-20230524180649013.png)

* Equities markets **have extremely high volumes of automated trading** - it can account for over 70% of trading volume on equities exchanges on some days.
* 股票市场的自动交易量非常高——在某些日子里，它可以占股票交易所交易量的70%以上。
* Moreover, automated trading is supported across **the different types of execution venue** for equities markets, namely, both limit order books and dark pools
* 此外，股票市场不同类型的执行场所(即限价单和暗池)都支持自动交易









## 4. Futures Markets, ETFs, and Trading Venues（2.3）



### 4.1 Futures 期货

*  A **forward** is an agreement to buy or sell a fixed quantity of a given asset at a certain price at a specific date in the future 
* **期货**是指在未来某一特定日期以特定价格买进或卖出固定数量的特定资产的一种协议
* A **futures contract** is a forward with standardized terms
* **期货合约**是一种具有标准化条款的远期合约

![image-20230216102009419](D:\笔记\笔记图片\image-20230216102009419.png)

* **Futures** exist for <font color=red>**a wide array of underlying assets** </font>
* 期货是为广泛的基础资产而存在的
* Futures markets are 
  * **exchange-based order-driven** markets; and 
  * **基于交易所的订单驱动**市场;而且
  * **automated trading** is prevalent
  * **自动交易**很普遍

![image-20230216102445920](D:\笔记\笔记图片\image-20230216102445920.png)

* We will discuss them again, in the context of inter-calendar spread trading strategies (near the end of the module)
* 我们将在跨日历点差交易策略的背景下再次讨论它们(接近模块的末尾)
* On the Chicago Mercantile Exchange (CME), the world's largest commodities and futures exchange, high-frequency algorithmic trading accounts for over 50% of trading volume
* 在全球最大的商品和期货交易所芝加哥商品交易所(CME)，高频算法交易占交易量的50%以上





### 4.2 Futures Contracts

* **<font size=5 color=red>Futures contracts have a fixed expiry </font>**
* **<font size=5>期货合约有固定的到期日</font>**
* Multiple futures contracts with different expiries can be traded at any one time 
* 在期货市场上，可以同时交易多个具有不同到期日的期货合约。
* <font color=blue>这里举个例子：</font>
* ![image-20230524182545297](D:\笔记\笔记图片\image-20230524182545297.png)
* This provides trading opportunities such as **spread trading**: trading one contract against another for the same underlying 
* 这提供了交易机会，如**价差交易**:为同一标的买卖一份合约与另一份合约

![image-20230216103935888](D:\笔记\笔记图片\image-20230216103935888.png)

* It also means there is no single data set: 
* 这也意味着没有单一的数据集:
* Often, a futures "**continuous contract**" data set is formed by "glueing together" individual contracts 
* 通常情况下，期货市场中的"连续合约"数据集是通过将各个单独的合约连接在一起形成的。
* One of the most common approaches is to **back-adjust** by adding the price gaps on to earlier prices
* 最常见的方法之一是通过在早期价格上增加价格差距来进行**反向调整**



### 4.3 Exchange-TradedFunds （ETFs）交易所贸易基金

* **Tradable share** in an investment fund 
* 投资基金的**可流通股**
* Since they represent baskets of assets they are an effective way to gain exposure to whole sectors or markets (much like index futures) 
* 因为它们代表了篮子资产,它们是获得整个行业或市场的有效途径(就像指数期货一样)
* There are index, commodity, bond and currency ETFs
* 有指数、商品、债券和货币etf
* <font color=blue>举个例子：现在有一个医疗基金，该基金由若干医疗股票组成，每个股票就相当于一个基金的指数表，另外台湾将其翻译成指数股票型基金</font>

![image-20230216105031508](D:\笔记\笔记图片\image-20230216105031508.png)

![image-20230524183420991](D:\笔记\笔记图片\image-20230524183420991.png)

* **<font color=blue>我认为关键在于对ETFs是对整个行业进行投资</font>**

### 4.4 Trading mechanisms 贸易机构

* **Dealers** (buys/sells securities on their own account)
* **交易商**(以自己的账户买卖证券)
* **Brokers** (buys/sells securities solely for clients) 
* **经纪人**(仅为客户购买/销售证券)
* **Broker**-Dealers (often investment banks) do both roles 
* **经纪自营商**(通常是投资银行)都扮演两个角色
* **Limit Order Books** (typically run by public exchanges) 
* **限制订单簿**(通常由公共交易所运营)
* **Dark Pools** (run e.g. by broker-dealers or public exchanges)
* **暗池**(如经纪商或公共交易所)

限制订单书籍和黑暗池允许自动交易;我们将详细讨论这些交易机制

### 4.5 Exchanges and alternative venues 交易所和替代场所

* **Traditional venue is the exchange**, e.g. LSE or NYSE 
* 传统的地点是交易所,如LSE或纽约证交所
* **Alternative venues are now allowed. Different names:** 
* 现在允许在其他场地比赛。不同的名称:
  * **Europe: Multi-lateral Trading Facility (MTF)** 
  * **欧洲:多横向交易设施(MTF)**
  * **US: Alternative Trading System (ATS)**
  * **美国∶另类交易系统(ATS)**

These typically provide limit order books and often also dark pools

![image-20230216160750273](D:\笔记\笔记图片\image-20230216160750273.png)

* Automated trading is prevalent in equities and futures markets; you should have these markets in mind as we continue to discuss market microstructure 
* 自动交易在股票和期货市场非常普遍;在我们继续讨论市场微观结构时，您应该记住这些市场
* Equities markets have led the way in terms of the adoption of trading innovations such as dark pools
* 在采用暗池等交易创新方面，股市走在了前列

## 5. Limit Order Books 限制订单列队（2.4）

https://zhuanlan.zhihu.com/p/34393718 -- Limit Order Books

* **限制订单(限价单)**：对于买入的订单，成交价格必须低于或者等于限价单价格，而对于卖出的订单，成交价格必须高于或者等于限价单价格。
* **Limit Order Books：**
* ![image-20230226153806870](D:\笔记\笔记图片\image-20230226153806870.png)

### 5.1 Limit Order Book Markets

* In academic work, often called **<font color=red>Continuous Double Auctions</font>** 
* 在学术工作中，常被称为**连续双拍卖CDA**

![image-20230216161915367](D:\笔记\笔记图片\image-20230216161915367.png)

* <font color=blue>以拍卖场举例，CDA就是多个卖家对多个买家，卖家的最低价与买家的最高价成交</font>

*  Mechanism to **match buyers and sellers** 
* 与买方和卖方**相匹配的机制**
* Consists of two types of order
  * **<font size=5>Limit orders</font>** 
  * **限制订单**
  * **<font size=5>Market orders</font>**
  * **市场订单**

* Limit orders are matched and/or stored 
* 限价单被匹配和/或存储
* ![image-20230216164342158](D:\笔记\笔记图片\image-20230216164342158.png)
* <font color=blue>我觉得这个的关键在于规定了买者愿意的最高价和卖者愿意的最低价</font>
* Market orders are matched against limit orders if possible 
* 如果可能的话,市场订单与限制订单相匹配
* **Unmatched limit orders** are stored in the **order book** 
* **未匹配的限价订单**存储在**订单簿**中
* <font color=red>**Buy orders** or **bids** are stored in **the bid book**</font>
* 购买订单或投标存储在投标书中 **(买家)**
*  <font color=red>**Sell orders** or **asks/offers** are stored in **the ask book**</font>
* 销售订单或询价/报价存储在询价簿中 **（卖家）**

![image-20230216165004579](D:\笔记\笔记图片\image-20230216165004579.png)

* 下面的表格是bids book， 上面的是ask book



![image-20230226153924928](D:\笔记\笔记图片\image-20230226153924928.png)



### 5.2 Tick sizes and bid-ask spreads

* **Tick size**: smallest increment in price that an equity, future, or other exchange-traded instrument can move by
* **指数大小**:公平、未来或其他交易所交易工具的最小增量
* <font color=red>利率变化的最小幅度，一般最小为1bp</font>
* Tick  sizes  can  be  fixed  (e.g.  $0.01,  which  is  common  for  US equities, or a fixed number of points like 0.25 for an equities futures index), or may vary according to the current price
* **Tick size**可以固定(例如,0.01美元,这对美国股票来说是常见的,或者是股票期货指数的0.25点的固定数量),或者可能根据目前的价格而有所不同
* For  **heavily-traded**  instruments  **the  bid-ask  spread**  will often be equal to the tick size ("the spread is one tick")
* 对于数目很大交易的工具，买卖价差通常等于刻度大小(“价差为一个刻度”)。

![image-20230226162239241](D:\笔记\笔记图片\image-20230226162239241.png)

* Similarly, **it is often argued that smaller bid-ask spreads indicate  more  efficient**  markets  because  a  wide  spread indicates uncertainty about the "real price"
* 同样,人们经常认为,规模较小的购买商品显示更有效的市场,因为广泛的传播表明了“真实价格”的不确定性。



### 5.3 Buying versus selling

* **Short  selling (also known as shorting or going short)** is the practice of selling securities or other financial instruments that are not currently owned, and subsequently repurchasing them ("covering")
* **做空(空头交易)**是出售目前未拥有的证券或其他金融工具的做法,随后重新购买它们(“覆盖”)
* 做空是先借入标的资产，然后卖出获得现金，过一段时间之后，再支出现金买入标的资产归还。
* <font color=blue>一个小的例子就是，我先将资产按照市场价卖出，然后在股票期货下跌之后再买入，以赚取中间的差价，**换句话说，投资者借入低价的资产卖出，再以更低的价格回购归还，从中获得利润**。</font>



* In  the  event  of  an  interim  price  decline,  the  short  seller  will profit,  since  the  cost  of  (re)purchase  will  be  less  than  the proceeds which were received upon the initial (short) sale
* 在中间价格下跌的情况下，卖空者将获利，因为(重新)购买的成本将低于最初(卖空)出售时收到的收益



* **<font color=red>Shorting is a prevalent practice in equities markets</font>**
* 做空是股票市场的普遍做法



* Note:  in  futures  markets  one  is  agreeing  to  delivery  in  the future and it is not necessary to borrow the underlying at the time the derivative contract is sold
* 注:在期货市场上,一个人同意在未来交货,在销售合同出售时没有必要借款





### 5.4 Limit orders versus market orders

* **Limit orders** guarantee price but not execution
* **限价单**保证价格，但不保证执行
* <font color=blue>它只限制买入或卖出的价格，但是能否有没有人买或者卖，则不归它管</font>
* **Market orders** guarantee execution (almost always) but not price
* **市场单**保证执行(几乎总是)，但不能保证价格
* For market orders, **slippage is an important consideration**
* 对于市场订单，**滑移是一个重要的考虑因素**



### 5.5 Market Data

* **Trading models** are developed using historical market data. There are several granularities of market data:
* **交易模型**是利用历史市场数据开发的。市场数据有几个粒度:
  * **Time-based Bars**, e.g., daily, 1-minute bars
  * **基于时间的条形图**，例如，每天的，1分钟的条形图
  * Tick data (tick stands for the change in prices due to a trade)
  * Tick data(指因贸易而价格的变化)
    * ![image-20230226165858225](D:\笔记\笔记图片\image-20230226165858225.png)

![image-20230226165912770](D:\笔记\笔记图片\image-20230226165912770.png)

![image-20230226165919133](D:\笔记\笔记图片\image-20230226165919133.png)

![image-20230226165932209](D:\笔记\笔记图片\image-20230226165932209.png)

![image-20230226165939691](D:\笔记\笔记图片\image-20230226165939691.png)

![image-20230226165946924](D:\笔记\笔记图片\image-20230226165946924.png)

![image-20230226165955023](D:\笔记\笔记图片\image-20230226165955023.png)

## 6. (2.5) Slippage 滑点

### 6.1 Limit orders versus market orders

![image-20230226171553450](D:\笔记\笔记图片\image-20230226171553450.png)

### 6.2 Slippage

* Defination:
* **The  slippage  of  a  trade  is  the  difference  between  the actual (average) execution price and expected execution price (also known as the "trigger" price)**
* **交易的下滑是实际(平均)执行价格和预期执行价格的区别(也称为“触发”价格)**
* **<font color=blue>所谓的滑点(Slippage)，是指在进行交易时，客户下达的指定交易点位与实际交易点位存在较大差别的一种现象。也就是说，当实际成交价格与起始报价不一样时，便会产生滑点。</font>**
  * With  **market  orders**,  slippage  is  a  crucial  consideration, and could be arbitrarily bad
  * 对于市场订单，滑移是一个关键的考虑因素，并且可能是任意糟糕的
  * With  **limit  orders**  your  worst-case  price  is  guaranteed,  but you may not execute at all
  * 限价单保证了你的最坏价格，但你可能根本不执行

![image-20230226172416236](D:\笔记\笔记图片\image-20230226172416236.png)

### 6.3 Expected execution price 预期执行价格

* How  accurately  one  can  compute  the  expected  execution price depends on what data is available
* 计算预期执行价格的准确性取决于可用的数据
* For example, if one only has daily data and the open price is the  trigger  price  that  causes  you  to  place  a  market  order  it will  be  very  hard  to  have  an  accurate  expectation  of  what price you will actually get executed at
* 例如，如果一个人只有每日数据，而公开价格是触发价格，导致你下市场订单，将很难有一个准确的预期价格，你将实际执行
*  For  a  market  order  **the  expected  execution  price  can  be calculated  if  one  knows  the  current  state  of  the  order book（就是bid order和ask order）** (e.g. see the earlier example of a buy market order)
* 对于市场订单，**如果知道订单簿的当前状态，则可以计算预期执行价格(例如，参见前面的买入市场订单示例)。**
* For  example,  for  a  small  enough  buy  order,  it  would  be the  best  ask;  for  a  larger  order  it  may  be  an  average  over multiple price levels
* 例如，对于一个足够小的购买订单，这将是最好的要求;对于较大的订单，它可能是多个价格水平的平均值

### 6.4 When does one incur slippage

One incurs slippage because: 导致滑倒的原因是:

* **<font color=red>the  state  of  the  order  book  changes</font>**  between  when  the order is placed and when it reaches the market; and/or
* 当订单被放置并到达市场时,订单的状态就会发生变化;/或

* **<font color=red>one  didn't  have  accurate  enough  data</font>**  to  compute  an accurate execution price
* 人们没有足够准确的数据来计算准确的执行价格

![image-20230226173027810](D:\笔记\笔记图片\image-20230226173027810.png)



* 请注意在制定交易策略时，滑移是一个非常重要的考虑因素:
  * 设计出出现的策略相对容易非常有利可图的历史数据，不包括滑动。他们通常会有一点利润往返贸易(完成买卖)。
  * 然而，这些策略可能会变得在实际交易中由于滑动而无利可图:他们每笔交易的预期利润太小。



## 7.（2.6）Market makers 做市商

### 7.1 Market makers

* **<font size=5>Ongoing liquidity providers that post bids and asks</font>**
* **发布竞价和询价的持续流动性提供者**
*  ![image-20230525173039729](D:\笔记\笔记图片\image-20230525173039729.png)
* **<font color=red size=5>市场做市商（Market makers）是金融市场中的一类参与者，他们在市场上同时提供买入和卖出的报价，并愿意以特定的价格和数量进行交易。他们的目标是促进市场的流动性和有效性。</font>**
* **Try to capture bid-ask spread**: try to repeatedly buy at the bid and sell at the (higher) ask
* 试着抓住买卖价差:试着反复在买入价买入，在(更高的)卖出价卖出
* Today  market  makers  are  normally  high-frequency  trading (HFT) algorithms (often referred to simply as "**high-frequency traders**")
* 如今，做市商通常进行高频交易(HFT)算法(通常简称为**“高频交易”**)
* Existence  of  market  makers  normally  ensures  a  reasonably tight spread, however, there is evidence that HFT high-frequency  traders  abandon  the  market  during  times  of market stress
* 做市商的存在通常确保了合理的息差，然而，有证据表明，高频交易商在市场压力时期会放弃市场
* We will in the next set of slides of how HFT can be predatory, and is thus controversial
* 我们将在下一组幻灯片中讲到高频交易是如何具有掠夺性的，因此是有争议的!

做市商的通俗解释就是股价的中间商，这个中间商可以通过对上市公司的评估，对公众投资者报出股票的买价和卖价，然后中间商就通过买价卖价间的差额来赚取利润。做市商要求具备一定的实力和信誉，且需要是证券经营法人。国际上一般由较大的金商或银行来担任做市商。

**<font color=blue>股市的中间商</font>**

![image-20230226185217426](D:\笔记\笔记图片\image-20230226185217426.png)

* 在这个图中，我们就可以知道，901号即出现在了卖方市场也出现在了买方市场，满足了同时可以提供买入和卖出的报价。



### 7.2 Toxic Order Flow 有毒订单流程

* An  important  problem  faced  by  a  market  maker  (MM)  is avoiding **toxic order flow**
* 做市商面临的一个重要问题是避免**有毒的订单流**
* **Toxic  order  flow  comprises  market  orders  from  informed traders  that  precede  price  moves  in  the  favour  of  the informed trader**
* **有毒订单流包括来自知情交易者的市场订单，这些订单先于有利于知情交易者的价格变动**
* <font color=blue>来自对于市场知情的交易者的订单被称为有毒的，因为做市商会发现自己在成交后会立刻处于亏损的状态，这会导致做市商将风险转移给其他人。有点像击鼓传花</font>
* After  transacting  with  toxic  order  flow,  an  MM  will  build  up (positive or negative) **inventory with a corresponding loss**
* 在处理有毒订单流后，一个MM将建立起来(正或负)**有相应损失的存货**
* additionally with a large inventory the MM faces **the inventory risk** of a further unfavourable price move
* 此外，由于大量库存，MM面临进一步不利价格变动的**库存风险**
* thus, MMs **prefer to hold no inventory (positive or negative)**
* 因此，mm倾向于不持有库存(正面或负面)



### 7.3 Market makers and HFT

* Today market makers are **<font color=red size=5>typically extremely high-frequency algorithmic traders</font>**
* 如今，做市商通常都是**高频算法交易员**
* The  practice  of  High-Frequency  Trading  (HFT)  is  somewhat controversial because:
* 高频交易(HFT)的实践是有争议的，因为:
  * as we will see in the next set of slides that HFT traders can  exploit  their  speed,  potentially  at  the  expense  of other traders
  * 正如我们在下一组幻灯片中看到的那样，高频交易交易者可以利用他们的速度，可能会牺牲其他交易者的利益
  * there is some evidence that HFT traders leave the market  during  times  of  stress,  which  is  exactly  when liquidity provision is most needed
  * 有证据表明，高频交易交易员在市场压力大的时候离开市场，而这正是最需要流动性提供的时候
* **什么是高频交易？**

![image-20230226190649310](D:\笔记\笔记图片\image-20230226190649310.png)



## 8. (2.7) Front running, Dark Pools

![image-20230318131229858](D:\笔记\笔记图片\image-20230318131229858.png)

### 8.1 Front Running 前置交易

* **<font color=red>前置交易（Front Running）是指在知晓其他人即将进行交易的情况下，通过提前进行交易以获取利益的行为。</font>**

* Suppose a trader wants to buy a large amount of a stock (or other security)、
* 假设一个交易者想要购买大量的股票(或其他证券)
* If the market finds out this intention the price of the stock will be driven up
* 如果市场发现了这一意图，股票价格将被推高
* This happens via front-running: knowing that a large buy order is coming to the market, others buy first (either with limit or market orders) with the intention to sell when the price has risen
* 这是通过提前交易发生的:知道一个大的买入订单即将进入市场，其他人先买入(限价或市价订单)，并打算在价格上涨时卖出
* This example could equally apply to a large sell order
* 这个例子同样适用于一个大的销售订单
* <font color=blue>可以看看下面的例子</font>

![image-20230318133006002](D:\笔记\笔记图片\image-20230318133006002.png)

#### 8.1.1 Limit Orders can be front run 限价订单可以提前办理

* Large limit orders can be "front-run" by **penny jumping**
* 大额限价单可以通过**前置交易**来 **“抢先”**

![image-20230318133142938](D:\笔记\笔记图片\image-20230318133142938.png)

<font color=blue>限价订单更容易受到front run的影响</font>



### 8.2 Motivation for Dark Pools

* Again, suppose a trader wants to buy a large amount of a stock (or other security)
* 同样，假设一个交易者想要购买大量的股票(或其他证券)
* Executing in one go as **a market order will be costly**
* 一次性执行**市场指令的成本很高**
* We have also just seen how **placing a single large limit order can be problematic too**
* 我们也刚刚看到**下一个大的限价订单也会有问题**
* Consequently, large orders are split into smaller ones (**iceberging**), either market or limit orders; we will discuss execution algorithms that do this in the next set of slides
* 因此，大订单被分成小订单 (**冰山**)，要么市场或限制订单;我们将在下一组幻灯片中讨论执行算法
* First, we consider a different type of execution mechanism, **dark pools**, that arose specifically to address the problem faced by traders wanting to trade large amounts
* 首先，我们考虑一种不同类型的执行机制，即暗池，它专门用于解决希望进行大量交易的交易者面临的问题



#### 8.2.1 Light pools of liquidity 清池的流动性

* **A limit order book is typically visible to market participants** 
* **限价单通常对市场参与者可见**
* Due to this transparency, limit order book markets are called light pools of liquidity (visible = light) 
* 由于这种透明度，限价单市场被称为流动性的轻池(可见=轻)。
* We now look at dark pools of liquidity

![image-20230318134938810](D:\笔记\笔记图片\image-20230318134938810.png)

### 8.3 Dark pools

* Used to reduce market impact when trading large orders 
* 用于交易大订单时减少市场影响
* **The intentions of a trader are hidden from other market participants until a trade happens** 
* **在交易发生之前，交易者的意图对其他市场参与者是隐藏的**
* Every individual trade happens at a single price per unit (and this is how market impact is limited)
* 每笔交易都以单一的单价进行(这就是市场影响有限的原因)
* <font color=red>关键在于隐藏！！！</font>

#### 8.3.1 Dark pools: the basic mechanism 基本机制

* **The intention to buy or sell at current market price is indicated to the platform**
* **以当前市场价格购买或出售的意图被指示给平台**
* If a match (i.e. trader "on the other side") is found the platform instigates a trade at the current market price (normally the mid-price of the relevant security in a light pool of liquidity)
* 如果发现匹配(即“另一方”的交易员)，平台就会以当前市场价格(通常是流动性较低的相关证券的中间价)进行交易。
* 黑池（Dark Pool）是一种非公开的交易平台，用于进行匿名交易。它的基本交易机制是通过匹配买家和卖家的交易订单，以实现交易的成交，同时保护交易双方的隐私。

  在黑池中，交易订单不会公开显示给其他市场参与者，而是在平台内部进行匹配。买家和卖家可以提交匿名的交易订单，其中包含他们希望购买或出售的资产、数量和价格等信息。黑池利用其匹配算法自动匹配符合条件的买家和卖家订单。

  一旦买家和卖家的订单匹配成功，交易就会在黑池内部进行成交，而不会公开显示给其他市场参与者。这种匿名交易机制有助于减少交易的市场冲击，降低对价格的影响，并保护交易双方的交易策略和敏感信息。

![image-20230318170712764](D:\笔记\笔记图片\image-20230318170712764.png)

![image-20230318170739506](D:\笔记\笔记图片\image-20230318170739506.png)

* Example 1: there was already a seller(s) waiting in the dark pool that wanted to sell y>x units. In this case, trader A buys x units. Trader A learns that there was a seller(s) willing to sell at least x units (but does not learn exactly how much was a available). After this match there will still by y-x units available for sale in the dark pool.
* 例1:已经有一个卖家在暗池中等待，想要出售y>x个单位。在这种情况下，交易者A买入x单位。交易者A了解到有一个卖家愿意出售至少x个单位(但不知道确切的可用数量)。比赛结束后，暗池中仍有y-x个单位可供出售。
* Example 2: there was already a seller(s) waiting in the dark pool that wanted to sell z<x units. In this case, trader A buys z units. Trader A learns that there was a seller(s) willing to sell z units but no more (i.e. trader A learns the exact liquidity that was available). After this match the buyer will remain in the dark pool with x-z units that he is still willing to buy.
* 例2:已经有一个卖家在暗池中等待，希望出售z<x个单位。在这种情况下，交易者A购买z个单位。交易者A了解到有一个卖家愿意出售z个单位，但不能再多了(即交易者A了解到确切的可用流动性)。在这场匹配之后，买家将留在暗池中，他仍然愿意购买x-z个单位。

#### 8.3.2 Polling dark pools 决定是否使用暗池

* When algorithmic traders decide whether to use light or dark pools of liquidity they often need to "poll" a dark pool to ascertain how much liquidity is available (i.e. place trades to see whether or not they are executed).
* 当算法交易员决定是使用浅色流动性池还是暗池时，他们通常需要“调查”暗池以确定有多少流动性可用(**即进行交易以查看是否执行**)。
* <font color=blue>因为暗池的流动性不公开</font>

![image-20230318172319566](D:\笔记\笔记图片\image-20230318172319566.png)

#### 8.3.3 Ownership of dark pools 黑池的所有权

* Dark pools are owned by different types of institution: 
* 暗池由不同类型的机构拥有:
  * **Alternative Trading Systems/Multilaterial trading facilities** 
  * **另类交易系统/多边交易设施**
  * **Broker-dealers** 
  * **债券经纪人**
  * **Exchanges**
  * **交换所**

#### 8.3.4 Prevalence of algorithmic trading 算法交易盛行

* There are lots of dark pools of liquidity (typically for equities) 
* 有很多流动性的暗池(通常是股票)
* **Liquidity in these pools is not directly visible** 
* **这些资金池的流动性并不直接可见**
* They are **typically only accessible electronically** 
* 它们通常**只能通过电子方式访问**
* **Algorithmic traders** utilize them heavily
* **算法交易者**大量利用它们

## 9. (2.8) Execution algorithms 执行算法

* 执行算法（Execution Algorithm）是在金融交易中用于执行交易订单的计算机程序或规则集合。它们被设计用于根据指定的交易策略和要求，以最佳方式执行交易订单，并尽量达到交易目标。

![image-20230318173052977](D:\笔记\笔记图片\image-20230318173052977.png)

* Pension funds or other buy-side firms often want trade a "large" volume and will often task this to an agent
* 养老基金或其他买方公司通常希望进行交易“大”卷，并经常将此任务分配给代理
* What is a large volume? **Depends on the market and order book. Large volume cannot be transacted as a market order without a significant price impact.** Recall: Market orders incur slippage; limit orders may not get executed
* 什么是大体积?这取决于市场和订单。**大量的交易量不能作为市场订单进行交易，而不会对价格产生重大影响**。召回:市场订单导致下滑;限价指令可能无法执行
* The agent typicallys uses an execution algorithm to automatically split the large volume and execute it incrementally (called **iceberging**) in an attempt to hide the existence of the large order and minimize price impact
* 代理通常使用一种执行算法自动分割大量订单并增量执行(称为冰山)，以试图隐藏大订单的存在并将价格影响最小化
* <font color=blue>冰山算法：将一个较大的订单分解成无数小的订单</font>
* Goal of the execution algorithm - minimize execution cost in comparison to a given execution benchmark; we discuss 3 common benchmarks in these slides
* 执行算法的目标-与给定的执行基准相比，最小化执行成本;我们在这些幻灯片中讨论了3个常见的基准测试



### 9.1 Benchmarks 基准

* We study 3 standard benchmarks for **execution algorithm**s:
* 我们研究3个执行算法的标准基准:
  * **VWAP - Volume-Weighted Average Price**
  * **VWAP -成交量加权平均价格**
  * **TWAP - Time-Weighted Average Price**
  * **TWAP - 加权平均价格**
  * **Implementation Shortfall**
  * **执行缺口**

![image-20230318174342413](D:\笔记\笔记图片\image-20230318174342413.png)

* **<font color=red>t执行时间，p执行价格，v执行体积</font>**

#### 9.1.1 Volume-Weighted Average Price 成交量加权平均价格 VWAP

![image-20230318174821599](D:\笔记\笔记图片\image-20230318174821599.png)

* **<font color=red>Volume-Weighted Average Price（VWAP）是一种衡量股票交易价格的指标，<font size=5>通常被用于评估交易成本和市场参与度</font>.</font>**
* **<font color=blue>VWAP of the order is compared to the VWAP of the market</font>**
* <font color=blue>将订单的VWAP与市场的VWAP进行比较</font>
* Goal is to do at least as well as VWAP of market 
* 目标是至少做得和市场的VWAP一样好
* Concentrates on minimizing market impact by splitting the order into quantities based on prediction of volume distribution (usually just the historic volume profile)
* 专注于根据预测的成交量分布(通常只是历史成交量分布)将订单分成数量，从而最大限度地减少市场影响

![image-20230318175049259](D:\笔记\笔记图片\image-20230318175049259.png)

* <font color=red>VWAP 通常被用于计算大型交易的成本，因为大型交易通常需要分批完成，而以 VWAP 为基准可以最大限度地减少交易成本。VWAP 也是一种评估算法交易表现的指标，因为算法交易通常会试图通过以 VWAP 为基准进行交易，最小化其对市场的影响。</font>

#### 9.1.2  Time-Weighted Average Price 时间权重平均价格TWAP

![image-20230318175529191](D:\笔记\笔记图片\image-20230318175529191.png)

* <font color=red>Time-Weighted Average Price（TWAP）是一种计算股票交易价格的指标，**用于表示在一段时间内的平均价格。**</font>
* Goal is to do at least as well as TWAP of market 
* 目标是至少达到市场TWAP的水平
* Trade based on a uniform time schedule, i.e., divide order into individual units and trade equi-spaced in time
* 根据统一的时间安排进行交易，即将订单分成单个单位，并在时间上等距进行交易

![image-20230318180202841](D:\笔记\笔记图片\image-20230318180202841.png)

* <font color=red>TWAP 是投资者在交易时使用的一种算法，以在一段时间内平均分散地执行买入或卖出股票，从而降低对市场的影响，最大限度地减少交易成本。对于大型交易，使用 TWAP 算法可以有效地分散交易成本。</font>

#### 9.1.3 Implementation Shortfall

* **<font color=red>Implementation Shortfall is the difference between the price (midprice) of an asset at the time of a trading decision and the (average) execution price.</font>**
* **<font color=red>执行差额是资产在交易决策时的价格(中间价)与(平均)执行价格之间的差额。</font>**
* **Implementation shortfall指的是执行差距，也就是投资者在交易执行过程中<font color=red>实际成交价格</font>与<font color=red>执行决策价格</font>之间的差距，包括市场冲击成本和交易成本**。

![image-20230318181554289](D:\笔记\笔记图片\image-20230318181554289.png)



![image-20230318203933428](D:\笔记\笔记图片\image-20230318203933428.png)

![image-20230318204125744](D:\笔记\笔记图片\image-20230318204125744.png)

![image-20230318204043940](D:\笔记\笔记图片\image-20230318204043940.png)

* **<font color=blue>`diff`函数在R中用于计算向量或时间序列对象中相邻元素的差异。在这个例子中，`index(trades)`返回`trades`时间序列对象的时间索引向量，`diff(index(trades))`则计算了这个时间索引向量中相邻元素之间的差异。</font>**

![image-20230318204144105](D:\笔记\笔记图片\image-20230318204144105.png)

* **<font color=blue>`colnames(trades)`用于获取`trades`时间序列对象的列名（变量名），而`ncol(trades)`返回`trades`对象的列数。</font>**
* **<font color=blue>`colnames(trades)[ncol(trades)]`表示获取`trades`对象的最后一列的列名。然后，通过赋值运算符`<-`，将字符串"TimeDiff"赋值给这个列名。</font>**

![image-20230318204156340](D:\笔记\笔记图片\image-20230318204156340.png)



![image-20230318204220698](D:\笔记\笔记图片\image-20230318204220698.png)

* <font color=blue>记得之前的公式，直接使用就行，这个还不用算diff的时间差值</font>
* 

#### 9.1.4 TWAP versus VWAP

* The two will in general be quite different, since: 
  * VWAP will place 
    * **<font color=red>low weight on the prices during time periods with low volume and </font>**
    * **<font color=red>在低交易量的时间段内，价格权重较低</font>**
    * **<font color=red>high weight on time periods with high volume</font>**
    * **<font color=red>在高容量的时间段内具有高权重</font>**
  * **TWAP places equal weight on prices from all time periods**
  * **TWAP对所有时期的价格给予同等的权重**

![image-20230526145940214](D:\笔记\笔记图片\image-20230526145940214.png)

* The discrepency is evidence that the volume curve is not flat: normally there is more trading at the open and close
* 这种差异是成交量曲线并非平坦的证据:正常情况下，开盘和收盘时交易量较大

![image-20230318204706050](D:\笔记\笔记图片\image-20230318204706050.png)

* Model the volume distribution using historical data 
* 使用历史数据建立体积分布模型
* Slice trades according to predicted distribution
* 切片交易根据预测的分布



![image-20230318204830023](D:\笔记\笔记图片\image-20230318204830023.png)

* Split order into slices (e.g. 1 lots) 
* 将订单分成几片(如1批)
* Divide time equally to give the correct number of trading points for the size of each slice
* 平均分配时间，为每个切片的大小给出正确的交易点数量



* **Notice that a TWAP strategy is like a VWAP one with a uniform (flat) volume distribution**
* **注意，TWAP策略类似于VWAP策略，具有均匀(平坦)的体积分布**



![image-20230318205122074](D:\笔记\笔记图片\image-20230318205122074.png)

#### 9.1.5 Implementation shortfall strategy 实施不足策略

![image-20230318205154622](D:\笔记\笔记图片\image-20230318205154622.png)



* Need to decide if price is going to move favourably or not 
* Trade off: 
* 需要决定价格走势是否有利
  * **<font color=red>market impact</font>** (place order now) with 
  * 市场影响(现在下单)与
  * **<font color=red>volatility risk</font>** (wait and risk adverse market moves)
  * 波动风险(等待并承担不利市场波动的风险)



## 10.(3.1) Returns 收益

![image-20230318220136570](D:\笔记\笔记图片\image-20230318220136570.png)

* In contrast to the execution algorithms, profit-seeking strategies aim to generate a positive profit/return, rather than just execute a pre-defined large order an minimum cost 
* 与执行算法相比，**逐利策略旨在产生正的利润/回报**，而不仅仅是以最低成本执行预定义的大订单
* We study two types of returns: **simple and logarithmic returns**
* 我们研究了两种类型的收益:**简单收益和对数收益**

### 10.1 Measuring performance

* **<font color=red>Relative returns</font>** are building blocks of performance measurement 
* **相对回报**是衡量业绩的基石
* There are two types:
  *  **simple returns** 
  * **简单收益**
  * **log returns** 
  * **对数收益率**
* Straightforward to convert either one to the other
* 将其中一个转换为另一个很简单



### 10.2 Definition of returns 

![image-20230319103118429](D:\笔记\笔记图片\image-20230319103118429.png)



* **The <font color=red>simple return</font> for being long from t-1 to t is defined as:**
* **从t-1到t的简单长返回值定义为:**
* ![image-20230319103421133](D:\笔记\笔记图片\image-20230319103421133.png)
* **The <font color=red>log return</font> (also called the continuously compounded return) is defined as:**
* **对数收益(也称为连续复合收益)定义为:**
* ![image-20230319103404148](D:\笔记\笔记图片\image-20230319103404148.png)

### 10.3 Simple correspondence 两种回报的转换关系

![image-20230319103644796](D:\笔记\笔记图片\image-20230319103644796.png)

* Log returns and simple returns are **essentially the same thing** just stated on a **different scale**
* **对数收益和简单收益本质上是一样**的只是用不同的**尺度表示**
* For **mathematical convenience** we often use **log returns**
* 为了方便计算，我们通常使用log返回

![image-20230319103708851](D:\笔记\笔记图片\image-20230319103708851.png)

### 10.4 Simple versus log returns 简单与log收益

* As the table shows:
  * **For realistic simple returns (smaller in aboslute value than 10%) simple and log returns are very similar** 
  * **对于现实的简单回报(绝对值小于10%)简单和日志的收益非常相似**
  * **For larger simple returns they start to diverge** 
  * **对于更大的简单回报，它们开始出现分歧**
  * When a non-zero price goes down to zero 
  * 当非零价格下降到零
    * **-1 is the simple return (smallest possible)** 
    * **-1是简单返回(尽可能小)**
    * **-Infinity is the log return (smallest possible)**
    * **-无穷大是日志返回值(尽可能小)**
  * Both simple and log returns can be arbitrarily high, but log returns grow much more slowly than simple returns
  * 简单收益和log收益都可以任意高，但是log收益增长比简单收益慢得多

![image-20230319104147761](D:\笔记\笔记图片\image-20230319104147761.png)

### 10.5 Terminology for positions 头寸术语

* For a given asset we can take three possible positions:
* 对于给定的资产，我们可以采取三种可能的立场:

![image-20230319104325851](D:\笔记\笔记图片\image-20230319104325851.png)

* **Long：多头，已经买了 ** 持仓
* **Flat：没有买也没有卖** 平仓
* **Short：空头，已经卖了** 空仓

* Those can be thought of as **the direction of the position**
* 这些可以被认为是**头寸的方向**
* In addition to the direction, there is the size of the position, e.g., the number of shares for equities, or the number of contracts (a.k.a lots) for futures
* 除了方向之外，还有头寸的大小，例如，股票的股份数量，或期货合约的数量(又名手)

![image-20230319104432012](D:\笔记\笔记图片\image-20230319104432012.png)



### 10.6 Return of a short position 空头头寸

* When we go short, the buying time is after the selling time 
* 当我们做空时，买入时间是在卖出时间之后
* **Log return** 
* 对数收益率
* **<font size=5>of a short position = negative of</font>**
* **<font size=5>rt = log(Pt-1)-log(Pt)</font>**
* <font size=5>空头=负的</font>
* **Simple return**
* 简单收益率
* **The relationship of the simple return of a short position relative to that of the long position is slightly more complicated:**
* **空头头寸相对于多头头寸的简单收益之间的关系稍微复杂一些:**

![image-20230319104839065](D:\笔记\笔记图片\image-20230319104839065.png)

![image-20230526180625060](D:\笔记\笔记图片\image-20230526180625060.png)

* 该公式常用于计算空头头寸的单期收益率或持有期收益率。在该公式中，Rt表示特定时间点t的收益率，Rt + 1表示时间点t后一期的收益率。
* **<font color=red size=5>做空的简单收益是在价格下跌时产生正收益，而做多的简单收益是在价格上涨时产生正收益。这是由于做空操作是通过卖出股票或其他资产来获利，而做多操作是通过买入资产来获利。因此，对于相同的价格变动，做空和做多的简单收益的符号是相反的。</font>**



![image-20230319104855873](D:\笔记\笔记图片\image-20230319104855873.png)

### 10.7 Simple Difference

* **The simple price difference (i.e. profit or loss) is occasionally used**
* **简单的价差(即利润或亏损)有时也会用到**
* ![image-20230319105040295](D:\笔记\笔记图片\image-20230319105040295.png)
* But many applications require relative returns
* 但许多应用需要相对回报



### 10.8 Returns versus price differences 回报率和价差

* The benefit is **normalization**: 
* 好处是**正常化**:
  * measuring all variables in a comparable (dimensionless) way 
  * 用可比的(无量纲的)方法测量所有变量
  * this allows the evaluation of relationships between asset prices of different levels 
  * 这允许评估不同水平的资产价格之间的关系
  * relative returns is required for **relevant statistical analysis**
  * 相关统计分析需要**相对收益**
* **<font color=red>Returns（收益率）</font>**：Returns是指资产价格相对于初始价格的变动比例。它衡量的是投资或交易的收益率。通常用百分比或小数表示。**收益率可以是单期收益率，表示两个时间点之间的价格变动；也可以是持有期收益率，表示在一段时间内持有资产的收益率。**
* **<font color=red>Price differences（价格差异）</font>**：Price differences是指资产价格在两个时间点之间的实际差异或变动量。**它表示价格的绝对变动值。价格差异可以是正数或负数，取决于价格的上升或下降。**

![image-20230526161138254](D:\笔记\笔记图片\image-20230526161138254.png)

![image-20230319105319184](D:\笔记\笔记图片\image-20230319105319184.png)

![image-20230319105332598](D:\笔记\笔记图片\image-20230319105332598.png)

### 10.9 ROC function

* Compute returns with function ROC from TTR package 
* 计算从TTR包返回函数ROC
  * ROC has parameter type which can either: 
  * ROC有参数类型，可以是:
    * discrete for simple returns  
    * 离散的简单回报
    * continuous for log returns
    * 连续的log回报

![image-20230319105542006](D:\笔记\笔记图片\image-20230319105542006.png)

![image-20230319105601806](D:\笔记\笔记图片\image-20230319105601806.png)

* **<font color=blue>round的方法是保存三位小数</font>**

![image-20230319105613757](D:\笔记\笔记图片\image-20230319105613757.png)



## 11 (3.2) Equity curves 股本曲线

![image-20230526162846171](D:\笔记\笔记图片\image-20230526162846171.png)

* We consider **equity curves**: time series plots that show the performance of a **sequence of trades**
* 我们考虑**股本曲线**:显示**一系列交易表现的时间序列图**
* First we introduce position vectors
* 首先我们引入位置向量
* Then we create equity curves **<font color=red>by combining position vectors with prices/returns</font>**
* 然后我们通过**<font color=red>组合头寸向量和价格/收益来创建股票曲线</font>**

### 11.1 Position Vectors 头寸向量

![image-20230319105914065](D:\笔记\笔记图片\image-20230319105914065.png)

* By signals, we mean **time series of positions**; **trades** occur when the value of **the signal changes**
* 通过信号，我们指的是头寸的时间序列;当信号的价值发生变化时，交易就发生了

### 11.2 Aggregating returns 聚合回报

![image-20230319110130176](D:\笔记\笔记图片\image-20230319110130176.png)

* Given a sequence of **<font color=red>simple returns</font>**, they are aggregated by:
* 给定一个简单的返回序列，它们通过以下方式聚合:
  *  **adding 1 to each of them, multiplying them together, and then subtracting 1 from the product (example on next slide)** 
  * **分别加1，相乘，然后乘积减1(下一张幻灯片的例子)**
* Given a sequence of**<font color=red> log returns</font>**, they are aggregated by: 
* 给定一个日志返回序列，它们由
  * **adding them up** 
  * **把它们加起来**
* This produces the **<font color=red size=5>cumulative return</font>**. In R we use the functions cumsum and cumprod, where cum stands for cumulative or cumulate. 
* 这就产生了**累积回报**。在R中，我们使用**cumsum和cumprod函数，其中cum代表累积或累积。**
* We will use this throughout the rest of the module
* 我们将在本模块的其余部分中使用它

![image-20230526170517397](D:\笔记\笔记图片\image-20230526170517397.png)

* 一个是一个投资在一段时间内的总体回报
* 一个是一些列投资回报按照一定方式进行汇总的过程



![image-20230319110351491](D:\笔记\笔记图片\image-20230319110351491.png)

* **<font size=5>Exercise</font>**

* Work through a similar example for aggregating log returns to convince yourself that aggregation is simply summation.
* 通过**汇总日志**返回的类似示例，使自己确信汇总只是简单的求和。
* Note that the same reasoning applies to the simple difference (profit and loss) as well as log returns.
* 请注意，同样的推理适用于简单的差异(利润和损失)以及log回报。

![image-20230526171738010](D:\笔记\笔记图片\image-20230526171738010.png)

* The methods we have just described assume that each time we place a new trade **all capital is reinvested**.
* 我们刚才描述的方法假设每次我们进行新的交易时，**所有的资本都被重新投资。**
* In reality, this is at best only approximately true due to the fact one can generally only buy whole units (of shares or contracts) and additionally there are trading costs such as commissions. For simplicity, we ignore these issues.
* 在现实中，这充其量只是大致正确的，因为人们通常只能购买整个单位(股票或合同)，另外还有交易成本，如佣金。为简单起见，我们忽略这些问题。
* For simple profit and loss, as opposed to returns, it is easier to account for injecting or removing capital, or trading costs, when computing an equity curve. However, returns are more usual for reporting performance.
* 对于简单的损益，而不是回报，在计算权益曲线时，更容易解释注入或撤出资本或交易成本。然而，返回更常用于报告性能。

![image-20230526171830339](D:\笔记\笔记图片\image-20230526171830339.png)

### 11.3 Equity Curves 股本曲线

* **Equity Curves：Time series plot of profitability of a trading strategy either in terms of profit/loss or return (log or simple)**
* **股本曲线:交易策略盈利能力的时间序列图，以损益或回报(对数或简单)表示**。
* ![image-20230526173033987](D:\笔记\笔记图片\image-20230526173033987.png)
* 上节课的例子

![image-20230526172844067](D:\笔记\笔记图片\image-20230526172844067.png)

* Simple returns: to directly compute an equity curve with simple returns, things are a bit more complicated
* 简单回报:用简单回报直接计算权益曲线，事情就有点复杂了

* ![image-20230526173908137](D:\笔记\笔记图片\image-20230526173908137.png)

* Gives same answer as going via log returns
* 和通过log返回得到相同的答案

![image-20230526174717457](D:\笔记\笔记图片\image-20230526174717457.png)

![image-20230526174724318](D:\笔记\笔记图片\image-20230526174724318.png)

![image-20230526174741419](D:\笔记\笔记图片\image-20230526174741419.png)

![image-20230526174825929](D:\笔记\笔记图片\image-20230526174825929.png)

![image-20230526174834896](D:\笔记\笔记图片\image-20230526174834896.png)



## 12 (3.3) Perfect Returns  完美的回报

#### 12.1 Perfect profit/return

![image-20230526183702236](D:\笔记\笔记图片\image-20230526183702236.png)

* **Perfect profit/return is computed via the perfect position: going long when the market goes up and short when it goes down**
* **完美利润/回报是通过完美头寸来计算的:当市场上涨时做多，当市场下跌时做空**
* ![image-20230526183417430](D:\笔记\笔记图片\image-20230526183417430.png)

![image-20230526183545844](D:\笔记\笔记图片\image-20230526183545844.png)

![image-20230526183902737](D:\笔记\笔记图片\image-20230526183902737.png)

![image-20230526183941490](D:\笔记\笔记图片\image-20230526183941490.png)

* ![image-20230526184112165](D:\笔记\笔记图片\image-20230526184112165.png)

![image-20230526184251767](D:\笔记\笔记图片\image-20230526184251767.png)

* <font color=red size=5>这段代码的目的是计算两种不同的投资策略在整个投资期间的累积收益率。</font>

![image-20230526184801056](D:\笔记\笔记图片\image-20230526184801056.png)

![image-20230526184923286](D:\笔记\笔记图片\image-20230526184923286.png)

![image-20230526184942099](D:\笔记\笔记图片\image-20230526184942099.png)



## 13 （3.4）Copycat Strategy 模仿策略

 

### 13.1 Simple strategy: Copycat

* While we can't get the perfect return (as we can't perfectly predict the future), here's a related rule to generate a position vector:
* 虽然我们无法获得完美的回报(因为我们无法完美地预测未来)，但这里有一个相关的规则来生成头寸向量:

![image-20230528095740529](D:\笔记\笔记图片\image-20230528095740529.png)

* Copycat strategy 
  * **If the close is higher than the open, buy the next day**
  * **如果收盘价高于开盘价，就在第二天买入**
  * **Otherwise, sell the next day**
  * **否则，第二天就卖出**
* Trys (stupidly) to capture momentum in price moves
* 试图(愚蠢地)抓住价格变动的势头
* We call it copycat to indicate that it copies what would have worked on the previous day
* 我们称其为copycat，是指它复制了前一天的工作



* If there are 
* **consecutive days where price moves in the same direction**
* **价格向同一方向移动的连续天数**
* and
* when the price move direction differs from the previous day's (i.e. we lose), the loss should not be too large, that is: 
* 当价格变动方向与前一天不同(即亏损)时，亏损不能太大，即:
* <font color=red>**losing days should not wipe out the gains from (possibly multiple) winning days**</font>
* 亏损的日子不应该抵消(可能是多次)盈利的日子的收益

![image-20230528100021187](D:\笔记\笔记图片\image-20230528100021187.png)

* Testing the strategy
* 测试策略
* From now on, we will repeatedly use functions from: 'utilities.R'.
* 从现在开始，我们将反复使用来自:'utilities.R'的函数。
* In this case we will use:
  * getLogReturns(prices) which computes log returns from adjusted prices
  * getEquityLog(log_ret,pos) which computes a simple returns equity curve from log returns and a position vector

![image-20230528100427741](D:\笔记\笔记图片\image-20230528100427741.png)

![image-20230528100519521](D:\笔记\笔记图片\image-20230528100519521.png)

![image-20230528100529242](D:\笔记\笔记图片\image-20230528100529242.png)

![image-20230528100541342](D:\笔记\笔记图片\image-20230528100541342.png)

![image-20230528100713028](D:\笔记\笔记图片\image-20230528100713028.png)

* The position today uses price data from today
* 今天的头寸使用今天的价格数据
* This is look-ahead bias:
* 这就是前瞻性偏见:
* **<font color=red>When we trade we cannot know the close before it happens!</font>**
* **<font color=red>当我们交易时，我们无法提前知道交易结束后的收盘价</font>**

![image-20230528101145226](D:\笔记\笔记图片\image-20230528101145226.png)

* 换句话说，我们需要尽可能的避免前瞻性偏见，因为我们不知道未来的数据

![image-20230528101421555](D:\笔记\笔记图片\image-20230528101421555.png)

![image-20230528101505279](D:\笔记\笔记图片\image-20230528101505279.png)

* **<font color=red>在R语言中，数组和向量的索引是从1开始的，因此不存在`pos[0]`的位置。</font>**
* **<font color=red>lag函数是R语言用于向后移动数据的函数，他将向量或者时间序列中的元素想后移动一定数量的位置。</font>**

![image-20230528101734459](D:\笔记\笔记图片\image-20230528101734459.png)

![image-20230528114823375](D:\笔记\笔记图片\image-20230528114823375.png)

![image-20230528114829612](D:\笔记\笔记图片\image-20230528114829612.png)





![image-20230528113725779](D:\笔记\笔记图片\image-20230528113725779.png)

* Warning
* We have not included **slippage** in any of these backtests 
* 我们没有在任何这些回测中包括滑点
* **Slippage** is one reason that **bad strategies cannot always be transformed into good ones** by "switching" positions
* 滑点是坏策略不能通过“转换”仓位转化为好策略的原因之一





## 14 （3.5）Risk reward measures 风险奖励措施

* We now study performance measures that combine a measure of **profitability (reward)** with a measure of risk:
* 我们现在研究将盈利能力(奖励)与风险相结合的绩效衡量标准
  * Sharpe Ratio
  * 夏普比率
  * Information Ratio
  * 信息比率
  * Sortino Ratio
  * 索丁诺比率
  * Maximum drawdown
  * 最大降深
  * Calmar Ratio
  * 卡玛比率
* They are **<font color=red size=5>implemented</font>** in the <font size=5>**PerformanceAnalytics**</font> package
* **它们是在PerformanceAnalytics包中实现的。**

![image-20230528115030894](D:\笔记\笔记图片\image-20230528115030894.png)

### 14.1 Risk/Reward measures

* Performance measures for trading strategies often **combine different aspects** of performance
* 交易策略的绩效衡量通常**结合了绩效的不同方面**
* In addition to profit/return a measure of **risk** is often incorporated, e.g., as the:
* 除了利润/回报之外，还经常纳入风险的衡量标准，例如
  * <font size=5 color=red>**standard deviation of returns (Sharpe ratio)**</font>
  * <font color=red>**收益标准差(夏普比率)**</font>
  * <font size=5 color=red>**downside deviation (Sortino ratio)**</font>
  * <font color=red>**下行偏差(索氏比)**</font>
  * <font size=5 color=red>**maximum drawdown**</font>
  * <font color=red>**最大降深**</font>
* Roughly you can have in mind:<font color=red> **Low risk = consistent returns**</font>
* 你大概可以这样想:**低风险=持续的回报**

![image-20230528115530007](D:\笔记\笔记图片\image-20230528115530007.png)

#### 14.1.1 Sharpe Ratio  夏普比率

![image-20230528115842752](D:\笔记\笔记图片\image-20230528115842752.png)

![image-20230528115939919](D:\笔记\笔记图片\image-20230528115939919.png)

![image-20230528120111035](D:\笔记\笔记图片\image-20230528120111035.png)

#### 14.1.2 Information Ratio 信息比率

![image-20230528121253998](D:\笔记\笔记图片\image-20230528121253998.png)



#### 14.1.3 Sortino Ratio 索丁诺比率

![image-20230528121323508](D:\笔记\笔记图片\image-20230528121323508.png)

#### 14.1.4   2 variants of Downside Deviation 2个变体的下行偏差

* Downside Deviation（下行标准差）是用于衡量投资组合或资产在下行风险（负回报）方面的波动性的指标。**<font color=red size=5>它是在计算标准差时，只考虑负回报的一种变体。</font>**

* 1. subset method: takes the root mean square only of those deviations where the return is below the MAR (**MAR:"Minimum Acceptable Return**)

  2. **子集法**:只取收益率低于MAR的偏差的均方根。

     "MAR" 是指 "Minimum Acceptable Return"，即最低可接受回报。

  3. full method: it includes a 0 in the root mean square for every return above the MAR, and the deviation below the MAR for every other return 

  4. **完全法**:对于每一个高于MAR的收益率，在均方根处都有一个0，对于其他每一个低于MAR的收益率，在均方根处都有一个0

* Note: because the extra entries in the full method are all zero, the sum in both cases is the same, the only (potential) difference is the divisor in the mean - see examples below

* 注意:因为full方法中的额外条目都是零，所以两种情况下的和是相同的，唯一的(潜在的)区别是平均值中的除数-参见下面的示例

![image-20230530220942358](D:\笔记\笔记图片\image-20230530220942358.png)

Warning 

* All three ratios assume that the "second moments" (e.g., standard deviation or downside deviation) are enough to measure risk. 
* 所有这三个比率都假定“第二时刻”(例如，标准偏差或下行偏差)足以衡量风险。

* **However it is widely accepted that financial return distributions have "fat tails", making this assumption invalid.** 
* **然而，人们普遍认为财务回报分布具有“肥尾”，这使得这种假设无效。**

* **Nonetheless, these ratios are still very commonly used in practice.**
* **尽管如此，这些比率在实践中仍然非常常用。**

![image-20230530221200404](D:\笔记\笔记图片\image-20230530221200404.png)



![image-20230530221404498](D:\笔记\笔记图片\image-20230530221404498.png)

#### 14.1.5 Issues with standard deviation 标准偏差问题

As a measure of risk it suffers from several drawbacks: 

作为一种衡量风险的方法，它有几个缺点:

* **Symmetric with respect to upside and downside** 
* **上下对称**
  * Upward and downward changes contribute equally 
  * 向上和向下的变化贡献相等
  * Investors typically associate risk only with the downside 
  * 投资者通常只把风险与下行联系在一起
  * Hence sometimes the Sortino ratio is used 
  * 因此有时使用索蒂诺比率
* **Oblivious to sequence of gains and losses** 
* **对得失顺序毫不在意**
  * Does not recognize strings of losses (i.e. drawdowns)
  * 不承认一连串的损失(即提款)

![image-20230530222300402](D:\笔记\笔记图片\image-20230530222300402.png)



## 15 （3.6）Risk reward measures (part 2)

![image-20230530222425420](D:\笔记\笔记图片\image-20230530222425420.png)

#### 15.1 Maximum drawdown

* decline from historical peak
* 从历史峰值下降



![image-20230530222443349](D:\笔记\笔记图片\image-20230530222443349.png)



![image-20230530224414655](D:\笔记\笔记图片\image-20230530224414655.png)

* Suppose the cumulative profit/loss at time t is
* 假设t时刻的累计损益为St
* The running maximum cumulative proft/loss is
* 最大累计盈亏为 Mt
* The drawdown is
* 缩减是 Dt = Mt-St

#### 15.2 Wealth index vs. Cumulative simple returns

![image-20230530225150032](D:\笔记\笔记图片\image-20230530225150032.png)

![image-20230530225327683](D:\笔记\笔记图片\image-20230530225327683.png)

* The reason for the minus sign is to make the drawdown positive, so that it is the same sign as in the profit/loss case defined earlier (and the term maximum is accurate)
* 使用负号的原因是为了使亏损为正，因此它与前面定义的损益情况中的符号相同 (“最大值”这个词是准确的)

![image-20230530225411464](D:\笔记\笔记图片\image-20230530225411464.png)

![image-20230530225433462](D:\笔记\笔记图片\image-20230530225433462.png)

![image-20230530225442105](D:\笔记\笔记图片\image-20230530225442105.png)

![image-20230530225450712](D:\笔记\笔记图片\image-20230530225450712.png)

![image-20230530225459589](D:\笔记\笔记图片\image-20230530225459589.png)

![image-20230530225507594](D:\笔记\笔记图片\image-20230530225507594.png)

![image-20230530225516751](D:\笔记\笔记图片\image-20230530225516751.png)

![image-20230530225523608](D:\笔记\笔记图片\image-20230530225523608.png)











# --------------------------------------------------

## 17.1 （4.1）Moving averages 移动平均线

* **Moving averages** are a useful way to incorporate more of the recent price history in trading decisions
* **移动平均线**是在交易决策中纳入更多近期价格历史的有效方法。
* <font color=blue>移动平均线是根据一定时间范围内的收盘价或其他指标的平均值来计算当前的平均值。这个时间范围可以是几天、几周、几个月或几个季度。这个时间范围越短，移动平均线就越接近价格变化的实际情况，但也越容易受到短期波动的影响。相反，如果时间范围越长，移动平均线就越平滑，但也越慢反应价格的变化。</font>

* **<font color=red>在实际的应用中，移动平均线可以被视为一种低通滤波器</font>**

* <font size=5>以下是关于这个Moving Averages的例子</font>

![image-20230506224419163](D:\笔记\笔记图片\image-20230506224419163.png)

* <font color=red>实际上就是通过之前一段时间的平均值来计算之后的平均值</font>





### 17.2 Filtering time series

![image-20230504143348850](D:\笔记\笔记图片\image-20230504143348850.png)

* Two types of filter we consider: 
  * **low-pass filter** 
  * **低通滤波器**
    * **removes short-term fluctuations (noise); leaves trend** 
    * **去除短期波动（噪音）；留下趋势**
  * **high-pass filter removes trend;** 
  * **高通滤波器消除了趋势**
    * **leaves short-term fluctuations** 
    * **留下短期的波动** 
* The terms low and high refer to frequencies A rich theory of filters is central to digital signal processing We will look at basic examples commonly used with time series
* 术语 "低 "和 "高 "指的是频率。丰富的滤波器理论是数字信号处理的核心，我们将看一下常用于时间序列的基本例子。

#### 17.2.1 Causal filters 因果滤波器

* A filter is 

  * **causal** if its output depends only on past and present inputs 
  * 如果它的输出只取决于过去和现在的输入，则为**因果关系**
  * **non-causal** if its output also depends on future inputs
  * 如果它的产出也依赖于未来的投入，则是**非因果的**
  * <font color=red>关键在于是否依赖未来的投入</font>

  

* *Causal filter是一种数字信号处理滤波器，它仅使用当前和过去的信号值来计算滤波器的输出。这意味着，滤波器输出的任何值都不依赖于未来的信号值。*

  *因此，Causal filter也被称为因果滤波器（causal filters），因为它们的输出只取决于“因果”关系，即当前和过去的信号值。这种特性使得Causal filter在实时信号处理和滤波应用中非常有用，因为它们可以保证滤波器输出的延迟时间是固定的，不会因为未来信号值的影响而发生变化。*

![image-20230504144246877](D:\笔记\笔记图片\image-20230504144246877.png)

* When developing trading systems we must avoid look-ahead bias (the system must only use data that is available at the time of a decision)
* 在开发交易系统时，我们<font color=red>必须避免瞻前顾后的偏见（**系统必须只使用决策时的数据**）。</font>
* 这就是为什么我们只考虑因果滤波器



##### 17.2.2.1 Low-pass filter 低通滤波器当中的移动平均线

* Often we are interested in the trend of a time series
* 通常我们对一个时间序列的趋势感兴趣 
* **Short-term fluctuations obscure the trend** 
* **短期波动掩盖了趋势**
* To remove this noise we apply a low-pass filter 
* 为了消除这种噪音，我们应用一个低通滤波器
* We consider a simple implementation via moving averages
* 我们考虑通过移动平均线进行简单的实现



* **Moving averages are a type of digital low-pass filter** 
* **移动平均线是一种数字低通滤波器**
* Sometimes called a **rolling average or rolling mean** 
  * (later we consider rolling standard deviations and rolling medians) 
  * (以后我们考虑滚动标准差和滚动中位数）
  * We consider **three types** of moving average: 
  * 1. **Simple (weights are all equal)  简单（权重都是一样的）** 
    2.  **Weighted (weights form arithmetic progression) 加权（权数形成算术级数）**
    3.  **Exponential (weights form geometric progression) 指数(权重形成几何级数)**

![image-20230504145650665](D:\笔记\笔记图片\image-20230504145650665.png)

###### 18.2.2.1 Simple moving average  简单移动平均线  SMA

![image-20230504145926434](D:\笔记\笔记图片\image-20230504145926434.png)

 

* **n is the number of periods to average over (the lookback)**
* **n是平均的周期数（回看）。** 
* 使用过去几天的东西
* Larger n gives more smoothing
* 较大的n可以提供更多的平滑度
* **<font color=red>下面这个例子是正确的，此时n=3,完全满足上述公式</font>**
* ![image-20230506225928971](D:\笔记\笔记图片\image-20230506225928971.png)

![image-20230504150424688](D:\笔记\笔记图片\image-20230504150424688.png)

###### 18.2.2.2 Exponential moving average  指数移动平均线  EMA

* Parameter: 0 < α < 1 
  * Weighted average of all previous values
  * 所有先前值的加权平均值
  *  Exponentially more weight on recent values
  * 最近值的权重呈指数级增加

![image-20230504150702225](D:\笔记\笔记图片\image-20230504150702225.png)

* 讲真这个公式不是很能看懂，不懂是为什么
* **与SMA不同，EMA赋予最近价格数据更大的权重，因此更能快速反应价格的变化**



**<font size=5>Simple versus Exponential MA</font>**

* Similarities: 
  * **lagging (they turn after the time series does)** 
  * **滞后性（它们在时间序列出现后才转向）**
  * Rule of thumb conversion: alpha = 2/(n+1), n = (2/alpha) - 1. One justification: centres of masses of SMA & EMA weight distributions equal with this rule.
  * 经验法则转换：α=2/(n+1)，n=(2/α) - 1。 一个理由：SMA和EMA的质心与此规则相等。



* Differences:
  * EMA responds more quickly to prices 
  * EMA对价格的反应更加迅速
  * EMA takes into account all past data; SMA takes into account only n most recent data points 
  * EMA考虑到所有过去的数据；SMA只考虑到最近的n个数据点. **但是最近的数据占权重比较大**
  * EMA only needs the most recent EMA value to be kept; SMA requires all n most recent data points be kept
  * EMA只需要保留最近的EMA值；SMA需要保留所有N个最近的数据点。

![image-20230504151634819](D:\笔记\笔记图片\image-20230504151634819.png)

![image-20230504151848047](D:\笔记\笔记图片\image-20230504151848047.png)

![image-20230504151856376](D:\笔记\笔记图片\image-20230504151856376.png)

* **你可以发现，这三个一个是全值平均值，一个是线性递减，一个是指数递减**



#### 17.2.2 High-pass filter

* **<font color=red>Detrending filter</font>**: lets through high-frequency noise; rejects low-frequency trend - can be implemented as follows:
* 去趋势滤波器：允许通过高频噪音；拒绝低频趋势--可按以下方式实施：
  * Apply low-pass filter to data 
  * 对数据应用低通滤波器 
  * Subtract filtered data from original data
  * 从原始数据中减去过滤后的数据



![image-20230504152150404](D:\笔记\笔记图片\image-20230504152150404.png)

* **Moving averages are simple methods to remove noise from time series** 
* **移动平均线是从时间序列中去除噪声的简单方法**
* They can also be used to de-trend time series 
* 它们也可以用来消除时间序列的趋势
* They are a building block for many technical analysis indicators that are used in trading strategies
* 它们是许多用于交易策略的技术分析指标的基础。



## 18 (4.2) Bollinger Bands overbought/oversold strategy

* Bollinger Bands are a standard technical analysis indicator built with a moving average and standard deviation. The bands define "high" and "low" price levels on a continual, relative basis.
* 布林带是一种标准的技术分析指标，由移动平均线和标准偏差组成。这些波段在连续的、相对的基础上定义了价格的“高”和“低”水平。
* **Bollinger Bands overbought/oversold strategy是一种基于Bollinger Bands指标的交易策略，用于判断价格的超买和超卖区域，并作出相应的交易决策。**
* **<font color=blue>Bollinger Bands是一种常用的技术分析指标，由三条线组成：中轨、上轨和下轨。中轨是移动平均线，通常使用20天的简单移动平均线；上轨和下轨则是围绕中轨上下两个标准差的距离，分别表示价格的高位和低位。Bollinger Bands的主要作用是用于识别价格的波动范围和趋势变化。</font>**
* **<font color=blue>Bollinger Bands overbought/oversold strategy的基本思路是，当价格触及上轨时，价格被认为处于超买状态，预示着价格即将回落；当价格触及下轨时，价格被认为处于超卖状态，预示着价格即将反弹。因此，在超买和超卖区域，投资者可以选择相应的交易策略，如买入（在超卖区域）或卖出（在超买区域）。</font>**

![image-20230506231215995](D:\笔记\笔记图片\image-20230506231215995.png)

* John Bollinger is a early proponent of technical analysis (https://en.wikipedia.org/wiki/John_Bollinger); he developed Bollinger Bands in the 1980s, but is still active to this day. 
* A "mean-reversion" trading strategy that uses Bollinger Bands to:
* 一种“均值回归”交易策略
  * **buys when they suggest the market "oversold";**
  * 当他们认为市场 "超卖 "时，就会买进。
  * **sells when they suggest the market "overbought".**
  * 当他们暗示市场“超买”时卖出
  
  * 解释一下这个超买和超卖
  * **<font color=red size>超买Overbought</font>**：**超买是指资产或证券的价格在短期内上涨过快或超过其内在价值的情况。这意味着市场参与者对该资产的需求过高，推动价格上涨到一个相对高位。** <font color=blue>买的人多了，导致价格上涨，所以此时价格虚高，所以卖出</font>
  * **<font color=red size>超卖Oversold</font>**：**超卖是指资产或证券的价格在短期内下跌过快或低于其内在价值的情况。这意味着市场参与者对该资产的需求过低，推动价格下跌到一个相对低位。** <font color=blue>卖的人多了，导致价格下跌，所以此时价格虚低，所以买进</font>

![image-20230504171232933](D:\笔记\笔记图片\image-20230504171232933.png)

* 由三部分组成：
  * upperBB：上轨
  * middleBB: 中轨
  * lowerBB：下轨
  * %b：**(xt − l)/(u − l) 是将当前价格 xt 转化为一个归一化的值，该值表示当前价格相对于布林带的范围位置，取值范围为 [0,1]。**

![image-20230504171744112](D:\笔记\笔记图片\image-20230504171744112.png)

![](D:\笔记\笔记图片\image-20230504171752629.png)

![image-20230504171933060](D:\笔记\笔记图片\image-20230504171933060.png)

* **Overbought/Oversold Strategy  超买或超卖的策略**
  * **Long when price is below lower band line** 
  * **当价格低于低带线时做多**
  * **Short when price is above upper band line**
  * **当价格高于上带线时做空**

* Attempts to trade corrections when the market has "overshot": In this sense it is a mean reversion type strategy: it bets that prices will move back towards the mean (i.e. the moving average)
* 试图在市场“超调”时进行修正交易:从这个意义上讲，这是一种均值回归型策略:它押注价格将向均值(即移动平均线)移动。

![image-20230504172342187](D:\笔记\笔记图片\image-20230504172342187.png)

![image-20230504172350356](D:\笔记\笔记图片\image-20230504172350356.png)

![image-20230504172410371](D:\笔记\笔记图片\image-20230504172410371.png)

* 1. A numerical or other measurable factor forming one of a set that defines a system or sets the conditions of its operation. 
  2. 定义系统或设置其运行条件的一组数字或其他可测量的因素。
  3. A quantity whose value is selected for the particular circumstances and in relation to which other variable quantities may be expressed.
  4. 一种量，其值是为特定情况而选定的，并可与之相联系地表示其他可变量。

![image-20230504174236969](D:\笔记\笔记图片\image-20230504174236969.png)

* Two obvious numerical parameters are: 
  * n the lookback, and 
  * 移动平均线取前多少天的值
  * sd the standard deviation multiplier 
  * sd 标准差乘数 
* (Non-numeric parameters include the markets we trade on) 
* (非数字参数包括我们交易的市场)
* Changing n and sd with have a large impact on this strategy, which we will reflect on in later slides (in Topic 5). 
* 改变n和sd对该策略有很大的影响，我们将在后面的幻灯片(主题5)中反映这一点。
* More generally we will also return to optimization of parameters and the robustness of trading strategies later.
* 更一般地说，我们稍后还会回到参数的优化和交易策略的鲁棒性

![image-20230504174637112](D:\笔记\笔记图片\image-20230504174637112.png)

## 19 (4.3) Path dependence 路径独立

* Definition 
* A strategy is path-independent if 
* 一个策略是路径独立的，如果
* **<font color=red>Trading decisions do not depend on past trading decisions</font>**
* <font color=red>交易决定不取决于过去的交易决定</font>
* ![image-20230531112124278](D:\笔记\笔记图片\image-20230531112124278.png)
* **Both strategies we looked at so far were path-independent** 
* **到目前为止，我们所看到的两种策略都是与路径无关的**
* **This allowed vectorized computation of positions** 
* **这允许对位置进行矢量计算**
* **In R, vectorized computation is both simple and efficient**
* **在R中，矢量计算既简单又高效**

* **<font color=red>如果一个投资策略是path-independent，那么它的盈利和亏损只与所选资产在一定时间内结束时的价格有关，而不考虑在此期间资产价格变化的路径。这种策略与市场趋势无关，也不需要对市场进行预测。</font>**



### 19.1 Entries and exits 入口和出口

* Our BBands mean reversion strategy is path independent because the position on day k is computed without reference to earlier positions 
* 我们的BBands均值回复策略是独立于路径的 因为在计算第k天的仓位时，不需要参考 衡量之前的头寸
* **In terms of entering and exiting trades (moving between the positions {long, short, flat}), there is symmetry property that results from the path independence:** 
* **在进入和退出交易方面（在{多头、空头、平头}的位置之间移动，存在由路径独立性产生的对称属性：**
* **<font color=red>Long position: enter when we cross below lower band line and exit when we cross above lower band line</font>** 
* **多头头寸：当我们越过下限线时进场 线时进场，并在越过下限线时出场。**
* **For short positions we have a similar symmetry between entering and exiting trades with reference to the upper band.** 
* **对于空头头寸，我们有一个类似的对称性 进入和退出交易时，也有类似的对称性。**
* Note: when exiting a long or short position we may either go to flat or "reverse positions" and enter the "opposite position"
* 注意：当退出一个多头或空头头寸时，我们可以去 平仓或 "倒仓 "并进入 "相反的位置"

### 19.2 Natural path-dependent variant 依赖路径的自然变体

![image-20230504193948025](D:\笔记\笔记图片\image-20230504193948025.png)

* Overbought/Oversold Strategy Variant 超买/超卖策略变体
  * Go Long when price **crosses below** lower band line; exit when price 超买/超卖策略变体e moving average
  *  当价格越过下限线时**做多**； 当价格越过移动平均线时**退出**
  * Go Short when price **crosses above** upper band line; exit when **price crosses** below moving average
  * 当价格越过上带线时**做空**;当价格跌破移动平均线时**退出**

## 20. (4.4)Path dependence: Holding periods, stop losses, and profit targets 路径依赖:持有期、止损和利润目标

### 20.1 Path dependence in general

* **Path independence is actually a serious limitation**
* **路径独立性实际上是一个严重的限制**
* ![image-20230504201355806](D:\笔记\笔记图片\image-20230504201355806.png)
* ![image-20230504205315645](D:\笔记\笔记图片\image-20230504205315645.png)
*  Most trading strategies are path-dependent 
* 大多数交易策略都是依赖于路径的
  * This means we that the strategy 
    * maintains a **state** and
    * 保持一个状态 
    * conditions its actions on this state
    * 它的行动以这种状态为条件



### 20.2 Other examples

* Many common strategy constructions require path dependence: 
* 许多常见的策略构建都需要路径依赖
  * Specialized exit conditions, e.g. 
  * 特殊的退出条件
    * **Holding period  持有时间**
    * **Profit target  利润目标**
    * **Stop loss  止损**
* Many other examples, e.g., related to entry conditions that depend on past performance
* 许多其他的例子，例如，与依赖于过去表现的入职条件有关

#### 20.2.1 Example of holding period

* In this example: 
  * our state will encode how long we have been in a trade 
  * 我们的状态将对我们从事某一行业的时间进行编码
  * we will use a parameter called hold (for "**holding period**") 
  * 我们将使用一个名为hold的参数(表示“**持有时间**”)
  * we will exit trades when we reach our hold 
  * 当我们到达持仓时，我们将退出交易
  * **<font color=red>规定一个时间，将其命名为持仓期，如果在持仓期过去之前，交易出现了亏损或其他不利因素，我们不会提前退出，而是等待持仓期结束之后再做决定。只有当计数器的值等于持仓期时，我们才会根据交易情况决定是否退出交易。</font>**
  * <font color=blue>更简单的说，在有在持仓期满时，我们才进行买卖操作</font>
* In terms of the code implementation, we: 
  * copy our current position forward to the next period if we have not yet reached our holding period
  * 如果我们还没有达到持仓期，将我们当前的仓位复制到下一期
  * if we are in a trade and have hit the holding period we reset the position to flat
  * 如果我们正在进行交易，并且已经达到了持仓期，我们将头寸重置为平仓

![image-20230504210831527](D:\笔记\笔记图片\image-20230504210831527.png)

##### 20.2.1.1 Holding period parameter hold 持有期参数

* We exit a trade if and only if hold periods have passed; 
* implemented by staying in a trade if count is smaller that hold
* 当且仅当持有期已过，我们退出交易;如果持仓数量小于持仓数量，则继续持有

![image-20230504211631374](D:\笔记\笔记图片\image-20230504211631374.png)

### 20.3 Position vector 头寸向量

* **The important point is the path-dependance** 
* **重要的一点是路径依赖性** 
* Fixed holding period for trades (5 in the example) 
* 固定的交易持有期（例子中为5个月）
* Position vector comprises 11111, -1 -1 -1 -1 -1, 0; i.e., five days long in a row, or five days short in a row, or a flat day
* 位置向量包括1111，-1-1-1-1-1，0；即连续5天长，或连续5天短，或一个平日
* **这三个向量分别代表：在过去的五天中，投资者持有了五天的多头头寸，五天的空头头寸，第六个元素0代表“不持仓”，即投资者在这一天没有进行任何交易并且没有持有多头或空头头寸。这是一种与市场无关的状态，也称为空仓或空头平仓。**

![image-20230531120046153](D:\笔记\笔记图片\image-20230531120046153.png)

#### 20.3.1 Position 头寸

<font size=5>这里临时插播一条关于头寸的内容</font>

* 在金融和投资领域中，头寸（Position）通常指投资者持有某种资产的数量和方向（即多头头寸或空头头寸）。头寸可以用来描述投资者在某个市场中的持仓情况和风险敞口。
* 多头头寸（Long Position）是指投资者购买某个资产（如股票、货币等）并持有该资产，以期待资产价格上涨，从而获得利润的投资策略。当投资者持有多头头寸时，他们相信该资产的价格将会上涨，因此持有该资产的时间将会较长。
* 空头头寸（Short Position）是指投资者通过出售某个资产（如股票、货币等）并以后再购回该资产，以期待资产价格下跌，从而获得利润的投资策略。当投资者持有空头头寸时，他们相信该资产的价格将会下跌，因此持有该资产的时间将会较短。

#### 20.3.2 Next example - stop loss

* **A stop loss limits the loss on a particular trade** 
* **止损限制了某项交易的损失** 
* We will measure the simple return of a trade 
* 我们将衡量一个交易的简单回报
* If it is too negative we will exit the trade
* 如果它过于消极，我们将退出交易。

![image-20230504215038479](D:\笔记\笔记图片\image-20230504215038479.png)

![image-20230504215250043](D:\笔记\笔记图片\image-20230504215250043.png)

![image-20230504215317410](D:\笔记\笔记图片\image-20230504215317410.png)

![image-20230504215328802](D:\笔记\笔记图片\image-20230504215328802.png)

##### 20.3.2.1 Insights from stop loss example

* As we increase the parameter stoploss, i.e., make it harder to stopout for a given trade, the number of stopouts generally decreases, but not monotonically: **due to path dependence one may increase the "stoploss parameter" and get more stopouts**
* 当我们增加止损参数（stoploss parameter），也就是使得在某个交易中更难被止损平仓时，一般来说，止损次数会减少。但是这种减少的关系不是单调的，也就是说增加止损参数不一定会一直减少止损次数。这是由于路径依赖性（path dependence）导致的，即之前的决策路径可能会对当前的交易决策产生影响。**因此，在一些情况下，即使增加了止损参数，止损次数可能仍会增加。**
* Also it is clear that by **having too small a stoploss parameter, we can actually hurt our performance** (we do best with a high parameter of 0.5 in this example); sometimes the market goes against us before going the way we want it to
* 同样明显的是，**如果止损参数太小，我们实际上会损害我们的表现**（在这个例子中，我们在0.5的高参数下表现最好）；有时市场在走向我们想要的方向之前就会与我们相悖。



<font size=5>解释一下很多奇怪的名词</font>

* **止损次数（stopout frequency**）是指在一段时间内，由于亏损超过一定比例而被止损平仓的交易次数。当交易亏损超过一定程度时，投资者通常会使用止损策略来控制风险和损失，即自动平仓以避免进一步的损失。止损次数可以反映投资者的风险管理能力和交易策略的有效性。如果止损次数过多，可能会减少交易的盈利，增加交易成本和风险。因此，投资者需要在平衡风险和收益的前提下，合理控制止损次数，避免过度频繁地平仓。

* **止损平仓（stop-loss order）**是一种常用的交易策略，用于限制亏损并控制风险。当投资者开仓后，如果交易出现亏损，止损平仓策略会自动触发，以平仓交易并避免进一步的损失。

  具体来说，止损平仓是一种在预设的价格下单的交易策略。当交易价格达到或低于止损价格时，止损平仓将自动下单，并以预设价格平仓该交易。这样可以限制亏损和控制风险。一旦止损平仓被触发，该交易将被强制平仓，投资者将无法继续持有该头寸。止损平仓是一种有效的风险管理工具，可以帮助投资者控制亏损并保护资金安全。

* **平仓（close position）**是指投资者在某个交易市场上，通过卖出（如果持有多头头寸）或买入（如果持有空头头寸）相应数量的资产，以结束当前的头寸并实现交易盈利或亏损的行为。
* <font color=red>简单来说，就是将自己持有的头寸卖出或者将自己借来的空头卖出去，成为平仓</font>

![image-20230504220920387](D:\笔记\笔记图片\image-20230504220920387.png)

### 20.4 Profit target

* **Profit target（盈利目标）是一种设定的价格水平或预期收益，用于确定在达到该水平或收益之后，投资者将执行卖出或平仓操作以实现预期的盈利。**
* 可以发现，刚好与stop loss相反

![image-20230504221137785](D:\笔记\笔记图片\image-20230504221137785.png)

* In Topic 5, we introduce a backtester framework where we can easily test path-dependent strategies such as the variant of the Bbands mean-reversion strategy where we exit only when reach the moving average price...
* 在主题5中，我们介绍了一个回测框架，我们可以很容易地测试路径依赖的策略，如Bbands均值回归策略的变种，我们只在达到移动平均价格时退出。

![image-20230504221207052](D:\笔记\笔记图片\image-20230504221207052.png)

* 路径依赖性测试

* 测试路径依赖性策略是指对一类交易策略进行回测和验证，这些交易策略的决策路径和持仓状态可能会对当前交易决策产生影响。在这种策略中，交易决策不仅依赖于当前市场价格等因素，还受到历史决策路径的影响。因此，对这类策略进行测试和验证需要考虑多种因素，如历史交易数据、交易成本、风险敞口等。

  在金融领域，一些交易策略是路径依赖性的，例如基于技术分析的策略，它们通常使用历史价格数据和指标来进行交易决策。另一个例子是基于风险管理的策略，它们可能会调整投资组合的权重或使用止损策略来控制风险。

  为了测试和验证这些策略的有效性，投资者通常会使用回测框架或模拟交易平台。这些工具可以模拟历史市场数据，并根据特定的交易策略执行交易。通过对模拟交易结果进行统计分析和风险评估，投资者可以评估不同交易策略的有效性和风险敞口，并选择最合适的策略来实现投资目标。

* <font color=red>感觉就是通读全文，然后测试路径依赖和什么有关，通过调整参数来模拟市场的变化</font>



## 21（4.5） Slippage Revisited 滑动重新审视

**Slippage**是指在实际交易中，由于市场价格波动、交易量变化等因素，导致**交易价格**与**预期价格**之间出现差异的情况。这种差异可能会导致实际交易结果与预期结果之间的差异，并对交易策略的有效性和风险控制产生重大影响。

* <font color=red>并不是什么太难的定义，就是交易价格和预期价格出现差异被称为Slippage</font>

Slippage revisited是指重新考虑Slippage对交易策略的影响，并寻找更好的方法来控制Slippage对交易的影响。在实际交易中，Slippage是不可避免的，因此需要使用一些方法来减少Slippage的影响。



### 21.1 Slippage

* Reminder: **Slippage** is the difference between **the expected execution price** (e.g. best bid or best ask) and **execution price**
* 提示:滑差是预期执行价格(如最佳买入价或最佳卖出价)与执行价格之间的差额
* For us, using daily data, the expected execution price may be the Open or Close price for example
* 对我们来说，使用每日数据，预期执行价格可能是开盘价或收盘价
* Execution price: (average) price you actually traded at; we won't find this our in backtesting so we will be conservative in our assumption
* 执行价格:你实际交易的（平均）价格;我们不会在回测中发现这一点，所以我们的假设是保守的

![image-20230504225130653](D:\笔记\笔记图片\image-20230504225130653.png)

#### 21.1.1 How to be conservative? 什么是保守的

* If the actual execution price differs from the expected one, either: 
* 如果实际执行价格与预期价格不同，要么：
  * The execution price was better **(positive slippage)** 
  * 执行价格较好（正滑移）。
  * The execution price was worse **(negative slippage)**
  * 执行价格更糟糕（负滑移）。



* We will be conservative and assume negative slippage: 
* 我们将采取保守的做法，假设出现负的滑坡：
  * **go long (buy): execution higher than expected price** 
  * **做多（买入）：执行高于预期的价格** 
  * **go short (sell) execution is lower than expected price** 
  * **做空（卖出）的执行率低于预期价格** 
* This is **the standard approach for backtesting**
* 这是回溯测试的标准方法

![image-20230504231315316](D:\笔记\笔记图片\image-20230504231315316.png)

* As noted before, one can quite easily design a strategy that: 
* 如前所述，我们可以很容易地设计一个策略：
  * historically perform excellently without slippage 
  * 历史上表现出色，没有打滑现象
  * performs poorly if realistic slippage is included
  * 如果包括现实中的滑移，则表现不佳

#### 21.1.2 Market versus limit orders

![image-20230505115557854](D:\笔记\笔记图片\image-20230505115557854.png)

* **Market orders guarantee execution but not price** 
* 市场订单保证执行，但不保证价格
  * You (almost always) get filled, but may incur large slippage 
  * 你（几乎总是）被填满，但可能会产生大的滑点 
  * Need to carefully model execution price
  * 需要仔细模拟执行价格
* **Limit orders guarantee price but not execution** 
* **限价单保证价格，但不保证执行** 
  * Need to carefully model whether we get filled
  * 需要仔细模拟我们是否得到填补

#### 21.1.3 How to model slippage? 如何建立一个滑块

* There are numerous issues to consider with modelling slippage: 
  * characteristics of the particular trading strategy, i.e., in what market conditions does one trade: Slippage tends to be worse if others are doing the same as you. For example:
  * 特定交易策略的特点，即在什么市场条件下进行交易：如果别人和你做的一样，滑点往往会更严重。比如说
    *  Negative slippage likely if buying during a rally 
    * 如果在涨势中买入，可能出现负滑点
    * Positive slippage likely if buying during a sell-off 
    * 如果在抛售期间买入，可能出现正向滑移
  * characteristics of the particular market and the type of data available - to properly model slippage we really need the data for prices and sizes in the book
  * 为了正确地模拟Slippage现象，需要考虑特定市场的特征以及可用的数据类型。具体来说，我们需要获得市场买卖盘中价格和数量等信息，以更准确地模拟Slippage。



#### 21.1.4 Limit order book data 限价订单簿数据

* **Limit order book data** allows to model market orders and limit orders much more accurately than without it
* **限价订单簿数据**允许对市场订单和限价订单进行建模，比没有这种数据要准确得多。

* With the best bid and best ask (price and volume) 
* 有了最好的出价和最好的要价（价格和成交量），就可以了
  * you can use the appropriate one as your expected price (bid for sell market order, ask for buy market order) 
  * 你可以使用适当的价格作为你的预期价格（卖出市场订单的出价，买入市场订单的要价）。
  * provided your trade size is significantly smaller than the corresponding volume you might assume no slippage 
  * 如果你的交易规模明显小于相应的交易量，你可以假设没有滑点
  * otherwise you can model slippage using **other levels** in the book or using **the bid-ask spread**
  * 否则，您可以使用账面上的其他水平或使用买卖价差来模拟滑动

#### 21.1.5 Our slippage model for daily data

* We describe the slippage model used in our backtester framework as used in COMP226 Assignment 2 and COMP396
* 我们描述了在COMP226作业2和COMP396中使用的回测框架中的滑点模型。
* Without order book data, strong assumptions are required 
* 如果没有订单数据，就需要强有力的假设
* We are using OHLC (Open/High/Low/Close) daily data 
* 我们使用OHLC(开/高/低/收盘)每日数据
* For simplicity we model profit and loss (not returns)
* 为了简单起见，我们对利润和损失(而不是回报)进行建模。
*  In the framework, all trades occur at the open 
* 在这个框架中，所有的交易都发生在开盘时
* The slippage incurred will be based on the overnight gap (difference between the previous close and the open) 
* 产生的滑差将基于隔夜差价(前一个收盘价与开盘价之间的差额)
* If the open is very different from the close then the market is currently volatile. Consequently, slippage (positive or negative) is likely to be greater
* 如果开盘和收盘有很大的不同，那么市场目前是不稳定的。因此，滑移(正或负)可能更大

![image-20230505124522751](D:\笔记\笔记图片\image-20230505124522751.png)

![image-20230505124538483](D:\笔记\笔记图片\image-20230505124538483.png)

![image-20230505124600768](D:\笔记\笔记图片\image-20230505124600768.png)

![image-20230505124701903](D:\笔记\笔记图片\image-20230505124701903.png)

![image-20230505124713178](D:\笔记\笔记图片\image-20230505124713178.png)

![image-20230505124729375](D:\笔记\笔记图片\image-20230505124729375.png)

![image-20230505124740396](D:\笔记\笔记图片\image-20230505124740396.png)

#### 21.1.6 Commissions/transaction costs

* These are costs of trading paid to a broker or exchange 
* 这些是支付给经纪人或交易所的交易成本
* A realistic model would include these too, however unlike including slippage, it is more clearcut how to incorporate transaction costs - just follow cost specification
* 一个现实的模型也应该包括这些，但与包括滑动不同，如何纳入交易成本更为明确——只需遵循成本规范



## 22 (4.6) Mean-reversion strategies 均值回归的策略



### 22.1 Types of trading strategy 贸易的策略类型

* There are two fundamentally different types of trading strategy:
* 1. **<font color=red>mean reversion/ contrarian / overbought-oversold</font>**
  2. **平均值回归/逆向思维/超买超卖**
  3. **<font color=red>trend following / momentum</font>**
  4. **趋势跟踪/动**
* We will give examples of both types of trading strategy.
* 我们将举出两类交易策略的例子。
  *  We have seen a Bollinger Bands Overbought Oversold strategy
  * 我们已经看到了布林线的超卖策略
  * **In this lecture we will look at an example of a mean reversion strategy that uses spreads**
  * **在本讲座中，我们将研究一个使用价差的均值回归策略的例子。**
  * In the next set of slides we will look at several simple examples of momentum strategies
  * 在下一组幻灯片中，我们将看一下几个简单的动量策略的例子







### 22.2 Indicators as strategy building blocks 作为战略构件的指标

#### 22.2.1 Indicators are not strategies 指标不是战略

*  **bbands.R that we saw earlier has a mean-reversion-type trading rule**
* **我们之前看到的bbands.R有一个均值反转型的交易规则**
  * **buy if below lower band**
  * **如果低于下限买入**
  * **sell if above upper band**
  * **卖出，如果高于上行区间**

* Swapping buy and sell completely changes strategy
* 买入和卖出的交换完全改变了策略
* Thus, Bollinger Bands, like most indicators, can be used for either mean-reversion or a trend-following strategies
* 因此，布林线和大多数指标一样，可以用于均线回归或趋势跟踪策略。



### 22.3 Spreads

* **<font color=red size=5>Weighted linear combination (usually difference) of two series</font>**
* **两个系列的加权线性组合（通常是差值）。**
* Strategy can try to exploit mean-reversion in a spread; for a pair of equities this is known as pairs trading, known more generally as statistical arbitrage
* 策略可以尝试利用价差中的均值回归；对于一对股票，这被称为成对交易，更普遍地被称为统计套利。
* Related to the theory of cointegration, which is an important topic within time series analysis. We will not cover this theory in this module...
* 与协整理论有关，它是时间序列分析中的一个重要课题。在本模块中，我们将不涉及这一理论...





### 22.4 Example spread mean-reversion strategy

![image-20230505143751670](D:\笔记\笔记图片\image-20230505143751670.png)



![image-20230505143802040](D:\笔记\笔记图片\image-20230505143802040.png)

![image-20230505143814012](D:\笔记\笔记图片\image-20230505143814012.png)

#### 22.4.1 Position sizing 头寸的大小

* For any trading strategy, position sizing is very important
* 对于任何交易策略来说，仓位大小是非常重要的
* <font color=red>Any spread has an **implicit position ratio**, sometimes called the **hedge ratio** - it is the ratio of the weights in the linear combination</font>
* 任何价差都有一个**隐含的仓位比率**，有时称为对**冲比率**--它是线性组合中的权重比率
* Essentially, in very loose terms, the position sizing should "make the two graphs look the same"
* 从本质上讲，用非常宽泛的术语来说，仓位大小应该 "使两个图形看起来一样"
* We would like this ratio to capture the ratio between expected price moves of the constituent price series - as an example, sometimes this ratio is derived via **via linear regression**
* 我们希望这个比率能够捕捉到组成价格系列的预期价格变动之间的比率--作为一个例子，有时这个比率是通过**线性回归**得出的。
* Next, we will derive it as a ratio of moving averages of prices
* 接下来，我们将把它推导为价格的移动平均线的比率

![image-20230505144409097](D:\笔记\笔记图片\image-20230505144409097.png)

#### 22.4.2 Spread example: finding weights

![image-20230505144633551](D:\笔记\笔记图片\image-20230505144633551.png)

* Spread = x - positionRatio * y
* Buy one unit of x when we sell positionRatio units of y
* 当我们卖出y的仓位比例单位时，买入一个单位的x

![image-20230505144755571](D:\笔记\笔记图片\image-20230505144755571.png)

#### 22.4.2 A spread strategy

* • The goal of creating a spread is to create a **stationary time series**, **that is one with a constant mean and standard deviation**
* 创建Spread的目的是创建一个**静止的时间序列的时间序列，即一个具有恒定的平均数和标准差的**
  **偏差**
* If we succeed we can then buy the spread (long the cheap product and short the expensive one) whenever the spread drops far below its mean and sell the spread whenever it goes too high above its mean
* 如果我们成功了，我们就可以买入价差（做多廉价产品，做空昂贵产品）。廉价产品，做空昂贵产品），只要价差 远远低于其平均值时，就可以买入价差（做多廉价产品，做空昂贵产品），而当价差 涨得太高，超过其平均值时，就可以卖出价差
* The theory of cointegration deals exactly with linear combinations of time series that are stationary - we will not go into the maths though..
* 协整理论确切地处理了线性的 稳态的时间序列的线性组合--我们将不 我们就不谈数学了。
* Next we will see a simple Bollinger Bands-based trading strategy idea for spreads. It is left as an exercise for you to implement it!
* 接下来我们将看到一个简单的基于布林线的价差交易策略想法。我们将把它作为一个练习，让你去实施它!

![image-20230505145454579](D:\笔记\笔记图片\image-20230505145454579.png)



### 22.5 Commonly traded spreads

* Here are some example. A spread can be established:
* 这里有一些例子。可以建立一个Spread:
  * Between different months of the same commodity (called an interdelivery spread/ calendar spread)
  * 同一商品的不同月份之间（称为交割间价差/日历价差）。
  * Between the same or related commodities, usually for the same month (intercommodity spread)
  * 相同或相关商品之间，通常为同一个月（商品间价差）。
  * Between the same or related commodities traded on two different exchanges (intermarket spread).
  * 在两个不同交易所交易的相同或相关商品之间（市场间价差）。
  * Pairs of equities (pairs trading)
  * 成对的股票(成对交易)

### 22.6 Summary on spreads

* Spreads are a common way to look for **mean reversion**
* 价差是寻找均值回归的一种常见方式
* **The two parts of the spread are called legs: Note that if we have a universe of k assets, there are**
* **价差的两个部分被称为支点:注意，如果我们有k个资产，就有**

![image-20230505150148057](D:\笔记\笔记图片\image-20230505150148057.png)

* possible pairs, e.g., for 10 assets there are 45 possible pairs
* 可能的组合，例如，对于10种资产，有45种可能的组合
* <font color=blue>这里并不难，只是一个简单的排列组合，10个取2个不考虑顺序，45种情况</font>
* In practice, trades with more that two legs exist, for example trades with three legs are not uncommon
* 在实践中，有两个以上腿的交易是存在的，例如，有三个腿的交易并不罕见。
* **Good mean-reverting spreads are typically comprised of two cointegrated time series**
* **良好的均值回归价差通常由两个协整的时间序列组成**
* Next we will next look at momentum strategies
* 接下来，我们将接着看一下动量策略



## 23 (4.7) Momentum strategies 动量策略

* **<font color=red size=5>Momentum strategies是指基于市场趋势的交易策略，即通过分析市场的历史价格走势和交易量等数据，来预测未来市场趋势并进行交易的一类策略。</font>**
* ![image-20230531150941384](D:\笔记\笔记图片\image-20230531150941384.png)

### 23.1 Two example momentum strategies

* aim to exploit continuation of a trend
* 旨在利用趋势的延续性
* mostly need to be implemented across a portfolio of markets
* 这些措施大多需要在一系列市场中实施
* often cut losers and let winners run; i.e., they will often have a (trailing) stop loss but no profit target
  经常裁掉失败者，让成功者逃跑;也就是说，他们通常会有一个(跟踪)止损，但没有盈利目标

We describe two examples of simple momentum strategies

#### 23.1.1 Example 1: Triple moving average

* This is a textbook "technical analysis" system 
* 这是一个教科书式的“技术分析”系统
* Three moving averages of price: short, medium, long 
* 价格的三个移动平均线:短、中、长
* Increasing timeframes: short < medium < long 
* 增加时间范围:短<中<长
* Trades when price movement is consistent
* 当价格变动一致时进行交易

![image-20230505161847215](D:\笔记\笔记图片\image-20230505161847215.png)

* 这句话描述了一种交易系统在哪些情况下会持平（即不持有头寸）。具体来说，当短期移动平均线（short MA）和中期移动平均线（medium MA）之间的关系不符合中期移动平均线和长期移动平均线（long MA）之间的关系时，交易系统会保持持平状态。

* <font color=red>解释一下这段话，原因如下：在技术分析中，移动平均线通常被用于识别市场趋势和确定交易信号。在一个三重移动平均线系统中，通常包括一个较短期的移动平均线（short MA）、一个较中期的移动平均线（medium MA）和一个较长期的移动平均线（long MA）。</font>

* <font color=red>在这种情况下，**短期移动平均线的变化会更加敏感，更快地反应价格变化，因此其与中期移动平均线之间的关系可以被用来捕捉短期市场趋势。**相比之下，**长期移动平均线则更加平滑，更能反映较长期的市场趋势。**因此，中期移动平均线和长期移动平均线之间的关系可以用来捕捉较长期的市场趋势。</font>

* <font color=red>如果**短期移动平均线和中期移动平均线之间的关系不符合中期移动平均线和长期移动平均线之间的关系，可能表明市场处于不稳定状态，或者交易信号不够明确，这时候交易系统可能选择保持持平状态，不做任何交易，以避免不必要的风险和损失。**</font>

  

#### 23.1.2 Example2: Relative strength

* Asset classes/ industry sectors have different relationships with the business cycle. This simple example uses 5 Exchange-Traded Funds (ETFs): 
* 该策略基于资产类别/行业部门与商业周期之间的不同关系。具体来说，这个策略选取了五个交易所交易基金（ETFs），包括：美国股票（SPY）、外国股票（EFA）、债券（BND）、房地产投资信托基金（VNQ）和大宗商品（GSG）。
* SPY - US stocks 
* EFA - Foreign stocks 
* BND - Bonds 
* VNQ - Real Estate Investment Trusts (REITs) 
* GSG - Commodities 
* **Pick 3 ETFs with strongest 12 month momentum (price change) into your portfolio and weight them equally. Rebalance once every month.**
* **在这个策略中，投资者将选择12个月动量（即价格变化）最强的三个ETF，将它们平均加权，形成一个投资组合。每个月调整一次投资组合的权重，以保持策略的有效性。**

![image-20230505163032501](D:\笔记\笔记图片\image-20230505163032501.png)

* Perhaps the main drawback of that example is that it is long-only. An alternative is to go both long and short: 
* 也许这个例子的主要缺点是它只做长线。另一个选择是同时做多和做空
  * Imagine a large universe of assets (e.g., 50 ETFs) 
  * 想象一个庞大的资产世界(例如，50只etf)
  * Go long the k with the strongest 12 month momentum (typically where the price has risen) 
  * 做多12个月动量最强的k(通常是价格上涨的时候)
  * Go short the k with the weakest 12 month momentum (typically where the price hard fallen) 
  * 做空12个月动量最弱的k(通常是价格大幅下跌的时候)
* Note that k, 12 months, the size and make up of the universe etc. are all parameters that can and will normally be carefully chosen.
* 请注意，k、12个月、宇宙的大小和组成等等都是可以而且通常会被仔细选择的参数。

<font size=5>关于做多和做空</font>

* **做多是指投资者相信市场价格将上涨，买入资产并持有，以获得价格上涨的收益。做多的目的是赚取买入价和卖出价之间的差价。**
* 例如，一名投资者认为某股票将在未来上涨，他会以当前市场价格买入该股票，随着股票价格上涨，他会在未来以更高的价格卖出股票，获得差价收益。
* **相反，做空是指投资者相信市场价格将下跌，卖出资产并持有，以获得价格下跌的收益。做空的目的是赚取卖出价和买入价之间的差价。**
* 例如，一名投资者认为某股票将在未来下跌，他会在当前市场价格卖出该股票，随着股票价格下跌，他将在未来以更低的价格买入股票，获得差价收益。



### 23.2 (Trailing) stop losses and profit targets (in the context of mean-reversion and momentum strategies)止损和盈利目标(在均值回归和动量策略的背景下)

* **Stop losses** and **profit targets** (discussed previously) provide a exit strategy based on the performance of the trade 
* 止损和盈利目标(前面讨论过)提供了一个基于交易表现的退出策略
* Often **trailing stop** loss is used: 
* A **trailing stop** measures the loss relative to the best price (high for a long trade, low for a short trade) since the trade was entered, rather than from the entry price 
* **移动止损**是指相对于交易开始后的最佳价格（多头交易的最高价，空头交易的最低价）的损失，而不是从入市价开始的损失。
* 称为**“移动止损”（trailing stop loss**）的退出策略，它会根据交易的表现情况调整止损价格。具体来说，**移动止损会以交易进入时的最佳价格（做多头寸为最高价，做空头寸为最低价）作为基准，然后以该基准价格为参照，根据交易价格的变化来不断调整止损价位，以确保止损价位与市场价格之间的距离不会过大。**
* Often (but not always) the **exits** are included as follows:
* 通常（但不总是），出口包括如下：

![image-20230505164207785](D:\笔记\笔记图片\image-20230505164207785.png)



### 23.3 Position sizing 头寸的规模

* **Position sizing** is crucial, especially when trading in multiple markets 
* **头寸规模**是至关重要的，尤其是在多个市场交易时
* We saw this is the context of spread trading, where the **<font color=red>position ratio</font>** measures the ratio of sizes for the two legs of the spread
* 我们看到这是点差交易的背景，头寸比率衡量的是两个点差的规模之比
* 头寸比例是指在资产组合中，不同头寸所占的比例。投资者可以根据自己的风险承受能力、预期收益和市场情况等因素来调整不同头寸的比例，以达到理想的风险收益平衡。

* 注意: 这里的两个腿，每一个腿指的是策略中的一个单独的交易，可以是买入或卖出某种资产或衍生品，也可以是对某种资产或衍生品进行多头或空头的交易。
* 在这里提到的两个腿，指的是套利策略中的两个交易腿，可以是同一资产或衍生品的不同合约，也可以是不同资产或衍生品之间的相关交易组合。对于跨品种套利交易，两个腿通常是不同品种的期货合约。

![image-20230505165416884](D:\笔记\笔记图片\image-20230505165416884.png)

* Warning
  * If the position sizing across multiple instruments is not carefully chosen according to expected moves in those markets, then some instruments will likely dominate the performance of the portfolio
  * 如果没有根据市场的预期走势仔细选择多个工具的头寸规模，那么一些工具可能会主导投资组合的表现

#### 23.3.1 Timeframe 时间框架

**时间框架（Timeframe）是指交易者在分析市场行情时所采用的时间尺度或周期。不同的时间框架可以用来观察市场不同的行情特征和趋势，以及不同程度的市场波动和价格波动。**

* We have touched on the issue of timeframe in terms of the lookback of moving averages: the longer the lookback, the longer the timeframe it targets 
* 我们已经在移动平均线的回顾中谈到了时间框架的问题:回顾越长，它所针对的时间框架就越长
* Clearly **timeframe is constrained by the available data**:
* 显然，**时间框架受到现有数据的限制**
  * for high-frequency trading one needs order book and tick data 
  * 对于高频交易，人们需要订单簿和价格数据
  * daily data is not sufficient to investigate intra-day strategies 
  * 每日数据不足以调查日内策略
* **Different timeframes exhibit different pheonomena.** For example, some studies show that equities exhibit momentum in the short-term and mean-reversion in the longer term. 
* **不同的时间框架表现出不同的现象。**例如，一些研究表明，股票在短期内表现出势头，而在长期内表现出均值回归
* Thus, by targeting different timeframes one may be able to employ a range of different types of trading strategy, which can be a usual form of diversification
* 因此，通过针对不同的时间框架，人们可以采用一系列不同类型的交易策略，这可能是一种常见的多样化形式

![image-20230505172314938](D:\笔记\笔记图片\image-20230505172314938.png)

## 24.(5.1) Strategy parameters 策略参数

### 24.1 Recap definition of trading strategy parameters

* For us trading strategy parameters are 
* 对我们来说，交易策略参数是
  * inputs (often numerical) required to define the strategy 
  * 定义策略所需的输入(通常是数字)
* For example: 
  * The parameters of the vanilla BBands overbought/oversold strategy we looked are: 
    * n: the size of the window of a moving average 
    * sd: the multiple of standard deviations for the Bollinger Bands
  * 以BBands策略为例，其参数包括n和sd。其中，**n是指移动平均线的窗口大小（时间长度），用于计算股价的平均值。sd是指布林带的标准偏差倍数，用于计算股价的上下限**。

![image-20230505174917064](D:\笔记\笔记图片\image-20230505174917064.png)

### 24.2 Effect of changing parameters 参数变化的影响]

* For fixed n, lower sd gives less stringent trading condition 
* 对于固定n，较低的sd给出的交易条件不那么严格
* Therefore the condition will likely be met more times so there will be more active days 
* 因此，这个条件可能会满足更多的时间，所以会有更多的活跃的日子
* Let's confirm this empirically
* 让我们用经验来证实这一点

![image-20230505175147991](D:\笔记\笔记图片\image-20230505175147991.png)

![image-20230505175201825](D:\笔记\笔记图片\image-20230505175201825.png)

![image-20230505175212547](D:\笔记\笔记图片\image-20230505175212547.png)

* This confirms that a lower sd results in more trades 
* 这证实了较低的sd会导致更多的交易
* This is a logical consequence of the strategy definition 
* 这是战略定义的逻辑结果
* We would find the same thing for other values of n
* 对于其他n值，我们也会得到同样的结果

![image-20230505175412834](D:\笔记\笔记图片\image-20230505175412834.png)

![image-20230505175426557](D:\笔记\笔记图片\image-20230505175426557.png)

* apply applies a function over an array (here params) 

* Apply在数组上应用函数(这里是params)

* second argument says: work over the rows of params, i.e., execute for each i: 

  run(prices,params[i,"n"],params[i,"sd"])

* 第二个参数说:遍历参数行

![image-20230505175605715](D:\笔记\笔记图片\image-20230505175605715.png)

![image-20230505175619000](D:\笔记\笔记图片\image-20230505175619000.png)

### 24.3 Best result

* Question: How representative are the best parameters? 
* 问题:最佳参数的代表性如何?
* We will return to this issue when we discuss backtesting and parameter optimization
* 当我们讨论回测和参数优化时，我们会回到这个问题

![image-20230505175719068](D:\笔记\笔记图片\image-20230505175719068.png)

### 24.4 Selecting parameters 选择参数

![image-20230505175811897](D:\笔记\笔记图片\image-20230505175811897.png)

*  Trading strategies are typically parameterized 
* 交易策略通常是参数化的
* How should one choose which parameter values to use? 
* 应该如何选择要使用的参数值?
* Typically parameter optimization is used
* 通常使用参数优化

* **Pick parameter values that are likely to produce good results in the future**. In the terminology of machine learning, we want a model (strategy) that will generalise (to the future).
* 选择将来可能产生良好结果的参数值。用机器学习的术语来说，我们想要一个泛化的模型(策略)。



## 25. （5.2） Counting parameter combinations

### 25.1  Counting parameter combinations 计数参数组合

![image-20230505181427778](D:\笔记\笔记图片\image-20230505181427778.png)

![image-20230505181500218](D:\笔记\笔记图片\image-20230505181500218.png)

![image-20230505181517317](D:\笔记\笔记图片\image-20230505181517317.png)

* Now we have the product of three cardinalities
* 现在我们有了三个基数的乘积

![image-20230505181547786](D:\笔记\笔记图片\image-20230505181547786.png)

* The total number of parameter combinations grows exponentially with the number of parameters
* 参数组合的总数随着参数的数量呈指数增长

![image-20230505181623802](D:\笔记\笔记图片\image-20230505181623802.png)

## 26 (5.3) Parameter optimization

### 26.1 Optimization criteria (aka fitness functions)

#### 26.1.1 What do we optimize?

* An **optimization criterion**, also known as a **fitness function**: 
* 一种优化准则，也称为适应度函数
  * **Maps trading results to fitness (usually a single number)** 
  * **将交易结果映射到适合度(通常是单个数字)**
  * **Higher fitness means better trading strategy results** 
  * **更高的适应度意味着更好的交易策略结果**
  * 需要注意的是，适应度函数的设计需要充分考虑策略的实际应用场景和优化目标，避免出现过拟合和过度优化的情况。同时，为了避免选择的参数组合在未来表现不佳，还需要使用一些**验证集**和**交叉验证**等技术来评估策略的**泛化**能力和**稳定性**。
* The simplest fitness functions are just **profit** or **return**; normally one would incorporate risk too, e.g., via the Sharpe ratio Other components that one might include are, for example: 
* 最简单的适应度函数只是利润或回报;通常也会考虑风险，例如，通过夏普比率。其他可能包括的因素有:
  * number of trades; or the 
  * 行业数量;或者是
  * balance between the number of long and short trades
  * 在多头和空头交易的数量之间保持平衡
*  (the challenge is then how to weight these components)
* (接下来的挑战是如何衡量这些组件的权重)

![image-20230505185248141](D:\笔记\笔记图片\image-20230505185248141.png)





### 26.2 Optimization of parameter combinations by grid search (brute force)

#### 26.2.1 Grid search 网格搜索

* **Grid search (exhaustive, or brute force)**, i.e., we define allowable parameter values for each parameter individually, and then look at all combinations 
* **网格搜索(穷举搜索，或蛮力搜索)**，即，**<font color=red>我们为每个参数单独定义允许的参数值，然后查看所有组合</font>**
* For a grid search we must specify **parameter ranges** for each parameter individually 
* 对于网格搜索，我们必须为每个参数单独指定参数范围
* We focus on **regularly-spaced sequences** as returned by the seq function in R, so we ultimately need to decide on: 
* 我们关注的是R中的seq函数返回的正则间隔序列，因此我们最终需要决定:
* Endpoints (the from and to arguments to seq) 
* 端点(seq的from和to参数)
* Increments (either via the by or length.out argument to seq)
* 增量(通过by或length)。输出参数到seq)

![image-20230505191649081](D:\笔记\笔记图片\image-20230505191649081.png)

* Some parameters have natural upper or lower bounds, e.g. The size of a moving average window is
* 有些参数有自然的上限或下限
  *  lower bounded by 0 
  * 下界为0
  * upper bounded by the length of historical data available 
  * 可用历史数据长度的上限
* Beyond some value a parameter may not effect trading results 
* 超过某个值，参数可能不会影响交易结果
  * multiple of standard deviation for BBands
  * b波段标准差的倍数

![image-20230505192621923](D:\笔记\笔记图片\image-20230505192621923.png)

#### 26.2.2 Heuristic for picking increments 选取增量的启发式方法

* Suppose you have already decided **endpoints**
* 假设您已经确定了**端点**
  * 1. Estimate backtest time for one parameter combination 
    2. 估计一个参数组合的回测时间
  * 2. Based on how long you have to run the backtest determine the number of parameter combinations to test 
    2. 根据运行回测的时间长短，确定要测试的参数组合的数量
  * 3. Test the same number of parameter values for each parameter to achieve a total close to the target
    4. 对每个参数测试相同数量的参数值，以达到接近目标的总数

![image-20230505213539056](D:\笔记\笔记图片\image-20230505213539056.png)

![image-20230505213734347](D:\笔记\笔记图片\image-20230505213734347.png)

* Use 2x2x2=8 combinations of endpoints to **estimate iteration time**
* 使用2x2x2=8个端点组合来**估计迭代时间**
* Suppose this indicates average iteration time is 20 seconds
* Target time for backtest 8 hours

![image-20230505213805569](D:\笔记\笔记图片\image-20230505213805569.png)

![image-20230505214222058](D:\笔记\笔记图片\image-20230505214222058.png)

#### 26.2.3 Grid Search

* Evaluate all parameter combinations 
* 计算所有参数组合
* For two parameters this is a 2d grid, in general a hypergrid 
* 对于两个参数，这是一个二维网格，通常是一个超网格
* With n parameters, a k-fold increase in number of parameter values for each results in a k^n-fold increase in the number of parameter combinations
* 对于n个参数，每个参数值的数量增加k倍会导致参数组合的数量增加k^n倍

![image-20230505214704470](D:\笔记\笔记图片\image-20230505214704470.png)

##### 26.2.3.1 Iterative approach 迭代渐进法

* Start with a coarse grid 
* 从一个粗糙的网格开始
* Pick promising region and repeat with corresponding smaller ranges and finer increments
* 选择有希望的区域，以相应的较小范围和较小的增量重复

![image-20230505214756137](D:\笔记\笔记图片\image-20230505214756137.png)

* For 2 parameters we can easily visualize the **fitness landscape** with fitness represented by colours over a 2d grid:
* 对于2个参数，我们可以很容易地将适应度景观可视化，适应度由2d网格上的颜色表示:

![image-20230505214918536](D:\笔记\笔记图片\image-20230505214918536.png)





### 26.3 Other optimization methods

* We mention, without going in to details, other methods you should be aware of. All are **gradient-free**, **black-box optimizers**:
* 我们将提及，但不涉及细节，您应该注意的其他方法。所有这些都是无梯度的黑盒优化器:
  * Local-search based methods: **simulated annealing**; **tabu search** (short-term memory prevents cycling); 
  * 基于局部搜索的方法：**模拟退火**、**禁忌搜索**等。这些方法通过对参数空间进行搜索，并根据某种准则对参数进行调整，以寻找最优解
  * Population-based methods: **particle swarm optimization**; **ant colony optimization**; **genetic algorithms** (the first 3 are all bio inspired); differential evolution 
  * 基于群体智能的方法：粒子群优化、蚁群算法、遗传算法等。这些方法模仿生物种群的行为和智能，通过群体的协作来搜索最优解。
  * Bayesian optimization (trades off exploitation and exploration)
  * 贝叶斯优化：通过构建参数的后验概率分布来优化参数。这种方法将参数优化问题看作是一个黑盒函数，通过不断探索参数空间来更新参数分布，并选择最有可能产生最优结果的参数组合。

![image-20230505215017127](D:\笔记\笔记图片\image-20230505215017127.png)



## 27 （5.4）Cross-validation 交叉验证

### 27.1 What is cross-validation? 什么是交叉验证

* What can we try to do to ensure our results are robust? Central question: How will a strategy perform in the future?
* 我们可以尝试做些什么来确保我们的结果是可靠的?核心问题:战略在未来的表现如何?
  * In statistics, cross-validation checks: How does a trained model generalize to an unseen data set?
  * 在统计学中，交叉验证检查:一个训练好的模型如何推广到一个未知的数据集
  * In our context of trading strategies, we want to know: how well will our strategy perform in the future?
  * 在我们的交易策略的背景下，我们想知道:我们的策略在未来的表现如何?
  * Thus we testing optimized strategy's on unseen, future data.
  * 因此，我们在看不见的未来数据上测试优化策略
  * Cross-validation mitigates the risk of data-snooping bias, which we discuss later
  * 交叉验证降低了数据窥探偏差的风险，我们将在后面讨论这个问题



#### 27.1.1 In-sample, out-of-sample test 样本内和样本外检验

![image-20230505235342815](D:\笔记\笔记图片\image-20230505235342815.png)

* Means one round of cross validation. Involves partitioning a sample of data into complementary subsets:
* 意味着一轮交叉验证。包括将数据样本划分为互补子集
  * optimize on one subset (the training set/in-sample set) 
  * 对一个子集(训练集/样本集)进行优化
  * validate on the other (the test set/out-of sample set)
  * 在另一个(测试集/样本外集)上验证



* **<font size=5>Protects against over-fitting</font>** 
* **<font size=5>防止过度拟合</font>**
* **Useful indicator of future performance**
* **未来表现的有用指标**

![image-20230505235805103](D:\笔记\笔记图片\image-20230505235805103.png)

![image-20230505235819026](D:\笔记\笔记图片\image-20230505235819026.png)

* Subset of endpoints above (and consecutive ones differ by ~120 for 6 months and ~250 for a year, which is roughly the number of trading days in a year)
* 上述端点的子集(连续的端点6个月相差约120，一年相差约250，这大致是一年中交易日的数量)

* For simplicity we are going to use do a backtest with no slippage It will use a simple rule using BBands that we have seen before
* 为了简单起见，我们将使用无滑动的回测，它将使用我们之前见过的使用bband的简单规则

![image-20230505235930739](D:\笔记\笔记图片\image-20230505235930739.png)

![image-20230506000242800](D:\笔记\笔记图片\image-20230506000242800.png)

![image-20230506000258450](D:\笔记\笔记图片\image-20230506000258450.png)

![image-20230506000445269](D:\笔记\笔记图片\image-20230506000445269.png)

![image-20230506000459332](D:\笔记\笔记图片\image-20230506000459332.png)

![image-20230506000509796](D:\笔记\笔记图片\image-20230506000509796.png)

![image-20230506000536140](D:\笔记\笔记图片\image-20230506000536140.png)

* **Degradation in performance** out of sample is common
* 许多交易策略在样本外的表现往往会下降，即使在样本内表现得很好。这是因为在样本内优化参数时可能过度拟合了数据，导致模型在未见过的数据上的表现不佳。因此，我们需要小心地处理样本内和样本外的性能表现，并采用适当的技术来避免过度拟合。



#### 27.1.2 Summary

* One round of cross-validation (in the next set of slides we will look at multiple rounds via walkforward schemes) comprises:
* 一轮交叉验证(在下一组幻灯片中，我们将通过前移方案查看多轮交叉验证)包括:
* In-sample optimization  样本内优化
  * Investigate fitness landscape e.g. via a grid search 
  * 通过网格搜索等方法来研究适应度函数的“景观”，以确定在哪些参数范围内可以获得更好的性能。
  * Choose parameters
  * 选择参数

* Out-of-sample testing
  * Apply chosen parameters to unseen data 
  * 将选择的参数应用于不可见的数据
  * Evaluate results
  * 评价结果

![image-20230506001054731](D:\笔记\笔记图片\image-20230506001054731.png)



### 27.2 Choosing parameters based on in-sample results

* It's not always sensible to just pick the best in-sample paramters 
* 只选择最佳样本内参数并不总是明智的
* It **normally makes sense to look at the fitness landscape more holistically** 
* 在更多情况下，更全面的看待fitness landscape是更全面的
* To illustrate we next look at an example (with a different 2-parameter strategy) and compare the in-sample and out-of-sample fitness landscapes 
* 为了说明这一点，我们接下来看一个例子(使用不同的2参数策略)，并比较样本内和样本外适应度景观
* Our goal is to **pick parameters that do well out-of-sample, but only knowing the in-sample results** 
* 我们的目标是**选择在样本外表现良好的参数，但只知道样本内结果**
* This is exactly what we try to do when we actually deploy a trading strategy
* 这正是我们在实际部署交易策略时所要做的

![image-20230506001612175](D:\笔记\笔记图片\image-20230506001612175.png)

* **RSI stands for Relative Strength Index** 
* **RSI代表相对强度指数**
* RSI is a standard indicator, implemented in the TTR package; you do not need to know its definition 
* RSI是一个标准指标，在TTR软件包中实现；你不需要知道其定义。
* **<font color=red>It takes values between 0 and 100, and higher (lower) values indicate that the market has recently been rising (falling) </font>**
* **<font color=red>它的取值范围在0到100之间，较高(较低)的值表明市场最近一直在上涨(下跌)。</font>**
* Let's look at an example mean-reversion strategy, like the one we have already seen that used Bollinger band, but using the RSI indicator
* 让我们看一个均值回归策略的例子，就像我们已经看到的那样，使用布林带，但使用RSI指标

![image-20230506001623024](D:\笔记\笔记图片\image-20230506001623024.png)

![image-20230506001847422](D:\笔记\笔记图片\image-20230506001847422.png)

![image-20230506001856920](D:\笔记\笔记图片\image-20230506001856920.png)

![image-20230506001905451](D:\笔记\笔记图片\image-20230506001905451.png)

![image-20230506001915853](D:\笔记\笔记图片\image-20230506001915853.png)

* Not always easy to pick parameters from in-sample results 
* 从样本内结果中选择参数并不总是容易的
* **Dataset drift** can cause the good parameter combination to differ between in-sample and out-of sample periods
* 数据集漂移会导致良好的参数组合在样本内和样本外周期之间存在差异
* **关于数据漂移**：
* **数据漂移**指的是模型在生产环境中应用时，模型的表现可能会因为环境和数据的变化而发生变化。在投资中，数据漂移的例子包括市场和经济条件的变化，以及政策和监管环境的改变等。这些变化可能导致在样本内（in-sample）表现良好的参数组合在样本外（out-of-sample）表现不佳，从而使策略的实际表现与预期不符。因此，我们需要时刻关注数据漂移的情况，以避免由此导致的策略失败。



## 28 (5.5) Walkforward schemes

* **前向验证**是一种回溯测试技术，包括将历史数据分成小块，或称 "前进期"，并在每个时期测试策略。这个想法是为了模拟现场交易的过程，在这个过程中，策略会根据新的市场数据不断地调整和更新。
* 在前行方案中，策略在第一块数据（"样本内 "时期）上进行训练，然后在下一块数据（"样本外 "时期）上测试。这个过程在随后的每个时期重复进行，策略在新的样本内数据上重新训练，在新的样本外数据上测试。

### 28.1 Walk-forward analysis

* If we use a single in-sample and out-of-sample periods, results will have an extreme dependence of the chosen periods 
* 如果我们使用单个样本内和样本外周期，结果将对所选周期有极大的依赖性
* A walk-forward scheme is a rolling implementation of 
* 向**前向验证**是滚动实现的
  * In-sample optimization 
  * 样本内优化
  * Out-of-sample testing 
  * 样本外优化
* Protects against the possibility for one round cross-validation that by chance we chose some input parameters that did well in both in and out-of-sample sets 
* 防止一轮交叉验证的可能性，即我们偶然选择了一些在样本内和样本外集都表现良好的输入参数
* Also allows more adaptability: each out sample-period can use a different set of parameters
* 也允许更多的适应性:每个外采样周期可以使用一组不同的参数

![image-20230506002647994](D:\笔记\笔记图片\image-20230506002647994.png)

![image-20230506003046454](D:\笔记\笔记图片\image-20230506003046454.png)

![image-20230506003058020](D:\笔记\笔记图片\image-20230506003058020.png)

![image-20230506003107731](D:\笔记\笔记图片\image-20230506003107731.png)

![image-20230506003118801](D:\笔记\笔记图片\image-20230506003118801.png)

### 28.2 Implementation

* In that last example, we took equal in and out of sample periods of one year 
* 在上一个例子中，我们取了相同的1年样本周期
* **In and out sample periods are actually parameters** 
* **输入和输出采样周期实际上是参数**
* We need to **validate our choices of these parameters** and a common approach is to 
* 我们需要**验证这些参数的选择**，常用的方法是
* 1. Develop and optimize walk forward scheme on training set
  2. 在训练集上开发和优化步进方案 
  3. Validate the scheme on a test set 
  4. 在测试集上验证方案
* (I.e., do one round of cross validation on our rolling cross validation scheme)
* (例如，对我们的滚动交叉验证方案进行一轮交叉验证)



## 29 （5.6）Biases 偏差

* Recap on Look-ahead Bias 前视偏差
* Discussion of 
  * Survivorship Bias  生存偏差
  * Data-snooping Bias  数据窥探偏差
  * Time period Bias 时间区间偏差



### 29.1 Biases 偏差

* There are a number of common biases that can arise when using historic data for trading strategy development. They usually bias results upwards 
* 在使用历史数据进行交易策略开发时，会出现一些常见的偏差。它们通常会使结果向上偏移 
* We discuss briefly several such biases. We already mentioned the first, **<font color=red>look-ahead bias</font>**, **where the backtest uses information that would not be available when a trading decision is made.** E.g.: 
* 我们简单讨论一下这种偏差的几种情况。我们已经提到了第一种，即前瞻偏差，即回测使用的信息在做出交易决定时是不存在的。如：： 
  * moving average calculation uses the close price on Monday when it make a trading decision at the open on Monday: available when it is not. 
  * 移动平均线计算使用周一的收盘价，当它在周一开盘时做出交易决定：当它不在时可用。
  * strategy uses annual earnings data to place trades in January, even though the earnings data is not available until March
  * 该策略使用年度收益数据在1月份进行交易，尽管收益数据要到3月份才能获得

![image-20230506004116045](D:\笔记\笔记图片\image-20230506004116045.png)

#### 29.1.1 Survivorship bias 幸存者偏差

* Survivorship bias occurs when backtests are conducted on datasets that excludes data for companies/funds etc. that no longer exist (e.g. due to bankruptcy) 
* 当在数据集上进行回测时，不包括不再存在的公司/基金等的数据，就会出现生存偏差。等已经不存在的公司/基金的数据（例如，由于破产）。
* **Such backtests are likely to have upwardly biased results**, since the surviving entities will tend to have performed better than those that no longer exist 
* 这类回测的结果很可能是向上偏倚的，因为幸存的实体往往比那些不再存在的实体表现得更好
* Example 1: mutual fund databases only contain funds that are currently in existence. Generally, funds that have ceased to exist have lower returns relative to surviving funds, and thus the average mutual fund return will be overestimated 
* 例1:共同基金数据库只包含当前存在的基金。一般来说，已不复存在的基金相对于幸存的基金的回报率较低，因此共同基金的平均回报率将被高估
* Example 2: data for stocks listed on an exchange will be subject to survivorship bias as delisted companies often have poor performance
* 例2:在交易所上市的股票的数据将受到生存偏差的影响，因为退市的公司往往表现不佳

![image-20230506005349280](D:\笔记\笔记图片\image-20230506005349280.png)

#### 29.1.2 Data-snooping bias 数据窥探偏差

* **Data-snooping bias can occur when data is used more than once to develop a model (by trial and error)**
* **当多次使用数据来开发模型(通过反复试验)时，可能会出现数据窥探偏差。**
* It is particularly problematic for trading strategy development due to **widespread use of the same datasets** - is difficult to avoid in trading strategy design because **historical data is, by definition, limited**
* 由于广泛使用相同的数据集，这在交易策略开发中尤其成问题——在交易策略设计中很难避免，因为历史数据根据定义是有限的
*  It is not surprising that models that appear to do well historically can be found by exhaustive/extensive search 
* 历史上表现良好的模型可以通过详尽/广泛的搜索找到，这并不奇怪
* Cross-validation (discussed earlier) can help to avoid data-snooping bias. 
* 交叉验证(前面讨论过)可以帮助避免数据窥探偏见
* Having strategies that make intuitive sense can also protect against data-snooping bias and overfitting
* 拥有具有直觉意义的策略也可以防止数据窥探偏见和过度拟合

#### 29.1.3 Time period bias 时间段偏差

* **Time period bias occurs when a test design is based on a time period that may make the results time-period specific** 
* **当测试设计基于可能使结果特定于时间段的时间段时，就会出现时间段偏差**
* For example, a strategy may be very biased to go long, and then would have excellent performance during a bull market (period of rising prices), but would perform poorly during a bear market (period of falling prices) 
* 例如，一种策略可能非常偏向于做多，然后在牛市(价格上涨期间)表现出色，但在熊市(价格下跌期间)表现不佳。
* Thus it is desirable that the test period contains **different types of market conditions**. However, if the time period is too long, the fundamental market structure may have changed during the time frame, resulting in two data sets that reflect different relationships
* 因此，测试期间应包含不同类型的市场情况。然而，如果时间周期太长，基本市场结构可能在时间框架内发生变化，导致两个反映不同关系的数据集

#### 29.1.4 





















