# COMP218

## WeeK1 Lecture1

### 1.Alphabets and strings（字母表和字符串）

Sting：谈论单词、数字、成对单词等的常用方法。<font color='red'>换句话说：字母表上的字符串string是由字母表alphabet当中的字符的一个有限序列</font>

Alphabets：字母表是一组有限的符号。

![image-20220926212448731](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220926212448731.png)

* ![image-20220926212907981](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220926212907981.png)

∑* 是内的字符所能组成的所有字符串的和

所有非空字符串的集合我们写∑+

### 2.Languages

Language：语言是相同字母表的一个子集。简单来说，language是这个字母表中所有的字符可以构成的集合的子集。

* A language is a set of strings (over the same alphabet).

![image-20220926213355830](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220926213355830.png)

![image-20220926213845371](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220926213845371.png)

* 解释一下第二个。因为L3要求的结构是s#s，所以可以将ab视为整体，所以满足条件。其他两个不行。

### 3.Finite Automata（有限自动机）

首先是个例子

![image-20220926215026230](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220926215026230.png)

***一个玩具机，投入不同的钱得到不同的结果***

通过上图，我们可以得到

1. 初始状态被称为<font color='blue' size=5>start state.</font>
2. 有两个圈的被称为<font color='blue' size=5> accepting state.</font>
3. <font color='blue' size=5> transitions</font>指从每个状态和每个字符对应的作用。

#### 3.1 确定有穷自动机（DFA）的定义

![image-20220926220500453](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220926220500453.png)

![image-20220926220606946](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220926220606946.png)

* **在图中，接受状态用双圆表示**

![image-20220926222803189](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220926222803189.png)

#### 3.2 Language of a DFA

<font color='red'>DFA(Q、S、d、q0、F)的语言是所有字符串的集合,从q0开始,在转换为字符串读取到右,将会到达一些接受状态。</font>

简单来说，经过若干操作后到达accept statue的所以操作集合被称为Language of a DFA。

![image-20220926223722542](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220926223722542.png)

例题

![image-20220926224241555](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220926224241555.png)

##### 3.2.1 Example of Language of a DFA

![image-20220926224440087](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220926224440087.png)

![image-20220926224643735](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220926224643735.png)

![image-20220929154438694](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220929154438694.png)

* <font color='red'>在这个题目中，statue总共有6个，其中包括dead state</font>



![image-20220926224929965](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220926224929965.png)

![image-20220926224949605](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220926224949605.png)

* 通过上面两个例子，我们可以看出，当要求结尾数是2时，图分成3层. 要求结尾数是3时，图分成四层。



##### 3.3 Dread Statue

![image-20220929164323510](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220929164323510.png)

在进行任何不被定义的transition时，都会导致dead state

**Example**

![image-20220929164408508](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220929164408508.png)

因为q1没有定义关于1的结果，所以当q1接受1时，die。

![image-20220929164452424](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220929164452424.png)

因为q3没有定义关于1，0的结果，所以一切输入都会导致die。









## WeeK1 Tutorial 1

Q1：

![image-20221107145243050](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221107145243050.png)

![image-20221107145258231](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221107145258231.png)

Q2

![image-20221107145312089](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221107145312089.png)

* **Kleene star operation** 

![image-20221107145458233](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221107145458233.png)

Q3：

![image-20221107145608031](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221107145608031.png)

* +表示至少有一个值，且不包含空值。

Q4：

![image-20221107150108993](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221107150108993.png)

![image-20221107150116689](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221107150116689.png)



Q5

![image-20221107150657621](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221107150657621.png)

字符上方的横线表示反制，寻找集合的补集

Q6：

![image-20221107150830512](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221107150830512.png)





## Week1 Lecture2

部分参考

https://blog.csdn.net/Huoon/article/details/106516565?ops_request_misc=&request_id=&biz_id=102&utm_term=NFA&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduweb~default-3-106516565.142^v51^control_1,201^v3^control_1&spm=1018.2226.3001.4187



https://blog.csdn.net/weixin_45427596/article/details/123596885?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522166530940016781432976119%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=166530940016781432976119&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduend~default-2-123596885-null-null.142^v52^js_top,201^v3^control_1&utm_term=nfa%E8%BD%AC%E5%8C%96%E4%B8%BAdfa&spm=1018.2226.3001.4187



### 1. 不确定的有穷自动机

NFA同一个符号可以标记离开同一状态的多条边，并且e也可以作为标记；所以同一输入可能会导致不同的结果。

![image-20220929163847440](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220929163847440.png)

<font color='red'>NFA在阅读一个给定的字符后可以达到几个不同的状态</font>

<font color='red'>如果这些状态中</font><font color=red size=5>有一个</font><font color='red'>可以到达最终状态，那么这个字符串就会被NFA接受。</font>



**Example**

![image-20220929164900889](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220929164900889.png)

在001之前的数字，都在q1被解决，在001之后的数字，都被q3解决。

#### 1.1 The Defination of NFA

![image-20220929165154417](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220929165154417.png)

![image-20221008223634789](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221008223634789.png)

![image-20221008224336508](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221008224336508.png)





![image-20221008224913402](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221008224913402.png)

![image-20221008225214529](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221008225214529.png)

<font color='red' size=5>Important</font>

![image-20221008225259960](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221008225259960.png)

### 2.e-NFA to DFA conversion



and regular expressions

<font color='red'>Every (e-)NFA can be converted into a DFA for the same language. 任何的e-NFA都可以转化成DFA</font> 

1. Eliminate e-transitions (e-NFA →NFA) 
2. Convert NFA →DFA

Example：

![image-20221009105146755](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221009105146755.png)

#### 2.1 简单的NFA转化为DFA（不含）

![image-20221009111618376](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221009111618376.png)

![image-20221107172811948](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221107172811948.png)



#### 2.2 从有空边的NFA到DFA

<font color='red'>推荐将e-NFA转换到NFA再转换到DFA</font>

![image-20221009111816972](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221009111816972.png)

![image-20221009111829306](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221009111829306.png)

#### 2.3 e-NFA转化到NFA

![image-20221009112514320](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221009112514320.png)

讲一下自己的理解

<font color='red'>States that can reach final state by eare all accepting</font>

如果q0和q1存在一条路径到达q2接收态，则将在NFA中将其写为接收态。则在上述图表中，我们可以看到，当input=0时，我们可以到达q1，q2和q0（从q1到达q0），则q0为接收态，同理，q1也一样。所以图如上图所画。

#### 2.4 e-closure



![image-20221009142815379](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221009142815379.png)



![image-20221009144718565](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221009144718565.png)





### 补充：NFA-DFA

![image-20221107172802831](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221107172802831.png)

### 3. String Concatenation（串联接）

![image-20221009145156322](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221009145156322.png)

![image-20221009145415238](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221009145415238.png)

![image-20221009145425767](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221009145425767.png)



#### 3.0 Operations On Languages

![image-20221009150229283](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221009150229283.png)

![image-20221009150437636](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221009150437636.png)

![image-20221009150502274](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221009150502274.png)

#### 3.1 Combining Languages 联合语言

![image-20221009150559756](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221009150559756.png)

如上图所示，很简单。

<font color=blue size=5>例子： Regular Expressions</font>

![image-20221009151522240](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221009151522240.png)

![image-20221009151819417](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221009151819417.png)

![image-20221009152413958](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221009152413958.png)

![image-20221009152453580](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221009152453580.png)

### 4.Regular Expressions 正则表达式

正则表达式是由以下规则组成的表达式:

1. ![image-20221020213807685](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221020213807685.png)

2. ![image-20221020213842087](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221020213842087.png)

3. ![image-20221020213857164](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221020213857164.png)

<font color='blue' size=5>**Analysing regular expressions**</font>

![image-20221020214601858](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221020214601858.png)

![image-20221020215144622](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221020215144622.png)

![image-20221020215258973](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221020215258973.png)

可以表示所有长度为1的字符，即0或1

![image-20221020215417803](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221020215417803.png)

**这个可以当作案例记住，很常用**

![image-20221020215640577](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221020215640577.png)

任意包含01的值

![image-20221020215752835](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221020215752835.png)

所有可以被2或3整除的字符串

![image-20221020215936530](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221020215936530.png)

所有可以被2整除的字符串

![image-20221020220009829](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221020220009829.png)

长度为2的字符串

![image-20221020220049349](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221020220049349.png)

所有可以被3整除的字符串

![image-20221020220121613](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221020220121613.png)

长度为3的字符串

![image-20221020220431274](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221020220431274.png)

可以被分成块的字符串，每个块的长度为2或3. 

* 这个相对来说更难，但是可以把他转换成

  {0,1}{0,1}+{0,1}{0,1}{0,1}外面加上*，类似于(0+1) *

  后者是由0和1组成的所有字符串，所以前者是由长度2和3组成的字符串

* 延申一下结果如下：

![image-20221020221139506](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221020221139506.png)

![image-20221020221019739](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221020221019739.png)

长度为2或3的字符串

![image-20221020221500895](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221020221500895.png)

![image-20221024102344231](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221024102344231.png)

![image-20221020221545757](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221020221545757.png)

前面一部分的结果如图，所以中间不可能有3个0. 之后再乘后面的部分可以知道结尾最多两个0

#### 4.1 Writing Regular Expressions

 ![image-20221020221851247](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221020221851247.png)

![image-20221024102601134](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221024102601134.png)

不包含超过2个0的正则表达式

（011）*是中间部分，是为了得到每块只有一个0的式子。如果是01 * 则可能会出现0 X 01的情况，所以要再多加一个0.

<font color=red>注意：+号代表“或”</font>

![image-20221024133854212](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221024133854212.png)

内部含有偶数个0的正则表达式

![image-20221027153441205](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221027153441205.png)

### 5. The Relation of the DFAs, NFAs, εNFAs, and regular expressions 

![image-20221027153914002](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221027153914002.png)

![image-20221027153927624](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221027153927624.png)

正则表达式 -> eNFA -> NFA -> DFA

#### 5.1 正则表达式转eNFA

https://blog.csdn.net/y3over/article/details/100742633



![image-20221027153043618](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221027153043618.png)

<font color='red'>关于a+b正则表达式转NFA更推荐这个解析</font>

![image-20221108171704755](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221108171704755.png)

![image-20221108214255791](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221108214255791.png)

![image-20221027153121443](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221027153121443.png)

![image-20221027153140195](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221027153140195.png)

![image-20221027154217149](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221027154217149.png)

![image-20221027154255934](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221027154255934.png)

#### 5.2  eNFA转换到Regular Expression

##### ![image-20221027160554624](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221027160554624.png)

 ![image-20221027160614356](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221027160614356.png)

![image-20221027160633387](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221027160633387.png)

Example2

注意反向图的画法

![image-20221027161218476](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221027161218476.png)

<font color=red>这一题的关键在于怎么画q2->q1->q2的正则表达式</font>

https://www.bilibili.com/video/av891338316/?vd_source=9d046a6203dde4f5f1794bf980388e63

![image-20221108214753991](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221108214753991.png)

* <font color='red' size=6>循环与循环之间是相加，循环与直线操作是相乘</font>

解释上图：

1. 将q1中的0循环与线性操作1相结合，得到0*1，消去q1的循环。
2. 将从q2出发的0-0*-1循环与q2的循环1相结合，因为二者都是循环，使用U即+，得到00 * 1+1的循环
3. 将线性操作0*1 与循环操作00 * 1+1结合，得到结果0*1(00 * 1+1)

Ex2



#### 5.3 正则表达式的基本运算

![image-20221027162451934](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221027162451934.png)

![image-20221027162656715](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221027162656715.png)

![image-20221027162725371](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221027162725371.png)

![image-20221110092558792](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221110092558792.png)



### 1. Regular Language的运算

![image-20221110092515507](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221110092515507.png)

### 2. Intersection （相交）

![image-20221110093236269](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221110093236269.png)

![image-20221110093344307](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221110093344307.png)

![image-20221110093449850](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221110093449850.png)

![image-20221110093509827](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221110093509827.png)

### 3.Reversal of regular languages

![image-20221110093809879](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221110093809879.png)

![image-20221110093838071](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221110093838071.png)









## 补充：

### Containment

![image-20221109001331204](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221109001331204.png)



参考：

https://sora.ink/archives/946 --非正则语言

https://blog.csdn.net/qq_42902997/article/details/120804292?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522166688716516782388084000%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=166688716516782388084000&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduend~default-1-120804292-null-null.142^v62^control_1,201^v3^control_1,213^v1^control&utm_term=%E9%9D%9E%E6%AD%A3%E5%88%99%E8%AF%AD%E8%A8%80&spm=1018.2226.3001.4187 -- 正则语言与DFA

### 1. Non-Regular Language(非正则语言)



![image-20221017111212838](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221017111212838.png)

首先明确一下定义：正则语言是可以通过正则表达式或者确定性和非确定性有限自动机或状态机表示的语言。

所以可以得出Non-Regular Language的定义

<font color=red>任何不能被正则表达式所定义的语言都是非正则语言(Nonregular languges)</font>

下面对于非正则语言的解释非常详细
\# 链接(URL)：https://sora.ink/archives/946

![image-20221029105418951](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221029105418951.png)

![image-20221029105829294](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221029105829294.png)

![image-20221029105845553](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221029105845553.png)





### 2. Pumping Lemma 

参考：

https://zhuanlan.zhihu.com/p/404708553 

https://abp.today/blog/2017/04/26/regular-language-pumping-lemma

-- 泵引理

![image-20221029113020322](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221029113020322.png)

<font color=red>注意看定义下面的解释</font>

Example：

![image-20221029113421889](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221029113421889.png)

![image-20221029113440892](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221029113440892.png)

<font color=red size=5>泵引例只能用来证明一个语言是非正则的，但**不能说一个语言符合泵引理所以就是正则的**。实际上有的非正则语言，依然满足泵引理。比如 L’= {0m1n / n、m 都是复数}。</font> (m和n是上标)

* <font color='red' size =5>一个有穷的正则表达式，存在一个DFA或NFA可以表达它</font> 存疑，不太确定
  * 来源于下面的题目 （ii）

![image-20221109173119627](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221109173119627.png)

![image-20221109173133647](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221109173133647.png)



课堂案例

![image-20221029113644903](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221029113644903.png)

最经典的题目，没啥好说的

![image-20221029114212403](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221029114212403.png)

这个w相当于任意值（取0，1），所以只要找一段重复值循环就导致两个w不相等，故可以解。

![image-20221029114426996](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221029114426996.png)

多转几次n，让n大于m就不成立了

![image-20221029114521944](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221029114521944.png)

![image-20221029114612029](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221029114612029.png)

一样，就是把a,b换成了01和1

![image-20221029123324059](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221029123324059.png)

![image-20221029123334392](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221029123334392.png)

 <font color=red>傻逼，只要01和10数字相同就行</font>

![image-20221029123434669](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221029123434669.png)

这个比较好玩，因为反面是正则表示，所以它不是。

![image-20221029125959154](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221029125959154.png)

重复几遍不是质数就行，prime是质数的意思

![image-20221029130036565](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221029130036565.png)

###### EX：回文数 palindrome

所谓"[回文数](https://so.csdn.net/so/search?q=回文数&spm=1001.2101.3001.7020)"是指具有如下性质的整数：一个整数，当它的各位数字逆序排列，形成的整数与原整数相同，这样的数称为回文数。例如，素数11，373，其各位数字对换位置后仍然为11，373，因此这两个整数均为回文数

例子如图

![image-20221029130632102](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221029130632102.png)

y=011111 然后循环，可以出现不满足L8的式子

比如011110111101111.。。。。。。等等

### 3. 最小DFA （DFA minimisation）

#### 3. 0 可区分状态和不可区分状态



#### 3.1 Defination

![image-20221106224212550](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221106224212550.png) 

#### 3.2 无关状态

![image-20221106224344331](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221106224344331.png)

![image-20221106224431025](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221106224431025.png)

![image-20221106224453758](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221106224453758.png)

![image-20221106224531540](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221106224531540.png)

#### 4. 如何最小化DFA

<font color='red' size=6>1. 子集法</font>

https://www.bilibili.com/video/BV1jQ4y1o76p/?spm_id_from=333.337.search-card.all.click&vd_source=9d046a6203dde4f5f1794bf980388e63 -- 视频解析

https://blog.csdn.net/weixin_44225182/article/details/106576746?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522166775733916800184122664%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=166775733916800184122664&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduend~default-2-106576746-null-null.142 -- 文字解析

### ![image-20221106222809895](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221106222809895.png)

![image-20221106222824816](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221106222824816.png)



<font color=red size=6>2. 列表法</font>

https://www.bilibili.com/video/BV1oE4116794/?p=20&vd_source=a0e8139ba1fc8c556842de1b7b54a9c5 -- 视频

* 最小化的过程就是合并相同的节点，所以第一步需要区分节点

![image-20221109224926398](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221109224926398.png)

<img src="C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221109225526859.png" alt="image-20221109225526859" style="zoom:80%;" />

<img src="C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221109225545814.png" alt="image-20221109225545814" style="zoom:80%;" />

<img src="C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221109225627854.png" alt="image-20221109225627854" style="zoom:70%;" />

<img src="C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221109225658901.png" alt="image-20221109225658901" style="zoom:60%;" />



----------------------------------------------------



## Context-Free Languages

### 1. Some Basic Grammer of Language

一个句子可以被分成名词短语和动词词组

![image-20221024111212282](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221024111212282.png)

### 2. The Defination of Context-Free Grammer

![image-20221024111828782](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221024111828782.png)

* 上下文无关的语法由(V， Σ， R, S)给出，其中

  * V是变量或非终结点的有限集合

  * Σ是一组有限的终端

  * R是一组形式的产生或替换规则

    ![image-20221117113257171](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221117113257171.png)

    * A是一个变量，α是一串变量和终结点

  * S是一个叫做起始变量的变量
  
  * **<font color='red' size=5>集合表达式是CFL，箭头语言是CFG</font>**

![image-20221024113801300](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221024113801300.png)

![image-20221031112128741](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221031112128741.png)

## 其他：关于从CFG到CFL rules的题目

![image-20221130231236055](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221130231236055.png)

![image-20221130231251280](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221130231251280.png)



#### 2.1 Derivation

* **派生**是产物的顺序应用:

  ![image-20221117113558245](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221117113558245.png)

<font color='red'>派生是对产品的一系列应用。</font>

<font color='red' size=5>如果两个Derivation在任何一点上使用了不同的**转换规则**，则两个Derivation是不同的, 注意，与顺序有关。</font>

* **比如SS转换成（）（），前后两个S先转换那个没有意义，不列入计数**，而SS到SS（）和SSS是不同的转换方式，计入数字  <font color=red>这个题目的例子是错的,这是解析树，不是derivation</font>
* ![image-20221201013427256](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221201013427256.png)
* ![image-20221201102804799](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221201102804799.png)

![image-20221031113215019](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221031113215019.png)

<font size=5>**|代表或**</font>

###  3. Ccontext-Free languages CFL

* CFG G生成的语言是派生结束时所有字符串的集合

![image-20221024112558037](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221024112558037.png)



**<font color=red>Example</font>**

1. 

![image-20221031112522875](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221031112522875.png)

使用A，B得到字符串L(G)

2. 

![image-20221031113329178](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221031113329178.png)



![image-20221031113353519](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221031113353519.png)

<font color='red' size=5>如果两个Derivation在任何一点上使用了不同的转换规则，则两个Derivation是不同的</font>

3. 

![image-20221031113432936](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221031113432936.png)

4. 

![image-20221031113927042](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221031113927042.png)

5. 

![image-20221031114133600](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221031114133600.png)

在纸上写一遍就可以发现S可以是any natural number in decimal notation.

6. 

![image-20221031114325374](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221031114325374.png)

这个的结果也很明显

7. 

![image-20221031114534277](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221031114534277.png)

这个相对来说就比较复杂，但也是自己写一遍的问题

![image-20221031115955340](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221031115955340.png)



#### 3.1Context-free vs regular  上下文无关语言与正则语言

* Write a CFG for the language (0 + 1)*111 

  ![image-20221117114151204](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221117114151204.png)

* **<font color='red'>Every regular language is context-free 每一种正则语言都是上下文无关语言</font>**

  ![image-20221117114240883](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221117114240883.png)

##### 3.1.1 From regular to context-free 

![image-20221031120150621](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221031120150621.png)

* **<font color='red' size=5>上下文无关语言不一定是正则语言</font>**
* 正则语言可以转成上下文无关语言，但是反之不行。

![image-20221117114455741](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221117114455741.png)



### 4.  Ambiguity, Parsing Algorithms, Probabilitistic Context-Free Grammars

#### 4.1 Ambiguity

* **<font color=red>A CFG is ambiguous if some string has more than one parse tree. 一个CFG是模糊的如果它拥有超过一个 解析树</font>**
* **因为解析树在不同或者相同的节点选择的转换方式不同**

![image-20221031121144280](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221031121144280.png)

![image-20221031121210831](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221031121210831.png)

<font color=red>Solutions</font>

1. **Rewrite the Grammer to Remove ambiguity 通过重写语法来消除歧义**

![image-20221031121805096](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221031121805096.png)

2. **Divide expression into terms and factors  将表达式划分为式子和因子**

![image-20221031122131077](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221031122131077.png)

* An expression is a sum of one or more terms 表达式是一个或多个项的和
* Each term is a product of one or more factors 每一项都是一个或多个因子的乘积
* Each factor is a parenthesized expression or a number 每个因子都是一个带括号的表达式或一个数字
  * **觉得像是因式分解，通过将一个整式分解来达到类似括号的作用**


![image-20221031122151607](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221031122151607.png)

**上面这个就是把两个整式分解成三个不同的式子来防止模糊（歧义）**

![image-20221031122242320](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221031122242320.png)

##### 4.1.1 Disambiguation 消除歧义

* 消除歧义并不总是可能的因为

1. 存在故有歧义的语言
2. 没有消除歧义的一般程序

* In programming languages, ambiguity comes from precedence rules, and we can deal with it like in the previous example. 在编程语言中，歧义来自于优先规则，我们可以像前面的例子一样处理它
  
  

#### 4.2 Parsing 解析

思考一个问题，在之前的问题里，程序为什么可以生成我们期待的解析树？

最容易想到的情况，**生成所有可能的解析树**，找到与input相对应的树。

如图：

![image-20221117131007682](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221117131007682.png)

但是这样有两个问题

1. **尝试所有的Derivations（派生）可能需要很长时间**

2. **如果输入的不是相应的语言，解析不会停止。**

* 那么什么时候让解析停止？

![image-20221031124341899](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221031124341899.png)

* **因为空集，派生字符串会不断变小**
* **因为单位程序，派生会进入循环**

##### 4.2.1 Removel of ε-productions 

* A variable N is nullable if it can derive the empty string **如果变量N可以派生空字符串，则它是可空的**

  ![image-20221117131420086](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221117131420086.png)

  * Identify all nullable variables N 识别所有可空变量N
  * Remove all ε-productions carefully (while adding extra productions to compensate for this)  小心删除所有ε-产品(同时添加额外的产品来弥补这一点)
  * If start variable S is nullable: 如果初始变量S为空:
    * 1.Add a new start variable S’  
    * 2.Add special productions S’ → S | ε

<font color='red'>Example</font>

* 如果X为空，则标记X是可空的
* 如果X为YZ...W,  YZ....W全部标记可空，包括X也标记为空

1. 识别所有的无效变量

![image-20221117131901643](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221117131901643.png)

2. Remove all ε-productions carefully  仔细移除所有的空集

![image-20221117153632611](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221117153632611.png)

<font color=red size=5> 注意条件：1. If you see X → αNβ, add X → αβ	2.If you see N → ε, remove it. </font>

![image-20221117160600180](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221117160600180.png)

##### 4.2.2 Removal of Unit Productions

* **A unit production is a production of the form  单位生产是一种形式的生产**

  ​													A → B 

![image-20221117154541889](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221117154541889.png)

1. If there is a cycle of unit productions 如果有单位生产的周期

   ![image-20221117154848541](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221117154848541.png)

​                 delete it and replace everything with A  替代它并将所有的东西换成A

![image-20221117155009146](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221117155009146.png)

<font color=blue size=5>用S将T替换，然后将两个S合并</font>

2. Replace every chain 替换每一个链条

   ![image-20221117155338568](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221117155338568.png)

![image-20221117155355192](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221117155355192.png)

<font color=blue size=5>用0SR将R替换，然后将S->0SR, R->0SR</font>

#### 4.3 Recap 总结

<font size=5>**Problem**:</font> If input is not in the language, parsing will never stop.如果输入不是用该语言编写的，解析将永远不会停止



<font size=5>**Solution:**</font>

1. Eliminate ε productions  消除ε产品
2. Eliminate unit productions 消除单位产品
3. Try all possible derivations but stop parsing when |derived	string| > |input|  尝试所有可能的派生直到|derived	string| > |input| 
   1. **必须严格按照顺序**


![image-20221129205201337](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221129205201337.png)



#### 4.4 Example of removal e-productions and unit productions

![image-20221117160945434](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221117160945434.png)



### 5. CYK Algorithm (Cocke-Younger-Kasami algorithm )



* **一种更快的解析方法，不需要列出所有的derivations**
* To use it we must prepare the CFG and convert it to Chomsky	Normal Form
* **转换规则**
* Step1. Eliminate ε productions  清除空集
* Step 2. Eliminate unit productions  清除单元集
* <font color='red'>Step 3. Add rules for terminals and split longer sequences of non-terminals (next slide) </font> 为终端添加规则并拆分更长的时间非终结符序列

#### 5.1 Chomsky Normal Form CNF & GNF

https://www.bilibili.com/video/BV1zb4y1b7U1/?spm_id_from=333.337.search-card.all.click&vd_source=9d046a6203dde4f5f1794bf980388e63

* A CFG is in Chomsky Normal Form if every production* has the form 

  一个CFG是乔姆斯基范式Chomsky Normal Form如果每一个production * 有from

  ![image-20221119122510697](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221119122510697.png)

* 1.用新变量替换终端

* 2.用新变量分解序列

* **<font color='red'>注意：只存在两种情况！！！就是以上两种！！！没有A->C 或者A->BCD</font>**

![image-20221119122537327](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221119122537327.png)

* Exception: We allow S → ε for the start variable only 

  例外:我们只允许S→ε作为起始变量

![image-20221124145720919](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221124145720919.png)

#### 5.2 CYK algorithm CYK算法

前提条件：该CFL必须满足Chomsky Normal Form，如果不满足，则将CFL转化为CNF格式后再使用。

![image-20221119164409602](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221119164409602.png)

以下面的图举例说明：

![image-20221119164531848](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221119164531848.png)

![image-20221119171612579](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221119171612579.png)

![image-20221119171649724](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221119171649724.png)

![image-20221119171705060](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221119171705060.png)

![image-20221119171713533](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221119171713533.png)

<font color='red'>最后结果baaba=SAC，存在初始production S。所以存在解</font>

### 6. Probabilistic Context Free Grammars （PCFG）概率上下文相关语法

* **A PCFG is a probabilistic version of a CFG where each production has a probability.  PCFG是CFG的概率版本，其中每个产品都有一个概率。**
* Probabilities of all productions rewriting a given non-terminal must add up to 1, defining a distribution for each non-terminal.  所有产品重写给定非终结符的概率之和必须为1，为每个非终结符定义一个分布。
* String generation is now probabilistic where production probabilities are used to non deterministically select a production for rewriting a given non-terminal.  字符串生成现在是概率的，其中生成概率用于不确定地选择一个生成来重写给定的非终结符。

#### 6.1 Statistical Parsing  概率句法分析研究

* Statistical parsing uses a probabilistic model of syntax in order to assign probabilities to each parse tree.  **统计解析Statistical parsing使用语法的概率模型，以便为每个解析树分配概率。**
* Provides a systematic approach to resolving syntactic ambiguity. 提供了一个系统的方法来解决语意模糊。

![image-20221119173728316](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221119173728316.png)

#### 6.2 Parse Tree Probability 概率解析树

* Assume productions for each node are chosen independently.  假设一个production的每一个节点都是独立的
* Probability of a parse tree is the product of the probabilities of its productions.  解析树的概率是这个产品所有概率的乘积。

![image-20221119175755764](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221119175755764.png)

![image-20221119175802300](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221119175802300.png)

##### 6.2.1 Syntactic Disambiguation  消除句法歧义

* Resolve ambiguity by picking most probable parse tree. 通过选择最可能的解析树来解决歧义。

  ![image-20221119180135220](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221119180135220.png)

<font color='red'>对比一下，可以知晓，概率解析树通过选择最有可能的树枝来解决歧义</font>

#### 6.2.2 Sentence Probability 句子的概率

* • Probability of a given sentence is the sum of the probabilities of all of its parse trees. 给定句子的概率是其所有解析树的概率之和。

![image-20221119180521075](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221119180521075.png)



### 7. Probabilistic CYK:  Most Likely Parse Tree  概率CYK算法



* **CYK can be modified for PCFG parsing by including in each cell a probability for each non terminal.  CYK可以通过在每个单元格中包含每个非终结符的概率来修改PCFG解析。**
* Cell *ij* contains the most probable parse tree of each non-terminal that can generate the part of the input word from *i* through *j* together with its associated probability.  单元格ij包含每个非终结符的最可能解析树，该非终结符可以生成从i到j的**输入单词的部分及其相关概率**

![image-20221119193108931](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221119193108931.png)

依旧以正常CYK的算法进行举例说明

![image-20221120121129215](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221120121129215.png)

![image-20221120121139131](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221120121139131.png)

![image-20221120121150551](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221120121150551.png)

![image-20221120121203840](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221120121203840.png)

![image-20221120121213872](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221120121213872.png)

![image-20221120121223435](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221120121223435.png)

![image-20221120121234486](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221120121234486.png)

![image-20221120121243076](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221120121243076.png)

![image-20221120121254940](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221120121254940.png)

![image-20221120121302544](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221120121302544.png)





### 8.Pushdown Automata 下推自动机

https://blog.csdn.net/shulianghan/article/details/106222997?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522166895473016800186515272%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=166895473016800186515272&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_positive~default-1-106222997-null-null.142 																

​																															-- 下推自动机

![image-20221120121435246](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221120121435246.png)

![image-20221107110639013](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221107110639013.png)

* PDA像NFA一样，但是有无限的栈堆

![image-20221107110756767](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221107110756767.png)

* 当PDA读取输入时，它可以从堆栈顶部推入/弹出符号

#### 8.1 Building a PDA

![image-20221107110927045](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221107110927045.png)

* 通过将x压入栈来记忆每一个0
* 通过将x推出栈来记忆每一个1
* 当到达栈堆底部时，PDA被接受
* We will use  $ to mark bottom 我们将使用$标记底部

![image-20221107111118362](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221107111118362.png)

![image-20221107111228025](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221107111228025.png)

#### 8.2 Defination of PDA

![image-20221107111424663](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221107111424663.png)

* **Q是有限的状态集**
* **Σ是输入的字母表**
* **Γ 是栈堆的字母表**
* **Q中的q0是初始状态**
* **属于Q的F是终止状态集**
* **δ 是转换函数**

![image-20221107111540617](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221107111540617.png)



#### 8.3 The language of a PDA

* A PDA is nondeterministic, i.e. multiple transitions on same pop/input are allowed.  PDA是不确定的，即允许在同一弹出/输入上进行多次转换

*  Transitions may but do not have to push, pop or read input.  转换可以但不一定要推入、弹出或读取输入

* <font color='red'>The language of a PDA is the set of all strings in Σ* that can lead the PDA to an accepting state after the whole input is read.  </font>

* <font color='red'>PDA的语言是所有字符串的集合Σ*，它可以在读取整个输入后将PDA引导到接受状态。</font>

Remark: Sometimes acceptance is defined by emptying the stack or even both: empty stack and accepting state. All of these variants correspond to the same class of languages.   有时接受是通过清空堆栈来定义的，甚至是同时清空堆栈和接受状态。所有这些变体都对应于同一类语言。

**Example1 ：**

![image-20221107111940563](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221107111940563.png)

<font color='red'>这个图看不太懂，但是记住PDA是利用栈来表示图，到达最终状态即栈空</font>

* 解释一下上图：
* 1.*w*#*w*R（R上标），则L1接受的是W#(W的反制)类型的字符串
* 2.然后就可以按照上图去进行解释。
* 3.q0到q1是标记栈底， q2到q3是取出栈底符号使栈底变为空
* 4.q1-q2即使#和它左右两边的w

<font color=blue>1. R认为是字符转置符号。</font>

<font color=blue>2. /认为是->, **/e, /e->$ 意思是当读取值为空，且栈顶为空，则将$压入栈**/</font>

**Example2:**

![image-20221120145641498](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221120145641498.png)

与EXAMPLE1同理，只是缺少#所以中间部分是空换空、

Example3：

![image-20221120145837513](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221120145837513.png)

同样的，与上述情况类似。

* 但是，因为存在字符串长度奇数偶数的问题，字符串中间的字符会有空，0，1三种情况，不过都使用/e->/e的方式来处理

**Example4：**

![image-20221120150201116](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221120150201116.png)

这个和上面三个不同，比较有意思（**其实就是用两个不同的字符表示m和n的数量**）

1. q0-q1，标记栈底
2. q1 当读取字符为0，将/e取出，将0推入
3. q2 当读取字符为1，将/e取出，将1推入
4.  这里形成了栈，栈：0*n* 1*m* （m和n是上标）
5. q3 当读取字符为0，将1取出，将/e推入
6. q4 当读取字符为1，将0取出，将/e推入
7.  这里将栈内的数字取空，到达栈底
8. 到达栈底，将S取出换成/e

**Example5：**

![image-20221120151719505](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221120151719505.png)

要求是0和1有相同的数量，那么就意味着二者在栈堆里要相互制约

* 根据读取字符的不同，共有四种情况

1. input=0，读取为空，放入0换空
2. input=0，读取为1，放入空换1
3. input=1,   读取为空，放入1换空
4. input=1，读取为1，放入空换1
5. 可以发现，当读取x个0时，栈里会有x个1，如果想消除x个1，那么需要读取1，将栈里的1转换为/e

**Example6:**

![image-20221120152243722](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221120152243722.png)

w中有两部分含有相同数量的0

![image-20221120153724643](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221120153724643.png)

详细解释：

![image-20221120155427100](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221120155427100.png)

![image-20221120155452398](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221120155452398.png)

![image-20221120155501772](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221120155501772.png)

### 9. CFG ↔ PDA conversions CFG与PDA之间的转换

* *L* has a context-free grammar if and only if it is accepted by some pushdown automaton.  L有一个上下文无关的语法，当且仅当它被某个下推自动机所接受。

![image-20221120164112476](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221120164112476.png)

#### 9.1 A Convention

* When we have a sequence of transitions like: 当我们有一系列这样的过渡时:

![image-20221120164651374](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221120164651374.png)

* We will abbreviate it like this: 我们将这样缩写:

![image-20221120164739575](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221120164739575.png)

* 如图所示，可以合并
* <font color=red>**注意反转顺序:第一个符号这个词在堆栈的顶部**</font>



#### 9.2 Converting a CFG to a PDA  将CFG转换为PDA

https://blog.csdn.net/shulianghan/article/details/106244977?ops_request_misc=&request_id=&biz_id=102&utm_term=CFG%E8%BD%AC%E6%8D%A2%E4%B8%BAPDA&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduweb~default-1-106244977.142

![image-20221120170947731](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221120170947731.png)

![image-20221125173753495](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221125173753495.png)

* **<font color='blue'>需要解释一下这里的开始start， ε, ε / A$ 这里的A是为了在下一步检测的时候有初始值，但是并不是栈低标志</font>**



* <font color='red'>CFG转换为PDA的具体流程</font>
* 因为下推自动机包含三个状态，需要一个一个转换

![image-20221129235535779](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221129235535779.png)

![image-20221130000547670](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221130000547670.png)

* **<font color='blue'>这里往往会像上面说的的一样，将初始状态压进来</font>**



![image-20221125173634968](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221125173634968.png)

* <font color='blue'>记得加上终端字符</font>

![image-20221130000805479](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221130000805479.png)

* <font color='blue'>**去除终端字符**  </font>



* **小心终端字符**、
* 下面这张图也是表现CFG to PDA

![image-20221125173816937](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221125173816937.png)

#### 9.3 From PDAs to CFGs(了解就行，不强求)

![image-20221125185634145](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221125185634145.png)

##### 9.3.1 Simplifying the PDA

![image-20221125190311461](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221125190311461.png)

* A simplified PDA:  简化的PDA:

  * Has a single accept state 是否有单一的接受状态
  * <font color='red'>Empties its stack </font>before accepting  在接受之前清空堆栈
  * Each transition is either a push, or a pop, but not both 每次转型要么是“push”，要么是“pop”，但不能两者兼而有之  
    * <font color=blue>  若出现 a/b之类的情况， 意思是将b推出，a读进去，这里同时出现了栈的pop和push所以并不满足条件。</font>

  ![image-20221125190807057](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221125190807057.png)



#### 9.4 PDA转CFG

![image-20221125231916935](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221125231916935.png)

![image-20221125231925435](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221125231925435.png)

![image-20221125233556053](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221125233556053.png)

![image-20221125233604199](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221125233604199.png)

![image-20221125233612642](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221125233612642.png)

![image-20221125233620454](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221125233620454.png)

![image-20221125233629301](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221125233629301.png)

![image-20221125233702478](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221125233702478.png)

* <font color='red' size=5>不太理解这个方法是为什么, 但是这个图很容易得出结论</font>

![image-20221125233935024](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221125233935024.png)





#### 9.5 下推自动机的限制 Limitations of pushdown automata 

![image-20221126155045902](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126155045902.png)

**怎么判断上下文无关语言？**



##### 9.5.1 Non comtext-free Languages 非上下无关语言

![image-20221126154924578](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126154924578.png)

![image-20221126155153748](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126155153748.png)

* If a derivation is long enough, some variable must appear twice on the same path in a parse tree 如果推导过程足够长，那么某个变量必须在解析树的同一路径上出现两次 (**简单来说，出现循环**)

![image-20221126160126750](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126160126750.png)

* Then we can “cut and paste” part of the parse tree 然后我们可以“剪切和粘贴”部分解析树 (**泵引理的内容**)

![image-20221126160409794](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126160409794.png)

###### 9.5.1.1 Pumping Example

* We can repeat this many times  我们可以重复多次

  ![image-20221126160545379](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126160545379.png)

* Every sufficiently large derivation will have a middle part that can be repeated indefinitely  **每一个足够大的推导都有一个中间部分可以无限重复**
* 但是很明显，上图不可以重复



**Pumping in General**

 ![image-20221126160717357](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126160717357.png)

Example

![image-20221126161014710](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126161014710.png)

* If *L*3 has a context-free grammar *G*, then      如果L3有一个上下文无关的语法G，那么
* ![image-20221126161640327](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126161640327.png)

* ![image-20221126161748294](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126161748294.png)

###### 9.5.1.2 Pumping lemma for context-free languages  对上下文无关语言的泵引理

* Pumping lemma: For every context-free language *L*  泵引理：对上下文无关语言

* <font color=red size=6> **但是若要证明不是cfl，你得满足无论你uvwxy如何选，uv^iwx^iy都不属于L**</font>

* **<font color='red'>但是正则语言的泵引理是找到一个不满足的就可以</font>**

  * **比如a^n b^n, 这个显然是cfl。因为存在某种情况使得uv^iwx^iy一直满足条件**
  * Example：
  * ![image-20221126235524396](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126235524396.png)
  * ![image-20221126235535693](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126235535693.png)

  ![image-20221126162001399](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126162001399.png)

![image-20221126162056485](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126162056485.png)

![image-20221126162206789](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126162206789.png)

Case1 ：*v* or *x* contains two kinds of symbols  v和x包含了两种符号

![image-20221126162459936](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126162459936.png)

* x包含了b和c

Case2：*v* and *x* both contain one kind of symbol  v 和x 都只包含了一种符号

![image-20221126162602705](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126162602705.png)



* More Example
  ![image-20221126162641898](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126162641898.png)



* ![image-20221126163518274](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126163518274.png)
* ![image-20221126163755120](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126163755120.png)
* ![image-20221126163812465](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126163812465.png)
* ![image-20221126163908152](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126163908152.png)

* ![image-20221126163920521](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126163920521.png)





### 10. Properties of Context-Free Language

#### 10.1 Union

如果L1是Context-Free Languages L2也是CFL。 那么L1UL2也是CFL

![image-20221126170016276](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126170016276.png)

![image-20221126170321448](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126170321448.png)

![image-20221126170418717](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126170418717.png)



#### 10.2 Concatenation 连结

![image-20221126170510506](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126170510506.png)

![image-20221126170522189](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126170522189.png)

#### 10.3 Star Operation

![image-20221126170555826](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126170555826.png)

![image-20221126170614268](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126170614268.png)

### 11.Negative Properties of Context-Free Languages 

#### 11.1 Intersection 

![image-20221126171448930](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126171448930.png)

![image-20221126171627304](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126171627304.png)

![image-20221126171807508](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126171807508.png)

#### 11.2 Intersection of Context-free languages and Regular Languages 

![image-20221126172550330](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126172550330.png)

![image-20221126172747877](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126172747877.png)

##### 11.2.1 PDA和DFA的相交转换

1. ![image-20221126172925664](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126172925664.png)
2. ![image-20221126172945459](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126172945459.png)
3. ![image-20221126173027165](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126173027165.png)
4. ![image-20221126173048037](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126173048037.png)



EXAMPLE：

![image-20221126173519067](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126173519067.png)

![image-20221126174411770](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126174411770.png)

* 从上面可以总结几个小规律

* 1. 条件取交集
  2. 如果是终止状态，要向他添加状态

  ![image-20221126175230638](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126175230638.png)

* <font color='red'>M只会接受M1 和M2都会接受的w</font>



#### 11.3 Applications Of Regular Closure 应用正则闭包

Example1

![image-20221126175535546](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126175535546.png)

![image-20221126175550617](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126175550617.png)

![image-20221126175737795](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126175737795.png)

![image-20221126175812038](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126175812038.png)

Example2

![image-20221126180246771](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221126180246771.png)

因为an bn cn 不是上下文无关语言，所以不成立





### 12. LR(0) Grammars 语法

#### 12.1 Compiler  编译器

* **A program that reads a program written in one language (source language) and translates it into an equivalent program in another language  (target language).**  
* **读取用一种语言(源语言)编写的程序并将其翻译成另一种语言的等价程序的程序(目标语言)。**

![image-20221127132610259](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221127132610259.png)

* Typically the source language is a high-level language and the target language is a low-level language (machine code).   通常，源语言是高级语言，而目标语言是低级语言(机器代码)。

#### 12.2 编译器的前端和后端

![image-20221127133023870](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221127133023870.png)

#### 12.3 Tokenising computer programs  标记计算机程序

![image-20221127133335387](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221127133335387.png)

* First the javac compiler does a lexical analysis:  首先,javac编译器做了一个词汇分析:

![image-20221127133406246](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221127133406246.png)

* The alphabet of java CFG consists of symbols like:  java CFG的字母由如下符号组成:

![image-20221127133442259](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221127133442259.png)



#### 12.4 Parsing computer programs  解析计算机程序

![image-20221127133604853](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221127133604853.png)

![image-20221127133646624](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221127133646624.png)



#### 12.5 Parsing algorithms 

* • How long would it take to parse this program? 
* 解析这个程序需要多长时间?

#### ![image-20221127133826182](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221127133826182.png)

#### 12.6 Left-to-right parsing 

![image-20221127134324600](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221127134324600.png)

![image-20230123223430694](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230123223430694.png)

* An item is a production augmented with a • 
* item是一个增加了a•的产品
* <font color=red size=5>The item is complete if the • is the last symbol </font>
* <font color=red size=5>如果•是最后一个符号，则该项完成</font>

![image-20230123223710025](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230123223710025.png)

* <font color=red size=5>Items represent possibilities at various stages of the parsing process</font>
* <font color=red size=5>Item表示解析过程各个阶段的可能性</font>

![image-20230123223833723](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230123223833723.png)

* **<font color=red size=5>When a complete item occurs, a part of the parse tree is discovered</font>**
* <font color=red size=5>**当出现一个完整的item时，就会发现解析树的一部分**</font>

![image-20230123225819199](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230123225819199.png)

* **没有合适的item，寻找下一个**

![image-20230123231137758](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230123231137758.png)

* 也没有，再找

![image-20230123231320135](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230123231320135.png)

![image-20230123231348796](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230123231348796.png)

![image-20230123231356212](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230123231356212.png)

![image-20230123231405834](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230123231405834.png)

![image-20230123231520926](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230123231520926.png)

#### 12.7 LR(0) grammars and deterministic PDAs

* The PDA for LR(0) parsing is deterministic
* LR(0)解析的PDA是确定性的 
* Some context-free languages require nondeterministic PDAs, e.g. ![image-20230123232058364](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230123232058364.png)
* 一些与上下文无关的语言需要不确定性pda
* The class of deterministic CFGs/PDAs is less expressive than CFGs/PDAs 
* 确定性的cfg / pda的表达能力不如cfg / pda

![image-20230123231929352](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230123231929352.png)

![image-20230123232158434](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230123232158434.png)

![image-20230123232234885](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230123232234885.png)

#### 12.8 When you can’t LR(0) parse

![image-20230123232328412](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230123232328412.png)



![image-20230123232403031](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230123232403031.png)

![image-20230123232410369](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230123232410369.png)









## Turing Machines

* If an algorithm can be implemented on any realistic computer, then it can be implemented on a Turing Machine.  如果一个算法可以在任何现实的计算机上实现,那么它可以在图灵机上实现。

### 1. Turing Machines

![image-20221128111252832](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221128111252832.png)

图灵机的四个特点：

1. **Can both read from and write to the tap 可以从磁带上读和写**
2. **Head can move both left and right  针头既可以左移也可以右移**
3. **Tape is infinite 磁带是有限的**
4. **Has two special states accept and reject  有接收态和拒绝态**

Example：

![image-20221128111827736](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221128111827736.png)

* 先读取第一个字母，然后跨到#读取其的第一个字母
* 两个相等，进行下一步。不相等，拒绝

![image-20221128111934289](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221128111934289.png)

* 最后的情况应该只有x和#，否则拒绝

#### 1.1 How Turing Machines operate 

![image-20221128112048695](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221128112048695.png)

* 如何判断字母向左移还是向右移
* **<font color=red>也就是说，我可以把图灵机理解成对磁盘内容的更改？？？不确定</font>**



#### 1.2 Formal Defination

![image-20221128112252503](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221128112252503.png)

![image-20221128112325702](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221128112325702.png)

#### 1.3 Configurations 配置 （中文翻译：图灵机的格局）

* A configuration consists of the current state,  the head position, and tape contents   
* 一个配置由当前状态、头部位置和磁带内容组成

![image-20221128112821818](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221128112821818.png)

* We say configuration *C* yields C**’* if the TM can go from *C* to C**’* in one step  

* 我们认为配置C yields（生产）C* ，如果图灵机只需要一步就可以从C到C*

* The start configuration of the TM on input *w* is q0*w*  

* TM在输入w上的启动配置为q0w

* An accepting configuration is one that contains qacc;  

* 可接受的配置是包含qacc的配置;

* A rejecting configuration is one that contains qrej   

* 拒绝配置是包含qrej的配置



![image-20221128112627098](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221128112627098.png)

![image-20221128112719430](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221128112719430.png)

#### 1.4 The Language of a Turing Machine

* We say *M* accepts *x* if there exists a sequence of configurations *C*0, *C*1, ..., *Ck* where   我们说M接受x如果存在一个序列,C0,C1,…Ck所在 

![image-20221128113714393](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221128113714393.png)

* **The language recognized by *M* is the set of all** 

  **inputs that *M* accepts   M所认可的语言是M接受的所有输入的集合**

#### 1.5 Looping

* Something strange can happen in a Turing Machine:   图灵机可能会发生一些奇怪的事情:

![image-20221128114045384](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221128114045384.png)

* Inputs can be divided into three types  输入可以被分成3哥类型

![image-20221128114125003](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221128114125003.png)



#### 1.6 Halting  犹豫

* We say *M* halts on *x* if there exists a sequence of configurations *C*0, *C*1, ..., *C**k* where 

  我们认为M停在x，如果存在一个系列的Configuration C0,C1,......Ck where

  ![image-20221128115132453](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221128115132453.png)

* **A TM *M* is total if it halts on every input.  如果在每次输入时都停止，则TM M是total。**
* **Language *L* is recursive (decidable) if it is recognised by a total TM.  语言L是递归的（可决定的）如果它可以被整个M识别**

#### 1.7 Programming Turing Machines

https://blog.csdn.net/weixin_47173597/article/details/118004467?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522166963404516800213038379%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=166963404516800213038379&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_click~default-2-118004467-null-null.142

![image-20221128115502338](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221128115502338.png)

![image-20221128120428017](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221128120428017.png)

![image-20221128120504156](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221128120504156.png)

1. 首先q0是起始位置， configuration为q0aab#aab 

2. 通过a/xR，将第一个a换成x，此时到达qa1，configuration为xqa1ab#aab

3. 通过qa1的自循环，下一个读取到a，用a替换a，且此时仍在qa1， configuration为xaqa1b#aab 

4. 通过qa1的自循环，下一个读取到b，用b替换b，且此时仍在qa1， configuration为xabqa1#aab 

5. 通过#/#R, 读取到#，将#替换为#，到达qa2， configuration为xab#qa2aab  

6. 然后读取a/xL, 到达q2

7. **<font color=red>从这一步开始返回到最左端</font>**,  在#前插入q2

   configuration为xabq2#xab 

8. 如上面所示，直到到达首端，然后开始新的一轮



![image-20221128194447913](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221128194447913.png)

![image-20221128195551587](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221128195551587.png)

* **High-level description of TM:  高层描述**
* For every a:
  * Cross off the same number of bs and cs  划掉相同数目的b和c
  * Uncross the crossed bs (but not the cs) 划掉被划掉的b(但不要划掉c)
  * Cross off this a  划掉这个a
* If all as and cs are crossed off, accept

* **Low-level description of TM: 底层描述**
* Scan input from left to right to check it looks like aa* bb* cc* 从左到右写入 aa* bb* cc*
* Move the head to the first symbol of the tape  移动头指针到第一个磁带上
* 之后的步骤和高层描述一样
* ![image-20221128195343327](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221128195343327.png)

![image-20221128195512169](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221128195512169.png)





![image-20221128195638201](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221128195638201.png)

**High-level description of TM:** 

* On input *w*,
  * For every pair of blocks *x* *i* and *x* *j* in *w*,
  * 对于每一对块 xi和xj在w,
  * Compare the blocks *x* *i* and *x* *j*   比较xi和xj
  * If they are the same, reject.   如果他们相等，拒绝

* Otherwise, accept. 

![image-20221128200037212](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221128200037212.png)

**Low-level description:** 

1. If input is ε, or has exactly one #, accept. 如果input是空，或者仅有一个#,接受
2.  Place a mark on the leftmost # (i.e. replace # by # ) and move right 
3. Place another mark on next unmarked # (If there are no more #, accept) 。。。。。

![image-20221128200448653](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221128200448653.png)



#### 1.8 How to describe Turing Machines?  如何描述图灵机

* Unlike for DFAs, NFAs, PDAs, Turing Machines are rarely given as complete state diagrams   不像dfa, nfa, pda，图灵机很少给出完整的状态图
* Instead usually a high-level description is given: A recipe about the workings of the Turing Machine  相反，往往会给一个高级的描述 ：关于图灵机的工作原理
* However, in the exam and class test state diagrams will be used  然而在考试和课堂测验状态图将被使用



使用状态图的图灵机工作描述：

![image-20221128201405814](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221128201405814.png)

On input <G>,

1. Verify that 〈*G*〉 is the description of a graph (no vertex repeats; edges only go between nodes)  判断G是否可以被图描述 （(没有顶点重复;边只存在于节点之间)）

2. Mark the first node of *G * 给G的第一个节点做标记

3. Repeat until no new nodes are marked: For each node, mark it if it is attached  to an already marked node

4. 重复操作，直到没有新节点被标记:对于每个节点，如果它附加到已标记的节点，则对其进行标记

5. If all nodes are marked accept, otherwise reject.   如果所有的节点都被标记，接受，否则拒绝





### 2.  Variants of Turing Machines 图灵机的变体

#### 2.1 The Church-Turing Thesis   (教堂图灵机？？？？)

**<font color=red size=5>Every effectively calculable function is a computable function. </font>**

<font color=red>每个有效可计算的函数都是可计算的函数。</font>

effectively calculable = produced by any intuitively effective’ means whatsoever

**有效的计算 = 1. 由直觉产生 2.effective意思是任何，什么都行**

effectively computable = produced by a Turing-machine or equivalent mechanical device 

**由图灵机生产或者等效的机械设备**

* 这两个中文翻译都是有效计算 
* Church是人名

![image-20221128204757466](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221128204757466.png)



#### 2.2 The multitape Turing Machine  多磁带图灵机

![image-20221128204856404](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221128204856404.png)

* The transition may depend on the contents of all the cells  这个转换取决于单元格内的内容
* Different tape heads can be moved independently  不同的磁带头有独立的运动

![image-20221128205210072](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221128205210072.png)

* 每一个可以服务一个暂时的存储器



#### 2.2.1 How to argue equivalence 如何认为相等

**Multitape Turing Machines are equivalent to single-tape Turing Machines**

多磁带图灵机等同于单磁带图灵机

![image-20221128205545516](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221128205545516.png)

![image-20221128205701284](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221128205701284.png)

* 发现多磁带是将单磁带的每一节分开了



##### 2.2.1.1 Simulating a multitape TM  模拟多磁带图灵机

* 我们演示了如何在单磁带TM上模拟多磁带TM

![image-20221128205945239](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221128205945239.png)

* **将多条磁带合并**



Single-tape TM: Initialisation  单磁带图灵机的初始化

![image-20221128210202402](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221128210202402.png)

![image-20221128210249700](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221128210249700.png)

**Single-tape TM: Simulating Multitape TM moves 模拟多磁带图灵机的移动**

![image-20221128210447006](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221128210447006.png)

具体步骤：

*S*: On input *w*1...*w**n*: 

1. ![image-20221128210939118](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221128210939118.png)

##### 2.2.1.2 Doing simulations 做模拟

* To simulate a model *M* by another model *N*:  通过其他模型N来模拟模型M

1.  Say how the state and storage of *N* is used to represent the state and storage of *M*    **说一下N的状态和存储是如何用来表示M的状态和存储的**
2. Say what should be initially done to convert the input of *N* (if anything) 说明在转换输入N(如果有的话)时最初应该做什么
3. Say how each transition of *M* can be implemented by a sequence of transitions of *N*   假设M的每个跃迁如何由N的一系列跃迁实现



#### 2.3 计算机长什么样子

![image-20221128211516950](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221128211516950.png)

##### 2.3.1 Instruction Set 指令集

![image-20221128211856899](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221128211856899.png)

##### 2.3.2 Random access machines 随机存储机

在[理论计算机科学](https://zh.m.wikipedia.org/wiki/理論計算機科學)中，**随机存取机**（英语：Random-access machine，缩写为RAM）是一种[抽象机器](https://zh.m.wikipedia.org/wiki/抽象機器)，属于[寄存器机](https://zh.m.wikipedia.org/wiki/寄存器机)的一种。近似于[计数器机](https://zh.m.wikipedia.org/wiki/計數器機)，但是它拥有能对[暂存器](https://zh.m.wikipedia.org/wiki/暫存器)间接定址的能力。随机存取机是[图灵机](https://zh.m.wikipedia.org/wiki/圖靈機)的一种，[等价](https://zh.m.wikipedia.org/wiki/圖靈完備性)于[通用图灵机](https://zh.m.wikipedia.org/wiki/通用圖靈機)。

![image-20221128214747392](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221128214747392.png)

* It has registers that can store integer values, a program counter, and a random-access memory 它有可以存储整数值的寄存器、一个程序计数器和一个随机访问存储器

![image-20221128215658674](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221128215658674.png)

* The instructions are indexed by the program counter  指令由程序计数器编制索引
* Initially, the input is in the first *k* memory cells, all registers and PC are set to 0    最初，输入在前k个内存单元中，所有寄存器和PC都被设置为0

![image-20221128220638665](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221128220638665.png)

###### 2.3.2.1Simulating a TM on a RAM 

![image-20221128220901154](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221128220901154.png)

###### 2.3.2.2 Simulating a RAM on a Turing Machine 

* The TM has a simulation tape and a scratch tape 
* The simulation tape stores RAM configuration 
* **TM有一个模拟磁带和一个刮擦磁带**
* **模拟磁带存储RAM配置**
* The TM has a set of states corresponding to each program instruction of the RAM 
* **TM具有一组与RAM的每个程序指令相对应的状态**
* The TM tape is updates according to RAM instruction 
* **TM磁带是根据RAM指令更新的**

![image-20230122211423014](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122211423014.png)

![image-20230122211640071](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122211640071.png)

![image-20230122211715841](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122211715841.png)

* Simulating a RAM on a 2-tape TM

![image-20230122211819069](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122211819069.png)



#### 2.3.3  Running  time

* The running time of TM *M* is the function *t*M*(*n):

![image-20230122212023746](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122212023746.png)

![image-20230122212058296](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122212058296.png)

* The Church-Turing thesis says all these are equivalent in computing power… 
* 丘奇-图灵的理论认为，所有这些在计算能力上是等同的……

![image-20230122212245623](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122212245623.png)

* 但是运算时间不同

![image-20230122212910355](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122212910355.png)

![image-20230122212944724](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122212944724.png)



![image-20230122213042799](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122213042799.png)

![image-20230122213049321](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122213049321.png)



### 3. Decidable and undecidable languag 决定与非决定语言

![image-20230122213249773](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122213249773.png)

![image-20230122213516081](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122213516081.png)

![image-20230122213527297](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122213527297.png)

![image-20230122214122962](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122214122962.png)

![image-20230122214129933](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122214129933.png)

![image-20230122214140013](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122214140013.png)

![image-20230122214218035](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122214218035.png)

![image-20230122215257866](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122215257866.png)

![image-20230122215304292](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122215304292.png)

![image-20230122215316716](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122215316716.png)

![image-20230122215324197](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122215324197.png)

#### 3.1 No Decidable

* 并不是所有的CFG都是可决定的

![image-20230122215352103](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122215352103.png)

![image-20230122215358058](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122215358058.png)



### 4. The universal Turing Machine and undecidability 通用图灵机和不确定性



![image-20230122215842088](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230122215842088.png)

![image-20230124163615027](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230124163615027.png)



![image-20230124163712955](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230124163712955.png)

![image-20230124163729844](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230124163729844.png)

![image-20230124163832447](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230124163832447.png)

![image-20230124163917883](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230124163917883.png)



![image-20230124163951383](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230124163951383.png)

* <font color=red>The language recognised by a TM is the set of all inputs that make it accept. </font>
* 被TM识别的语言是使它接受的所有输入的集合。
* **<font color=red>A TM decides language L if it recognises L and halts (does not loop) on every input. </font>**
* **<font color=red>如果TM识别L并在每次输入时停止(不循环)，则TM决定语言L。</font>**

![image-20230124164058883](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230124164058883.png)



![image-20230124164209602](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230124164209602.png)

![image-20230124164222821](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230124164222821.png)

![image-20230124165325284](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230124165325284.png)

![image-20230124164239543](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230124164239543.png)



#### 4.1 Unrecognisable languages 不可识别语言

![image-20230124165806010](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230124165806010.png)

![image-20230124165852519](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230124165852519.png)

![image-20230124170052023](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230124170052023.png)

![image-20230124170110435](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230124170110435.png)



![image-20230124181704243](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230124181704243.png)

![image-20230124174235369](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230124174235369.png)

