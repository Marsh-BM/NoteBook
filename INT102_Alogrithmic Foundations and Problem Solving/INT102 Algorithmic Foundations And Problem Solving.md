



# INT102 Algorithmic Foundations And Problem Solving

## Lecture1

## OUTLINE

1. Able to tell what an algorithm is and have some understanding why we study algorithms
2. Able to use pseudo(假的，虚拟的) code to describe algorithm



### Algorithm:

**Algorithm的定义**：A sequence of **precise** and **concise**(简洁的) instructions that guide you(or a computer) to solve a class of a **specific** problem.

 ![image-20220401150354300](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220401150354300.png)

### Algorithm VS Program

1. Algorithms are free from grammatical rules.
   1. Content is more important than form
   2. Acceptable as long as it tells people how to perform a task
2. Programs must follow some syntax(语法，句法) rules
   1. Form is important
   2. Even if the idea is correct, it is still not acceptable if there is syntax error

**More Generally: Program = Data Structure + Algorithm**

### Pseudo Code(虚拟码)

![image-20220401154502343](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220401154502343.png)

不同语句的Pseudo Code 表达形式：

1. **Statement(声明语句)：**

![image-20220401154726585](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220401154726585.png)

2. **Conditional(条件语句)：**

![image-20220401154914682](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220401154914682.png)

3. **iterative(loop)(迭代和循环)：**

![image-20220401155143087](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220401155143087.png)

​	for循环的例子：

![image-20220401155657076](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220401155657076.png)

​	while循环的例子：

![image-20220401155741422](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220401155741422.png)

repeat的循环：

![image-20220401155903355](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220401155903355.png)

## Exercise(练习)

![image-20220401160025639](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220401160025639.png)

1. ![image-20220401160124107](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220401160124107.png)

2. ![image-20220401160137838](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220401160137838.png)

一样的题目，while格式

![image-20220401160348799](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220401160348799.png)

repeat格式：

![image-20220401160457552](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220401160457552.png)

## Lecture2

## OUTLINE

1. Understand the notations of asymptotic analysis.(渐进分析)
2. Able to carry out simple asymptotic analysis of algorithms

* 渐进分析, 时间复杂度O



### Time Complexity Analysis

![image-20220327162921392](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220327162921392.png)

注意：n！是最大的。

1.常数阶

无论代码执行了多少行，只要是没有循环的复杂结构，，那么这个代码的时间复杂度都是常数阶复杂度。

2.对数阶

![image-20220327163445082](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220327163445082.png)

3.线性阶

![image-20220327163516650](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220327163516650.png)

4.线性对数阶

![image-20220327163533405](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220327163533405.png)

5.平方阶

 ![image-20220327163642109](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220327163642109.png)

其余的是上述几种时间复杂度的组合。

**？那么指数阶怎么办？**

### 平均时间复杂度和最坏时间复杂度

1. 平均时间复杂度是指所有可能的输入实例均以等概率出现的情况下，该算法的运行时间。
2. 最坏情况下的时间复杂度称为最坏时间复杂度。**一般讨论的时间复杂度均是在最坏条件下的时间复杂度**。原因是可以保证算法时间不会比最坏的情况更长。
3. 平均时间复杂度和最坏时间复杂度是否一致和算法有关。

![image-20220327165048140](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220327165048140.png)

### 空间复杂度

![image-20220327165356478](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220327165356478.png)

 

## Lecture3

## OUTLINE

1. See some examples of polynomial(多项式) time and exponential(指数) time algorithms
2. Able to carry out simple asymptotic analysis of algorithms
3. Able to apply searching/sorting algorithms and derive their time complexities



* ![image-20220401172825564](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220401172825564.png)

​	当这个符号内的式子结果是一个包含小数时，忽略小数部分。

### Selection Sort

Pseudo Code:

![image-20220401201739384](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220401201739384.png)

### Bubble Sort

![image-20220401202014055](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220401202014055.png)

### Insertion Sort

![image-20220401202056945](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220401202056945.png)

![image-20220401202751437](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220401202751437.png)



## Lecture4

## OUTLINE

1. Understand how divide（分） and conquer（治） works and able to analyze complexity of divide and conquer methods by solving recurrence
2. See examples of divide and conquer methods

![image-20220403185333413](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220403185333413.png)

## Recurrence(递归式)

Definition：A recurrence is an equation or inequality that describes a function in terms of its value on smaller inputs.

递归式是在较小输入值时来描述的等式或不等式。

![image-20220403191203723](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220403191203723.png)

* To solve a recurrence is to derive asymptotic bounds on the solution

![image-20220403191644833](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220403191644833.png)





## MergeSort(归并排序)

![image-20220403185806407](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220403185806407.png)

## Lecture 5

### 欧拉回路(Euler circuit)

一个简单的电路最多只访问一次边缘，<font color='red'>最终回到原点</font>

图G中的欧拉电路是一个只访问G的每条边一次的电路。

![image-20220529150943077](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220529150943077.png)

如果每对顶点之间都有一条路径，则称无向图G是连通的。

如果G没有连接，那么就不存在访问所有边或顶点的单个电路

<font color='red'>即使图是连通的，也可能没有欧拉回路。</font>

欧拉回路:图连通；图中所有<font color='red'>节点度（向外延申的线）</font>均为偶数

### 欧拉路径 （Euler path）

一个简单的电路最多只访问一次边缘，<font color='red'>只需要经过每一个点，并不一定回到起始点</font>

设G是一个无向图。欧拉路径是经过的每条边一次的路径

一个无向图包含欧拉路径，如果它是连通的，并且包含恰好两个奇数次的顶点。

欧拉通路:图连通；图中只有<font color='red'>0个或2个度为奇数</font>的节点

### 哈密顿回路（Hamiltonian circuit）

哈密顿图: 图G的一个回路,若它通过图的**每一个节点一次,且仅一次**,就是<font color='blue'>哈密顿回路</font>.存在[哈密顿回路](https://so.csdn.net/so/search?q=哈密顿回路&spm=1001.2101.3001.7020)的图就是哈密顿图.哈密顿图就是从一点出发,经过所有的必须且只能一次,最终回到起点的路径.图中有的边可以不经过,但是不会<font color='red'>有边被经过两次.</font>

## Lecture6 

### BFS宽度优先搜索

![image-20220529153221934](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220529153221934.png)



### DFS深度优先搜索

它的思想是从一个顶点V0开始，沿着一条路一直走到底，如果发现不能到达目标解，那就返回到上一个节点，然后从另一条路开始走到底，这种尽量往深处走的概念即是[深度](https://so.csdn.net/so/search?q=深度&spm=1001.2101.3001.7020)优先的概念。

![image-20220529153414370](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220529153414370.png)

## Lecture7 

### 最小生成树-Prim算法

**一个有N个点的图，边一定是大于等于N-1条的。图的最小生成树，就是在这些边中选择N-1条出来，连接所有的N个点。这N-1条边的边的权之和是所有方案中最小的。**

https://blog.csdn.net/xiaoxi_hahaha/article/details/118940121?ops_request_misc=&request_id=&biz_id=102&utm_term=%E6%9C%80%E5%B0%8F%E7%94%9F%E6%88%90%E6%A0%91prim%E7%AE%97%E6%B3%95%20&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduweb~default-0-118940121.142



### 最小生成树-Kruskal’s algorithm 

![image-20220529181216238](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220529181216238.png)

然后不断选择线，注意不要生成循环即可。

### Single-source shortest-paths（最短路径问题）--Dijkstra’s

#### 最短路径和最小生成树的区别

最小生成树能够保证整个拓扑图的所有路径之和最小，但不能保证任意两点之间是最短路径。

最短路径是从一点出发，到达目的地的路径最小。

![image-20220529182729837](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220529182729837.png)

### 动态规划 Dynamic programming

![image-20220529185210397](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220529185210397.png)

![image-20220529185927154](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220529185927154.png)

![image-20220529191611227](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220529191611227.png)



### 一些概念

![image-20220529192456631](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220529192456631.png)

#### 相邻矩阵和相邻表adjacency matrix

![image-20220529192443870](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220529192443870.png)

![image-20220529192509066](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220529192509066.png)

#### 关联矩阵和关联表incidence list

![image-20220529192542343](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220529192542343.png)

![image-20220529192556754](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220529192556754.png)



# Week8

## lecture 10

### 时间换空间（Space for time tradeoffs）

首先介绍一下交换u，v数值的两种方式

![image-20220504104326236](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220504104326236.png)

#### 输入强化法（Input-enhancement）

定义：对于输入进行预处理以保证储存更多的信息来在之后解决问题。

##### 1. 分布计数排序（Distribution counting sort）

因为之前使用的sort algorithm最小的时间复杂度都是O(nlogn) ，所有这里引用一个计数排序（Counting Sort）：各个元素之间没有比较。

<font color='red'>**先介绍一个比较计数排序：**</font>

###### **定义**

针对排序列表中的每一个元素，**算出列表中小于该元素的元素个数**，并把**结果记录在一张表**中。这个“个数”指出了该元素在有序列表中的位置。例如一个列表A中有一个元素为10，而小于10的元素个数有5个，那么10应该排在第六个位置上，也就是A[5]（下标从0开始）。这个算法称为比较计数排序。

**图像说明：**

![image-20220504163018132](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220504163018132.png)

![image-20220504163030351](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220504163030351.png)



分布计数排序

* 需要使用一个额外数组C，C的长度取决于数组中数据的范围
* 分布值指的是在最后的有序数组中它们的元素最后一次出现时的正确位置

![image-20220506132554718](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220506132554718.png)

![image-20220506132723249](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220506132723249.png)

**分布值表示的是最后一次出现的正确位置，11的个数是一个，因为11是第一个元素，那么11的分布值就等于频率。12的个数有三个，那么它最后出现的位置就是它前面一个数的分布值加上自己出现的频率，也就是3+1=4。而13的分布值就等于12的分布值加上自己出现的频率，就是4+2=6。** <font color='red'>从后往前排</font>

![image-20220530213516117](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220530213516117.png)



代码实例：

```
/**
 * @author 巩泽楷
 * @version 1.0
 */
public class Distribution_counting_sort {
      //数组A中所有均大于等于min，小于等于max，并且min~max之间的所有元素在数组A中均出现
    public void distributionCountingSort(int[] A, int min, int max) {
        int[] temp = new int[A.length]; //
        int[] D = new int[max - min + 1]; // 建立一个临时数组存放分布值
        for(int i = 0;i < A.length;i++) {
            D[A[i] - min]++;
        } // 计算各个位置的分布值

        for(int i = 0;i < max - min;i++){// max-min是D.length-1
            D[i + 1] = D[i + 1] + D[i];
        } //获得每一种数字最后出现的位置。

        for(int i = 0;i < A.length;i++) {
            int j = A[i] - min;
            temp[D[j] - 1] = A[i];
            D[j]--;
        } //通过和最小值进行比较获得每个数字出现的位置，从右往左。

        for(int i = 0;i < A.length;i++){
            A[i] = temp[i];
        }   // 把temp中的顺序转到A中

        return;
    }

    public static void main(String[] args) {
        Distribution_counting_sort test = new Distribution_counting_sort();
        int[] A = {1,1,2,3,4,5,6,7,8,9,2,4,5,4,3,4,5,2,3,4,5,2,3,5,4,2,3,5,4,3,2,5,3,3,5};
        test.distributionCountingSort(A, 1, 9);
        for(int i = 0;i < A.length;i++)
            System.out.print(A[i]+" ");
    }
}
```

* 总结： 因为 Distributed computing sort 不是 comparison sorting， 不需要进行比较
* 时间复杂度为O(n)
* 



##### 2.Horspool (字符串匹配算法)

**注意这是一种对Boyer-Moore的简化算法**

定义：Horspool算法是一种基于模式预处理的输入增强的简单字符串搜索算法。

* 对模式进行预处理，生成一个移位表(**shift**)，确定在发生不匹配时将模式移位多远
* 始终根据文本的字符c进行移位，并根据移位表中的c项与模式中的最后一个字符对齐

**图解：**

![image-20220504173427861](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220504173427861.png)

**情况1：**看第一行，模式中不存在c（此时c就是字母A），模式的移动长度就是它的全部长度，移到第二行所示的位置。

**情况2：**看第二行，c（此时c就是字符O）正好是模式的最后一个字符，但是从右向左比较时，有字符不匹配，比如此时的**A**和**E**不匹配。而且模式中的其他**m-1**个字符也不包含c。移动的情况类似情况1，移动的幅度等于模式的全部长度，移到第三行所示的位置。

![image-20220504174016121](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220504174016121.png)

**情况3：**看第一行，模式中存在c（此时c就是字符L），但是它不是模式的最后一个字符，移动时应该把模式中最右边的c和文本中的c对齐，移到第二行所示的位置。

**情况4：**看第二行，c（此时c就是字符O）正好是模式的最后一个字符，但是从右向左比较时，有字符不匹配，比如此时的**A**和**E**不匹配。而此时模式中的其他**m-1**个字符包含c。移动的情况类似情况3，移动时应该把前**m-1**个字符中最右边的c和文本中的c对齐，移到第三行所示的位置。



-- 总结：

该算法是将子字符串P与母字符串T进行比较，将P中的每一种字符赋予对应的跳转距离，因为跳转距离等于各个字符串到最后一个字符的距离（不存在在P中的字符串的跳转距离为P字符串长度，最后一个字符不予计算），所以不需要一个个进行对比寻找，速度更快。



但是这代码我卡住了，不知道该怎么写

public static void  judge (String text, String pattern) {
		//text是文本 pattern是模式字符串
		int textIndex=pattern.length()-1;//文本游标,负责匹配
		int patternIndex=pattern.length()-1;//模式下标,负责匹配
		while(textIndex<text.length()) {
			int number=0;//判断是否满足存在模式串
			for(int i=patternIndex;i>=0;i--) {
				if(text.charAt(textIndex)==pattern.charAt(i)) {
					number++;
					textIndex--;
				}
				else {
					number=0;
					boolean flag=true;
					for(int j=0;j<i;j++) {
						if(pattern.charAt(j)==text.charAt(textIndex)) {
							textIndex+=(i-j);
							flag=false;
							break;
						}
					}
					if (flag) {
						textIndex+=1+patternIndex-i;
					}
					break;
				};
				if (number==patternIndex+1) {
					System.out.println("yes");
					return;
				}
			}
		}
		System.out.println("no");
	}

#### 提前结构化（Pre-Structuring）

定义：使用数据结构来预处理输入值来让访问元素更加容易



## Lecture 11

### Single-Source shortest-paths

#### Bellman-Ford algorithm-Short paths

因为Dijlstra`s Algorithm并不能处理权值边为负数的情况

##### 放松操作

![image-20220505012333765](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220505012333765.png)

上面就是**放松**的定义，它的实质就是判断一个顶点能不能有更好的选择，已知的最短路径能不能更短；如果满足那个不等式，就说明我们可以找到一条更好的路径，就**更新**它，**改进**它！

上面我们谈到的是**对边的放松**，但是在实际的代码实现中，我们的操作是**对一个顶点进行放松**。这儿理解起来很自然，**对一个顶点进行放松就是对所有从该顶点发出的边进行放松的总和**

* 记住，放缩的顺序非常重要！

![image-20220505013331896](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220505013331896.png)

* 决定放松顺序的是**【有环无环】【有无负权重边】**
* 负权环：权值均为负数的环

###### 课堂实例：

1.

![image-20220505015633621](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220505015633621.png)

2.

![image-20220505020245136](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220505020245136.png)

![image-20220530202845257](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220530202845257.png)



#### Dynamic Programming

写出一个将问题的解与子问题的解联系起来的公式。

![image-20220505020526047](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220505020526047.png)

将一个问题分解成诺干小问题求解的方法。

##### Floyd`s Algorithm(弗洛伊德算法)

![image-20220505023008478](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220505023008478.png)

其中[matrix](https://so.csdn.net/so/search?q=matrix&spm=1001.2101.3001.7020)[i,j]表示i到j的最短距离，k是穷举i到j之间可能经过的中间点，当中间点为k时，对整个矩阵即从i到j的路径长度进行更新，对所有可能经过的中间点进行遍历以得到全局最优的最短路径。

![image-20220530204326075](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220530204326075.png)

#### Warshall Algorithm

https://www.bilibili.com/video/BV1UZ4y1K7Uu/?spm_id_from=333.788.recommend_more_video.3

![image-20220506121600933](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220506121600933.png)

![image-20220506114133350](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220506114133350.png)

![image-20220506131754088](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220506131754088.png)

![image-20220506131724201](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220506131724201.png)



## Week9

### Lecture12

#### Longest Common Subsequencce (LCS)最长公共子序列

给定序列s1={1,3,4,5,6,7,7,8},s2={3,5,7,4,8,6,7,8,2}，s1和s2的**相同子序列**，且该子序列的长度最长，即是**LCS**。
s1和s2的其中一个最长公共子序列是 {3,4,6,7,8}

* 子序列：去除母序列中的部分字母，并**保持原有元素序列**所得到的结果就是子序列。
* 最长公共子序列方法不可以使用蛮力破解，因为其时间复杂度程指数型，太麻烦。

#### 动态规划解决LCS问题

https://www.bilibili.com/video/BV14A411v7mP?spm_id_from=333.337.search-card.all.click

**讲的很好，可以作为参考。**

##### 初始化Initialization

Optimal Substructure 优化子结构

![image-20220505203213589](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220505203213589.png)

![image-20220505205247884](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220505205247884.png)

#### 递归解决Recursive Solution

![image-20220505205610207](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220505205610207.png)

![image-20220505212223538](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220505212223538.png)



计算LCS长度

![image-20220505213235070](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220505213235070.png)

#### 回溯Trace Back

### Pairwise Sequence Alignment Problem（成对序列比对问题）

**例子：**

Given

-- a pair of sequences(DNA or protein)

-- a method for scoring a candidate alignment

![image-20220505213830453](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220505213830453.png)



##### 全局对比（Global Alignment）

![image-20220505220824361](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220505220824361.png)

![image-20220505220852178](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220505220852178.png)

我们将两个表分成名为大表和小表

以求-2为例子， 

* c1 = 0+-2(这个-2是小表中（P，H）的值，与大表的位置相对。)
* c2 = -8+d = -8+-8=-16
* c3 = -8+d = -8+-8=-16

##### Local Alignment(局部对比)

与全局对比类似，但多了一个可能出现的情况

![image-20220505221549126](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220505221549126.png)

![image-20220505221625315](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220505221625315.png)

![image-20220506140821187](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220506140821187.png)

**<font color='red'>注意大表和小表的xy不对应,找！！！！！PH对应PH，而不是1，1对应1，1</font>**

## Week10

### Lecture13

#### P问题(easy to find)

定义：在**多项式时间**内可以解决的问题(在多项式的时间里是可以验证的)

![image-20220506154450628](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220506154450628.png)

#### NP问题(easy to check)   non-deterministic Polynomial time

定义： 非确定性**多项式时间**可以解决的问题

![image-20220506154506068](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220506154506068.png)

 **P=NP 问题在表达什么：是否所有NP类问题都可以在多项式时间内解决并验证，也就是转化为P类问题。**

![image-20220506161012207](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220506161012207.png)

#### 归约化

![image-20220506155631255](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220506155631255.png)

![image-20220506155937416](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220506155937416.png)



#### NPC问题（Non-deterministic Polynomial complete problem）

基本定义

- NPC问题属于NP问题
- 对于所有NP问题都可以归约化到它

NPC问题Non-deterministic Polynomial complete problem又称NP完全问题，NP问题就是大量的NP问题经过**归约化**而发现的终极bossNP问题。



#### NP-hard问题（(NP-hard problems）

定义：

* NPH问题不一定是NP问题
* 对于所有NP问题都可以归约化到它

![image-20220506160554369](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220506160554369.png)

#### 多项式时间

![image-20220506153429440](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220506153429440.png)

![image-20220506153634254](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220506153634254.png)



## Week11

### Lecture14

#### 回溯

回溯：当不满足条件时，自动回溯到上一步，而省去了继续试错的时间。

例子：

##### **八皇后问题**

![image-20220506172424476](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220506172424476.png)

![image-20220506172518096](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220506172518096.png)

##### **哈密顿回路问题**

**定义：哈密顿图:图G的一个回路,若它通过图的每一个节点一次,且仅一次,就是哈密顿回路.**

* 欧拉图：
  * **通过图**（无向图或有向图）中所有边一次且仅一次行遍图中所有顶点的通路称为欧拉通路，通过图中所有边一次且仅一次行遍所有顶点的回路称为欧拉回路。具有欧拉回路的图称为欧拉图（Euler Graph），具有欧拉通路而无欧拉回路的图称为半欧拉图。

![image-20220506172612240](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220506172612240.png)

**下面的图解只寻找了一个解，实际上不止一个。**

![image-20220506173751262](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220506173751262.png)

##### Subset-sum problem (子集和问题)

定义：**给定一个包含N个非负数的set， 并且给定K, 从[集合](https://so.csdn.net/so/search?q=集合&spm=1001.2101.3001.7020)中找出一组元素子集， 使得这组子集的各个元素相加起来和是K。** 

![image-20220506174408236](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220506174408236.png)

![image-20220506174417194](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220506174417194.png)

#### Branch-and-Bound 分支定界

![image-20220506183413811](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220506183413811.png)

##### 分配问题 Assignment Problems

![image-20220506184236887](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220506184236887.png)

![image-20220506184245660](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220506184245660.png)

![ ](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220506184300206.png)

![image-20220506184308734](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220506184308734.png)

##### 旅行商问题 Traveling Salesman Problem

![image-20220506184416190](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220506184416190.png)

lb是相邻最近的两个城市之间距离的平均值

**<font color = red size = 3>如果已经确定了一条边或两条边，则在某条边距离固定的情况下找另一条边以求Ib。</font>**

<font color = red size = 3>字母的顺序代表有字母1到字母2再到字母3的顺序。</font> 

![image-20220506201205273](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220506201205273.png)

 

## Week12

### Lecture15

#### 01背包问题的动态规划解决

https://blog.csdn.net/mu399/article/details/7722810?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522165215279516782248544522%2522%252C%2522scm%2522%253A%252220140713.130102334.pc%255Fall.%2522%257D&request_id=165215279516782248544522&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~first_rank_ecpm_v1~rank_v31_ecpm-1-7722810-null-null.142

![image-20220510120359128](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220510120359128.png)



##### 01 背包问题寻找物品（Finding the Items）

![image-20220510120533476](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220510120533476.png)

k指的是背包现在可以承受的重量

wi指此时i物体的重量。

![image-20220510121446078](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220510121446078.png)

![image-20220510121508069](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220510121508069.png)

![image-20220510121519382](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220510121519382.png)

![image-20220510121532058](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220510121532058.png)

![image-20220510121543009](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220510121543009.png)











