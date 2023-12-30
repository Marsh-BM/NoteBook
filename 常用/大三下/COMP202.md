# COMP202

## 1. Introductory Lectures

### 1.1 What is an algorithm?

* For computational algorithms, we use **data structures to store, access, and manipulate data.**
* 对于计算算法，我们使用数据结构来存储、访问和操作数据。
* What data structures have you encountered in the past?
* 您过去遇到过哪些数据结构?

#### 1.1.1 Algorithm Analysis

* **Primary interest:** Running time (time-complexity) of the algorithm and the operations on data structures.
* 主要的关注点是运行时间，即时间复杂度，以及算法的运行结构
* **Secondary interest**: Space (or “memory”) usage(**space-complexity**).
* 次要兴趣:空间(或“内存”)使用 (空间复杂性)。
* **Also of interest: (Near)** Optimality of the output solution (for optimisation problems).
* 同样有趣的是:(接近)输出解的最优性

##### 1.1.1.1 Experimental Analysis of Algorithms 算法实验分析

* We are interested in dependency of the running time on size of the input.
* 我们感兴趣的是运行时间对输入大小的依赖关系。
* <font color=red>要求的是运行时间和输入大小的依赖关系</font>

![image-20230204150126491](D:\笔记\笔记图片\image-20230204150126491.png)

* 为了分析算法，我们可以通过实验来观察算法的运行时间。

![image-20230204150253772](D:\笔记\笔记图片\image-20230204150253772.png)

* 此外，**运行时间取决于输入的大小和实例、所使用的算法，以及运行它的软件和硬件环境。**



###### 1.1.1.1.1 Drawbacks of Experimental Analysis

* Experiments are performed on a limited set of test inputs.
* 实验是在有限的测试输入集上进行的。
* Requires all tests to be performed using same hardware and software.
* 要求使用相同的硬件和软件执行所有测试。
* Requires implementation and execution of algorithm.
* 需要算法的实现和执行。

##### 1.1.1.2 Theoretical Analysis 理论分析

<font size=5>理论分析的好处</font>

* Can take **all possible inputs** into account.
* 能考虑所有可能的输入。
* Can compare efficiency of two (or more) algorithms, **independent of hardware/software environment.**
* 可以比较两种(或更多)算法的效率，与硬件/软件环境无关。
* Involves studying high-level descriptions of algorithms **(e.g. pseudo-code).**
* 涉及学习算法的高级描述(例如:伪代码)。



* When we analyse an algorithm in this fashion **we aim to associate a function f (n) to each algorithm**, where f (n) characterizes the running-time in terms of some measure of the input-size, n. (For example, n could be the number of items to be sorted in a list.)
* 当我们以这种方式分析算法时，**我们的目标是将函数f (n)与每个算法关联起来**，其中f (n)用输入大小n的某种度量来描述运行时间(例如，n可以是列表中要排序的项的数量)。

![image-20230204152609297](D:\笔记\笔记图片\image-20230204152609297.png)

<font size=5>理论分析的需求</font>

* A language to describe algorithms.
* 一种描述算法的语言。
* Computational model in which algorithms are executed.
* 执行算法的计算模型。
* Metric for measuring running-time.
* 用于测量运行时间的度量
* A way of characterizing running-time.
* 一种描述运行时间的方法。



#### 1.1.2 Pseudo-Code 伪代码

* **Pseudo-code is a high-level description language for algorithms.**
* **伪代码是一种高级算法描述语言。**

* Pseudo-code provides more structured description of algorithms.
* 伪代码提供了更结构化的算法描述。
* Allows high-level analysis of algorithms to determine their running time (and space requirements).
* 允许对算法进行高级分析，以确定它们的运行时间(和空间需求)。

![image-20230204154423002](D:\笔记\笔记图片\image-20230204154423002.png)



* Pseudo-code is a mixture of natural language and high-level programming language (e.g., Java, Python, C,etc.).
* 伪代码是自然语言和高级编程语言(如Java、Python、C等)的混合。

![image-20230204154708387](D:\笔记\笔记图片\image-20230204154708387.png)



#### 1.1.3 Computational Model 计算模型

* **Our computational model is like that typically found on modern-day computers.**
* **我们的计算模型类似于现代计算机上的典型模型。**
  * CPU connected to a bank of memory cells.
  * CPU连接到一组内存单元。
  * Each memory cell can store a number, character, or address.
  * 每个存储单元可以存储一个数字、字符或地址。
* We use a set of high-level primitive operations: assignment, method invocation, arithmetic operations, comparison of numbers, array indexing, returning from a method, etc.
* 我们使用一组高级原语操作:赋值、方法调用、算术操作、数字比较、数组索引、从方法返回等。

##### 1.1.3.1 primitive operations 原始操作

* **Assumption: <font color=red>primitive operations</font> (like a single addition, multiplication, or comparison) require constant time to perform.**
* **假设:基本操作(如单个加法、乘法或比较)需要常数时间来执行。**
* (Not necessarily true, e.g. on modern processors, multiplication generally takes about three to four times as long to perform on a computer than addition. Division typically takes at least twice as long as multiplication.)
* (不一定，例如，在现代处理器上，计算机上执行乘法的时间通常是加法的三到四倍。除法的时间通常至少是乘法的两倍。)
* **Average-case complexity** refers to running time as an average taken over all inputs of the same size.
* 平均复杂度指的是运行时间是相同大小的所有输入的平均值
* **平均复杂度是在算法的所有可能的输入情况下，算法的平均复杂度。**
*  **Worst-case complexity** refers to running time as the maximum taken over all inputs of the same size.
* 最坏情况复杂度指的是运行时间是所有相同大小的输入所占用的最大时间。
* 

![image-20230204155158202](D:\笔记\笔记图片\image-20230204155158202.png)

![image-20230204155725713](D:\笔记\笔记图片\image-20230204155725713.png)



* for循环中的i算一个**length[A]-1**, 比较元素算一个Compare  **lengA[j]-1**， min<-A[j]再算一个**lengA[j]-1**
* 另外的两个是**min <- A[1]**, 因为在索引值中寻找，所以算一个

#### 1.1.4 Average- vs. Worst-Case Complexity

* An algorithm may run faster on some inputs compared to others.
* 算法在某些输入上可能比其他输入运行得更快。
  * **Average-case complexity refers to running time as an average taken over all inputs of the same size.**
  * **平均复杂度指的是运行时间是相同大小的所有输入的平均值。**
  * **平均复杂度是在算法的所有可能的输入情况下，算法的平均复杂度。**
  * **Worst-case complexity refers to running time as the maximum taken over all inputs of the same size.**
  * **最坏情况复杂度指的是运行时间是所有相同大小的输入所占用的最大时间。**
* Usually, we’re most interested in worst-case complexity.

![image-20230204161155256](D:\笔记\笔记图片\image-20230204161155256.png)

#### 1.1.5 Asymptotic notation 渐进表示法

* **<font color=red>Asymptotic notation</font> allows characterization of the main factors affecting running time.**
* **渐近表示法允许描述影响运行时间的主要因素。**
* **Used in a simplified analysis that estimates the number of primitive operations executed up to a constant factor.**
* **用于估计执行的基本操作的数量直到一个常数因子的简化分析。**
* Such notation lets us compare the running times of two algorithms.
* 这样的符号可以让我们比较两种算法的运行时间。

##### 1.1.5.1 “Big-Oh” Notation (用于表示算法上界，即最坏的时间复杂度)

* “Big-Oh” notation is probably the most commonly used form of asymptotic notation.
* “Big-Oh”符号可能是最常用的渐近符号形式。
* **Given two positive functions f (n) and g(n) (defined on the nonnegative integers), we say f (n) is O(g(n)), written f (n) ∈O(g(n)), if there are constants c and n0 such that:**
* **给定两个正函数f (n)和g(n)(定义在非负整数上)，我们说f (n)是O(g(n))，写成f (n)∈O(g(n))，如果存在常数c和n0，使:**

![image-20230204161831488](D:\笔记\笔记图片\image-20230204161831488.png)

![image-20230204161918056](D:\笔记\笔记图片\image-20230204161918056.png)

* <font color=red>也就是说g(n)是f(n)的上界，用于对f（n）的增长趋势做出限制</font>



* Need to find constants c and n0 such that: 7n −4 ≤c n, for all n ≥n0.
* 需要找到常数c和n0，使7n−4≤c n，对于所有n≥n0。
* One possible choice is c = 7 and n0 = 1.
* 一个可能的选择是c = 7和n0 = 1。
* **I In fact, this is just one of infinitely many choices, because any real number c ≥7 and any integer n0≥1 would be OK.**
* **事实上，这只是无穷多个选项中的一个，因为任何实数c≥7和任何整数n0≥1都是好的。**

![image-20230204162238602](D:\笔记\笔记图片\image-20230204162238602.png)

![image-20230204183013416](D:\笔记\笔记图片\image-20230204183013416.png)

* <font color=red>下面的这个很重要！！！</font>

![image-20230516170316161](D:\笔记\笔记图片\image-20230516170316161.png)

![image-20230204183021094](D:\笔记\笔记图片\image-20230204183021094.png)

![image-20230516171150950](D:\笔记\笔记图片\image-20230516171150950.png)



###### 1.1.5.1.1 O(n) and Ω(n) , Θ(n)

<font size=5>O(n)</font>

* **O(n) is a mathematical notation used in computational complexity theory to describe an upper bound of the growth rate of an algorithm's time complexity.** It gives the maximum amount of time an algorithm could take to complete for a given size of input.
* **O(n)是计算复杂度理论中用于描述算法时间复杂度增长速度的上限的数学符号。**它给出了对于给定大小的输入，算法完成所需要的最大时间。
* **<font color=red>常见的时间复杂度的增长</font>**
* ![image-20230205163246311](D:\笔记\笔记图片\image-20230205163246311.png)

![image-20230205163435769](D:\笔记\笔记图片\image-20230205163435769.png)

<font size=5>Ω(n)</font> **最优情况**

* **Ω(n) represents the lower bound of an algorithm's time complexity,** meaning it gives the minimum amount of time an algorithm could take to complete.
* **Ω(n)表示算法时间复杂度的下界**，这意味着它给出了算法完成所需的最小时间。

![image-20230205163352574](D:\笔记\笔记图片\image-20230205163352574.png)

![image-20230516171440020](D:\笔记\笔记图片\image-20230516171440020.png)



<font size=5>Θ(n)</font>

* Θ(n) represents the tight bound of an algorithm's time complexity, **meaning it gives both the lower and upper bounds of the time an algorithm could take to complete** and is used to describe algorithms that are within a constant factor of the best possible running time.
* Θ(n)表示算法时间复杂度的严格边界，**这意味着它给出了算法完成所需时间的下限和上限**，用于描述在最佳可能运行时间的常数因子内的算法。

![image-20230205163655854](D:\笔记\笔记图片\image-20230205163655854.png)

![image-20230516171650618](D:\笔记\笔记图片\image-20230516171650618.png)

![image-20230205163806172](D:\笔记\笔记图片\image-20230205163806172.png)

![image-20230205164056193](D:\笔记\笔记图片\image-20230205164056193.png)



#### 1.1.6 Optimisation Example: Online Algorithms 优化示例:在线算法

* Optimisation problem: for a given instance the objective is to find a solution that optimises (min or max) a given objective function.
* 优化问题:对于给定实例，目标是找到优化给定目标函数(最小或最大)的解决方案。
* Consider a real-life problem of **Renter’s dilemma:**
* 想想现实生活中的租房者困境:
* **通过使用时间，来计算出是买一间房子还租一间房子那个省钱。**
* Alice wants to try out a streaming music service to listen to some songs by The Beet Less.
* 爱丽丝想试试流媒体音乐服务，听听The Beet Less的几首歌。
* Each time she streams a song, it costs x pounds to “rent” the song (replying without paying is not allowed).
* 她每播放一首歌，就要花x英镑来“租”这首歌(不付费回复是不允许的)。
* Suppose it costs y pounds to buy all the songs on the new The Beet Less album, and let y = 10 ·x
* 假设购买新专辑the Beet Less中的所有歌曲需要花费y英镑，设y = 10·x
* Dilemma: Decide when to buy the whole album instead of streaming songs one at a time?
* 困境:决定什么时候买整张专辑，而不是一次只买一首歌?

![image-20230205173011203](D:\笔记\笔记图片\image-20230205173011203.png)

* Online Algorithm A responds to a sequence of service requests, each associated with cost.
* 在线算法A响应一系列服务请求，每个请求都与成本相关。
  * **Online setting: Requests arrive sequentially one-by-one and upon arrival of a request, A must completely finish serving that request, before it receives the next request.**
  * **在线设置:请求按顺序一个接一个到达，当一个请求到达时，a必须在接收下一个请求之前完全完成该请求的服务。**
  * **Offline setting: The offline algorithm is given the entire sequence of requests in advance.**
  * **脱机设置:脱机算法提前给出整个请求序列。**

![image-20230205173153798](D:\笔记\笔记图片\image-20230205173153798.png)

##### 1.1.6.1 Online Algorithms: Competitive Analysis 竞争分析

* **Competitive analysis: Compare a given online algorithm A to an optimal offline algorithm, OPT .**
* **竞争分析:将给定的在线算法a与最优离线算法OPT进行比较。**
* **OPT指的是最优离线算法**
* Given a sequence R = (r1,r2,...,rn) of service requests, let cost (A,R) denote the cost of A on R, and cost (OPT ,R) denote the cost of OPT on R.
* 给定一个服务请求序列R = (r1,r2，…，rn)，设cost (a,R)表示a在R上的代价，cost (OPT,R)表示OPT在R上的代价。
* **<font size=5>Algorithm A is c-competitive, for some c ≥1, for R if cost (A,R) ≤c ·cost (OPT ,R) + b,</font>**         
* **算法A具有c竞争性，当c≥1时，对于R，如果cost (A,R)≤c·cost (OPT,R) + b，**
*  ![image-20230205173343982](D:\笔记\笔记图片\image-20230205173343982.png)                   
  * for some constant b >0.
  * 对于某个常数b> 0。
* **If A is c-competitive for every sequence R, then we say that A is c-competitive, c is competitive ratio (if b = 0, then A is strictly c-competitive).**
* **如果A对于每个序列R都是c竞争性的，那么我们说A是c竞争性的，<font color=red>c是竞争比率</font>(如果b = 0，那么A是<font color=red>严格c竞争性</font>的)。**
* <font color=blue>就是</font>



<font size=5>Example</font>

![image-20230205173942062](D:\笔记\笔记图片\image-20230205173942062.png)

![image-20230205173949043](D:\笔记\笔记图片\image-20230205173949043.png)

![image-20230205174006046](D:\笔记\笔记图片\image-20230205174006046.png)

* **<font color=red>仔细看这个图解，c就是A与OPT之间比例关系</font>**
* 最坏的情况就是买了10首歌之后还要把专辑买下来。





#### 1.1.7 NP-Completeness

NP问题

#### 1.1.8 Simple Justification Techniques

##### 1.1.8.1 Proof by mathematical induction 数学归纳法

![image-20230206212904623](D:\笔记\笔记图片\image-20230206212904623.png)

* **<font color=red>数学归纳法（Mathematical Induction）</font>**是一种证明数学命题的常用方法。它通常用于证明关于自然数集（通常从0或1开始）的命题，包括等式、不等式、递归定义、性质等。
* 数学归纳法的基本思想是通过两个步骤来证明命题：
  1. **基础步骤（Base Case）**：首先证明当n等于某个特定值（通常是最小的自然数）时，命题成立。这是数学归纳法的起点。
  2. **归纳步骤（Inductive Step）**：假设当n等于k时，命题成立（归纳假设）。然后，通过基于归纳假设的推理，证明当n等于k+1时，命题也成立。这个步骤用来建立命题在后续自然数上的递推性。
* 通过基础步骤和归纳步骤的结合，可以得出结论：命题对于所有符合条件的自然数n都成立。
* 数学归纳法的关键是确保基础步骤成立，并且在归纳步骤中能够正确地应用归纳假设。这样，我们可以通过推地将问题从一个特定值扩展到更大的值，最终涵盖了所有符合条件的自然数。

##### 1.1.8.2 Proof by contradiction 反证法

![image-20230206212942622](D:\笔记\笔记图片\image-20230206212942622.png)

* 反证法（Proof by Contradiction），也称为**间接证明法，是一种常用的证明方法**。它通过假设命题的否定，然后推导出一个矛盾的结论，从而证明原命题的正确性。
* 反证法的基本思想是：
  1. 假设待证明的命题为假，即假设它的否定是正确的。
  2. 利用这个假设，推导出一个或多个矛盾的结论。
  3. 由于这些矛盾是由于假设的否定导致的，所以假设的否定是错误的。
  4. 因此，原命题的否定是错误的，即原命题为真。
* 反证法可以用于证明很多类型的命题，包括数学、逻辑和计算机科学等领域的命题。它常用于证明一些重要的数学定理，如无理数的存在性、唯一分解定理等。

##### 1.1.8.3 Proof by contrapositive argument 逆否命题证明法

![image-20230206213151215](D:\笔记\笔记图片\image-20230206213151215.png)

* Proof by contrapositive argument（逆否命题证明法）是一种证明方法，它与直接证明和反证法相对。

  <font color=red>逆否命题证明法的基本思想是**通过证明一个逻辑等价的命题来间接证明原命题的正确性**。逆否命题是通过对原命题的否定和逆序得到的命题。</font>

  逆否命题证明法的步骤如下：

  1. 假设要证明的命题为 "如果 P，则 Q"。这是原命题。
  2. 将原命题的否定形式转换为 "如果非 Q，则非 P"。这是逆否命题。
  3. 证明逆否命题是真的，即证明 "如果非 Q，则非 P" 为真。
  4. **由于逆否命题与原命题是逻辑等价的，如果逆否命题为真，则原命题也为真。**

* 证明逆否命题的过程通常通过逻辑推理或推导来完成。如果能够证明逆否命题是真的，那么根据等价性，原命题也被证明为真。

##### 1.1.8.4 (Dis)Proof by counterexample 反例证明

![image-20230206213159712](D:\笔记\笔记图片\image-20230206213159712.png)



* 就是举一个反例，没什么太好说的

## Exercises_1_Solutions

1. Put these functions in order so that if f(n) ∈ O(g(n)) (i.e. f(n) is Big-Oh of g(n)), then f(n) appears before g(n) in the list. Group together functions that have the same asymptotic order of growth (i.e. f(n) ∈ Θg(n)). In each case provide some justification to your claim.

![image-20230516220401877](D:\笔记\笔记图片\image-20230516220401877.png)









## 2. Binary Search Trees and Other Search Trees

### 2.1 Data Structure

* **Algorithmic computations require data (information) upon which to operate.**
* **算法计算需要数据(信息)来进行操作。**
* The speed of algorithmic computations is (partially) dependent on efficient use of this data.
* 算法计算的速度(部分)依赖于这些数据的有效使用。
* **Data structures are specific methods for storing and accessing information.**
* **数据结构是存储和访问信息的特定方法。**
* We study different kinds of data structures as one kind may be more appropriate than another depending upon the type of data stored, and how we need to use it for a particular algorithm.
* 我们研究不同类型的数据结构，因为一种数据结构可能比另一种更合适，这取决于存储的数据类型，以及我们需要如何将它用于特定的算法。
* <font color=red>不同的数据结构适用于不同的情况</font>

#### 2.1.1 Arrays

* **Arrays are available in some manner in every high-level programming language. You have encountered this data structure in some programming course(s) before.**
* **数组在每种高级编程语言中都以某种方式可用。您以前在一些编程课程中遇到过这种数据结构。**
* Abstractly, an array is simply a collection of items, each of which has its own unique ”index” used to access this data. So if A is an array having n elements, we (typically) access its members as A[0],A[1],...,A[n −1].
* 抽象地说，数组只是一个项的集合，每个项都有自己唯一的“索引”用于访问该数据。所以如果A是一个有n个元素的数组，我们(通常)访问它的成员为A[0]，A[1]，…(n−1)。

![image-20230206214304833](D:\笔记\笔记图片\image-20230206214304833.png)

![image-20230206214245134](D:\笔记\笔记图片\image-20230206214245134.png)

#### 2.1.2 Linked Lists

* In contrast to arrays, data can be easily inserted anywhere in a linked list by inserting a new node into the list and reassigning pointers.
* 与数组相反，通过在链表中插入新节点并重新分配指针，可以轻松地将数据插入链表中的任何位置。

* A list abstract data type (ADT) supports: referring, update (both insert and delete) as well as searching methods.
* 列表抽象数据类型(ADT)支持:引用、更新(插入和删除)以及搜索方法。
* We can implement the list ADT as either a singly-, or doubly- linked list.
* 我们可以将列表ADT实现为单链表或双链表。



* A node in a **singly-linked list** stores a next link pointing to next element in list (null if element is last element).
* 单链表中的节点存储指向列表中下一个元素的下一个链接(如果元素是最后一个元素则为空)。
* ![image-20230206214911976](D:\笔记\笔记图片\image-20230206214911976.png)

* A node in a **doubly-linked list** stores two links: a next link, pointing to the next element in list, and a prev link, pointing to the previous element in the list.
* 双链表中的节点存储两个链接:一个是next链接，指向列表中的下一个元素;另一个是prev链接，指向列表中的上一个元素。
* ![image-20230206215004749](D:\笔记\笔记图片\image-20230206215004749.png)

![image-20230206215019567](D:\笔记\笔记图片\image-20230206215019567.png)

![image-20230206215143572](D:\笔记\笔记图片\image-20230206215143572.png)

![image-20230206215215676](D:\笔记\笔记图片\image-20230206215215676.png)

![image-20230206215237956](D:\笔记\笔记图片\image-20230206215237956.png)

* <font color=red size=5>关于List的时间复杂度</font>
* ![image-20230312224111833](D:\笔记\笔记图片\image-20230312224111833.png)
* **If only the address of the head of the list is known, then the cost of an update is O(p) (we need to traverse the list from positions 0, . . . , p to first find p).**
* **如果只有列表头部的地址是已知的，那么更新的代价是O(p)(我们需要从位置0开始遍历列表，……， p首先找到p)。**
* **<font color=red>同时，这也意味着如果需要修改头部的值，只需要O(1), 虽然大部分情况都是O(n)</font>**

#### 2.1.3 Ordered Data

* We often wish to store data that is ordered in some fashion (typically in numeric order, or alphabetical order, but there may be other ways of ordering it). 
* 我们经常希望存储以某种方式排序的数据(通常是数字顺序，或字母顺序，但也可能有其他的排序方式)。
* Arrays and lists are obvious structures that may be used to store this type of data.
* 数组和列表是可以用来存储这类数据的明显结构。
* Based on our previous discussions, arrays aren’t generally efficient to maintain data where we must add/delete items and maintain a sorted order. Linked lists may provide a better method in that case, but it is generally harder to search for an item in a list.
* 根据我们前面的讨论，对于必须添加/删除项和维护排序顺序的数据，数组通常不是有效的。在这种情况下，链表可能提供了一种更好的方法，但在列表中搜索项目通常比较困难。

##### 2.1.3.1 Ordered Dictionary

* **A dictionary is a set of elements and keys, supported by dictionary operations:**
* **字典是一组元素和键，由字典操作支持**
* 字典是一种数据结构，用于存储一组元素和与每个元素相关联的键（Key）。字典中的每个元素都有一个唯一的键，用于标识和访问该元素。每个键与一个对应的值（Value）相关联，表示该键对应的元素的信息或属性。
* **<font color=red>在这方面类似于Java里的Map数据结构，每一个值都一个唯一对应的key作为关键的键</font>**
  * findElement(k): position k
  * insertElement(k,e): position k , element e
  * removeElement(k): position k
  * ![image-20230517153425499](D:\笔记\笔记图片\image-20230517153425499.png)
* An ordered dictionary maintains an order relation for its elements, where the items are ordered by their keys. 
* 有序字典维护其元素的顺序关系，其中的**项是按键**排序的。
* There are times when the keys and elements are the same, i.e. k = e for each pair.
* 有时键和元素是相同的。每对K = e。

![image-20230206215921544](D:\笔记\笔记图片\image-20230206215921544.png)

* If a dictionary D, is ordered, we can store its items in a vector or array, S, by non-decreasing order of keys. (This generally assumes that we’re not going to add more items into the dictionary.)
* 如果字典D是有序的，我们可以通过键的非递减顺序将其项存储在向量或数组S中。(这通常假设我们不会向字典中添加更多的项。)
* Storing the dictionary in an array in this fashion allows faster searching than if S is stored using a linked list.
* 以这种方式将字典存储在数组中可以比使用链表存储S更快地搜索。
* An ordered array implementation is typically referred to as a lookup table.
* 有序数组实现通常称为查找表。

##### 2.1.3.2 Binary Search

![image-20230206220034108](D:\笔记\笔记图片\image-20230206220034108.png)

<img src="D:\笔记\笔记图片\image-20230206220045145.png" alt="image-20230206220045145" style="zoom:150%;" />

![image-20230209183645938](D:\笔记\笔记图片\image-20230209183645938.png)

<img src="D:\笔记\笔记图片\image-20230209190311896.png" alt="image-20230209190311896" style="zoom:25%;" />

###### 2.1.3.2.1 Complexity of Binary Search

* Let the function T(n) denote the running time of the binary search method.
* 设函数T(n)表示二分搜索方法的运行时间。
* We can characterize the running time of the recursive binary search algorithm as follows：
* 我们可以将递归二元搜索算法的运行时间定性为 搜索算法的运行时间如下

![image-20230517155156850](D:\笔记\笔记图片\image-20230517155156850.png)

* **<font color=red>当n的数量变为原来的2倍时，其实也就多查了一次。</font>**

![image-20230209190436065](D:\笔记\笔记图片\image-20230209190436065.png)

* <font color=red>我这边需要解释一下原因：Linked List的查找节点为什么是O(n)。**因为链表的节点不是连续存储的，而是通过指针链接在一起。要找到链表中的特定节点，需要从链表的头部开始逐个遍历节点，直到找到目标节点。**也就是说由于链表中的节点没有索引或随机访问的能力，因此无法像数组那样通过索引直接访问指定位置的元素。</font>
* 1. FindElement:

     1. Linked List : 因为链表的节点不是连续存储的，而是通过指针链接在一起。要找到链表中的特定节点，需要从链表的头部开始逐个遍历节点，直到找到目标节点。也就是说由于链表中的节点没有索引或随机访问的能力，因此无法像数组那样通过索引直接访问指定位置的元素。
     2. Array: 因为数组是连续存储的，所以当你尝试寻找某一个节点时，你需要使用二分查找来降低时间复杂度。

  2. Insertltem：

     1. Linked List: 因为链表只需要移动相邻的节点的对应指针，所以时间复杂度一般可计算。故为O(1)
     2. Lookup Table: 因为你想要插入某一个值的时候，你同时需要对之后的n-1个元素进行移动，把他们全部向后移动一位。所以时间复杂度很高

  3. RemoveElement

     1. Linked List: 因为我们需要寻找到目标，LinkedList的寻找时间复杂度为O(n),remove操作类似于Insert操作，只需要改变前后的指针就行
     2. Lookup Table: 与InsertItem类似，因为要先寻找到需要删除的点，此时时间复杂度为O(logn),然后删除之后需要将删除位置以后的所有的元素向前平移一位，所以时间复杂度为n

  4. ClosestKeyBefore：**这里的操作是找到目标值之前的最接近的Key**

     1. Linked List: 因为要寻找到目标值，这个时间复杂度为n，然后找到它之前的值。
     2. Lookup Table: 类似的，先找到之前的目标值，然后找前一个。

* List are somewhat costly (in terms of time) to find an item, but it is easy (i.e. quick) to add an item once we know where to insert it.
* 列表是有点昂贵(就时间而言)找到一个项目，但它很容易(即快速)添加一个项目，一旦我们知道在哪里插入它。
* Arrays are efficient when we search for items, but it is expensive to update the list and maintain items in a sorted order.
* 当我们搜索项时，数组是有效的，但是更新列表和按排序顺序维护项是昂贵的。





* One data structure that seems to have this possibility is abinary search tree.
* 二分查找树有可能能做到我们所要求的

* 下面是二分查找的java算法实现

    
  
        public static ArrayList<Integer> binarySearch2(int[] arr, int left, int right, int findVal){
            int mid = (left+right)/2;
            int midVal = arr[mid];
        
        	if (left>right){
            	return new ArrayList<Integer>();
        	}
        
        	if (findVal<arr[mid]){
            	//左边进行递归
            	//System.out.println("左递归"+mid);
            	return binarySearch2(arr,left,mid-1,findVal);
        	}else if (findVal>arr[mid]){
            	//右递归
            	//System.out.println("右递归"+mid);
            	return binarySearch2(arr,mid+1,right,findVal);
        	}else if (findVal==arr[mid]){
            	//如果不修改的情况下，只会找到重复值中距离mid较近的那一个值重复值。
            	//如果要进行修改，那么我们需要寻找arr[mid]后的值是否与之重复。
            	ArrayList<Integer> restIndexList = new ArrayList<>();//用于存放重复数的下标
            	//在向左遍历时
            	int temp = mid-1;
            	while(true){
                	if (temp<0||arr[temp]!=findVal){
                    	break;
                	}
                    	restIndexList.add(temp);
                    	temp--;
            	}
            	restIndexList.add(mid);//把中间的加上去！！！
            	temp = mid+1;
            	//向右遍历
            	while (true){
                	if (temp>arr.length-1||arr[temp]!=findVal){
                    	break;
                	}
                    	restIndexList.add(temp);
                    	temp++;
            	}
        
            	return restIndexList;
        	}else {
            	return new ArrayList<Integer>();
        	}
        	}
    
    



#### 2.1.4 Rooted Trees 根树

* **A rooted tree, T , is a set of nodes which store elements in a parent-child relationship.**
* **根树T是一组以父子关系存储元素的节点**
* T has a special node, r , called the root of T .
* T有一个特殊的节点r，叫做T的根。
* Each node of T (excluding the root node r ) has a parent node.
* T的每个节点(不包括根节点r)都有一个父节点。

![image-20230209190946701](D:\笔记\笔记图片\image-20230209190946701.png)

* If node u is the parent of node v, then v is a child of u.
* 如果节点u是节点v的父节点，那么v就是u的子节点。
* Two nodes that are children of the same parent are called **siblings.** 
* 属于同一父节点的两个节点称为**兄弟节点**。
* **A node is a leaf (external) if it has no children and internal otherwise.**
* **如果一个节点没有子节点，它就是叶节点(外部)，否则就是内部节点。**



![image-20230209192338935](D:\笔记\笔记图片\image-20230209192338935.png)

##### 2.1.4.1 Binary Trees

* **A binary tree is a rooted ordered tree in which every node has at most two children.**
* **二叉树是一种有根的有序树，其中每个节点最多有两个子节点。**
* A binary tree is proper if each internal node has exactly two children.
* 如果每个内部节点恰好有两个子节点，那么二叉树就是合适的。
* Each child in a binary tree is labeled as either a left child or a right child.
* 二叉树中的每一个子结点都被标记为左子结点或右子结点。



* **The depth of a node, v , is number of ancestors of v** , excluding v itself. This is easily computed by a recursive function.
* **节点v的深度是v的祖先节点的个数**，不包括v本身。这很容易通过递归函数计算。

![image-20230209192950614](D:\笔记\笔记图片\image-20230209192950614.png)

![image-20230518122025749](D:\笔记\笔记图片\image-20230518122025749.png)



* **The height of a tree is equal to the maximum depth of an external node in it.** The following pseudo-code computes the height of the subtree rooted at v .
* 树的高度等于树中外部节点的最大深度。下面的伪代码计算以v为根的子树的高度。

![image-20230209193229450](D:\笔记\笔记图片\image-20230209193229450.png)



* As a brief reminder, there are essentially three ways that trees are generally explored/traversed. These methods are the
* 简单地提醒一下，基本上有三种探索/遍历树的方式。这些方法是
  1. **Pre-order traversal**
  2. **前序遍历**
  3. **Post-order traversal**
  4. **后序遍历**
  5. **In-order traversal**
  6. **顺序遍历**

![image-20230209193802408](D:\笔记\笔记图片\image-20230209193802408.png)

![image-20230313134021008](D:\笔记\笔记图片\image-20230313134021008.png)

##### 2.1.4.2 Data structures for trees 使用link存储树

* **Linked structure: each node v of T is represented by an object with references to the element stored at v and positions of its parents and children.**
* **链接结构:T的每个节点v都由一个对象表示，该对象引用了存储在v上的元素及其父节点和子节点的位置。**

![image-20230209194239932](D:\笔记\笔记图片\image-20230209194239932.png)



##### 2.1.4.3 Data structures for rooted t -ary trees 使用数组Array存储树

* 使用Array来存储树tree

![image-20230209194837285](D:\笔记\笔记图片\image-20230209194837285.png)

* 关于为什么子节点是A[2*i+1]或者A[2 * i+2],可以看上一张图的例子
* <font color=red>因为是二叉树，除了叶子点以外的所有点都有两个子节点。所以可以用i和2*i+1 和2*i+2来表示</font>

![image-20230209195122615](D:\笔记\笔记图片\image-20230209195122615.png)

* 我们使用数组来存储树，但是数组是连续的，怎么让数组中的数字和树的节点对上，用<font color=red>**的就是A[2*i+1]或者A[2 * i+2]**</font>
* 通过下面的例子可以发现当前节点的索引值i与其子节点的关系
* ![image-20230518125158104](D:\笔记\笔记图片\image-20230518125158104.png)

#### 2.1.5 Binary Search Tree 

* A Binary Search Tree (BST) applies the motivation of binary search to a tree-based data structure.
* 二叉搜索树(BST)将二叉搜索的动机应用到基于树的数据结构中。
* **In a BST each internal node stores an element, e (or, more generally, a key k which defines the ordering, and some element e).**
* **在BST中，每个内部节点存储一个元素e(或者，更一般地说，一个定义顺序的键k，以及一些元素e)。**
* **A BST has the property that, given a node v storing the element e, all elements in the left subtree at v are less than or equal to e, and those in the right subtree at v are greater than or equal to e.**
* **BST具有这样的性质:给定一个存储元素e的节点v，左子树v处的所有元素都小于或等于e，而右子树v处的所有元素都大于或等于e。**

![image-20230209200438779](D:\笔记\笔记图片\image-20230209200438779.png)

![image-20230209200645892](D:\笔记\笔记图片\image-20230209200645892.png)

<font color=red>使用迭代对结果进行求解</font>

* **二分查找的时间复杂度最大是树的高度**
* <font color=red>根据下图可知，二分查找在树中的时间复杂度为h</font>

![image-20230209200743496](D:\笔记\笔记图片\image-20230209200743496.png)

![image-20230209230258852](D:\笔记\笔记图片\image-20230209230258852.png)

![image-20230209230309927](D:\笔记\笔记图片\image-20230209230309927.png)



![image-20230209230441000](D:\笔记\笔记图片\image-20230209230441000.png)

* All operations in a BST are performed in O(h), where h is the height of the tree. 
* BST中的所有操作都在O(h)中执行，其中h是树的高度。
* Unfortunately, h may be as large as n, e.g. for a **degenerate tree(退化树，一种完全倾斜的树)**
* 不幸的是，h可能和n一样大，例如对于简并树
* **<font color=red>The main advantage of binary searching (i.e. the O(log n) search time) may be lost if the BST is not balanced. In the worst case, the search time may be O(n).</font>**
* **如果BST不平衡，二分搜索的主要优势(即O(log n)搜索时间)可能会丢失。在最坏的情况下，搜索时间可能是O(n)。**
* <font color=blue>就是说，时间复杂度理想为h或者说logn**(2^h - 1 = n)**，但是也有可能为n</font>



##### 2.1.6.1 Complexity of BST

![image-20230313135107229](D:\笔记\笔记图片\image-20230313135107229.png)

![image-20230313141508796](D:\笔记\笔记图片\image-20230313141508796.png)

#### 2.1.6 AVL Trees 平衡二叉搜索树

* **<font color=red>Height-Balance Property: for every internal node, v , of T , the heights of the children of v can differ by at most 1.</font>**
* **高度平衡性质:对于T的每个内部节点v, v的子节点的高度最多可以相差1**。
* <font color=purple>**子树高度（Subtree Height）：指以某个节点为根的子树的高度，即从该节点到子树中的最远叶子节点的路径长度。**</font>
* **<font color=purple>节点高度（Height）：指从某个节点到其最远叶子节点的路径长度。根节点的高度通常被定义为树的高度。</font>**
* All operations (search, insertion, and removal) on an AVL tree with n elements can be performed in O(log n) time.
* **<font color=red>在有n个元素的AVL树上的所有操作(搜索、插入和删除)都可以在O(log n)时间内完成。</font>**

![image-20230209230630379](D:\笔记\笔记图片\image-20230209230630379.png)

* AVL树是具有高度平衡属性的树
* 定理:存储n个元素的AVL树的高度为O(log n)
* 下面的公式推导：

![image-20230518142258511](D:\笔记\笔记图片\image-20230518142258511.png)

![image-20230209231614216](D:\笔记\笔记图片\image-20230209231614216.png)

![image-20230209231639935](D:\笔记\笔记图片\image-20230209231639935.png)

##### 2.1.6.1 Rebalancing  after insertion and delection

https://infinityglow.github.io/study/algorithm/transform-and-conquer/AVL-tree/

<font size=5>平衡因子</font>

* **平衡因子的定义是一个节点的左孩子高度-右孩子高度**

![image-20230209232731155](D:\笔记\笔记图片\image-20230209232731155.png)

![image-20230209233312188](D:\笔记\笔记图片\image-20230209233312188.png)

![image-20230209233400650](D:\笔记\笔记图片\image-20230209233400650.png)

![image-20230209233414695](D:\笔记\笔记图片\image-20230209233414695.png)

###### 2.1.6.1.1 插入，删除后的再平衡AVL树

<font size=5>Insertion</font>

* An insertion in an AVL tree begins as an insertion in a general BST, i.e., attaching a new external node (leaf) to the tree.
* AVL树中的插入开始于一般BST中的插入，即将一个新的外部节点(叶子)附加到树中。
  * This action may result in a tree that violates the height-balance property because the heights of some nodes increase by 1.
  * 这个动作可能会导致一棵树违反了 因为一些节点的高度增加了1。
* A bottom-up mechanism (based on rotations) is applied to rebalance the unbalanced subtrees.
* 应用自底向上机制(基于旋转)来重新平衡不平衡的子树。

![image-20230518155544387](D:\笔记\笔记图片\image-20230518155544387.png)



![image-20230518155554459](D:\笔记\笔记图片\image-20230518155554459.png)



![image-20230518155616564](D:\笔记\笔记图片\image-20230518155616564.png)

<font size=5>Delection</font>

https://blog.csdn.net/chenlong_cxy/article/details/121481845?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522168444177816800225524107%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=168444177816800225524107&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_positive~default-1-121481845-null-null.142

* A deletion in an AVL tree begins as a removal in a general BST. 
* AVL树中的删除开始于一般树中的移除BST。
* Action may violate the height-balance property. 
* 动作可能会违反高度平衡属性。
* Bottom-up mechanism (based on rotations) is applied to rebalance the tree.
* 应用自底向上机制(基于旋转)来重新平衡树。

![image-20230518155934669](D:\笔记\笔记图片\image-20230518155934669.png)

![image-20230518160201182](D:\笔记\笔记图片\image-20230518160201182.png)

* <font color=red>**All operations (search, insertion, and removal) on an AVL tree with n elements can be performed in O(log n) time.**</font>
* <font color=red>**在有n个元素的AVL树上的所有操作(搜索、插入和删除)都可以在O(log n)时间内完成。**</font>

![image-20230518160418467](D:\笔记\笔记图片\image-20230518160418467.png)

#### 2.1.7 (2,4)trees

* Every node in a (2,4) tree has at least 2 and at most 4 children. Each internal node v in a (2,4) tree contains, 1, 2 or 3 keys defining the range of keys stored in its subtrees.
* **<font color=red>(2,4)树中的每个节点至少有2个子节点，最多有4个子节点。(2,4)树中的每个内部节点v包含1、2或3个键，</font>**它们定义了存储在其子树中的键的范围。
*  (2,4)trees的相关性质：
* 1. 每个节点最多有 4 个子节点：(2,4) 树的每个节点最多可以有 4 个子节点。这意味着每个节点可以存储最多 3 个关键字，并且可以有最多 4 个指向子节点的指针。
  2. 节点的关键字有序：在每个节点中，存储的关键字按照从小到大的顺序排列。这使得在节点中进行查找操作时可以使用二分查找法。
  3. <font color=red size=5>**所有叶节点在同一层级**：(2,4) 树的所有叶节点都位于同一层级，也就是说从根节点到任意叶节点的路径长度相等。</font>
  4. **非叶节点的关键字数量：非叶节点中的关键字数量总是比指向子节点的指针数量少 1。例如，一个非叶节点有 3 个子节点，那么它应该存储 2 个关键字。**
  5. 根节点的特殊性：根节点可以是一个叶节点，也可以是一个非叶节点。如果根节点是一个叶节点，则它可以包含 1 到 3 个关键字。如果根节点是一个非叶节点，则它可以包含 0 到 2 个关键字。

![image-20230209234321567](D:\笔记\笔记图片\image-20230209234321567.png)

* All external nodes (leaves) in a (2,4) tree have the same depth.
* (2,4)树中的所有外部节点(叶)具有相同的深度。
* Theorem: The height of a (2,4) tree storing n items is Θ(log n).
* <font color=red>**定理:存储n个元素的(2,4)树的高度为Θ(log n)。**</font>
* ![image-20230313143534755](D:\笔记\笔记图片\image-20230313143534755.png)

![image-20230209234850634](D:\笔记\笔记图片\image-20230209234850634.png)

* Search for a key k in a (2, 4) tree T is done via tracing the path in T starting at the root in a top-down manner.
* 在(2, 4)树T中搜索一个密钥k是通过自上而下的方式追踪T中从根开始的路径来完成的。
* Visiting a node v we compare k with keys (ki ) stored at v: 
* **访问一个节点v，我们将k与存储在v的键(ki)进行比较**
  * **If k = ki the search is completed.** 
  * **如果k = ki，则搜索完成。**
  * **if ki ≤ k ≤ ki+1, the i + 1 th subtree of v is searched recursively**
  * **如果ki≤k≤ki+1，则递归搜索v的第i +1个子树**



##### 2.1.7.1 Insertion

* An insertion of k into a (2, 4) tree T begins with a search for an internal node on the lowest level that could accommodate k without violating the range. 
* 在(2,4)树T中插入k，首先在最低层上搜索一个内部节点，该节点可以容纳k而不违反范围。
* This action may overflow the node-size of a node v acquiring the new key k.
* 该操作可能会溢出节点v的node-size，从而获得新的密钥k。
* Bottom-up mechanism (based on split-operation) is applied to fix overflows.
* 自底向上的机制(基于分步操作)用于修复溢出。

![image-20230216113020591](D:\笔记\笔记图片\image-20230216113020591.png)

![image-20230216113543153](D:\笔记\笔记图片\image-20230216113543153.png)

![image-20230518171018055](D:\笔记\笔记图片\image-20230518171018055.png)



* <font color=blue>注意一件事：父节点的key数+1为子节点的数量。比如上图5,12有两个key，所以此时有3个子节点。</font>

![image-20230216113946529](D:\笔记\笔记图片\image-20230216113946529.png)

![image-20230216114007432](D:\笔记\笔记图片\image-20230216114007432.png)

##### 2.1.7.2 Delection

https://blog.csdn.net/qq_25940921/article/details/82183601?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522167654664316800184192670%2522%252C%2522scm%2522%253A%252220140713.130102334.pc%255Fall.%2522%257D&request_id=167654664316800184192670&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~first_rank_ecpm_v1~rank_v31_ecpm-4-82183601-null-null.142

![image-20230216115235107](D:\笔记\笔记图片\image-20230216115235107.png)

![image-20230216115333310](D:\笔记\笔记图片\image-20230216115333310.png)



![image-20230216115348806](D:\笔记\笔记图片\image-20230216115348806.png)



![image-20230518171052478](D:\笔记\笔记图片\image-20230518171052478.png)

![image-20230518171102610](D:\笔记\笔记图片\image-20230518171102610.png)

![image-20230518171603670](D:\笔记\笔记图片\image-20230518171603670.png)



* **The height of a (2, 4) tree storing n elements in O(log n).**
* **存储n个元素的（2，4）树的高度为O（log n）。**
* **<font color=red>Split, transfer and fusion operations take O(1) time.</font>**
* **分割、转移和融合操作需要O(1)时间。**
* **<font color=red>Search, insertion and removal of an elements in a tree visits O(log n) nodes</font>**
* **在树中搜索、插入和删除一个元素 访问O(log n)个节点**



* <font color=red size=5>还是删除操作比较迷，可以看一下这个链接</font>

http://mingnote.com/234-tree-algorithm-analysis.html

## Exercise_2_Solutions



<font color=red size=6>这方面感觉对AVL树的删除后的再平衡有些误解，不太理解原因！！！</font>

![image-20230518222938901](D:\笔记\笔记图片\image-20230518222938901.png)





## 3. Complexity of Algorithms Sorting

### 3.1 Priority Queues 优先队列

* <font color=red>**A Priority Queue is a container of elements, each having an associated key.** </font>
* **优先队列是一个元素容器，每个元素都有一个相关联的键。**
* **Keys determine the priority used in picking elements to be removed.**
* **键决定在选择要删除的元素时使用的优先级。**

![image-20230313145010089](D:\笔记\笔记图片\image-20230313145010089.png)

![image-20230519001232395](D:\笔记\笔记图片\image-20230519001232395.png)

* **Priority Queue（优先队列）是一种数据结构，类似于队列和堆栈，但每个元素都有与之关联的优先级。在优先队列中，元素按照优先级顺序插入和删除，而不是按照它们插入队列的顺序。具有较高优先级的元素可以更快地被检索、处理和删除。通常，优先队列使用<font color=red size=5>堆</font>来实现。**

![image-20230313161442765](D:\笔记\笔记图片\image-20230313161442765.png)

#### 3.1.1 Heap Data Structure 堆数据结构

* **<font color=red>数据结构堆(Heap)：堆是一种完全二叉树或近似完全二叉树的数据结构</font>**
* 注意要点：
  * <font size=5 color=red>1.堆中的某一个节点总是不大于或者不小于其父节点的值</font>
  * <font color=red size=5>2.堆总是一棵完全的二叉树</font>
* **<font color=blue>我在最开始给你理一下关于堆和优先队列，首先，堆这个数据结构的性质就非常适合优先队列，毕竟已经有了一个优先级。然后，使用堆满足优先队列需要有一个很重要的性质！！！无论删除和增加，都是从最高优先级或者最低优先级开始，这个东西它不是链表！！！！不是数组！！！！</font>**

![image-20230313163513053](D:\笔记\笔记图片\image-20230313163513053.png)

* <font color=red size=5>注意堆是一个完全二叉树</font>

* A heap is a realization of a Priority Queue that is efficient for both insertions and deletions. 
* 堆是优先队列的一种实现，它对插入和删除都很有效。
* A heap allows insertions and deletions to be performed in logarithmic time. （O(logn)）
* 堆允许在对数时间内执行插入和删除操作。
* **In a heap the elements and their keys are stored in an almost complete binary tree. Every level of the binary tree, except possibly the last one, will have the maximum number of children possible.**
* **在堆中，元素及其键值存储在几乎完整的二叉树中。二叉树的每一层，可能除了最后一层，都有尽可能多的子结点。**
* I In a heap T, for every node v (excluding the root) the key at v is greater than (or equal to) the key stored at its parent
* 在堆T中，对于每个节点v(不包括根节点)，v上的键都大于(或等于)存储在其父节点上的键。

![image-20230313162440903](D:\笔记\笔记图片\image-20230313162440903.png)

* 堆的有效实现可以使用**数组**来存储元素(即我们前面讨论过的树的向量表示)。
* **heap**: A (nearly complete) binary tree T containing elements with keys satisfying the heap-order property, stored in an array
* **heap**:一个(几乎完整的)二叉树T，包含键满足堆顺序属性的元素，存储在数组中
* **last**: A reference to the last used node of T in this array representation.
* last:对数组表示中T的最后一个使用节点的引用。
* **comp**: A comparator function that defines the total order relation on keys and which is used to maintain the minimum (or maximum) element at the root of T.
* **comp**:一个比较器函数，它定义键的总顺序关系，用于维护T的根处的最小(或最大)元素。

![image-20230313162913213](D:\笔记\笔记图片\image-20230313162913213.png)

![image-20230313162928456](D:\笔记\笔记图片\image-20230313162928456.png)

* Inserting a new item into a heap begins by adding this element to the bottom of the tree in the position of the first unused, or empty, child. 
  在向堆中插入新项时，首先将该元素添加到树的底部，即第一个未使用的或空的子元素的位置。
* **Then, if necessary, this new element “bubbles” its way up the heap until the heap-order property is restored.**
* **然后，如果有必要的话，这个新元素会在堆中 "冒泡"，直到堆的顺序属性被恢复。**
* 1.
* ![image-20230519002540447](D:\笔记\笔记图片\image-20230519002540447.png)
* 2.
* ![image-20230519002612309](D:\笔记\笔记图片\image-20230519002612309.png)
* 3.
* ![image-20230519002624586](D:\笔记\笔记图片\image-20230519002624586.png)
* 4

![image-20230519002930112](D:\笔记\笔记图片\image-20230519002930112.png)

* 5.

![image-20230519002944760](D:\笔记\笔记图片\image-20230519002944760.png)

**<font size=5>Delection in a Heap</font>**

* **<font color=red size=5>Deletion in a heap consists of removing the minimum (or maximum) element (at the root) from the heap. Then the bottom, right-most element in the heap (the element at the end of the array that stores the heap) is moved to the root.</font>**
* **堆中的删除包括从堆中删除最小(或最大)元素(位于根)。然后，堆中最底部、最右边的元素(存储堆的数组末尾的元素)被移动到根节点。**
* To restore the heap-order property, this item then “sinks” or bubbles down the heap.
* 若要恢复堆顺序属性，则此项将“下沉”或“冒泡”到堆中。
* <font color=blue>因为只能从最大优先级或者最小优先级开始嘛（因为堆主要应用于优先队列），这里删除最大优先级的数值</font>
* ![image-20230519003852289](D:\笔记\笔记图片\image-20230519003852289.png)
* ![image-20230519003908268](D:\笔记\笔记图片\image-20230519003908268.png)



![image-20230313163831775](D:\笔记\笔记图片\image-20230313163831775.png)

* 注意：**<font color=red>堆排序很多情况下还是存储在二叉树里的，所以还是按照二叉树的那一套方法去理解</font>**

* **另外解释一下IsEmpty：**
* 这是因为堆的实现通常会维护一个属性来记录堆中元素的数量。在每次插入或删除操作时，会相应地更新这个属性。因此，判断堆是否为空只需要检查该属性是否为零即可，不需要遍历整个堆结构。无论堆中有多少元素，只需要常数时间即可完成判断操作。
* 还有Remove
* 因为当你删除某个节点后，堆需要重新进行再构建，父节点和字节点需要重新比较大小，所以时间复杂度为logn





### 3.2 Heap Sorting 堆排序

https://blog.csdn.net/weixin_51609435/article/details/122982075?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522167872037316800197045694%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=167872037316800197045694&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_positive~default-1-122982075-null-null.142

* Theorem: The heap-sort algorithm sorts a sequence, S, of n comparable items in O(n log n) time, where
* 定理:堆排序算法在O(n log n)时间内对n个可比项的序列S进行排序，其中

![image-20230313165051338](D:\笔记\笔记图片\image-20230313165051338.png)

* Bottom-up construction of heap with n elements takes O(n log n) time, and
* 自下而上构建有n个元素的堆需要O(n log n)时间，而
* Extraction of n elements (in increasing order) from the heap takes O(n log n) time.
* 从堆中提取n个元素（按递增顺序）需要O（n log n）的时间。
* <font color=red>这个问题的关键在于彼此交换</font>
* 1. 先找到非叶子节点的最后一个节点
  2. 将这个节点与它的两个子节点比较，如果子节点存在比他大的，就交换![image-20230313171649854](D:\笔记\笔记图片\image-20230313171649854.png)
  3. 换完之后迭代，在看是否存在上述情况
  4. 知道将整个数组遍历完成



* 这里是要构建出一个二叉堆

![image-20230313171306845](D:\笔记\笔记图片\image-20230313171306845.png)

* 很明显，这边构筑出来之后，但是没有进行排序，然后我们需要排序

![image-20230519143256224](D:\笔记\笔记图片\image-20230519143256224.png)

![image-20230519143337433](D:\笔记\笔记图片\image-20230519143337433.png)

* 通过上面的排序方法可以看出，堆排序其实就是通过堆的数据结构的“冒泡“来不断改变对节点进行交换
* **优点是空间复杂度很低**

```
void HeapAdjust(int* arr, int start, int end)
{
	int tmp = arr[start];
	for (int i = 2 * start + 1; i <= end; i = i * 2 + 1)
	{
		if (i < end&& arr[i] < arr[i + 1])//有右孩子并且左孩子小于右孩子
		{
			i++;
		}//i一定是左右孩子的最大值
		if (arr[i] > tmp)
		{
			arr[start] = arr[i];
			start = i;
		}
		else
		{
			break;
		}
	}
	arr[start] = tmp;
}
void HeapSort(int* arr, int len)
{
	//第一次建立大根堆，从后往前依次调整
	for(int i=(len-1-1)/2;i>=0;i--)
	{
		HeapAdjust(arr, i, len - 1);
	}
	//每次将根和待排序的最后一次交换，然后在调整
	int tmp;
	for (int i = 0; i < len - 1; i++)
	{
		tmp = arr[0];
		arr[0] = arr[len - 1-i];
		arr[len - 1 - i] = tmp;
		HeapAdjust(arr, 0, len - 1-i- 1);
	}
}
int main()
{
	int arr[] = { 9,5,6,3,5,3,1,0,96,66 };
	HeapSort(arr, sizeof(arr) / sizeof(arr[0]));
	printf("排序后为:");
	for (int i = 0; i < sizeof(arr) / sizeof(arr[0]); i++)
	{
		printf("%d ", arr[i]);
	}
	return 0;
}
```





### 3.3 Divide-and-Conquer 分治算法

* The divide-and-conquer method is a means that can be used to solve some algorithmic problems. This general method consists of the following steps:
* 分治法是一种可以用来解决一些算法问题的方法。这种通用方法包括以下步骤:

1. **Divide：**If the input size is small then solve the problem directly; otherwise, divide the input data into two or more disjoint subsets
   1. 如果输入大小较小，则直接解决问题;否则，将输入数据分成两个或多个互不关联的子集
2. **Recur:** Recursively solve the sub-problems associated with subsets.
   1. 递归地解决与子集相关的子问题。
3. **Conquer**: Take the solutions to sub-problems and merge into a solution to the original problem.
   1. 将子问题的解决方案合并为原始问题的解决方案。

### 3.4 Merge Sort 归并排序

* <font color=red>**inversions:Inversions（逆序对）是指在一个序列中，两个元素的顺序与它们在排序后的顺序相反的情况。**</font>
* ![image-20230519224519047](D:\笔记\笔记图片\image-20230519224519047.png)

* **MergeSort** is one way we can apply the divide-and-conquer method to perform sorting. The MergeSort method consists of the following steps:
* **归并排序**是一种我们可以应用分治方法来执行排序的方法。MergeSort方法由以下步骤组成:
* ![image-20230313183241522](D:\笔记\笔记图片\image-20230313183241522.png)

![image-20230313183255556](D:\笔记\笔记图片\image-20230313183255556.png)

![image-20230313183330472](D:\笔记\笔记图片\image-20230313183330472.png)

* Theorem: Merging two sorted sequences S1 and S2 takes O(n1 + n2) time, where n1 is the size of S1 and n2 is the size of S2. 
* 定理:合并两个排序序列S1和S2需要O(n1 + n2)的时间，其中n1为S1的大小，n2为S2的大小。
* Theorem: MergeSort runs in O(n log n) time in the worst (and average) case. 
* 定理:在最坏(和平均)的情况下，归并排序的运行时间为O(n log n)。
* Idea: During every recursive step, dividing each sublist takes time at most O(n) time. Merging all of the lists in each level takes at most O(n) time as well. 
* 思想:在每个递归步骤中，**划分每个子列表最多需要O(n)时间。**合并每层中的所有列表最多也需要O(n)时间。
* How many times do we recurse? This is at most O(log n) times. Hence this gives the O(n log n) running time for MergeSort.
* 递归多少次?最多是O(log n)次。因此，这为归并排序提供了O(n log n)的运行时间。



* 解释：
* ![image-20230313183811295](D:\笔记\笔记图片\image-20230313183811295.png)

* <font color=red>这个方法的主要难点在合并，在合并两个已经排序的序列时，先比较第一位，将小的那一位放到新的数组里，然后用第一位里相对大的和另一个的下一位比较，再把较小的塞进去。以此类推</font>
* ![image-20230313184700981](D:\笔记\笔记图片\image-20230313184700981.png)

* 在将序列分块的时候，根据二分查找，时间复杂度为logn，在合并的时候需要移动和比较n个元素，所以总的时间复杂度为nlogn


    package Sort;
    
    import java.text.SimpleDateFormat;
    import java.util.Arrays;
    import java.util.Date;
    
    /**
     * @author 巩泽楷
     * @version 1.0
     * 归并排序
     */
    public class MergeSort {
        public static void main(String[] args) {
            int[] arr = new int[80000];
            for (int i = 0; i < 80000; i++) {
                arr[i] = (int) (Math.random()*80000);
            }
            //int arr[] = {8,4,5,7,1,3,6,2};
            int temp[] = new int[arr.length];
            Date date1 = new Date();    //时间类
            SimpleDateFormat simpleDateFormat = new SimpleDateFormat("yyyy-MM-dd HH:mm:ss");
            String date1Str = simpleDateFormat.format(date1);
            System.out.println("排序前的时间是："+date1Str);
    
            mergeSort(arr,0,arr.length-1,temp);
    
            Date date2 = new Date();
            String date2Str = simpleDateFormat.format(date2);
            System.out.println("排序后的时间是："+date2Str);
            //System.out.println(Arrays.toString(arr));
        }
        //分解方法:
        public static void mergeSort(int[] arr, int left, int right, int[] temp){
            if (left<right){
                int mid = (left+right)/2;
                //向左递归分解
                mergeSort(arr,left,mid,temp);
                //向右的递归分解
                mergeSort(arr,(mid+1),right,temp);
                //合并
                merge(arr,left,mid,right,temp);
            }

```
    
​        }
​        //合并方法
​        /*
​            1.arr排序的原始数组
​            2.left 左边有序序列的初始索引
​            3.mid 中间的索引
​            4.right 右边的索引
​            5.temp 作为中转的数组
​         */
​        public static void merge(int[] arr, int left, int mid, int right, int[]temp){
​            int i = left;
​            int j = mid+1;
​            int t = 0;//中转数组的索引
​    
            //(一)
            //先把左右两边(有序)的数据按照规则填充到temp数组。
            //直到其中一边处理完为止。
            while (i<=mid&&j<=right){
                if (arr[i]<=arr[j]){//左边的小于或等于右边的元素
                    temp[t] = arr[i];
                    t++;
                    i++;
                }else {//右边的小于或等于左边的元素
                    temp[t] = arr[j];
                    t++;
                    j++;
                }
            }
```


​    
​            //(二)
​            //把剩余的数据依次填充到temp中。
​            while (i<=mid&&i>=0){
​                temp[t] = arr[i];
​                t++;
​                i++;
​            }
​            while (j>=mid&&j<=right){
​                temp[t] = arr[j];
​                t++;
​                j++;
​            }
​    
​            //(三)
​            //将temp的数组拷贝到arr
​            //注意：并不是每一次拷贝都将所有的数据。
​            t = 0;
​            int tempLeft = left;
​            while (tempLeft<=right){
​                arr[tempLeft] = temp[t];
​                t++;
​                tempLeft++;
​            }

```
    
​        }
​    }


```

* ![image-20230519145617853](D:\笔记\笔记图片\image-20230519145617853.png)



* ![image-20230519145630569](D:\笔记\笔记图片\image-20230519145630569.png)







### 3.5 QuickSort 快速排序

https://blog.csdn.net/qq_40941722/article/details/94396010?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522168445426016782425177502%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=168445426016782425177502&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_positive~default-1-94396010-null-null.142

* 快速排序
* ![image-20230519153619553](D:\笔记\笔记图片\image-20230519153619553.png)
* ![image-20230519153644228](D:\笔记\笔记图片\image-20230519153644228.png)

* **<font color=red>利用两个指针，一个从前往后读，一个从后往前读, 注意是j先走，j走完再走i</font>**

![image-20230313185820336](D:\笔记\笔记图片\image-20230313185820336.png)

![image-20230528180926924](D:\笔记\笔记图片\image-20230528180926924.png)

* <font size=5>课本内容：</font>
* The QuickSort algorithm is yet another divide-and-conquer method for performing sorting. This method differs from MergeSort in that the steps for QuickSort are as follows:
* QuickSort算法是执行排序的另一种分治法。此方法与归并排序的不同之处在于快速排序的步骤如下:
  * Divide: If |S| > 1, select a pivot element x in S and create three sequences: L, E, and G where 
  * 分割:如果|S| > 1，在S中选择一个枢轴元素x，并创建三个序列:L, E和G，其中
    * L stores elements in S that are less than x, 
    *  L存储S中小于x的元素;
    * E stores elements in S that are equal to x, and 
    * E存储S中等于x的元素，以及
    * G stores elements in S that are greater than x.
    * G存储S中大于x的元素。
  * Recur: Recursively sort the sequences L and G.
  * 递归排序:递归排序序列L和G。
  * Conquer: Put sorted elements from L, E, and G together to form a sorted list.
  * 将L、E和G中的分类元素放在一起 形成一个排序的列表。

![image-20230519154046450](D:\笔记\笔记图片\image-20230519154046450.png)

![image-20230519154259439](D:\笔记\笔记图片\image-20230519154259439.png)



* **一般来说最坏时间复杂度是n^2**

![image-20230528175920447](D:\笔记\笔记图片\image-20230528175920447.png)



### 3.6 Basic Probability 基础概率

* **Probability theory is useful in many contexts in the theory of algorithms.**
* **概率论在算法理论的很多方面都很有用。**
* **It can be used to analyze the average-case performance of algorithms (by weighting the running time according to a probability distribution on inputs.**
* 它可以用来**<font color=red>分析算法的平均情况性能(通过根据输入的概率分布加权运行时间)。</font>**
* Randomized algorithms (those that use random bits during their execution to make decisions) are also becoming more commonplace and useful in recent years. Analysis of such randomized algorithms also requires use of probability theory.
* 近年来，随机算法(那些在执行过程中使用随机比特来做出决策的算法)也变得越来越普遍和有用。分析这种随机算法还需要使用概率论



* Sample space is the set of all possible outcomes from an experiment.

* 样本空间是一个实验中所有可能结果的集合。

* Examples:

* 1. Rolling a fair (6-sided) die. The sample space is {1, 2, 3, 4, 5, 6}.

     掷一个均匀的(六面)骰子。样本空间为{1,2,3,4,5,6}。

  2. Flipping a fair coin. The sample space is {H, T}

     抛一枚均匀的硬币。样本空间为{H, T}

  3. Flipping a fair coin until it comes up heads. Here the sample space is infinite, with the i th possible outcome being a sequence of i − 1 tails followed by a single heads, for i = 1, 2, 3, 4, . . .

     抛一枚均匀的硬币，直到正面朝上。这里的样本空间是无限的，第i个可能的结果是i−1个反面跟着一个正面的序列，对于i = 1,2,3,4，…



#### 3.6.1 Probability spaces, Events 概率空间和事件

* A Probability space is a sample space S and a probability function Pr, which maps subsets of S to [0, 1]. Each subset, A ⊆ S, is called an event.
* 概率空间是一个样本空间S和一个概率函数Pr，它将S的子集映射到[0,1]。每个子集(A: S)称为一个事件。
* ![image-20230519202120758](D:\笔记\笔记图片\image-20230519202120758.png)
* Consider the sample space earlier, namely that of flipping a fair coin until it comes up heads. 
* 考虑之前的样本空间，即投掷一枚均匀硬币直到出现正面的空间。
* We can represent the sample space as an infinite set of strings, namely {H, TH, TTH, TTTH, . . .}. 
* 我们可以将样本空间表示为字符串的无限集合，即{H, TH, TTH, TTTH，…}。
* The probability function on this sample space assigns these probabilities to events:
* 这个样本空间上的概率函数将这些概率分配给事件:

![image-20230519202354734](D:\笔记\笔记图片\image-20230519202354734.png)

* (These statements make use of the independence of coin flips discussed on the next slide, and the last statement uses the final property of the probability function on the previous slide.)
* (这些陈述利用了下一张幻灯片中讨论的抛硬币的独立性，最后一个陈述使用了前一张幻灯片中概率函数的最终性质。)



#### 3.6.2 Independent Events 独立事件

* Two events are independent if Pr(A ∩ B) = Pr(A) · Pr(B). 
* 如果Pr(A∩B) = Pr(A)·Pr(B)，则两个事件是独立的。
* A collection of events {A1, A2, . . . , An} is mutually independent if 
  * Pr(Ai1 ∩ Ai2 ∩ . . . ∩ Aik ) = Pr(Ai1) · Pr(Ai2) · . . . · Pr(Aik ) for any subcollection of events {Ai1, . . . , Aik }.

![image-20230519202623247](D:\笔记\笔记图片\image-20230519202623247.png)

#### 3.6.3 Conditional Probability 条件概率

* The conditional probability of an event A occurring, given another event B, denoted Pr(A|B) is Pr(A|B) = Pr(A ∩ B)/Pr(B), assuming that Pr(B) > 0. 
* 给定另一个事件B，事件A发生的条件概率，记为Pr(A|B)是Pr(A|B) = Pr(A∩B)/Pr(B)，假设Pr(B) > 0。
* **In other words, conditional probability talks about the probability of some event occurring, given the knowledge that some other event has already occurred.**
* **换句话说，条件概率讲的是在已知其他事件已经发生的情况下，某个事件发生的概率**

![image-20230519203033180](D:\笔记\笔记图片\image-20230519203033180.png)



#### 3.6.4 Random variables 随机变量

* **A random variable is a function X that maps outcomes from some sample space to real numbers**
* **随机变量是一个函数X，它将某个样本空间的结果映射为实数**
* **<font color=red>离散随机变量是概率论和统计学中的概念，用于描述随机试验结果的变量，其可能取值为一组离散的数值。</font>**
* In algorithm analysis we often use a random variable X with a discrete set of outcomes to characterize the running time of a randomized algorithm.
* 在算法分析中，我们经常使用具有离散结果集的随机变量X来表征随机算法的运行时间。



* The expected value of a discrete random variable X is defined as E(X) = P i i · Pr(X = i) where the summation is over the range of possible values of X.
* 离散随机变量X的期望值定义为E(X) = pi·Pr(X = i)，其中总和在X的可能值范围内。
* The expected value is linear, meaning that for any two random variables X and Y we have E(X + Y) = E(X) + E(Y).
* 期望值是线性的，这意味着对于任意两个随机变量X和Y，我们有E(X + Y) = E(X) + E(Y)。
* 

![image-20230519204036616](D:\笔记\笔记图片\image-20230519204036616.png)

![image-20230519204133708](D:\笔记\笔记图片\image-20230519204133708.png)



* Consider the problem from before of flipping a fair coin until it comes up heads for the first time.
* 考虑之前抛一枚均匀硬币直到第一次正面朝上的问题。
* Let X denote the number of flips that must be made until the heads appears (including the final flip). Then X is a random variable that takes values in {1, 2, 3, . . .}.
* 令X表示在正面出现之前必须进行的投掷次数(包括最后一次投掷)。那么X是一个随机变量，取{1,2,3，…}中的值。

![image-20230519204343757](D:\笔记\笔记图片\image-20230519204343757.png)

![image-20230519204354381](D:\笔记\笔记图片\image-20230519204354381.png)



![image-20230519210929229](D:\笔记\笔记图片\image-20230519210929229.png)

![image-20230519211236121](D:\笔记\笔记图片\image-20230519211236121.png)

![image-20230519211243872](D:\笔记\笔记图片\image-20230519211243872.png)



### 3.7 Randomized QuickSort ！！！！！！！！！！！！！！！！！！！！！！！

![image-20230519215736208](D:\笔记\笔记图片\image-20230519215736208.png)

![image-20230519215745179](D:\笔记\笔记图片\image-20230519215745179.png)

![image-20230519215758144](D:\笔记\笔记图片\image-20230519215758144.png)

![image-20230519215806931](D:\笔记\笔记图片\image-20230519215806931.png)



![image-20230519215831298](D:\笔记\笔记图片\image-20230519215831298.png)

### 3.8 Sorting in Linear time (Bucket Sort) 桶排序

* Bucket Sort is not based on comparisons but on using keys as indices of a bucket array B that has entries within an integer range [0, 1, . . . , N − 1].
* 桶排序不是基于比较，而是使用键作为桶数组B的索引，桶数组B的条目在整数范围内[0,1，…]。， n−1]。
* Initially all items from input sequence, S, are moved to appropriate buckets, i.e., an item with key k is moved to bucket B[k].
* 最初，输入序列S中的所有项都被移动到相应的桶中，即键为k的项被移动到桶B[k]中。
* Then move all items back into S according to their order of appearance in consecutive buckets B[0], B[1], . . . , B[N − 1].
* 然后将所有项目按照其在连续桶B[0]， B[1]，…中出现的顺序移回S。， b [n−1]。

* Bucket sorting (or some variant) is performed by the postal service to deliver mail. Letters and parcels are sorted based on postal addresses, then gathered up for the actual delivery process.
* 桶排序(或某种变体)由邮政服务执行，以传递邮件。信件和包裹根据邮政地址进行分类，然后收集起来进行实际投递。
* (Typically this could actually require several bucket sorts, e.g. first on county, then on town, then on post code, etc.)
* (通常，这实际上可能需要几个桶排序，例如: 首先是县，然后是城镇，然后是邮政编码，等等)

![image-20230519221244145](D:\笔记\笔记图片\image-20230519221244145.png)

* <font color=red>桶排序就是将每一个数值放到对应范围内的桶里，然后在桶里进行排序，每个桶内排序的时间复杂度是桶内元素的数量k O(n+k)</font>
* 但是桶排序的时间复杂度最差为n^2



### 3.9 Radix Sorting 基数排序

* Radix sorting was a method that was used by punched card sorting machines. 
* 基数排序是穿孔卡片分选机使用的一种方法。
* It is based on a card sorting technique which sorts column by column using a bucket sorting algorithm on each successive column.
* 它基于卡片排序技术，对每个连续的列使用桶排序算法逐列排序。

![image-20230519221635209](D:\笔记\笔记图片\image-20230519221635209.png)



![image-20230519221702197](D:\笔记\笔记图片\image-20230519221702197.png)

1. **基数排序**属于“分配式排序”，又称“桶子法bucket Sort/bin sort”, 它是通过键值的各个位的值，将要排序的元素分配至某些"桶"中，从而达到排序的作用。
2. 基数排序属于稳定性排序，基数排序法是效率高的稳定性排序法。
3. 基数排序(Radix Sort)是桶排序的扩展。
4. 实现原理：**将整数按位数切割成不同的数字，然后按照每个位数进行比较**。
5. 缺陷：不能比较负数。需要对于代码进行改写。

基本思想：

1. 将所有带比较的数值统一为同样的数位长度，数位**较短的数前面补0**。然后，从最低位开始，依次进行一次排序。这样从最低为开始一直到最高位排序完成后，数列就变成一个有序序列。

2. ![image-20220411132022067](D:\笔记\笔记图片\image-20220411132022067.png)

   ![image-20220411132055545](D:\笔记\笔记图片\image-20220411132055545.png)

​					![image-20220411132129132](D:\笔记\笔记图片\image-20220411132129132.png)

![image-20220411132214250](D:\笔记\笔记图片\image-20220411132214250.png)

* 由此，你可以得出时间复杂度为O(n), 更具体一点时间复杂度为**<font color=red>O(d*(n+r))</font>**
* d为最大的位数，n为比较的数字的数量，r为基数
* 重点解释一下r：
* 因为每一次排序要新建r个桶，所以要加上r
* <font color=red>**相当于，新建r个桶，然后进行for循环n次，重复以上步骤d次**</font>

![image-20230519224014436](D:\笔记\笔记图片\image-20230519224014436.png)









## 4. Complexity of Algorithms Fundamental Solution Techniques Divide & Conquer

### 4.-1 Divide -and-Conquer的一般思想

* To remind you, here is the general outline for using this method:
  * Divide: If the input size is small then solve directly, otherwise divide the input data into two or more disjoint subsets.
  * 分割:如果输入数据很小，则直接求解，否则将输入数据分成两个或多个不相交的子集。
  * Recur: Recursively solve the sub-problems associated with the subsets.
  * 递归:递归地解决与子集相关的子问题。
  * Conquer: Take the solutions to the sub-problems and merge them into a solution to the original problem.
  * 合并:将子问题的解决方案合并成原始问题的解决方案。



### 4.0主定理

![image-20230520021107987](D:\笔记\笔记图片\image-20230520021107987.png)

![image-20230520021626141](D:\笔记\笔记图片\image-20230520021626141.png)

![image-20230520021639660](D:\笔记\笔记图片\image-20230520021639660.png)

![image-20230520022205452](D:\笔记\笔记图片\image-20230520022205452.png)

* **特殊情况，不允许使用主定理，需要变化格式后后使用**



https://blog.csdn.net/qq_41739364/article/details/101224786?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522167872097016800182129029%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=167872097016800182129029&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_positive~default-1-101224786-null-null.142

![image-20230313204532987](D:\笔记\笔记图片\image-20230313204532987.png)



<font color=red size=6>这节课的后半段挺懵，没搞懂它想说什么？？？</font>

### 4.1 Fast Multiplication of Integers 整数的快速乘法

#### 4.1.1 karatsuba算法

![image-20230520024008347](D:\笔记\笔记图片\image-20230520024008347.png)

* 因为每一层的每一段需要进行3次运算，然后可以得出总计算次数为
* **<font color=red>3^0 + 3^1 + 3^2 + ... + 3^(log2(n))</font>**
* ![image-20230520110145013](D:\笔记\笔记图片\image-20230520110145013.png)
* 这里在举一个8位数的例子，以方便更好的理解该题目：
* ![image-20230520110223127](D:\笔记\笔记图片\image-20230520110223127.png)
* **因为AC和BD还有(A+B)*(C+D)都是比较大的位数，所以都可以使用karastuba算法**
* **在这里(A+B)*(C+D)是两个较大位数的乘积，这里同样可以使用karatsuba算法**
* ![image-20230520110451484](D:\笔记\笔记图片\image-20230520110451484.png)
* <font color=red>这里可以发现，如果数字足够大还可以继续往下求，不过这里没必要了</font>



#### 4.1.2 Matrix Multiplication

* **<font color=red>该算法主要用于简化矩阵之间的乘法</font>**
* ![image-20230520114448616](D:\笔记\笔记图片\image-20230520114448616.png)



* **<font color=red>通过递归地应用Strassen算法，我们可以在O(n^log2(7))的时间复杂度下计算两个矩阵的乘法。</font>**

* 其他方面，比如需要计算一个8X8的矩阵的大小，我们需要将它拆成四个4X4的矩阵，然后在计算P1-P7的时候，将这四个矩阵再次拆分成2X2的矩阵在进行运算，一次类推。但因为例子实在难打，不写了。

![image-20230520115307409](D:\笔记\笔记图片\image-20230520115307409.png)



## 5. Fundamental Solution Techniques Greedy Algorithms

### 5.1 Greedy Method

* An optimization problem is a problem that involves searching for a configuration that minimizes or maximizes some objective function. 
* 优化问题是一个问题，涉及到寻找一个构型，使一些目标函数最小化或最大化。
* The greedy method solves (or tries to solve) a given optimization problem by going through a sequence of (feasible) choices. 
* 贪心方法通过一系列(可行的)选择来解决(或试图解决)给定的优化问题。
* **The sequence starts from a well-understood starting configuration, and then iteratively makes the decision that seems best from all those that are currently possible.** 
* **这个序列从一个很好的开始配置开始,然后迭代地做出决定,似乎最好从现在可能的所有。**
* Problems that have a greedy solution are said to possess the greedy-choice property.
* 据说有一个贪婪的解决方案的问题是具有灰色选择的属性。

![image-20230227142453055](D:\笔记\笔记图片\image-20230227142453055.png)

* Greed Works
* A word of warning! The greedy approach does not always lead to an optimal solution. (And we will see some problems for which it doesn’t work.)
* 一个警告!贪婪的方法并不总是导致一个最优的解决方案。(我们将会看到一些问题,但这是行不通的。)
* **<font color=blue size=5>每一次都寻找相应的最优解，但是汇总起来不一定是全局的最优解</font>**
* The greedy method is also sometimes used for some hard (i.e. difficult to solve) problems in order to generate approximate solutions.
* 贪婪的方法有时也被用于一些困难(即很难解决)问题,以产生近似解。



### 5.2 Fractional Knapsack Problem (FKP) 部分背包问题（分数背包问题）

https://blog.csdn.net/ccc369639963/article/details/122578180?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522167752794916800192229550%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=167752794916800192229550&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduend~default-2-122578180-null-null.142

* **<font color=blue>部分背包问题：每件物品是可再分的，即允许将某件物品的一部分（例如 1/3）放入背包；</font>**

* Let S be a set of n items, where each item i has a positive benefit bi and a positive weight wi . 
* 设S是n个项目的集合，其中每个项目i的收益为正bi，权重为正wi。
* **Goal: Find the maximum benefit subset that does not exceed total weight W.** 
* **目标:找到不超过总权重W的最大利益子集。**
* In a FKP we are allowed to take arbitrary fractions, xi , of each item, i.e. the solution is a set of values xi such that
* 在FKP中,我们可以取任意的分数,xi每个项,即解决方案是一组值xi
* ![image-20230227143758628](D:\笔记\笔记图片\image-20230227143758628.png)



* <font color=blue>部分背包问题</font>
* 在给定容量的基础上，求出最大的价值。

![image-20230227145122089](D:\笔记\笔记图片\image-20230227145122089.png)

* **求出单位价值最高的物品，然后一直放到直到物品放完或者容量已满。**

* <font color=blue>注意伪代码</font>

![image-20230227145153763](D:\笔记\笔记图片\image-20230227145153763.png)

![image-20230227145229784](D:\笔记\笔记图片\image-20230227145229784.png)

* **该问题并没有太过复杂，就是计算单位价值，先拿单位价值最高的物品，拿完为止，然后再拿第二高的，以此类推，直到装满**





### 5.3 01背包问题

https://blog.csdn.net/Biteht/article/details/124651895?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522167752801716800211569182%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=167752801716800211569182&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_positive~default-2-124651895-null-null.142

![image-20230520145236759](D:\笔记\笔记图片\image-20230520145236759.png)

* 这个图虽然草率了一点，但是很清晰
* 比如我们一开始有一个f(4,8),可以放四个物品，负重最多为8
* 由上图我们可以得到：
* ![image-20230520145551732](D:\笔记\笔记图片\image-20230520145551732.png)
* ![image-20230520145627955](D:\笔记\笔记图片\image-20230520145627955.png)


```
/**
     * 0-1背包
     * @param val 价值
     * @param weight 重量
     * @param W 背包容量
     * @return 最优解
     */
    public static int func(int[] val, int[] weight, int W) {
        int N = weight.length;   //记录所有的物品数
        int[][] V = new int[N + 1][W + 1];  //创建背包矩阵
        //初始化矩阵 列，背包容量为0
        for (int col = 0; col <= W; col++) {
            V[0][col] = 0;
        }
        for (int row = 0; row <= N; row++) {
            V[row][0] = 0;
        }
        for (int i = 1; i <= N; i++) {  //一行一行填充值
            for (int j = 1; j <= W; j++) {  //一列一列填充值
                if (weight[i - 1] <= j) {  //如果当前物品重量小于等于背包中的当前重量 i为1是，weight[0]是第一个物品的重量
                    //比较不加入该物品时该重量的最大价值（前一行）与当前物品的价值+可以容纳的剩余重量的价值
                    V[i][j] = Math.max(val[i-1] + V[i-1][j - weight[i-1]],V[i-1][j]);
                } else { //如果当前物品重量大于背包中的当前重量
                    V[i][j]=V[i-1][j];  //直接使用前一行的最优解
                }
            }
        }
        /*打印矩阵
        for (int[] rows: V) {
            for (int col : rows) {
                System.out.format("%5d",col);
            }
            System.out.println();
        }*/
        return V[N][W];

    }

```

* <font color=blue>连接里的图表很有用，注意看</font>





### 5.4 Interval Scheduling 区间调度问题

https://blog.csdn.net/qq_40991687/article/details/104995441?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522167753680616782425122596%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=167753680616782425122596&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~baidu_landing_v2~default-2-104995441-null-null.142

* 什么是区间调度问题？
* Here we have a collection of tasks (or intervals of requested time to use a room, etc.), and a single machine that can process these tasks (or a single room in which meetings can be held, etc.).
* 这里我们有一组任务(或使用某个房间的请求时间间隔等)，以及一台可以处理这些任务的机器(或可以举行会议的单个房间等)。
* : We want to select a subset of the tasks in order to maximize the number of tasks that we can schedule on the machine.
* 我们希望选择任务的一个子集，以最大化我们可以在机器上调度的任务数量。
* <font color=blue>注意一下，最大化工作的数量，而不是时间</font>
* ![image-20230227223027949](D:\笔记\笔记图片\image-20230227223027949.png)

* 1. **<font color=red>在可选的工作中，每次都选取结束时间最早的工作。</font>**
  2. **<font color=red>在可选的工作中，每次都选取用时最短的工作。</font>**
  3. **<font color=red>在可选的工作中，每次都选取与最少可选工作有重叠的工作。</font>**

![image-20230227223302448](D:\笔记\笔记图片\image-20230227223302448.png)



![image-20230227223741810](D:\笔记\笔记图片\image-20230227223741810.png)

<font color=red size=6>课堂内容</font>

* We now consider a problem sometimes referred to as the Interval Scheduling Problem.
* 我们现在考虑一个有时被称为区间调度问题的问题。
* Here we have a collection of tasks (or intervals of requested time to use a room, etc.), and a single machine that can process these tasks (or a single room in which meetings can be held, etc.).
* 这里我们有一组任务(或请求使用房间的时间间隔等)，以及一台可以处理这些任务的机器(或一个可以举行会议的房间等)。
* Goal: We want to select a subset of the tasks in order to maximize the number of tasks that we can schedule on the machine.
* 目标:我们希望选择任务的一个子集，以便最大化我们可以在机器上调度的任务数量



* **More formally (and keeping with the task/machine terminology), suppose we are given a set T of n tasks, where each task i has a start time si and a finish (or completion) time fi .**
* **更正式地说(并与任务/机器术语保持一致)，假设我们给定一个由n个任务组成的集合T，其中每个任务i有一个开始时间si和一个结束(或完成)时间fi。**
* **Two tasks i and j are non-conflicting (or compatible) if**
* **如果两个任务i和j不冲突(或兼容)**
* ![image-20230520160943242](D:\笔记\笔记图片\image-20230520160943242.png)
* So two tasks can be executed on the machine only if they are non-conflicting.
* 因此，只有当两个任务不冲突时，它们才能在机器上执行。
* <font color=red>**Goal: Select a maximum size subset of non-conflicting tasks.**</font>
* **目标:选择非冲突任务的最大大小子集。**
* **<font color=red>Order the tasks in terms of their completion times.</font> Then select the task that finishes first, remove all tasks that conflict with this one, and repeat until we’re done.**
* **根据完成时间对任务进行排序。然后选择第一个完成的任务，删除所有与这个任务冲突的任务，重复直到我们完成。**
* <font color=blue size=5>这一部分考虑的是在同一台机器完成尽可能多的任务</font>

![image-20230227223805634](D:\笔记\笔记图片\image-20230227223805634.png)

* 说实话我觉得老师这个伪代码给的不是很好。能表达，但是怪怪的
* 首先需要对事件集T进行排序，按照结束时间，此时的时间复杂度一般为nlogn
* 然后对T进行循环，将合适的任务添加到新的集合A中
* 故，<font color=red size=5>该算法的时间复杂度一般为nlogn</font>

    IntervalScheduling(T):
        Sort T based on the end time of each interval in non-decreasing order
    	result = []
    	lastEndTime = 0
    
    for interval in T:
        if interval.start >= lastEndTime:
            result.append(interval)
            lastEndTime = interval.end
    
    return result

![image-20230520175750699](D:\笔记\笔记图片\image-20230520175750699.png)

* Theorem: The algorithm IntervalSchedule returns a set of non-compatible tasks having maximum size. 
* 定理:算法IntervalSchedule返回一组具有最大大小的不兼容任务。
* Furthermore, we can make this algorithm run in time O(n log n) (the main time will lie in sorting the tasks by their completion times).
* 此外，我们可以使该算法在O(n log n)时间内运行(主要时间在于根据任务的完成时间对任务进行排序)。

![image-20230520162246391](D:\笔记\笔记图片\image-20230520162246391.png)

![image-20230520162329837](D:\笔记\笔记图片\image-20230520162329837.png)

![image-20230520162339118](D:\笔记\笔记图片\image-20230520162339118.png)

![image-20230520162412878](D:\笔记\笔记图片\image-20230520162412878.png)



**<font color=red size=6>这里又是想干嘛？</font>**

### 5.5 Task Scheduling 任务调度问题

* <font color=blue size=5>这一部分考虑的是使用尽可能少的机器完成全部的任务</font>

![image-20230520164928681](D:\笔记\笔记图片\image-20230520164928681.png)

* In this case, a greedy algorithm will still work to solve this problem. 
* 在这种情况下，贪婪算法仍然可以解决这个问题。
  * <font color=red size=5>**This time we consider the tasks ordered by their start times.** </font>
  * **这一次，我们考虑按开始时间排序的任务。**
* Then for each task i, if we have the machine that can handle task i, it is scheduled on that machine. 
* 然后对于每个任务i，如果我们有一台可以处理任务i的机器，它就会被调度到那台机器上。
* Otherwise, we allocate a new machine, schedule task i on it, and repeat the greedy selection process until we have considered all tasks in T.
* 否则，我们分配一台新机器，在其上调度任务i，并重复贪婪选择过程，直到我们考虑了T中的所有任务。

    MachineScheduling(T):
        Sort T based on the start time of each task in non-decreasing order
    	machines = []
    
    for task in T:
        assigned = False
    
        for machine in machines:
            if task does not conflict with any task on machine:
                assign task to machine
                assigned = True
                break
        
        if not assigned:
            create a new machine and assign task to it
            machines.append(new machine)
    
    return machines

* **这个算法的时间复杂度是nlogn+n*m（n是事件的数量，m是机器的数量），一般来说，机器肯定比事件少，所以可以写成nlogn**



![image-20230520165550448](D:\笔记\笔记图片\image-20230520165550448.png)

* Theorem: Given an instance of the Task Scheduling Problem with a set of n tasks, the algorithm TaskSchedule produces a schedule of the tasks with the minimum number of machines in **O(n log n)** time.
* 定理:给定一个有n个任务的任务调度问题实例，TaskSchedule算法在**O(n log n)**时间内生成机器数量最少的任务调度。

* <font color=black size =5>解释说明：</font>
* We want to show that this greedy algorithm produces a schedule that uses the smallest number of machines. 
* 我们想要证明贪婪算法产生的调度使用的机器数量最少。
* Suppose that our method finds a schedule that uses k machines, but that there is some other (non-conflicting) schedule that uses at most k − 1 machines. 
* 假设我们的方法找到了一个使用k台机器的调度，但是存在其他一些(不冲突的)调度，最多使用k−1台机器。
* Let k denote the last machine allocated by our algorithm, and let i be the first task that we scheduled on machine k. 
* 设k表示我们算法分配的最后一台机器，设i是我们在机器k上调度的第一个任务。
* Now, from how our algorithm works, when we scheduled task i, we used the new machine k because each of the other tasks had tasks already scheduled on them. **Because we consider the tasks ordered by their start times, each of these other tasks have a start time that began before si , and since they conflict with task i, each of them has a finish time after si .**
* 现在，从我们算法的工作原理来看，当我们调度任务i时，我们使用了新的机器k因为其他任务上都有已经调度的任务。因为我们考虑按开始时间排序的任务，**<font color=red>所以这些其他任务的开始时间都在si之前开始，并且由于它们与任务i冲突，因此每个任务的结束时间都在si之后。</font>**
* This means that each of these other k − 1 tasks not only conflict with task i, they conflict with each other too!
* 这意味着每一个其他k−1个任务不仅与任务i冲突，它们也相互冲突!
* So this means we have a set of k tasks in T that all conflict with each other, hence it is impossible to schedule them using k − 1 machines (contradicting our assumption that there is a schedule that uses only k − 1 machines).
* 因此，这意味着我们在T中有k个相互冲突的任务，因此不可能使用k−1台机器来调度它们(与我们假设存在只使用k−1台机器的调度相矛盾)。
* Hence, k is the minimum number of machines needed to schedule all tasks in T, and our greedy method gives us an optimal solution.
* 因此，k是调度T中所有任务所需的最小机器数量，我们的贪婪方法给出了一个最优解。



### 5.6 Clustering 聚类

* Clustering arises when we try to group together or classify a collection of objects (photographs, documents, microorganisms, etc) **based on the idea of distance.** 
* 当我们试图**根据距离的概念**将一组对象(照片、文档、微生物等)分组或分类时，就会出现聚类。
* For example, we might characterize the “distance” between two documents using the edit distance, i.e. the number of characters that you have to add, delete, or alter to transform one document into another. 
* 例如，我们可以使用编辑距离来描述两个文档之间的“距离”，即必须添加、删除或更改以将一个文档转换为另一个文档的字符数量。
* For photographs, we might use the number of pixels at which their color differs by some threshold (of the wavelength of light), or by the intensity of the light, etc. 
* 对于照片，我们可能会使用像素的数量，在这些像素上，它们的颜色因某些阈值(光的波长)或光的强度而不同，等等。
* For microorganisms (or animals), the distance could be the number of years since they diverged on the evolutionary scale.
* 对于微生物(或动物)来说，这个距离可以是它们在进化尺度上分道扬镳的年数。

![image-20230520175450106](D:\笔记\笔记图片\image-20230520175450106.png)

* Regardless of what we use for distance, we will assume that we have a collection of n objects p1, p2, . . . , pn, together with a distance function, i.e. a function that satisfies the three properties that
* 不管我们用什么来表示距离，我们假设我们有一个n个对象的集合p1, p2，…， pn，以及距离函数，即满足以下三个性质的函数

* Suppose that we want to group the objects into k (non-empty) clusters, C1, . . . , Ck .
* 假设我们想要将对象分组到k(非空)簇，C1，…， Ck。



* In particular, given a clustering C1, . . . , Ck , define the spacing of the clustering to be the minimum distance between any pair of points lying in different clusters. 
* 特别地，给定一个聚类C1，…， Ck将聚类的间距定义为位于不同聚类中的任意对点之间的最小距离。
* Our goal is, given the n objects and the value k, find a k-clustering with maximum spacing. 
* 我们的目标是，给定n个对象和k值，找到一个具有最大间距的k聚类。
* How do we do this?

![image-20230520180610992](D:\笔记\笔记图片\image-20230520180610992.png)

* <font color=red size=5>最终的结果是一组聚类，其中同一簇内的数据点之间的距离最小化，而不同簇之间的距离最大化。</font>
* **<font size=5>Maximum Spacing Clustering</font>**

* We can consider the idea of building a graph, where the objects p1, . . . , pn are the vertices of the graph. 
* 我们可以考虑建立一个图，其中对象p1，…， pn是图的顶点。
* The connected components of the graph that we build will be the clusters. We want to try to bring objects that are close together into the same cluster, as quickly as possible (so that they don’t end up in different clusters). 
* 我们构建的图的连接组件将是集群。我们希望尽可能快地将靠近的对象放到同一个集群中(这样它们就不会在不同的集群中结束)。
* So, we take the two closest objects, and add an edge between them (as the first edge in our graph). 
* 因此，我们取两个最接近的对象，并在它们之间添加一条边(作为图中的第一条边)。
* Then take the next two closest objects and add an edge between them.
* 然后取下两个最近的物体并在它们之间添加一条边。
* We continue, considering the distances between pairs in increasing order. So we are growing a graph on the n objects. If we are about to add an edge between two objects that are already in the same cluster, then we don’t bother doing so (as this gives us no additional information about the clustering).
* 我们继续，以递增的顺序考虑对之间的距离。我们要在n个对象上画一个图。如果我们打算在已经在同一集群中的两个对象之间添加一条边，那么我们就不用这么做了(因为这不会给我们提供关于集群的额外信息)。
* This means that during our clustering process, we never form a cycle in our graph. Adding an edge corresponds to merging two clusters into one.
* 这意味着在我们的聚类过程中，我们不会在图中形成一个循环。添加一条边相当于将两个簇合并为一个。
* (We can consider starting the process with n clusters, each object belonging to its own cluster.)
* (我们可以考虑用n个集群开始这个过程，每个对象属于它自己的集群。)
* If you think about this process, the procedure we are following is exactly the same as that for Kruskal’s algorithm for finding a minimum spanning tree of a graph. 
* 如果你考虑一下这个过程，我们所遵循的过程和Kruskal算法中寻找图的最小生成树的过程是完全一样的。
* We add edges in increasing order of the edge length, without ever creating a cycle. 
* 我们按边长递增的顺序添加边，而不需要创建一个循环。
* In this case, we can stop Kruskal’s algorithm when we have a graph that has exactly k connected components. Or, equivalently, if we run Kruskal’s algorithm, and then delete the last k − 1 edges that were added, this will result in a k-clustering of maximum spacing.
* 在这种情况下，当我们有一个恰好有k个连通分量的图时，我们可以停止Kruskal算法。或者，同样地，如果我们运行Kruskal的算法，然后删除最后添加的k−1条边，这将导致最大间距的k聚类。

![image-20230520191701380](D:\笔记\笔记图片\image-20230520191701380.png)

* Given n objects, and the collection of their pairwise distances, a maximum spacing k -clustering can be found in time O(n^2 log n).
* 给定n个对象及其成对距离的集合，可以在时间O(n^2logn)内找到最大间距k -聚类
* (The main bottleneck is to perform the sort of the pairwise distances.)
* (主要的瓶颈是执行成对距离排序。)

* <font size=5>证明过程：</font>
* ![image-20230520191856519](D:\笔记\笔记图片\image-20230520191856519.png)





## Week6

## 6. Complexity of Algorithms Fundamental Solution Techniques Dynamic Programming

### 6.1 Dynamic Programming 动态规划

* The Dynamic Programming technique is somewhat similar to Divide-and-Conquer algorithms. 
* 动态规划技术有点类似于分治算法。
* The main difference is that (possibly) repetitive recursive calls are replaced by a reference to already computed values stored in a special table
* 主要区别在于(可能)重复的递归调用被对存储在特殊表中的已计算值的引用所取代

![image-20230520192233018](D:\笔记\笔记图片\image-20230520192233018.png)

* <font size=5>动态规划和分治算法最大的不同是，动态规划得到的子问题往往不相互独立，会互相影响。而分治算法不会！！！</font>



* Dynamic programming is primarily used for optimization problems (maximizing or minimizing some function).
* 动态规划主要用于优化问题(最大化或最小化某些函数)。
* It is often applied where a brute force search for optimal value is infeasible.
* 它通常应用于暴力搜索最优值是不可行的地方。
* However, dynamic programming is efficient only if the problem has a certain amount of structure that can be exploited.
* 然而，只有当问题具有一定数量的可利用结构时，动态规划才是有效的。
* An effective dynamic programming solution depends on the following factors:
* 一个有效的动态规划方案取决于以下因素:
  * **Simple sub-problems: <font color=red>There must be a way of breaking the whole problem into smaller sub-problems which have a similar structure.</font>**
  * **简单的子问题:必须有一种方法将整个问题分解成具有相似结构的更小的子问题。**
  * **Sub-problem optimality:<font color=red> An optimal solution to the global problem must be composed of optimal solutions to a sub-problem, or collection of sub-problems.</font>**
  * **子问题最优性:全局问题的最优解必须由子问题或子问题集合的最优解组成。**
  * **Sub-problem overlap: <font color=red>Optimal solutions to some sub-problems can themselves contain sub-problems in common (and often do).</font>**
  * **子问题重叠:某些子问题的最优解本身可能包含共同的子问题(而且经常如此)。**

* <font size=5>动态规划解决问题的一般思路</font>

* A typical approach to solve a problem using Dynamic Programming is to first find a recursive solution to the problem. 
* 使用动态规划解决问题的典型方法是首先找到问题的递归解。
* Once this recursive solution is found, we then try to determine a way to compute solutions to the subproblems “from the bottom up”, so that we avoid recomputing solutions many times.
* 一旦找到这个递归解，我们就会尝试确定一种“自下而上”计算子问题解的方法，这样我们就可以避免多次重新计算解。



### 6.2 {0 1}Knapsack Problem

https://blog.csdn.net/Biteht/article/details/124651895?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522167752801716800211569182%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=167752801716800211569182&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_positive~default-2-124651895-null-null.142

![image-20230520145236759](D:\笔记\笔记图片\image-20230520145236759.png)

* 这个图虽然草率了一点，但是很清晰
* 比如我们一开始有一个f(4,8),可以放四个物品，负重最多为8
* 由上图我们可以得到：
* ![image-20230520145551732](D:\笔记\笔记图片\image-20230520145551732.png)
* ![image-20230520145627955](D:\笔记\笔记图片\image-20230520145627955.png)


```
/**
     * 0-1背包
     * @param val 价值
     * @param weight 重量
     * @param W 背包容量
     * @return 最优解
     */
    public static int func(int[] val, int[] weight, int W) {
        int N = weight.length;   //记录所有的物品数
        int[][] V = new int[N + 1][W + 1];  //创建背包矩阵
        //初始化矩阵 列，背包容量为0
        for (int col = 0; col <= W; col++) {
            V[0][col] = 0;
        }
        for (int row = 0; row <= N; row++) {
            V[row][0] = 0;
        }
        for (int i = 1; i <= N; i++) {  //一行一行填充值
            for (int j = 1; j <= W; j++) {  //一列一列填充值
                if (weight[i - 1] <= j) {  //如果当前物品重量小于等于背包中的当前重量 i为1是，weight[0]是第一个物品的重量
                    //比较不加入该物品时该重量的最大价值（前一行）与当前物品的价值+可以容纳的剩余重量的价值
                    V[i][j] = Math.max(val[i-1] + V[i-1][j - weight[i-1]],V[i-1][j]);
                } else { //如果当前物品重量大于背包中的当前重量
                    V[i][j]=V[i-1][j];  //直接使用前一行的最优解
                }
            }
        }
        /*打印矩阵
        for (int[] rows: V) {
            for (int col : rows) {
                System.out.format("%5d",col);
            }
            System.out.println();
        }*/
        return V[N][W];

    }

```

* <font color=blue>连接里的图表很有用，注意看</font>

* <font size=5>{0,1}背包问题的课堂论述</font>

![image-20230520211317125](D:\笔记\笔记图片\image-20230520211317125.png)

* The running time of 01KNAPSACK is dominated by the two nested “for” loops, where the outer loop iterates n times, and the inner loop W times.
* 01KNAPSACK的运行时间主要由两个嵌套的“for”循环支配，其中外部循环迭代n次，内部循环迭代W次。
* **<font color=red size=5>Theorem: The 01KNAPSACK algorithm finds a highest benefit subset of S with total weight at most W in O(nW) time.</font>**
* **<font color=red size=5>该定理： 01KNAPSACK算法在O(nW)时间内找到一个总权重最多为W的S的最高利益子集。</font>**



### 6.3 Weighted Interval Scheduling 加权区间调度

* A related problem we consider is Weighted Interval Scheduling. 
* 我们考虑的一个相关问题是加权区间调度。
* Here we still have a collection of n intervals (or tasks). Each interval has a start time si and a finish time fi . Furthermore, each interval has a value vi . 
* 这里我们仍然有n个区间(或任务)的集合。每个间隔有一个开始时间si和一个结束时间fi。此外，每个区间都有一个值vi。
* **Goal: In this case, the aim is to schedule a subset of non-conflicting intervals having maximum total value**
* **目标:在这种情况下，目标是调度具有最大总价值的非冲突间隔子集。**
* ![image-20230520225538773](D:\笔记\笔记图片\image-20230520225538773.png)

* 

![image-20230520225615161](D:\笔记\笔记图片\image-20230520225615161.png)

* <font color=red size=5>注意，我理解了这个方法之后我才意识到另一个事情，老师说的方法似乎和这个有些区别, 索性差别不大</font>
* https://blog.csdn.net/qq_37657182/article/details/102891495?ops_request_misc=&request_id=&biz_id=102&utm_term=%E5%8A%A0%E6%9D%83%E5%8C%BA%E9%97%B4%E8%B0%83%E5%BA%A6&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduweb~default-3-102891495.142
* 下面这个是关于老师的方法：

![image-20230520230451804](D:\笔记\笔记图片\image-20230520230451804.png)

* **设p ( j ) p(j)p(j)是与任务j jj相容的最大下标的任务，如：p ( 8 ) = 1 , p ( 7 ) = 3 , p ( 2 ) = 0 p(8)=1,p(7) = 3, p(2)=0p(8)=1,p(7)=3,p(2)=0 （通过二分搜索计算）** 划重点
* 另外，关于寻找相容的任务这件事情上，**<font color=red size=5>我们寻找的是距离任务i最近，且不冲突的任务的索引，如果存在多个不冲突索引，找结束时间最近得那一个</font>**

![image-20230520230607414](D:\笔记\笔记图片\image-20230520230607414.png)

![image-20230520231629704](D:\笔记\笔记图片\image-20230520231629704.png)



<font color=red size=6>我认为这里需要好好问一下,时间复杂度为什么为nlogn</font>



## Week7 Complexity of Algorithms Graphs

### 7. Complexity of Algorithms Graphs

#### 7.1 Connectivity information

* Connectivity information can be defined by many kinds of relationships that exist between pairs of objects. 
* 连接信息可以通过存在于对象对之间的多种关系来定义。
* For example, connectivity information is present in city maps, where the objects are roads, and also in the routing tables for the Internet, where the objects are computers. 
* 例如，连通性信息存在于城市地图中，其中的对象是道路，也存在于互联网路由表中，其中的对象是计算机。
* Connectivity information is also present in the parent-child relationships defined by a binary tree, where the objects are tree nodes. 
* 连通性信息也存在于由二叉树定义的父子关系中，其中的对象是树节点。
* **Graphs are one way in which connectivity information can be stored, expressed, and utilized.**
* **图是存储、表示和利用连接性信息的一种方式。**

#### 7.2 Graphs 图像

* <font color=red>**A graph is a set of objects, called vertices (or nodes), together with a collection of pair-wise connections, called edges, between them.** </font>
* **图是一组对象，称为顶点(或节点)，以及它们之间成对连接的集合，称为边。**
* Graphs have applications in a number of different domains, including
* 图在许多不同的领域都有应用，包括
  * mapping (geographic information systems); 
  * 制图(地理信息系统);
  * transportation (road and flight networks); 
  * 交通(道路和飞行网络);
  * electrical engineering (circuit design); 
  * 电气工程(电路设计);
  * process scheduling (job makespans and assembly-line scheduling); and 
  * 流程调度(作业完成时间和装配线调度);和
  * computer networking (connectivity of networks)
  * 计算机网络(网络连接)
* <font color=red>**More formally, a graph G = (V, E), is a set, V, of vertices and a collection, E, of pairs of vertices from V, called edges.**</font>
* **更正式地说，图G = (V, E)是顶点的集合V和来自V的顶点对的集合E，称为边。**
* **Edges in a graph are either directed or undirected.**
* **图中的边可以是有向的，也可以是无向的。**
  * **An edge (u, v) is said to be directed from u to v if the pair (u, v) is ordered. If all edges of a graph are directed, we usually refer to G as a digraph.**
  * **如果对(u, v)是有序的，则说边(u, v)是从u指向v的。如果一个图的所有边都是有向的，我们通常称G为有向图。**
  * **An edge (u, v) is said to be undirected if the pair (u, v) is unordered. Typically, undirected edges are written as {u, v} (using braces instead of parentheses).**
  * **如果对(u, v)是无序的，则称边(u, v)是无向的。通常，无向边被写成{u, v}(使用大括号代替圆括号)。**

* **<font color=red>在图论中，一个图被称为连通的（Connected），如果图中的每一对顶点之间都存在一条路径。也就是说，从任意顶点出发，都能通过一系列的边达到任意其他的顶点。</font>**

![image-20230521113019927](D:\笔记\笔记图片\image-20230521113019927.png)

##### 7.2.1 Graph Terminology 图的术语

* Two **vertices** are said to be <font color=red>**adjacent**</font> if they are end-points of the same edge. 
* 如果两个**顶点**是同一条边的端点，则称它们<font color=red>**相邻**</font>。
* An edge is said to be **incident to a vertex** if the vertex is one of its end-points. 
* 如果一个顶点是某条边的一个端点，那么我们就说这条边与**这个顶点是邻接的**。
* An outgoing edge of a vertex is a directed edge whose origin is that vertex. 
* 一个顶点的外向边是一条有向边，其原点是该顶点。
* <font color=blue>由某一个点指向其他位置</font>
* An **incoming edge** of a vertex is a directed edge whose destination is that vertex
* 对于一个顶点，如果有一条有向边的方向指向该顶点，那么我们就说这条有向边是顶点的入边（incoming edge）。
* <font color=blue>注意是指向该顶点，并不是由该顶点指向</font>

![image-20230521114002021](D:\笔记\笔记图片\image-20230521114002021.png)

* **The degree of a vertex v**, denoted deg(v), is the number of edges incident to v. 
* 顶点v的度数，**记作deg(v)**，**<font color=red>是与v相关的边的个数。</font>**
* In a directed graph, the in-degree (out-degree) of a vertex v is the number of **incoming (outgoing) edges** of v, and is denoted by **indeg(v) (outdeg(v)).**
* 在有向图中，顶点v的进(出)度是顶点v的进(出)边的个数，用**indeg(v) (outdeg(v))**表示。
* ![image-20230521114131982](D:\笔记\笔记图片\image-20230521114131982-16846657035795.png)

* We have the following two elementary results about graphs.
* 我们有以下两个关于图的基本结果。
* <font color=red>因为是重复运算，所以为2m</font>
* ![image-20230521120005513](D:\笔记\笔记图片\image-20230521120005513.png)

* **An undirected graph G is said to be simple if there is at most one edge between each pair of vertices u and v.** 
* **无向图G是简单的，如果在每一对顶点u和v之间最多有一条边。**
* **A digraph is simple if there is at most one directed edge from u to v for every pair of distinct vertices u and v.**
* **有向图是简单的，如果对于每一对不同的顶点u和v，从u到v最多有一条有向边。**
* Theorem: Let G be a simple graph with n vertices and m edges.
* 定理:设G是一个n顶点m边的简单图。
  * ![image-20230521120054321](D:\笔记\笔记图片\image-20230521120054321.png)

##### 7.2.2 More graph terminology

* A walk in a graph is a sequence of alternating vertices and edges, starting at a vertex and ending at a vertex. 
* 图中的行走是一个交替的顶点和边的序列，从一个顶点开始，结束于一个顶点。
* A path is a walk where each vertex in the walk is distinct. 
* 路径是一种行走，其中每个顶点都是不同的。
* A circuit is a walk with the same start and end vertex. 
* 环路是具有相同起始点和结束点的行走。
* A cycle is a circuit where each vertex in the circuit is distinct (except for first and last vertex). 
* 循环是一个回路，其中每个顶点都是不同的(除了第一个顶点和最后一个顶点)。
* **A directed walk is a walk in which all edges are directed and are traversed along their direction. Directed paths, circuits, and cycles are defined similarly.**
* **有向行走是一种行走，其中所有的边都是有向的，并沿着它们的方向遍历。有向路径、电路和周期的定义类似。**

![image-20230521120546978](D:\笔记\笔记图片\image-20230521120546978.png)



* If G is a simple graph, then giving the sequence of vertices is sufficient to describe a walk, path, circuit, or cycle (as then the edges are implied). 
* 如果G是一个简单的图，那么给出顶点序列就足以描述行走、路径、回路或循环(因为边是隐含的)。
* For example, the path joining G and B on the previous slide could be (more compactly) represented as
* 例如，在上一张幻灯片中，连接G和G的路径可以(更紧凑地)表示为
* ![image-20230521121215096](D:\笔记\笔记图片\image-20230521121215096.png)

* Similarly the cycle could be written as
* 同样，这个循环可以写成
  * ![image-20230521121247162](D:\笔记\笔记图片\image-20230521121247162.png)

##### 7.2.3 森林 Forest

* **A forest is a graph without cycles.** 
* **森林是一个没有循环的图。**
* A tree is a connected forest, i.e. a connected graph without cycles. 
* 树是连通森林，即无环连通图。
* A tree with a distinguished node (root) is called a rooted tree, otherwise it is called a free tree (or, often, simply a tree). 
* 具有不同节点(根)的树称为有根树，否则称为自由树(或者通常简称为树)。
* A spanning tree of a graph is a spanning subgraph that is a free tree.
* 一个图的生成树是一个生成子图，它是一棵自由树。

* 在图论中，"森林"（Forest）被定义为一个无环图，也就是说，森林是由若干棵树（Tree）组成的图。一棵树是一种特殊的图，它是连通的（即从任何一个顶点都可以到达任何其他顶点）并且没有环。
* 所以，森林可以被视为是一种特殊类型的图，其中每个连通分量（也就是每个独立的部分）都是一棵树。这意味着森林可以由一个或多个树组成，或者它可以是一个空图（即没有顶点或边的图）。
* 如果一个森林只包含一个树，那么这个森林就是这棵树本身。如果一个森林包含多个树，那么这些树是不相交的，也就是说，没有边会连接两棵不同的树。
* **<font color=red size=5>前提条件是无向图！！！</font>**

![image-20230521125227716](D:\笔记\笔记图片\image-20230521125227716.png)

* 1.情况一中，G是一个环，我们可以轻松得到m>=n-1
* 2.结合树的定义去看
* 3.**因为森林由若干树构成，所以有：m1=n1-1, m2=n2-1 m=m1+m2 => m1+m2 = n1 +n2 -1 -1 => m<=n-1**

##### 7.2.4 Representing Graphs

* **Linked List**

![image-20230521130010913](D:\笔记\笔记图片\image-20230521130010913.png)

* **Adjacency Matrix**

![image-20230521130202142](D:\笔记\笔记图片\image-20230521130202142.png)

#### 7.3 Digraphs 有向图

* <font color=red>**A digraph is a graph whose edges are all directed.** </font>
* **有向图是边都是有向的图**。
* A fundamental issue with directed graphs is the notion of reachability, which deals with determining where we can get to in a directed graph. 
* 有向图的一个基本问题是可达性的概念，它决定了我们在有向图中可以到达的位置。
* **Given two vertices u and v of a digraph G, we say that u reaches v (or v is reachable from u) if G has a directed path from u to v.**
* **给定有向图G的两个顶点u和v，如果G有一条从u到v的有向路径，我们说u到达v(或者v可以从u到达)。**
* **<font color=red>在图论中，一个图被称为连通的（Connected），如果图中的每一对顶点之间都存在一条路径。也就是说，从任意顶点出发，都能通过一系列的边达到任意其他的顶点。</font>**



* A digraph G is **strongly connected** if, for **any two distinct vertices u and v, we have that u reaches v, and v reaches u.**
* 一个有向图G是**强连通的**，如果对于**任意两个不同的点u和v，我们有u到达v, v到达u。**
* <font color=red>前提条件是左右方向相同</font>
* A directed cycle of G is a cycle where all the edges are traversed according to their respective directions. 
* G的有向环是指所有的边都按照各自的方向经过的环。
* **有向环必须沿着边的指向方向移动, 并且最终回到起始位置**
* A digraph is **acyclic** if it has no directed cycles.
* 如果一个有向图没有有向环，它就是**无环**。



##### 7.3.1 Graph Search Methods 图像的搜索方法

* Two common methods for exploring graphs are **the Depth-First Search (DFS)** and **Breadth-First Search (BFS)** methods. 
* 探索图的两种常用方法是**<font color=red>深度优先搜索(DFS)</font>**和**<font color=red>宽度优先搜索(BFS)</font>**方法。
* **As a very brief reminder, DFS starts at a vertex, chooses an edge from that vertex and “walks out as far as possible”, finding new vertices until it encounters one it has already seen, then it backs up (as little as possible) to find other un-encountered vertices.** 
* **作为一个非常简单的提示，DFS从一个顶点开始，从那个顶点选择一条边，然后“走得尽可能远”，寻找新的顶点，直到遇到一个它已经见过的顶点，然后它返回(尽可能少)去寻找其他未遇到的顶点。**
* **In contrast to the DFS method, the Breadth First Search algorithm starts at a vertex and first explores the entire neighborhood of that vertex before moving onto another vertex**
* **与DFS方法相反，广度优先搜索算法从一个顶点开始，在移动到另一个顶点之前首先探索该顶点的整个邻域**

![image-20230521131711883](D:\笔记\笔记图片\image-20230521131711883.png)

* **DFS是尽可能的向下找，直到找不到了为止**
* **BFS是在同级中尽可能的找，直到找不到了开始找下一层**



* Therefore, the DFS method generates “long, skinny” search trees, while the BFS method generates “short, bushy” ones. 
* 因此，DFS方法生成“长而细”的搜索树，而BFS方法生成“短而密”的搜索树。
* **The running time of BFS and DFS is the same, namely O(n + m).** 
* **BFS和DFS的运行时间相同，均为O(n + m)。**
* Generally speaking, we may utilize a stack data structure to control a DFS search, while a queue data structure may be used for a BFS search. 
* 一般来说，我们可以使用堆栈数据结构来控制DFS搜索，而队列数据结构可以用于BFS搜索。
* 堆的很好理解，但是这里需要解释一下队列的，**注意队列的特点是先进先出**
* ![image-20230521132429974](D:\笔记\笔记图片\image-20230521132429974.png)
* ![image-20230521132447378](D:\笔记\笔记图片\image-20230521132447378.png)
* We will not go into great detail about these search methods here. Any book on (graph) algorithms should contain more detailed descriptions of these procedures.
* 在这里，我们不会详细讨论这些搜索方法。任何关于(图)算法的书都应该包含这些过程的更详细的描述。



* BFS and DFS can be used to answer a variety of questions about graphs including: 
* BFS和DFS可以用来回答关于图的各种问题，包括:
  * Testing whether G is connected. 
  * 测试G是否连通。
  * Computing the connected components of G. 
  * 计算G的连通分量。
  * Finding a spanning forest of G (or spanning tree if G is connected). 
  * 找到G的生成森林(如果G是连通的，则为生成树)。
  * Searching for a cycle in G, or reporting that G is acyclic. 
  * 在G中寻找环，或者报告G是非环。
  * Given a start vertex x of G, computing, for every vertex v of G, a path with the minimum number of edges between x and v, or reporting that no such path exists (BFS). 
  * 给定G的起始顶点x，对于G的每个顶点v，计算x和v之间具有最小边数的路径，或者报告不存在这样的路径(BFS)。
  * Testing for strong connectivity of digraphs. (Is there a directed path from u to v, for all u and v in D?)
  * 测试有向图的强连通性。(对于D中的所有u和v，是否存在从u到v的有向路径?)



#### 7.4 Weighted Graphs 权重图

* **<font color=red>A weighted graph is a graph that has a numerical label w(e) associated with each edge e, called the weight of e.</font>** 
* **加权图是一个与每条边e相关联的数字标签w(e)的图，称为e的权重。**
* Alternatively, we might sometimes **consider graphs having weights on the vertices, or on both the vertices and edges.**
* 或者，我们有时可能会考虑**在顶点上或在顶点和边上都有权重的图。**



* Often in the case of weighted graphs, we want to consider the following problem: 
* 通常在加权图的情况下，我们要考虑以下问题:
* For some fixed vertex v, find a shortest path from v to all other vertices u != v in G (viewing weights on edges as distances between adjacent vertices).
* 对于某些固定的顶点v，找到从v到G中所有其他顶点u != v的最短路径(将边的权重视为相邻顶点之间的距离)。
* ![image-20230521133508705](D:\笔记\笔记图片\image-20230521133508705.png)
* **The distance from a vertex u to a vertex v in G, denoted d(u, v) is the value of a minimum length path (also called a shortest path) from u to v.**
* **G中顶点u到顶点v的距离，记作d(u, v)，是u到v的最小长度路径(也称为最短路径)的值。**
* **This problem is known as <font color=red>the Single-Source Shortest Path problem (SSSP for short)</font>.**
* **这个问题被称为单源最短路径问题(SSSP)。**



#### 7.5 Dijkstra’s algorithm 迪杰斯特拉算法

* Dijkstra’s algorithm算法是一种典型的最短路径算法，主要用于计算从一个结点到其他结点的最短路径。它主要的特点是以起始点为中心向外层层层扩展(广度优先搜索思想)，直到扩展到终点为止。
* **We assume that all edges in the graph have non-negative weights. (This is a requirement for Dijkstra’s algorithm to work correctly.)**
* **我们假设图中的所有边的权值都是非负的。(这是Dijkstra算法正常工作的必要条件。)**
* Let v be a source vertex and let D[u] represent the temporary distance in G from v to u. Initially we take D[v] = 0 and D[u] = +∞ for all u ！= v.
* 设v为源顶点，D[u]表示G中从v到u的临时距离。最初我们取D[v] = 0, D[u] = +∞对于所有u != v。
* At the start of the algorithm, all entries in the array D are temporary, but after each round of the algorithm one entry in D becomes fixed.
* 在算法开始时，数组D中的所有条目都是临时的，但在算法的每一轮之后，D中的一个条目变得固定。
* ![image-20230521162217743](D:\笔记\笔记图片\image-20230521162217743.png)

![image-20230521162226048](D:\笔记\笔记图片\image-20230521162226048.png)

![image-20230521163411311](D:\笔记\笔记图片\image-20230521163411311.png)

![image-20230521163427880](D:\笔记\笔记图片\image-20230521163427880.png)

* ![image-20230521164110922](D:\笔记\笔记图片\image-20230521164110922.png)

* **<font size=5>关于时间复杂度：</font>**
* Let G = (V, E) where |V| = n and |E| = m
* Construction of the initial heap for the set of n vertices takes time O(n log n).
* 构建n个顶点的初始堆需要O(n log n)时间。
* In each step of the “while” loop, getting the minimum entry from the heap requires O(log n) time (to update the heap), and then O(deg(u) log n) time to perform the edge relaxation steps (and update the heap as necessary).
* **在“while”循环的每一步中，从堆中获取最小条目需要O(log n)时间(更新堆)，然后O(deg(u) log n)时间来执行边缘松弛步骤(并在必要时更新堆)。**
* So the overall running time of the “while” loop is
* 所以while循环的总运行时间是
* ![image-20230521164432188](D:\笔记\笔记图片\image-20230521164432188.png)

* <font color=red size=5>注意dijkstra算法只能用于非负数权重之中，在另外一种方法Floyed-Warshall算法可以用于所有的最小路径问题SSSP</font>
* ![image-20230528143428128](D:\笔记\笔记图片\image-20230528143428128.png)
* ![image-20230521164839793](D:\笔记\笔记图片\image-20230521164839793.png)

* ![image-20230521161850459](D:\笔记\笔记图片\image-20230521161850459.png)



* ![image-20230521164822745](D:\笔记\笔记图片\image-20230521164822745.png)



## Week 8 

## 8. Complexity of Algorithms The Maximum Flow Problem Bipartite Matchings

### 8.1 Network Flow - The basics

* A flow network G = (V, E) is a directed graph in which each edge (u, v) ∈ E has a **<font color=red>non-negative integer capacity c(u, v) ≥ 0</font>**.
* 流网络G = (V, E)是一个有向图，其中每条边(u, V)∈E具有**非负整数容量c(u, V)≥0**。
* We distinguish two vertices in the flow network: **<font color=red>a source s and a sink t.</font>** We assume that s has no in-edges, and that t has no out-edges
* 我们在流网络中区分两个顶点:**源s**和**汇t**。我们**假设s没有入边，t没有出边**
* <font color=red>入边是指向是指向该节点的边，即边的起点不是该节点。出边是从该结点出发的边，即起点是该节点，但是终点不是</font>
* Each edge (u, v) also has an associated **<font color=red>flow value f(u, v)</font>** which tells us how much flow has been sent along an edge. These values satisfy **0 ≤ f(u, v) ≤ c(u, v)**.
* 每条边(u, v)也有一个相关的**流量值f(u, v)**，它告诉我们沿边发送了多少流量。这些值满足**0≤f(u, v)≤c(u, v)**。
* <font color=blue>在这里我们就可以得到：流网罗的每条边存在两个数字：</font>
* <font color=blue>1.流量（流量代表了当前实际通过该边的资源数量。）</font>
* <font color=blue>2. 容量（容量代表了可以通过该边的最大资源数量，可以理解为这条边的最大承载能力。流量不能超过边的容量）</font>
* **For every vertex other than s and t, the amount of flow into the vertex must equal the amount of flow out of the vertex.**
* **对于除s和t以外的每个顶点，流入顶点的流量必须等于流出顶点的流量。**
* <font color=red>流量不可以凭空产生或者消失</font>
* **In the maximum flow problem, we are given a flow network G, with source, s and sink, t and we wish to <font color=red>find a flow of maximum value from s to t.</font>**
* **在最大流量问题中，给定一个流网络G，源s和汇t，我们<font color=red>希望找到一个从s到t的最大值的流量。</font>**

![image-20230521213238550](D:\笔记\笔记图片\image-20230521213238550.png)

* 注意Network的条件：
* 1. s没有入边，t没有出边
  2. 每条线2个数值，且流量不大于容量
  3. 流入顶点的流量必须等于流出顶点的流量

### 8.2 Network Flow Algorithms 流网络算法（寻找从s->t的最大流量）

https://www.bilibili.com/video/BV1Pv41157xh/?spm_id_from=333.337.search-card.all.click&vd_source=9d046a6203dde4f5f1794bf980388e63

* **<font color=red size=5>这个链接，解释的非常清楚</font>**

* There are several algorithms for solving this maximum flow problem. 
* 有几种算法可以解决这个最大流量问题。
* One algorithm we will look at is the Ford-Fulkerson algorithm. 
* 我们要看的一个算法是Ford-Fulkerson算法。
* This algorithm searches for a **flow-augmenting path** from the source vertex s to the sink vertex t. 
* 该算法搜索从源顶点s到汇聚顶点t的**流增强路径**。
* We then send as much flow as possible along the **flow augmenting path**, whilst obeying the capacity constraints of each edge.
* 然后，我们沿着**流量增强路径发送尽可能多的流量**，同时服从每个边的容量约束。 
* **The maximum flow that we can send along the path is limited by the minimum of c(u, v) − f(u, v) of an edge on this path.**
* **我们可以沿着这条路径发送的最大流量受到c(u, v)−f(u, v)在这条路径上的最小值的限制。**

#### 8.2.1 Network Flows: Ford-Fulkerson Algorithm

* The Ford-Fulkerson algorithm depends on three important ideas 
* Ford-Fulkerson算法依赖于三个重要的思想
  * residual networks 
  * **残余网络（Residual Network）**：残余网络是从原图中派生出来的，它包含了原图中未使用的或者可逆转的容量。具体来说，如果一条边在原图中有容量c，并且已经有了流f，那么在残余网络中，这条边就有残余容量c-f，并且可以添加一个反向的边，其容量为f。这样做的好处是，我们可以在残余网络中寻找增广路径，增加流，而不需要直接修改原图。
  * augmenting paths 
  * 在网络流中，**增广路径（Augmenting Path）**是一个在残余网络（Residual Network）中从源点（source）到汇点（sink）的路径，这个路径表示我们可以通过它在当前流中增加更多的流量。增广路径的容量是由路径上残余容量最小的那条边决定的，因为这条边限制了我们可以通过这条路径传送的额外流量的最大值。
  * cuts 
  * **切割（Cut）和最大流最小割定理（Max-Flow Min-Cut Theorem）**：一个切割是将图分割成两部分的一种方式，使得源点在一侧，汇点在另一侧。**切割的容量是从源点一侧指向汇点一侧的边的容量之和**。**Ford-Fulkerson算法的终止条件就是找不到增广路径，这时候流的值等于任何切割的容量**，这就是最大流最小割定理。
* These three ideas are essential for the important Max-Flow/Min-Cut theorem.
* 这三个思想对于重要的是必不可少的
* 

![image-20230521222554399](D:\笔记\笔记图片\image-20230521222554399.png)

* The Ford-Fulkerson method is iterative
* Ford-Fulkerson方法是迭代的
  * Start with f(u, v) = 0 for all u, v ∈ V. I At each iteration, we increase flow by finding an **augmenting path** from s to t along which we can push more flow. (We consider the residual network when we search for augmenting paths.) 
  * 从f(u, v) = 0开始，对于所有u, v∈v . I在每次迭代中，我们通过寻找从s到t的增加路径来增加流量，我们可以沿着这条路径推动更多的流量。(我们在搜索增广路径时考虑残差网络。)
  * This process is repeated until no more **augmenting paths** can be found. 
  * 重复这个过程，直到找不到更多的扩展路径。
  * The Max-Flow Min-cut theorem shows us that this process yields a maximum flow.
  * 最大流量最小割定理告诉我们，这个过程产生最大流量。

![image-20230522003937955](D:\笔记\笔记图片\image-20230522003937955.png)

* 这是一个例子，说明了整个的流程

![image-20230521222958206](D:\笔记\笔记图片\image-20230521222958206.png)



#### 8.2.2 Residual Networks 残余网络

* **<font color=red size=5>这里还是非常建议去看一下上面的链接的网课，真挺好，很清楚，比课件清楚</font>**

* A residual network consists of edges that can admit more net flow. 
* **残余网络由可以容纳更多净流量的边组成。(<font color=blue>这个解释太玄学了，还是看下面这个</font>)**
* **残余网络（Residual Network）**：残余网络是从原图中派生出来的，它包含了原图中未使用的或者可逆转的容量。具体来说，如果一条边在原图中有容量c，并且已经有了流f，那么在残余网络中，这条边就有残余容量c-f，并且可以添加一个反向的边，其容量为f。这样做的好处是，我们可以在残余网络中寻找增广路径，增加流，而不需要直接修改原图。
* Given the flow network G, and a flow f in that network, we define **the residual network Gf** . (So this depends upon the given flow f.)
* 给定流网络G，以及该网络中的流f，我们**定义残余网络Gf**。(这取决于给定的流量f。)

* Gf has the same vertices as G. The edges of Gf are of two types:
  * **“Forwards edges” 正向边**
    * **常指的是从源点（source）到汇点（sink）或从某一顶点到另一顶点的边，这条边的方向与所期望的流动或移动的方向一致。**
    * For any edge (u, v) in G for which f(u, v) < c(u, v), there is an edge (u, v) in Gf . 
    * 对于G中f(u, v) < c(u, v)的任意边(u, v)，在Gf中存在一条边(u, v)。
    * The residual capacity ∆f(u, v) of (u, v) in Gf is defined as ∆f(u, v) = c(u, v) − f(u, v).、
    * (u, v)在Gf中的剩余容量∆f(u, v)定义为∆f(u, v) = c(u, v)−f(u, v)。
  * **“Backwards edges” 反向边**
    * **在网络流或图论中，"backward edge"（反向边）是一种特殊类型的边，主要用于在残余网络中表示已经通过某条边发送了一部分流量。**
    * **在算法中，这条线用来后悔，如果我们做出了错误的决定，可以通过nackward edges来修改**
    * For any edge (u, v) in G for which f(u, v) > 0, there is an edge (v, u) in Gf.
    * 对于G中f(u, v) > 0的任意边(u, v)，在Gf中存在一条边(v, u)。 
    * The residual capacity ∆f(v, u) of (v, u) in Gf is defined as ∆f(v, u) = f(u, v).
    * (v, u)在Gf中的剩余容量∆f(v, u)定义为∆f(v, u) = f(u, v)。

#### 8.2.3 Augmenting Paths 增量路径

* Given a flow network G = (V, E) and a flow f, an augmenting path P is a (directed) path from s to t in the residual network Gf . 
* 给定流网络G = (V, E)和流f，则增强路径P是残差网络Gf中从s到t的(有向)路径。
* Informally, an augmenting path is a path from the source to the sink in which we can send more net flow, i.e. flow along each edge has not reached the capacity. 
* 非正式地说，增强路径是从源到汇的一条路径，在这条路径中，我们可以发送更多的净流量，即沿每条边缘的流量都没有达到容量。
* 广路径（Augmenting Path）**是一个在残余网络（Residual Network）中从源点（source）到汇点（sink）的路径，这个路径表示我们可以通过它在当前流中增加更多的流量。增广路径的容量是由路径上残余容量最小的那条边决定的，因为这条边限制了我们可以通过这条路径传送的额外流量的最大值。
* <font color=red>就是在残余网络中，继续找可以给当前路径增加流量的路线，这条路线被称为增量路径，就是上面手写图里的红色加粗线</font>
* The Ford-Fulkerson method sends flow along augmenting paths until no more flow augmenting paths exist.
* Ford-Fulkerson方法沿着增强路径发送流，直到不再存在流增强路径。

![image-20230522010442606](D:\笔记\笔记图片\image-20230522010442606.png)

#### 8.2.4 Updating the flow 更新流

* Once an augmenting path P has been identified, we need to update the flow. How is this done? 
* 一旦确定了扩展路径P，我们就需要更新流。这是如何做到的呢?
* First of all, the amount of flow to send along P is limited by the minimum residual capacity of the edges on P, i.e. define
* 首先，沿P发送的流量受到P上边缘的最小剩余容量的限制，即定义
  * ![image-20230522010620932](D:\笔记\笔记图片\image-20230522010620932.png)
* ![image-20230522010701570](D:\笔记\笔记图片\image-20230522010701570.png)

#### 8.2.5 Cuts in Networks

**<font color=red>这个，上面链接，也有！！！！快去看！</font>**

* **The Ford-Fulkerson method repeatedly augments the flow along augmenting paths until a maximum flow has been found.** 
* **Ford-Fulkerson方法沿着增加路径反复增加流量，直到找到最大流量。**
* **The Max-Flow/Min-Cut Theorem tells us that a flow is maximum if and only if no augmenting path exists.** 
* **Max-Flow/Min-Cut定理告诉我们，当且仅当不存在扩展路径时，流是最大的。**
* A cut (S, T) in a flow network G = (V, E) is a partition of the vertices V into S and T = V − S such that s ∈ S and t ∈ T.
* 流网络G = (V, E)中的切口(S, T)是将顶点V划分为S和T = V - S，使得S∈S, T∈T。
* <font color=red>说穿了就是将G分成两部分S，T。**其中连接S和T的线的容量和被称为最小cut 容量**</font>

![image-20230522011151899](D:\笔记\笔记图片\image-20230522011151899.png)

![image-20230522011211716](D:\笔记\笔记图片\image-20230522011211716.png)

* **<font color=red size=5>The maximum flow is a network is equal to capacity of a minimum cut in the network.</font>**
* **网络的最大流量等于网络中最小通道的容量**
* **这个定理将最小cut容量和最大流联系在了一起**
* <font color=blue size=5>Min-Cut最小割并不唯一，可能存在多种情况的最小割的capacity是相同的</font>
* ![image-20230527165948609](D:\笔记\笔记图片\image-20230527165948609.png)

















* ![image-20230522011330664](D:\笔记\笔记图片\image-20230522011330664.png)

![image-20230522011345713](D:\笔记\笔记图片\image-20230522011345713.png)

![image-20230522011358282](D:\笔记\笔记图片\image-20230522011358282.png)

![image-20230522011415449](D:\笔记\笔记图片\image-20230522011415449.png)

* **<font color=red>链接，有，快看~~~~~</font>**
* What is the running time of the Ford-Fulkerson algorithm?
*  **Let |f ∗ | denote the value of a maximum flow f ∗ in a network with n vertices and m edges.** 
* **设|f * |表示有n个顶点和m条边的网络中最大流f *的值。**
* Finding an augmenting path in the residual network can be done using a DFS or BFS algorithm. These run in time O(n + m) = O(m). 
* 在残差网络中寻找扩展路径可以使用DFS或BFS算法。运行时间为O(n + m) = O(m)。
* Each augmentation increases the flow by at least one unit (using the fact that the capacities are integers), so there are at most |f ∗ | augmentation steps.
* 每次增加流量至少增加一个单位(利用容量为整数的事实)，因此最多有f * |个增加步骤。
* **So the Ford-Fulkerson algorithm runs in time O(|f ∗ |m). (This isn’t ideal, as a poor choice of augmenting paths can result in this large time bound.)** 
* **因此Ford-Fulkerson算法的运行时间为O(|f * |m)。(这并不理想，因为扩展路径的糟糕选择可能会导致这么大的时间限制。)**
* Other algorithms exist (such as the Edmonds-Karp algorithm) that run in time that is asymptotically better than the Ford-Fulkerson algorithm when |f ∗ | is very large. 
* 存在其他算法(如Edmonds-Karp算法)，当|f∗|非常大时，其运行时间渐近优于Ford-Fulkerson算法。
* **Edmonds-Karp works by selecting shortest augmenting paths in the residual network (considering each edge to have length 1 when finding an augmenting path). This algorithm has a running time of O(nm^2 ).**
* **<font color=red>Edmonds-Karp的工作原理是在残差网络中选择最短的增强路径(在寻找增强路径时考虑每条边的长度为1)。该算法的运行时间为O(nm^2)。</font>**



### 8.3 Bipartite graphs 二分图

* A bipartite graph is a graph whose vertex set can be partitioned into two sets X and Y, such that every edge joins a vertex in X to a vertex in Y.
* 二分图是这样一种图，它的顶点集可以划分为两个集合X和Y，使得每条边都连接X中的一个顶点和Y中的一个顶点。
* **Bipartite graph（二分图）是图论中的一个概念，指的是一个图可以被分为两个独立的顶点集合，且图中的每条边都连接着这两个集合中的顶点，而不连接同一集合中的顶点。**
* ![image-20230522142041743](D:\笔记\笔记图片\image-20230522142041743.png)

* Bipartite graphs arise naturally is many situations when objects are being assigned to other objects. 
* 当一个对象被分配给另一个对象时，自然会出现二分图。
* For example, the set X could represent jobs and the set Y might represent machines. An edge (xi , yj) means that job xi is capable of being assigned to machine yj.
* 例如，集合X可以表示作业，而集合Y可以表示机器。一条边(xi, yj)表示作业xi能够分配给机器yj。 
* A bipartite graph could also represent relations between job applicants and available positions (i.e. people who are qualified for a particular job), customers and stores, houses and nearby police stations, etc, etc.
* 二分图还可以表示求职者和可用职位(即适合某一特定工作的人)、客户和商店、房屋和附近警察局等之间的关系。



* A matching is a subset of the edges of a bipartite graph where each vertex appears in at most one edge (i.e. edges in the **matching** share no common endpoints).
* 匹配是二分图的边的子集，其中每个顶点最多出现在一个边中(即匹配中的边没有公共端点)。
* 在图论中，Matching（匹配）是指图中的一组边，这些边之间没有公共顶点，也就是说没有两条边共享同一个顶点。

![image-20230522142413945](D:\笔记\笔记图片\image-20230522142413945.png)

* **最大匹配（Maximum Matching）是指在一个图中，具有最大边数的匹配。换句话说，最大匹配是图中可以找到的边数最多的匹配。**



#### 8.3.1 Finding a bipartite maximum matching

* To use the augmenting path algorithm (or the Edmonds-Karp algorithm or some other maximum flow algorithm), we need to define our flow network. 
* 为了使用增强路径算法(或Edmonds-Karp算法或其他最大流量算法)，我们需要定义流网络。
* The flow network is obtained from the bipartite graph by adding two new vertices, a source vertex s and a sink vertex t. 
* 通过在二分图中增加两个新的顶点，即源顶点s和汇顶点t，得到流网络。
* Join all vertices in X to s and all vertices in Y to t. Direct all edges from s to X, from X to Y, and from Y to t. 
* 将X中的所有顶点连接到s，将Y中的所有顶点连接到t。将所有边从s指向X，从X指向Y，从Y指向t。
* Finally, give each edge a capacity of 1.
* 最后，让每条边的容量为1。

![image-20230522143640712](D:\笔记\笔记图片\image-20230522143640712.png)



* **Claim: The value of a maximum flow in the newly constructed flow network is equal to the size of a maximum matching in the original bipartite graph.**
* **<font color=red>声明:新建流网络中最大流量的值等于原二分图中最大匹配的大小。</font>**
* As a result, we can find a maximum matching (using, say, the Ford-Fulkerson augmenting path algorithm) in time O(nm) (in this case the value of a maximum flow |f ∗ | is O(n)).
* **因此，我们可以在O(nm)时间内找到一个最大匹配(例如使用Ford-Fulkerson增强路径算法)(在这种情况下，最大流量的值|f * |是O(n))。**
* 这方面有点问题，为什么等于|f*|是O(n)？？？







## Week 9

## 9. Cryptographic communications 密码交流

* Throughout history there has often been the need (or desire) to securely transmit information through insecure channels. Such applications include communications for military purposes and business reasons (to keep proprietary information secure), and most recently, transactions through the Internet. 
* 纵观历史，人们经常需要(或渴望)通过不安全的通道安全地传输信息。这些应用包括出于军事目的和商业原因(保证专有信息安全)的通信，以及最近通过Internet进行的交易。
* A variety of cryptographic methods have been developed to facilitate this type of communication. These methods include encryption/decryption transformations and digital signatures.
* 已经开发了各种各样的密码方法来促进这种类型的通信。这些方法包括加密/解密转换和数字签名。

### 9.1 Encryption schemes 加密方案

* **Confidentially in communication can be achieved by <font color=red>encryption schemes, or ciphers</font>.** 
* **通信中的机密性可以通过<font color=red>加密方案或密码</font>来实现。**
* The general idea behind these schemes is that **the message M** to be sent, often referred to as **<font color=red>the plaintext</font>**, is encrypted (before transmission) into an unrecognizable string (we hope!) of characters C, **<font color=red>the ciphertext</font>.** 
* 这些方案背后的一般思想是，要发送的**消息M**，通常被称为**明文**，在传输之前被加密为一个无法识别的字符串(我们希望!)字符C，即**密文**。
* The ciphertext C is then transmitted to the recipient who decrypts C to recover the original message M.
* 密文C传输给接收方，接收方对密文C进行解密，得到原始消息M。

![image-20230417142823074](D:\笔记\笔记图片\image-20230417142823074.png)

### 9.2 Symmetric encryption schemes and secret keys 对称加密方案和秘密密钥

* In a traditional encryption scheme a **common secret key**, K, is shared by Alice and Bob. 
* 在传统的加密方案中，Alice和Bob共享一个**公共密钥K**。
* **This common key K is used for both encryption and decryption of messages.** 
* **这个公共密钥K用于消息的加密和解密。**
* Such an **encryption scheme is called symmetric** since the recipient and receiver both have access to the same secret key, and it is used for both the encryption and decryption processes.
* 这样的**加密方案被称为对称的**，因为接收方和接收方都可以访问相同的秘密密钥，并且它用于加密和解密过程。

#### 9.2.1 Substitution Ciphers

* **A classic example of a symmetric cipher is a substitution cipher.** 
* **对称密码的一个经典例子是替换密码。**
* In this case the secret key is a permutation π of the characters of the alphabet. (For example, each A gets replaced by the letter D, each B gets replaced by the letter H, etc.) 
* 在这种情况下，密钥是字母表字符的排列π。(例如，每个A都被字母D取代，每个B都被字母H取代，等等)
* Encryption of the plaintext M is accomplished by mapping each character x with its corresponding character y = π(x). 
* 明文M的加密是通过将每个字符x映射到对应的字符y = π(x)来完成的。
* Decrypting the ciphertext C is easily accomplished with knowledge of the permutation π, i.e. each character y of C is replaced with x = π^ −1 (y).
* 解密密文C是很容易完成的知识的排列π，即每个字符y C替换为x = π^−1 (y)。

#### 9.2.2 The Caesar Cipher 凯撒密码

* The Caesar cipher is an early example of a substitution cipher wherein each character x is replaced by the character y = (x + k) mod n, where n is the size of the alphabet and the integer k, 1 ≤ k < n, is the secret key.
* 凯撒密码是替换密码的一个早期例子，其中每个字符x都被字符y = (x + k) mod n替换，其中n是字母表的大小，整数k(1≤k < n)是密钥。
* 它是一种替换密码，通过将明文中的每个字母按照一个固定的偏移量进行替换来进行加密。偏移量表示字母在字母表中向后移动的位置数。例如，偏移量为3时，字母A将被替换为D，字母B将被替换为E，以此类推。如果达到字母表的末尾，则回到字母表的开头。
* ![image-20230522161803590](D:\笔记\笔记图片\image-20230522161803590.png)

* 这种类型的密码被称为“凯撒密码”因为朱利叶斯 恺撒在k = 3时使用了它。



#### 9.2.3 Breaking substitution ciphers

* While very easy to use, **substitution ciphers** are not secure. 
* 虽然很容易使用，但**替换密码**并不安全。
* **The secret key of a substitution cipher is very easily broken by using frequency analysis, based on knowledge of the frequency of the various letters, or groups of letters, in the alphabet being used.** 
* **<font color=red>替换密码的秘密密钥很容易通过使用频率分析来破解，这种分析是基于对所使用字母表中各种字母或字母组的频率的了解。</font>**
* For example, “e” is the most common letter in the English language, followed by “t”, etc.
* 例如，“e”是英语中最常见的字母，其次是“t”，等等。

#### 9.2.4 The One-Time Pad 一次性便笺簿

* Secure symmetric ciphers do exist! 
* 安全对称密码确实存在!
* In fact, the most secure cipher known is the symmetric cipher that’s referred to as the one-time pad. 
* 事实上，已知的最安全的密码是称为一次性密码的对称密码。
* For this encryption scheme Alice and Bob share a random bit string K that is as long as any message that they are going to send. 
* 对于这个加密方案，Alice和Bob共享一个随机的比特串K，它和他们将要发送的任何消息一样长。
* This key K is the symmetric key that is used for the encryption and decryption process.
* 密钥K是用于加密和解密过程的对称密钥。



* 加密过程
  * 准备明文和密钥，明文是待加密的消息，密钥是与明文长度相等的随机字符串。
  * 将明文和密钥转换为二进制形式。
  * 对明文和密钥的每一位进行异或运算。如果明文和密钥的对应位相同，则结果为0；如果不同，则结果为1。
  * 得到加密后的密文。
* 解密过程
  * 准备密文和密钥，密文是待解密的消息，密钥是与密文长度相等的相同随机字符串。
  * 将密文和密钥转换为二进制形式。
  * 对密文和密钥的每一位进行异或运算，与加密过程中相同的规则。
  * 得到解密后的明文。

![image-20230522163913669](D:\笔记\笔记图片\image-20230522163913669.png)

* The One-time pad (encryption)
* 一次性键盘(加密)
* To encrypt the message M, Alice computes C = M ⊕ K, where the ⊕ symbol denotes the bitwise “exclusive-or” operation. 
* 为了加密消息M, Alice计算C = M⊕K，其中⊕符号表示按位的“异或”操作。
* (Note: 0 ⊕ 0 = 1 ⊕ 1 = 0 and 0 ⊕ 1 = 1 ⊕ 0 = 1.) 
* Alice then sends C to Bob on any reliable communications channel. 
* 然后，Alice通过任何可靠的通信通道将C发送给Bob。
* The communication is secure because C is computationally indistinguishable from a random bit string. (This relies highly on the fact that K was selected randomly!!)
* 通信是安全的，因为C在计算上与随机位串无法区分。(这很大程度上依赖于K是随机选择的事实!!)

![image-20230522164322286](D:\笔记\笔记图片\image-20230522164322286.png)

* Bob can easily decrypt the ciphertext C to recover M in the following fashion:
* Bob可以很容易地通过以下方式解密密文C来恢复M:
* ![image-20230522164416510](D:\笔记\笔记图片\image-20230522164416510.png)
* where 0 represents the all-zero string with the same length as M.
* 其中0表示与M长度相同的全零字符串。
* This is clearly a symmetric scheme as Alice and Bob use the same key K for encryption and decryption.
* 这显然是一个对称方案，因为Alice和Bob使用相同的密钥K进行加密和解密

##### 9.2.4.1 The advantages amd Disadvantages of the One-time pad

* Advantages: 
  * Computationally efficient since the bitwise exclusive-or is easy to perform. 
  * 计算效率高，因为按位排他或很容易执行。
  * Very secure (provided K is chosen randomly)!!
  * 非常安全(假设K是随机选择的)!!
* Disadvantages:
  * Alice and Bob must share a very long key K. 
  * 爱丽丝和鲍勃必须共享一个很长的密钥K。
  * Security depends on the fact that the key is used only once!!
  * 安全性取决于密钥只使用一次的事实!!

* In practice, we prefer secret keys that can be reused, and that the keys we use are much shorter than the messages that we must transmit.
* 在实践中，我们更喜欢可以重用的密钥，并且我们使用的密钥比我们必须传输的消息短得多。

### 9.3 Public-key cryptography（非对称加密策略）

* A major problem with symmetric encryption schemes is key distribution, or how to securely distribute the secret keys. 
* 对称加密方案的一个主要问题是密钥分发，或者如何安全地分发密钥。
* One idea is to dispense with using symmetric encryption schemes and seek another method for generating (and deciphering) the ciphertexts. 
* 对称加密方案的一个主要问题是密钥分发，或者如何安全地分发密钥。
* In 1976 Diffie and Hellman described an abstract system that overcomes the problem of key distribution – Public-key cryptosystems.
* 1976年，Diffie和Hellman描述了一个抽象的系统，它克服了密钥分发的问题——公钥密码系统。



#### 9.3.1 Public-key cryptosystems 公钥密码系统

* **A public-key cryptosystem consists of an encryption function E and a decryption function D. For any message M, the following properties must hold:** 

* **公钥密码系统由加密函数E和解密函数D组成，对于任何消息M**，必须满足以下属性:

  * D(E(M)) = M. 
  * Both E and D are “easy” to compute. 
  * It is computationally infeasible to derive D from E. I E(D(M)) = M.
  * 从E推导出D在计算上是不可行的。
  * 有加密函数E不可以推导出解密函数D

  ![image-20230522170106260](D:\笔记\笔记图片\image-20230522170106260.png)

* The third property is the particularly important one. It means that knowledge of the encryption method gives no information about the decryption scheme. Anybody can send a private message to the holder of the function D, but only that person knows how to decrypt it.
* 第三个性质尤为重要。这意味着对加密方法的了解不会提供关于解密方案的信息。任何人都可以向函数D的持有者发送私人消息，但只有那个人知道如何解密它。

* For this reason **E is referred to as a one-way function, or sometimes a trapdoor function.** In this kind of encryption method E is made public and D is kept private.
* 因此，**E被称为单向函数，有时也称为活板门函数。**在这种加密方法中，E是公开的，D是私有的。
* The fourth property allows for digital signatures. This can allow someone to send a message to another person and the recipient can verify that it came from the sender, assuming that the sender is the only person who has the private key. (More on this later.)
* 第四个属性允许数字签名。这可以允许某人向另一个人发送消息，并且假设发送方是唯一拥有私钥的人，接收方可以验证消息是否来自发送方。(稍后会详细介绍。)





#### 9.3.2 The RSA Encryption Scheme RSA加密方案

* Diffie and Hellman’s idea was ingenious, but it was an abstract concept about how such a system would operate. 
* 迪菲和赫尔曼的想法很有创意，但对于这样一个系统如何运作，这是一个抽象的概念。
* Rivest, Shamir, and Adleman proposed a public-key encryption method that is probably the most well-known, and is still in use today for communications via web-browsers, etc. 
* Rivest、Shamir和Adleman提出了一种公开密钥加密方法，这种方法可能是最著名的，并且今天仍然用于通过web浏览器等进行通信。
* Their method is tied to the difficulty of factoring large numbers. 
* 他们的方法与分解大数的困难有关。
* Before we can get into the details of the RSA method, we must first discuss some concepts from the branch of mathematics called “number theory”.
* 在我们进入RSA方法的细节之前，我们必须首先讨论数学分支“数论”中的一些概念。



##### 9.3.2.1 Elementary number theory - Divisibility 初等数论, 可整除性

* **Given integers a and b, we use the notation a|b to denote that a divides b, i.e. b is a multiple of a.** 
* **给定整数a和b，我们用记号a|b表示a整除b，即b是a的倍数。**
* <font color=red>如同字面意思一般，这里的意思就是整除</font>
* If a|b then there is another integer k such that b = a · k.
* 如果a|b，则存在另一个整数k使得b = a·k。 
* We note the following properties about this divisibility relationship:
* 我们注意到这个可除关系的下列性质:
* Theorem: Let a, b, c be integers. 
  * 1. **If a|b and b|c, then a|c. (transitivity)** 
    2. **如果a|b和b|c，则a|c。(传递性)**
    3. **If a|b and a|c, then a|(i · b + j · c) for all integers i and j.** 
    4. **如果a|b和a|c，则a|(i·b + j·c)适用于所有整数i和j。**
    5. **If a|b and b|a then either a = b or a = −b.**
    6. **如果a|b和b|a，则a = b或a = - b。**



##### 9.3.2.2 Prime numbers and composite numbers 质数(也可以被称为素数)和合数

* An integer n ≥ 2 is said to be prime if the only divisors of n are the trivial divisors 1 and n. 
* 如果n的唯一约数是平凡约数1和n，则称整数n≥2为素数。
* **质数和素数是同一个概念，指的是只能被1和自身整除的正整数。因此，质数和素数是可以互换使用的。**
* An integer n ≥ 2 that is not prime is said to be composite. 
* 非素数的整数n≥2称为合数。
* For example, 11, 107, and 98711 are prime, but 25, 69, and 10403 = 101 · 103 are composite.
* 例如，11、107和98711是素数，而25、69和10403 = 101·103是合数。





##### 9.3.2.3 Fundamental Theorem of Arithmetic 算术基本定理

* Theorem: Let n > 1 be an integer. Then there is a unique set of prime numbers {p1, . . . , pk } and positive integers {e1, . . . , ek } such that
* 定理:设n > 1为整数。那么就有一个唯一的质数集{p1，…， pk}和正整数{e1，………这样}
  * ![image-20230522222627861](D:\笔记\笔记图片\image-20230522222627861.png)
* The product p e1 1 · · · p ek k is known as the prime decomposition of n. It is unique, up to the ordering of the primes in the factorization.
* 乘积p e1 1···p ek k被称为n的素数分解。它是唯一的，直到因数分解中素数的顺序。

![image-20230522222916683](D:\笔记\笔记图片\image-20230522222916683.png)



##### 9.3.2.4 Greatest common divisor (GCD)最大公除数（GCD）

* **Let a and b denote positive integers. The greatest common divisor of a and b, denoted gcd(a, b), is the largest integer that divides both a and b.**
* **设a和b为正整数。a和b的最大公约数，记为gcd(a, b)，是能同时整除a和b的最大整数。**
* **If gcd(a, b) = 1, then we say that a and b are <font color=red>relatively prime</font>.** 
* **如果gcd(a, b) = 1，那么我们说a和b是<font color=red>相对素数</font>**
* The definition of the GCD can be extended in a natural fashion:
* GCD的定义可以以一种自然的方式扩展:
  * **If a > 0, then gcd(a, 0) = gcd(0, a) = a.** 
  * **<font color=red size=5>gcd(a, b) = gcd(|a|, |b|) if a and/or b is negative.</font>**

![image-20230522223506589](D:\笔记\笔记图片\image-20230522223506589.png)

* **Note that gcd(0, 0) is undefined (as, of course, there is no largest integer that divides 0).**
* **注意，gcd(0,0)是未定义的(因为，当然，没有能整除0的最大整数)。**



* We note the following important fact: 
* **Theorem: If d = gcd(a, b), then there exist integers j and k such that** 
* **<font size=5>定理:若d = gcd(a, b)，则存在整数j和k，使得</font>**
  * **<font size=5>d = j · a + k · b.</font>** 
* In other words, the greatest common divisor of a and b is expressible as a linear combination of a and b.

![image-20230522224123917](D:\笔记\笔记图片\image-20230522224123917.png)



##### 9.3.2.5 The modulo operator and congruences(模运算符和同余)

* **<font size=5>模运算符（The modulo operator）</font>**
* **模运算符是一种数学运算符，通常用符号"%"表示。它计算一个数除以另一个数的余数。**
* 例如，10 % 3 = 1，表示10除以3的余数是1。

* For b > 0, the modulo operator, **denoted by a mod b**, defines the remainder of a when divided by b. That is, r = a mod b means that r = a − |a/b|*b.
* 当b > 0时，模算子**用a模b**表示，定义a除以b时的余数。即r = a模b意味着r = a−|a/b|*b。

![image-20230522225009757](D:\笔记\笔记图片\image-20230522225009757.png)







* **<font size=5>同余（Congruences）</font>**

* 同余是一个数论的概念，用于描述两个整数之间的关系。**<font size=5>如果两个整数除以一个正整数得到的余数相同，我们称这两个整数对于该正整数来说是同余的。</font>**可以用符号"a ≡ b (mod n)"表示，表示a与b在模n下是同余的。
* ![image-20230522224635097](D:\笔记\笔记图片\image-20230522224635097.png)

![image-20230522225649892](D:\笔记\笔记图片\image-20230522225649892.png)

* **In other words, if a ≡ b (mod n), then a − b = kn for some integer k.**
* **换句话说，如果a≡b (mod n)，那么对于某个整数k, a - b = kn。**
* <font size=5 color=red>注意是三道杠</font>

![image-20230522230052234](D:\笔记\笔记图片\image-20230522230052234.png)

![image-20230527220548892](D:\笔记\笔记图片\image-20230527220548892.png)

* <font color=red>注意下面的要求解的值是否为负数</font>

#### 9.3.3 Euclid’s algorithm 欧几里得算法

* **Euclid’s algorithm** is a method to find **the greatest common divisor （GCB）**of two integers a and b. 
* <font color=red size=5>**欧几里得算法**是一种求两个整数a和b的**最大公约数**的方法。</font>
* This algorithm relies on an important property that involves the modulo operator, namely, the following:
* 该算法依赖于一个涉及到模算子的重要性质，即:

![image-20230522230337361](D:\笔记\笔记图片\image-20230522230337361.png)

* **<font color=red>这段话的意思是gcd(a,b)的最大公约数等于gcd(b, a mod b)即b和a mod b的最大公约数</font>**

![image-20230522231458612](D:\笔记\笔记图片\image-20230522231458612.png)



![image-20230522231515039](D:\笔记\笔记图片\image-20230522231515039.png)

* Note: If b = 0, this routine will return the value of a (which, by our assumption on the input, is not zero), giving the correct result.
* 注意:如果b = 0，这个例程将返回a的值(根据我们对输入的假设，它不为零)，给出正确的结果。

![image-20230522231705334](D:\笔记\笔记图片\image-20230522231705334.png)

* ![image-20230522232121772](D:\笔记\笔记图片\image-20230522232121772.png)

* ![image-20230522232149962](D:\笔记\笔记图片\image-20230522232149962.png)



### 9.3.4 The Extended Euclidean Algorithm 扩展的欧几里德算法

* **As mentioned earlier, if d = gcd(a, b), there are integers j and k such that d = j · a + k · b.** 
* **如前所述，如果d = gcd(a, b)，则存在整数j和k，使得d = j·a + k·b。**
* We can modify Euclid’s algorithm to find these numbers j and k while we compute gcd(a, b). This is the so-called “Extended Euclidean algorithm.”
* 我们可以在计算gcd(a, b)的同时修改欧几里得的算法来找到这些数字j和k，这就是所谓的“扩展欧几里得算法”。

![image-20230523000856295](D:\笔记\笔记图片\image-20230523000856295.png)

![image-20230523000526062](D:\笔记\笔记图片\image-20230523000526062.png)

* <font color=red size=5>这边来正经解释一下这个东西</font>
* https://blog.csdn.net/qq_45954726/article/details/123718717?spm=1001.2101.3001.6650.1&utm_medium=distribute.pc_relevant.none-task-blog-2%7Edefault%7EOPENSEARCH%7ERate-1-123718717-blog-38130115.235%5Ev36%5Epc_relevant_default_base&depth_1-utm_source=distribute.pc_relevant.none-task-blog-2%7Edefault%7EOPENSEARCH%7ERate-1-123718717-blog-38130115.235%5Ev36%5Epc_relevant_default_base&utm_relevant_index=2
* https://www.bilibili.com/video/BV1bp4y1S7bW/?spm_id_from=333.337.search-card.all.click&vd_source=9d046a6203dde4f5f1794bf980388e63
* <font color=red>我会以上面的题目为例进行求解</font>

![image-20230523001904736](D:\笔记\笔记图片\image-20230523001904736.png)

* **重点是最后得到ax1+by1 == ay2 +b(x2-[a/b]*y2)**
* **<font size=5>x1 = y2; y1 = x2-[a/b]*y2</font>**
* 那么我们是不是可以推论得到以下结果
* **<font size=5>x(n-1) = yn; y(n-1) = xn-[a/b]*yn</font>**

那么xn与yn是不是可以通过迭代欧几里得算法得出？

* 上述题目中， a=4, b=0, gcd(a,b)=4
* axn + byn = gcd(a,b)
* xn = 1, yn=0
* 然后就可以通过这个迭代求解

![image-20230523002508493](D:\笔记\笔记图片\image-20230523002508493.png)



### 9.3.5 The RSA Method

* Given the previous information (review?) about same very basic number theory, we are now ready to describe the basic method of the RSA encryption/decryption method. 
* 鉴于前面关于相同的非常基本的数论的信息(复习?)，我们现在准备描述RSA加密/解密方法的基本方法。
* **Recall that this is a public-key encryption method. So this is a non-symmetric encryption scheme, where there is an encryption function and a separate decryption function.** 
* **回想一下，这是一种公钥加密方法。这是一个非对称加密方案，其中有一个加密函数和一个单独的解密函数。**
* The main idea of the RSA method is that I can publish my encryption function (i.e. make it freely available to anyone who wishes to use it to send a message to me), but only I know the decryption function.
* RSA方法的主要思想是，我可以发布我的加密函数(即，让任何希望使用它向我发送消息的人都可以免费使用它)，但只有我知道解密函数。



* ![image-20230523003022535](D:\笔记\笔记图片\image-20230523003022535.png)

* 下面是RSA算法的主要步骤：

  1. 密钥生成： 

     a. 选择两个大素数p和q，计算它们的乘积n：n = p * q。 

     b. 计算欧拉函数φ(n)：φ(n) = (p - 1) * (q - 1)。 

     c. 选择一个整数e，满足1 < e < φ(n)，且e与φ(n)互质。e成为公钥的一部分。 

     d. 计算e的模反元素d，满足 (d * e) % φ(n) = 1。d成为私钥的一部分。

     ​	 (给定e，我们可以使用扩展欧几里得算法求出d。)

     e. 公钥为(n, e)，私钥为(n, d)。

  2. 加密： 

     a. 将明文消息表示为整数m，满足 0 ≤ m < n。 

     b. 加密计算：c = (m^e) % n。c为加密后的密文。

  3. 解密： 

     a. 收到密文c后，使用私钥中的d进行解密计算：m = (c^d) % n。m为解密后的明文

* ![image-20230523015114877](D:\笔记\笔记图片\image-20230523015114877.png)

![image-20230523014341693](D:\笔记\笔记图片\image-20230523014341693.png)

* Let us assume that the message M is an integer and that 0 < M < n. 
* 假设消息M是一个整数，且0 < M < n。
* (We can suppose that M is obtained by concatenating the bits of the ASCII representation of its characters, for example, and break up M into blocks of appropriate sizes if M ≥ n. This characterizes a padding scheme which we won’t discuss here.) 
* (我们可以假设M是通过连接其字符的ASCII表示的位来获得的，例如，如果M≥n，则将M分成适当大小的块。这是我们在这里不讨论的填充方案的特征。)
* **The plaintext M is encrypted using the public keys e and n by the following operation:**
* **明文M使用公钥e和公钥n进行加密，操作如下:**

![image-20230523014450686](D:\笔记\笔记图片\image-20230523014450686.png)

* Decryption of the received ciphertext, C, is again handled by modular exponentiation:
* 接收到的密文C的解密，同样由模幂处理:
* ![image-20230523014724008](D:\笔记\笔记图片\image-20230523014724008.png)
* The correctness of the RSA method is guaranteed because it can be shown that with the choices of e, n, and d (with the properties listed earlier), then for every integer 0 < x < n we have
* RSA方法的正确性得到了保证，因为可以证明，对于e、n和d的选择(具有前面列出的属性)，那么对于我们拥有的每个整数0 < x < n
* ![image-20230523014805008](D:\笔记\笔记图片\image-20230523014805008.png)



![image-20230523014624210](D:\笔记\笔记图片\image-20230523014624210.png)



#### 9.3.5.0 如何将欧几里得算法与RSA串联在一起

![image-20230527215207834](D:\笔记\笔记图片\image-20230527215207834.png)











#### 9.3.5.1 The difficulty of breaking RSA

* Note that even knowing e doesn’t allow us to figure out d, unless we know φ(n). 
* 注意，即使知道e也不能求出d，除非我们知道φ(n)
* Most cryptographers believe that breaking RSA requires the computation of φ(n), which in turn requires factoring n. 
* 大多数密码学家认为，破解RSA需要计算φ(n)，而φ(n)又需要分解n。
* Factoring has not been proven to be difficult, but many (many!) people have worked on this problem over the last several hundred years. 
* 保理并没有被证明是困难的，但是在过去的几百年里，很多(很多!)人都在研究这个问题。
* For example, it took some heavy duty mathematics and a network of 700 computers (including one supercomputer) four months to factor the number 2512 − 1 which is 155 digits long. 
* 例如，它花费了一些繁重的数学和700台计算机(包括一台超级计算机)的网络四个月来分解长度为155位的数字2512−1。
* As the ability to factor larger numbers increases, we simply have to choose larger primes p and q so that n = p · q is outside of the current factoring capabilities.
* 随着分解更大数的能力的提高，我们只需要选择更大的质数p和q，这样n = p·q就超出了当前的分解能力。

#### 9.3.5.2 Digital signatures 数字签名

![image-20230523015441225](D:\笔记\笔记图片\image-20230523015441225.png)

#### 9.3.5.3 Fast Exponentitation  快速模幂运算

![image-20230523015827492](D:\笔记\笔记图片\image-20230523015827492.png)

![image-20230523015905536](D:\笔记\笔记图片\image-20230523015905536.png)

![image-20230523015927031](D:\笔记\笔记图片\image-20230523015927031.png)

#### 9.3.5.4 Complexity of RSA

* **Using the FASTEXPONENTIATION(x, k, n) algorithm, the size of the operands is never more than O(log n) bits, and it takes O(log k) arithmetic operations to find x k mod n.** 
* **使用FASTEXPONENTIATION(x, k, n)算法，操作数的大小永远不会超过O(log n)位，并且需要O(log k)个算术运算才能找到x k对n取模。**
* This leads to the following result: 
* **Theorem: Let n be the modulus of the RSA algorithm. Then RSA encryption, decryption, signature, and verification each take O(log n) arithmetic operations (per block).**
* **定理:设n为RSA算法的模数。然后RSA加密、解密、签名和验证每个都需要O(log n)个算术运算(每个块)。**





## Week10 Complexity of Algorithms N P-completeness

![image-20230527234138417](D:\笔记\笔记图片\image-20230527234138417.png)

### 10.1 Hard Computational Problems 计算难题

![image-20230530115638112](D:\笔记\笔记图片\image-20230530115638112.png)

* Some computational problems seem hard to solve. 
* Despite numerous attempts we do not know any efficient algorithms for these problems. 
* However, we are also far away from a proof that these problems are indeed hard to solve. We simply “don’t know” or are unsure right now.
* 有些计算问题似乎很难解决。
* 尽管我们做了很多尝试，但我们不知道任何有效的算法来解决这些问题。
* 然而，我们还远远不能证明这些问题确实很难解决。我们现在只是“不知道”或不确定。

![image-20230528001008279](D:\笔记\笔记图片\image-20230528001008279.png)

* In more formal language, we don’t know if N P = P or N P ！= P. 
* This is an important question in theoretical computer science! And this set of lecture notes is designed to shed some light on this question. 
* As pointed out on the first set of lecture notes, this question is one of the seven Millennium Prizes set out by the Clay Institute, and can earn someone $ 1 million dollars for its solution (as well as a place in math/computer science history). See http://www.claymath.org/millennium-problems/p-vs-np-problem for their description of this problem.

![image-20230528001449917](D:\笔记\笔记图片\image-20230528001449917.png)

### 10.2 NP问题的例子

![image-20230528001808902](D:\笔记\笔记图片\image-20230528001808902.png)

![image-20230528001826997](D:\笔记\笔记图片\image-20230528001826997.png)

![image-20230528001820276](D:\笔记\笔记图片\image-20230528001820276.png)

![image-20230528001839331](D:\笔记\笔记图片\image-20230528001839331.png)





![image-20230528001951363](D:\笔记\笔记图片\image-20230528001951363.png)

![image-20230528001959789](D:\笔记\笔记图片\image-20230528001959789.png)





























































