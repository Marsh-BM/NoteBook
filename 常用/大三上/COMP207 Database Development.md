# COMP207 Database Development

## Lecture2 Reaminder of logistics and start of SQL



### 0. Introduction to SQL/relational databases
#### 0.1 Relation Database

![image-20230108152507337](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230108152507337.png)

* Data is organised in tables (also called relations)
* 数据组织在表中(也称为关系)
* Each table has a schema.  每个表都有一个模式。
* The schema of Items is:Items(name,price,number) and the schema of Employees is Employees(birthday,first_name,family_name)
* <font color=blue>schema指的是表名和列名</font>

##### 0.1.1 In typical use (Tables)

![image-20230108153404423](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230108153404423.png)

* Few columns/attributes that are fixed (i.e. in name and type of content)
* 固定的列/属性很少(即名称和内容类型)
* The number of rows depends on the table and can change
* 行数取决于表，并且可以更改

##### 0.1.2 In typical use (Rows)

![image-20230108153645684](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230108153645684.png)

* Each row corresponds to an entity or similar, or to a relationship between such
* 每行对应于一个实体或类似实体，或对应于两者之间的关系
* <font color=blue>数据库的每一行往往代表着一个客观物体，或者物体间的关系(比如自然连接的时候)</font>

#### 0.2 SQL

![image-20230108154030135](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230108154030135.png)

* Relational databases are accessed using SQL (Standard Query Language)
* 关系数据库使用SQL接入
* The standard for SQL is updated every few years, but it has been awhile currently
* SQL标准每隔几年就会更新一次，但是现在已经有一段时间了
* The implementations does not follow the standard that well though
* 不过，实现并没有很好地遵循标准
* 对于某些事情，实现遵循一些标准，但对于SQL，标准反映了实现中的新特性

![image-20230108154234296](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230108154234296.png)



### 1. Data Defination Language

#### 1.1 Create

<font color='blue'>Create Table databasename; </font>//创建数据库

<font color='blue'>CREATE TABLE Table_name (</font>
<font color='blue'>column1 datatype,</font>
<font color='blue'>column2 datatype,</font>
<font color='blue'>column3 datatype</font>
<font color='blue'>);</font> //创建表，以及表存在的列

Example：

![image-20221010171158190](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221010171158190.png)

**对于SQL语言来说，格式无所谓**

![image-20230108154605907](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230108154605907.png)

#### 1.2 Use 

USE CS_Store;

#### 1.3  DataTypes

![image-20221010171138571](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221010171138571.png)

#### 1.4 Unique

**unique函数，它的功能是元素去重。即”删除”序列中所有相邻的重复元素(只保留一个)。**此处的删除，并不是真的删除，而是指重复元素的位置被不重复的元素给占领了(详细情况，下面会讲)。由于它”删除”的是相邻的重复元素，所以在使用unique函数之前，一般都会将目标序列进行排序。
![image-20221010172246289](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221010172246289.png)

**避免添加重复数据, 也就是说如果想保证某一个字段的值永远不重复, 那么就可以将这个字段设置为唯一键。**

#### 1.5 Primary Key

![image-20221010172337296](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221010172337296.png)

**主键用于唯一标识表中的每一条数据。**

<font color=red>主键的特征: 不能重复, 不能为空。</font>

auto_increment（自动增量）的字段必须是主键, 但是主键不一定是auto_increment的。
一个表只能有一个主键, **但是主键可以是1个或多个字段组成**



#### 1.6 Foreign Key

**外键用来建立主表与从表的关联关系，为两个表的数据建立连接，约束两个表中数据的一致性和完整性**。

**外键可以有<font color='red'>重复的, 可以是空值，</font>用来建立和加强两个表数据之间的连接**

![image-20221010173702297](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221010173702297.png)

**为什么外键可以为空？**

![image-20221013234248339](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221013234248339.png)

**为什么外键可以重复？**

细想一下，一个学生表，一个专业表。二者关联时，在学生表里，专业编号为主键，可以出现重复，但是在专业表里，专业编号为唯一主键。

![image-20221013234525466](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221013234525466.png)

**主要原因就是这是两个表**

#### 1.7 Remove Things

删除表或者库

![image-20221010173726843](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221010173726843.png)

#### 1.8 Modifying Tables

![image-20221010173800349](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221010173800349.png)

* 最后就是modify，modify用于修改表中字段的数据长度，数据类型以及字段的约束条件的。

## Lecture1&2 Quiz and Assignment

### Week1 Quiz

#### Quiz  for introduction to SQL

元组tuple是关系数据库中的基本概念，关系是一张表，表中的每行(即数据库中的每条记录)就是一个元组，在二维表里，元组也称为记录。

![image-20230108160307163](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230108160307163.png)

schema指的是表名和列名的汇总

![image-20230108160420522](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230108160420522.png)



SQL中使用Varchar(20)来代替String类型

![image-20230108161047960](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230108161047960.png)

#### Quiz for SQL DDL

没啥好讲的，记住标准的SQL语言规则

![image-20230108161153656](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230108161153656.png)

#### Quiz for SQL DML except queries

可能会误伤其他人

![image-20230108161607937](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230108161607937.png)



什么是SQL injection？

* A common attack based on excecuting SQL received from the internet, without any checks
* 一种常见的攻击，基于执行从互联网接收的SQL，没有任何检查

![image-20230108161755846](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230108161755846.png)



#### Week1 Quiz

**没什么难的题，基本上都是格式与文字游戏，关键是读题，一大堆各自英语字母叠起来是真的不想读**



### Week2 Quiz

#### Quiz for SQL queries - required part

![image-20230108172941347](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230108172941347.png)

两个表的自然连接最多是笛卡尔积的值，最少为0（）

![image-20230108174717925](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230108174717925.png)

Select哪里来的Size(R)*Size(S)这种结构啊。。。。。傻逼

![image-20230108174820825](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230108174820825.png)

![image-20230108174828699](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230108174828699.png)

注**意：Natural Join会根据两个表列名相同的部分进行Join，如果没有相同的列名，就使用笛卡尔积**



#### Quiz for SQL queries - optional part

![image-20230108175952020](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230108175952020.png)

没能太搞懂这个

![image-20230108180235850](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230108180235850.png)

**很怪，这个意思是在合成为一个组的时候，如果a对b不是独一无二的，就会出现错误？可是一般也会出现结果啊**



#### Quiz for SQL queries - misc.

![image-20230108181518404](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230108181518404.png)

![image-20230108181532604](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230108181532604.png)

下节课Lecture6的内容

![image-20230108181552128](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230108181552128.png)

#### Week2 Quiz

![image-20230108214458028](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230108214458028.png)

**感觉对于我来说，这些题目最麻烦的在读题方面**





## Lecture3

### 1. Data Manipulation Language 数据控制语言

![image-20230108214614507](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230108214614507.png)

#### 1.1 Insert 

![image-20221010180145830](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221010180145830.png)

![image-20221010180216098](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221010180216098.png)

##### 1.2.1 SQL Injections SQL注射

![image-20230108214836742](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230108214836742.png)

* A common attack based on excecuting SQL received from the internet, without any checks
* 一种常见的攻击，基于执行从互联网接收的SQL，没有任何检查

![image-20230108215002590](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230108215002590.png)

![image-20230108215010447](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230108215010447.png)

**如图，非常明白的。因为没有检查输入的值，导致整个表Users被删除。这个也和SQL语言对格式要求不严格的关系有关。**

###### 1.2.1.1 How to avoid SQL Injection attacks

![image-20230108215210994](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230108215210994.png)

![image-20230108215611188](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230108215611188.png)

SQL中，;代表着一个查询的结束



#### 1.2 Where

**具体查询语句：select <字段> from <表名> where <查询条件>**

![image-20221010233018064](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221010233018064.png)

![image-20221010233047193](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221010233047193.png)

![image-20221010233157096](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221010233157096.png)

![image-20221010233217956](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221010233217956.png)



#### 1.3 Update

![image-20221010233331167](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221010233331167.png)

#### 1.4 Arithmetic Operator 算术运算符

![image-20221023152819783](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221023152819783.png)



### 2. Queries - Required Part

##### 2.1 The Order of Queries

![image-20221010235203987](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221010235203987.png)

### 3. Select

##### 3.1 Projection (𝜋)

![image-20221010235345370](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221010235345370.png)

##### 3.2 DISTINCT

<font color='red'>DISTINCT用于删除重复的行</font>

![image-20221010235429070](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221010235429070.png)

![image-20221010235436011](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221010235436011.png)

##### 3.3 Renaming (𝜌)

Renaming 允许重命名属性

![image-20221010235539888](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221010235539888.png)

##### 3.4 Creating New Columns

![image-20221010235926725](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221010235926725.png)

<font color='red'>如图，可以看出price*number</font>

![image-20221011000019416](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221011000019416.png)

![image-20230108220749515](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230108220749515.png)

这些很多都是给Lecture6做铺垫的



### 4. Cross Product（交叉连接）

交叉连接 主要作用是按照交叉相乘的方式将多个表格连接成一个表格 俗称**笛卡尔积**

![image-20221011000810525](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221011000810525.png)

通过上图，很明显可以看到是由图1（3 row）X 图2（2 row）相乘得到的。





## Lecture4 

### 1. Natural Join

![image-20221011130831228](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221011130831228.png)

通过观察上图可以看出，Natural Join 直接通过两个表都存在的元素e_id将两个表进行连接。因为Employee中的David不存在相对应的表在Transactions。所以得出表没有与之相对应的列。

![image-20221011131227292](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221011131227292.png)

在这里我觉得比较有意思的是<font color='blue'>From Employee E, Transactions T</font>

在这一段里发现我们可以在From 里将表的名称进行简写，并在下面进行引用。

<font color=red size=5>自然连接的缺点</font>

自然连接不需要指定连接条件，可以自动匹配同名的列，不需要指定匹配的列。

 但也有缺点，虽然可以指定查询结果包括哪些列，但不能人为地指定哪些列被匹配,而内连接就可以自由指定。

<font color='red' size=5>注意：自然连接在两个表没有相同的表名时，自然连接会使用笛卡尔积进行连接</font>

### 补充：多表连接

![image-20221017234925775](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221017234925775.png)



### 2. Where

#### 2.1 Where: In

![image-20221011132920141](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221011132920141.png)

或者

**<font color=red>后面加一个表，与表中的内容进行对比</font>**

![image-20221011132937964](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221011132937964.png)

#### 2.2 Where: EXISTS

![image-20221011133245141](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221011133245141.png)

本质上，使用EXISTS编写子查询，如果它返回一些内容，则当前行将被保留，否则将被抛出。您可以在子查询中使用当前行的属性

下面这个就是EXISTS的一个很好的例子

![image-20230109152512512](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230109152512512.png)



#### 2.4 Where：Semi-Join

<font color='red'>半连接 Semi-Join根据行集合中的行是否包含在另一个行集中来过滤行集的方法

![image-20230109152843824](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230109152843824.png)

### 3. Group By

![image-20221011134354406](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221011134354406.png)

![image-20221011135313661](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221011135313661.png)

情况1：

当Group by后接一个列名时，就按照列名进行分类。如果当后面接两个列名时，则使用两个列名进行分类。

![image-20221011135600859](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221011135600859.png)

![image-20221011135522789](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221011135522789.png)



### 4. Having

用于Group by的后面进行修饰，作用类似where，但是用于Group by后面

因为之前的规则，where出现在Group by之前，而在这之后的限定条件则是使用having

![image-20230109154050407](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230109154050407.png)

### 5. Order By

![image-20221011140010704](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221011140010704.png)

**排序，默认是按照从小到大的数字顺序或字母顺序。**

## Lecture5

### 1. About the full queries instead of parts

书写顺序

![image-20221011175759459](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221011175759459.png)

**程序的执行顺序**

![image-20221011175826355](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221011175826355.png)



### 2. Views

**<font color=red>在SQL中，Views是基于SQL语句的结果集的可视化的表。</font>**

个人理解：View会对数据库进行重构，而不影响程序的执行。通俗的讲，视图只保存了查询的SQL逻辑，不保存查询结果。

#### 2.1. The function Of Views

1. 提高了<font color='red'>**重用性**</font>，就像一个函数。如果要频繁获取user的name和goods的name。就应该使用以下sql语言。示例：

![image-20221011180939747](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221011180939747.png)

![image-20221011220032607](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221011220032607.png)



2. <font color='red'>对数据库重构，却不影响程序的运行</font>。假如因为某种需求，需要将user拆房表usera和表userb，该两张表的结构如下：

![image-20221011181233580](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221011181233580.png)

`create view user as select a.name,a.age,b.sex from usera as a, userb as b where a.name=b.name;`

3. <font color='red'>提高了安全性能。可以对不同的用户，设定不同的视图。</font>例如：某用户只能获取user表的name和age数据，不能获取sex数据。则可以这样创建视图。示例如下：

`create view other as select a.name, a.age from user as a;`

4. <font color='red'>让数据更加清晰。想要什么样的数据，就创建什么样的视图。</font>

#### 2.2 The Operation for Views

根据视图中的默认数据,不能修改(即更新、删除或插入)可以用触发器来完成,但在这个模块中<font color='red'>没有覆盖</font>

![image-20221011220220624](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221011220220624.png)

![image-20221011220351847](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221011220351847.png)

### 3. Union

Union的作用非常简单且易于理解

![image-20221011220553984](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221011220553984.png)

* 注意Union的两个Select的列的数量需要保证一致。
* ![image-20230109154832519](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230109154832519.png)

## Lecture6 Relational Algebras

### 1. Relational Algebra 关系系数

<font color=red size=7>**参考文章**</font>

https://www.jianshu.com/p/f7f9440e30a5



**<font color='red' size=6>关系代数是一种抽象的查询语言，使用对关系的运算来表达查询。</font>**

![image-20221011222500368](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221011222500368.png)

#### 1.1 选择运算（Select）𝜎  where

![image-20221011223318408](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221011223318408.png)

<font color='black' size=6 >𝜎</font>

选择谓词的分类

- 比较：=、≠、<、≤、>和≥
- 连词：and(∧)、or(∨)和not(¬)==>可以将多个谓词合并成一个大的谓词
- 可以包括两个属性（字段的比较）：σCOMM>SAL(EMP)表示抽成大于工资的人

![image-20221011223840491](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221011223840491.png)

#### 1.2 投影运算（project）∏  Select

<font color='red'>相当于SQL语句中的SELECT子句的职能</font>

- #### 格式：∏字段序列(关系)

![image-20221011224035422](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221011224035422.png)

<font color=blue size=6>关系的组合运算</font>

就像SQL中select、where子句那样的组合效果

![image-20221011225333224](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221011225333224.png)

#### 1.3 并运算（Union）∪

相当于SQL中UNION关键字的职能

- #### 格式：（关系r）∪（关系s）

![image-20221011225622828](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221011225622828.png)

**几点需要额外注意的**：

- 此处的并运算是集合运算，所以结果是<font color='red'>去重</font>的，结果集中不存在重复的元组（***而在SQL语句中，指定UNION ALL是可以保留重复的\***）
- 关系r与关系s必须是<font color='red'>同元</font>的，即它们的属性的<font color='red'>数目要求必须相同</font>（这就和SQL语句中UNION使用的时候要求上下两个语句的字段数相同是一样的意思）
- 关系r和关系s对应位置的**属性域应该是类型兼容**的（同样和SQL中UNION使用时，每个对应位置字段类型兼容是一样的意思

#### 1.4 集合的差运算（set-defference） —

相当于SQL语句中的EXCEPT

- #### 格式：(关系r)-(关系s)

![image-20221011230035792](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221011230035792.png)

#### 1.5 笛卡尔积运算（Cartesian-product）X

等价于SQL语句中两个表进行笛卡尔积（全匹配）得到的结果，即SQL中进行多表连接时不指定连接条件的情况

- #### 格式：(关系r)×(关系)

![image-20221011230608669](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221011230608669.png)

![image-20221011230643997](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221011230643997.png)

#### 1.6 更名运算（rename） 𝜌

等价于SQL语句中as的职能

<font size=6>𝜌</font>

![image-20221011230817503](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221011230817503.png)

![image-20221011230829198](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221011230829198.png)

#### 1.7 自然连接Natural Join  ⋈

<font size=6>⋈</font>

![image-20221011231046527](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221011231046527.png)



## Lecture7 Transact-SQL

### 1. Transaction

这个词的中文意思尚不明朗，在此全部用英文代称，个人认为事项较为合适。

#### 1.1 The defination of Transaction

A transaction is a sequence of operations performed (using one or more SQL statements) on a database as a single logical unit of work. 事务是在数据库上作为单个逻辑工作单元执行的一系列操作(使用一个或多个SQL语句)。



**简而言之，我们将<font color=red>一些系列的SQL称为Transaction</font> Transaction是一个单个的工作单元，由一系列SQL语句构成，如果Transaction成功，则Transaction期间所做的所有数据修改都将提交并成为数据库的永久部分。**



虽然这听上去很简单，但是在多个SQL语言的执行过程中，许多复杂的事情可能同时发生，进而导致不同的问题。比如，在实际生活中，由于多个SQL语言同时执行导致<font color='red'>并发(Concurrency)</font>或者由于各种原因导致SQL语句<font color='red'>部分执行(Partial Execution)</font>。

#### 1.2 The Problem1: Concurrency 并发

下图中的情况是一个很明显的例子：

User1 进行航班座位的搜索，但是在结果出现前，User2也进行了航班搜索，由于二者的先后关系，1先得到结果，148，而后2得到结果148。但是此时148已经被1预选了。进而导致并行。(Concurrency)

![image-20221013201103986](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221013201103986.png)

![image-20221013201430287](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221013201430287.png)

**那么，怎么解决这个问题？**

![image-20221013201735190](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221013201735190.png)

答案是通过Transaction对语句进行**声明**。(说实话，给我感觉有点像封装，将一部分数据封起来，不受其他东西的干扰。不过肯定不对就是了。)提醒一下，注意上图的格式。

**<font color='red'>SQL允许我们声明必须执行一组SQL语句，这样就不会产生冲突</font>**



#### 1.3 The Problem2：Partical Execution 部分执行

SQL允许我们声明事务必须原子地执行(作为一个整体或根本不执行)

简单说就是：<font color='red' size=5>经过Transaction的整体，要么整体全部执行，要么根本不执行。</font>

比如如果一个事项是付钱，拿东西，你在付完钱后的步骤连接断开，那这个东西还能拿吗？就是解决这个问题

![image-20221013204546232](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221013204546232.png)

**和Concurrency一样，也可以通过声明来解决**

![image-20221013230548129](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221013230548129.png)

**模板**

![image-20221013230812523](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221013230812523.png)

结束选项有两种，一。commit(结果写入数据库)或者 Rollback（放弃该transaction）



### 2. Making things lower level (and simpler)

![image-20230109171018470](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230109171018470.png)

没啥好说的，将SQL Statements转换成相对应的操作

下面是简化

![image-20230109171135787](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230109171135787.png)

#### 2.1 Basic Operations of Transactions Transactions的基础操作

![image-20230109171251361](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230109171251361.png)

* read(X): 主要是读取包含X的地址以及从磁盘或者缓冲区复制
* write(X): 将程序变量X的值写入名为X的数据库项. 也是找地址，复制，修改

#### 2.2 Transactions的模板

![image-20230109171618826](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230109171618826.png)

#### 2.3 Schedules 时间表

* Schedules hold many transactions for execution
* 进度表包含许多待执行的事务
* The operations making up the transactions are then executed by the schedule in some order
* 构成事务的操作然后由调度以某种顺序执行
  * It must preserve that the operations in each transaction happens in the right order!
  * 它必须保证每个事务中的操作以正确的顺序发生!
* Two types:
  * Serial Schedules 串行表
    * Executes the transactions one after another (i.e. first each operation of the first schedule, then each operation of the second and so on)
    * 一个接一个地执行事务(即首先执行第一个调度的每个操作，然后执行第二个调度的每个操作，以此类推)
  * Concurrent Schedules 并行表
    * Can interleave operations from the transactions (while still preserving that the operations in each transaction happens in the right order) - formally speaking, a serial schedule is therefore also concurrent...
    * 可以在事务中穿插操作(同时仍然保持每个事务中的操作以正确的顺序发生)-从形式上讲，串行调度因此也是并发的…

![image-20230109171902709](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230109171902709.png)

![image-20230109172112313](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230109172112313.png)

##### 2.3.1 Shorthand Notation for Schedules 时间表的速记

![image-20230109172207280](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230109172207280.png)

![image-20230109172249488](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230109172249488.png)

![image-20230109172314828](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230109172314828.png)

**<font size=5>并行时间表</font>**

![image-20230109172328302](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230109172328302.png)

不太明白为什么？？？



## Lecture8

<font color=red>这节课主要讲了一些关于Transaction更加具体的东西</font>

### 1. Problem 3: Concurrency & Partial 
![image-20221021100632246](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221021100632246.png)

### 2. ACID Properties

https://blog.csdn.net/dengjili/article/details/82468576?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522167328091416800180656549%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=167328091416800180656549&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_positive~default-1-82468576-null-null.142^

![image-20221021100728151](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221021100728151.png)

#### 2.1 Atomicity 原子性

**[原子性](https://so.csdn.net/so/search?q=原子性&spm=1001.2101.3001.7020)是指事务是一个不可分割的工作单位，事务中的操作要么都发生，要么都不发生。**

![image-20230109192528749](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230109192528749.png)

A transaction is an atomic unit of processing 事项是处理的原子单元

* 一个不可分割的执行单位

* 全部执行或不执行

Deals with failure (“aborts”)处理失败(“中止”)

* 用户终止事务(例如，取消按钮)

* 系统终止事务(例如，死锁)

* 事务终止自己(例如，意外的数据库状态)

* 系统崩溃，网络故障等。

<font color='red' size=4>Abort</font>

当事项出现错误时

中止——一个错误阻止了完全执行

* 我们撤消到错误点的工作

* 系统重新创建数据库状态，因为它是在事务中止之前开始

<font color='red' size=4>Commit</font>

当事项没有出现错误时

提交-没有错误，整个事务执行

* 系统正常更新

![image-20230109192955624](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230109192955624.png)

![image-20221021102232274](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221021102232274.png)

![image-20230109194414115](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230109194414115.png)

#### 2.2 Consistency 一致性

<font color='red' size=5>事务的正确执行必须使数据库从一种一致状态变为另一种一致状态。事务前后数据的完整性必须保持一致。</font>

![image-20230109194658824](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230109194658824.png)

* 弱版本:交易可能不违反约束

* 强大的版本:它应该正确地转换数据库状态，以反映现实世界事件的影响

* ![image-20230109194554721](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230109194554721.png)

这会产生两种结果

1. Commit (Successful)
   1. 执行成功，数据库保留
2. Abort(Failed)
   1. 执行不成功，则将数据库恢复到原来的状态。

![image-20230109194722781](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230109194722781.png)



#### 2.3 Isolation 隔离

<font color='red'>**事务的隔离性是多个用户[并发](https://so.csdn.net/so/search?q=并发&spm=1001.2101.3001.7020)访问数据库时，数据库为每一个用户开启的事务，不能被其他事务的操作数据所干扰，多个并发事务之间要相互隔离。**</font>

![image-20221026191837992](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221026191837992.png)

![image-20230117233925891](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117233925891.png)

* **Read uncommitted (basically, not having Isolation at all): It is fine if you read data which has not been committed**
* **读取未提交的数据(基本上，根本没有隔离功能):如果读取未提交的数据也没问题**
* **Read committed: Everything you read must have been committed before you can see it**
* **认真阅读:你读的个东西在你看到之前必须提交**
* **Repeatable read: ... and If you read the same thing twice in a transaction, you must get the same return value**
* **可重复读取:…如果你在一个事务中读相同的东西两次，你必须得到相同的返回值**
* **Serializable**





隔离的基本版本也是**Serializable可序列化**的

* 再次，时间表是串行的，如果它等价于串行时间表

![image-20221021104439002](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221021104439002.png)

#### 2.4 Durability **持久性**

<font color=red>**一旦事务提交并更改了数据库，这些更改就不会因为后续的失败而丢失. 持久性是指一个事务一旦被提交，它对数据库中数据的改变就是永久性的，接下来即使数据库发生故障也不应该对其有任何影响**</font>

![image-20230109195545659](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230109195545659.png)

* Once a transaction commits and changes the database, these changes cannot be lost because of subsequent failure 
* 一旦事务提交并更改了数据库，这些更改就不会因为后续的失败而丢失
  * The effect of a transaction on the database should not be lost after the commit point
  * 事务对数据库的影响不应在提交点之后消失
    * But could be overwritten by a later update
    * 但可能会被稍后的更新覆盖
  * We REDO the transaction if there are any problems after the update
  * 如果更新后出现任何问题，我们将重做事务
  * Durability deals with things like media failure
  * 持久性涉及媒体失败等问题

![image-20221021104502997](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221021104502997.png)

##  Lecture9  Serial vs concurrent schedules

![image-20221022094410050](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221022094410050.png)

![image-20221022095135087](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221022095135087.png)

* We had two components in transaction management: 
* 我们在事务管理中有两个组件:
* Concurrency control  
* 并发控制
* Logging and recovery
* 日志和恢复

### 1. Serial Schedules and Concurrent Schedules (串联和并联时间表)

#### 1.1 Serial Schedules and Concurrent Schedules (串联和并联时间表)

**Serial Schedules 串行进度**/串行时间表

* execute correctly **正确执行**

* maintain consistency of the database **维护数据库的一致性**

* inefficientin multi-user environments (because transactions have to wait until 
  others are finished)  **低效的多用户环境(因为事务必须等到其他人完成)**

**Concurrent Schedules** 并行时间表

* may not execute correctly **可能无法正确执行**
* may not guarantee consistency of the database or isolation **不能保证数据库的一致性或隔离性**
* efficientin multi-user environments (if you get asked to do something, just do it!) **高效的多用户环境(如果你被要求做某事，就去做!)**

![image-20230109200139734](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230109200139734.png)

![image-20221022100105997](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221022100105997.png)

![image-20221022100117293](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221022100117293.png)

通过上图可以看出，并行时间表Concurrent Schedule也并不是同时执行两个任务，只是两个任务在极短的时间间隔内交替进行。

![image-20230109200901094](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230109200901094.png)

**时间表不是总等同于serial schedule的。**



### 2. Basic Operations Of Transactions(事项的基本操作)

#### 2.1 Read(X)

将数据库中的X读取到程序变量中。 

<font color='red'>从数据库中读取数据到程序中</font>

1. 找到包含X项的磁盘块(页)的地址
2. 将磁盘块复制到主内存中的缓冲区
3. 将项目X从缓冲区复制到程序变量X

#### 2.2 Write(X)

将程序中的变量X的值写入数据库X并命名为X

<font color=red>将程序中的变量写入数据库</font>

1. 找到包含X项的磁盘块(页)的地址。
2. 将磁盘块复制到主内存中的缓冲区
   1. 如果磁盘块还没有在一些主存储器中
   2. 将项目X从程序变量X复制到它的正确位置
   3. 将更新后的块从缓冲区立即存储回磁盘

![image-20230109201005152](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230109201005152.png)

### 3. Concurrent Schedules Do Not Guarantee Consistency or Isolation

并发时间表并不能保证一致性和隔离性

<font color='red' size=5>下面是一个非常详细的例子</font>

1. 刚刚开始，Transaction和DataBase为null

![image-20221025144556607](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221025144556607.png)

2. 开始，显示数据库的数据

![image-20221025144657102](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221025144657102.png)

3. 将数据库的数据读入缓冲区，并从缓冲区读入Transaction1

![image-20221025144731000](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221025144731000.png)

4. 将数据库从缓冲区读入Transaction2

![image-20221025144948411](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221025144948411.png)

5. X：=X+M，将Transcation2中的X更改

![image-20221025145116765](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221025145116765.png)

6. X：=X+N，将Transcation1中的X更改

![image-20221025145312141](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221025145312141.png)

7. Write(X) 将程序中的值写入缓冲区，因为此时整个事项没有结束，所以数据库没有更新。此时X=1+N

![image-20221025145649848](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221025145649848.png)

8. Read()将数据库中的Y读入缓冲区，并复制进Transcation1

![image-20221025145906453](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221025145906453.png)

9. Write() 将2中的X写入缓冲区，X被更改为1+M

![image-20221025150729703](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221025150729703.png)

10. Commit，结束2.数据库更新

![image-20221025150741767](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221025150741767.png)

11. 将Y更改为Y+N

![image-20221025150822067](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221025150822067.png)

12. 将缓冲区域的Y值写入数据库

![image-20221025150937322](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221025150937322.png)

13. Commit，1结束，更新数据库，将缓冲区域的数据写入数据库

![image-20221025151029285](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221025151029285.png)

结束，发现这个并不正确。所以得出结论：**<font color='red' size=5>并行时间表并不保证一致性和隔离性。</font>**

### 4. Serializable Schedules 

 **在数据库中，事务在[并发](https://so.csdn.net/so/search?q=并发&spm=1001.2101.3001.7020)调度过程中，会产生多种结果，什么样的调度是正确的？只有串行调度才是正确的结果。并发过程的结果只有与串行调度结果一样的才是正确的。这种并发调度被称为可串行化调度。**

**<font size=5>A schedule S is serialisable if there is a serial schedule S’ that has the same effect as S on every initial database state.</font>**

**<font color='red' size=5>一个时间表S是可序的，如果存在一个串行调度S '，它对每个初始数据库状态都具有与S相同的效果。</font>**

**注意：每个步骤都要求是一样的，比如下图2，红色的read(x)读到的是X，绿色的read()读到的也是X，但是如果换成Serializable的S`，则不存在两者都可以读到X的情况，一般是一个读到X，一个读到X+N或者X+M**

![image-20221025160021741](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221025160021741.png)

![image-20230109202024920](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230109202024920.png)

**<font color='red'>注意，对每个数据库都有相同的效果</font>**

#### 4.1 Conflict - Serializability

##### 4.1.2 Conflict – Characterisation 冲突特征

![image-20221025160403530](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221025160403530.png)

**时间表中的冲突是来自不同事项的同一操作，如果不改变其中至少一个操作，则不能交换。**

**冲突Conflict在时间表上是一对操作**

![image-20221025160753892](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221025160753892.png)

1. **来自不同的事项**
2. **访问相同的item**
3. **至少有一个是写事项**



##### 4.1.3 Conflict-equivalent and Conflict-Serializability

* Two schedules S and S’ are conflict-equivalent if S’ can be obtained from S by swapping any number of (1) consecutive (2) non-conflicting operations from (3) different transactions.
* 如果S’可以通过交换**任意数量**个**连续的**来自**不同事务的**不冲突的操作从S中获得，则两个调度S和S’是冲突等效的。

![image-20230109205636444](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230109205636444.png)

* **<font color=red>A schedule is conflict-serialisable if it is conflict-equivalentto a serial schedule.</font>**
* **<font color=red>如果调度与串行调度冲突等效，则调度是可冲突串行化的。</font>**

Example

![image-20221025161105557](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221025161105557.png)

**<font color=red>冲突可串行性：一个调度，如果可以通过交换两个无冲突的操作能够转换到某个串行的调度，则称此调度为冲突可串行化调度。</font>**

**<font color=red>注意此时的isolation等级是read uncommitted</font>**

![image-20221025160644817](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221025160644817.png)

![image-20230109205907929](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230109205907929.png)



![image-20221025162346757](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221025162346757.png)



## Lecture10 How to dicide Conflict Serializability

<font color='red'>关于判断冲突可串行化</font>

https://blog.csdn.net/LEE18254290736/article/details/79531550?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522166673094616782395330805%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=166673094616782395330805&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~top_positive~default-2-79531550-null-null.142^v59^control_1,201^v3^control_1,213^v1^control&utm_term=%E5%86%B2%E7%AA%81%E5%8F%AF%E4%B8%B2%E8%A1%8C%E5%8C%96&spm=1018.2226.3001.4187

### 1.Review The Transactions

事务(如果单独运行)总是将一个一致的数据库状态转换为另一个一致的数据库状态。

1. Commit 执行成功
2. Abort 执行失败，将数据库恢复到原来的样子

### 2 判断冲突操作的条件

冲突串行化：<font color='red'>**交换2个 没有冲突的操作 最终变成 串行调度**</font>

![image-20221025215817380](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221025215817380.png)

![image-20221025223342308](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221025223342308.png)

 串行化就是把同一个事务要做的读写操作按先后顺序排到一块。<font color='red'>并发事务可以调整成串行化的话，就称为可串行化调度。</font>

#### 2.1 Precedence Graph（前驱图）

一个有向循环图，用于描述进程之间执行的先后顺序。

![image-20221025224854842](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221025224854842.png)

非常好画，根据事项将事项分成1，2，3. 然后L2的顺序，先执行1的部分任务，然后到2，2后再到1，再从1到3.

![image-20221025225300214](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221025225300214.png)

![image-20230110153418333](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230110153418333.png)

#### 2.2 Testing Conflict-Serializability

![image-20230110154519179](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230110154519179.png)

* **To test if a schedule S is conflict-serializable:**
* **测试调度S是否可冲突序列化:**
  * **Construct the precedence graph for S.**
  * **构造S的优先级图。**
  * **If the precedence graph is no cycle, then S is conflict-serializable. Otherwise not.** 
  * **如果优先图不是循环，那么S是可冲突序列化的。否则不。**

![image-20230110160755591](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230110160755591.png)

![image-20230110160934021](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230110160934021.png)

* Consider some serial schedule
* 考虑一些串行表
* It must put some transaction T in the cycle first by definition
* 它必须首先在周期中设置一些事务
* Since there is a cycle, there must be a transaction S in the cycle that points to T
* 既然有一个循环，那么在这个循环中一定有一个指向T的事务S
* By last slide, one of the operations in S must be before one of the operations in T
* 在最后一张幻灯片中,S的操作之一必须是在T的操作之前
* But then T is not the first transaction in the cycle
* 但是T不是循环中的第一个交易
* That is a contradiction, and we can therefore not have any serial schedule
* 这是一个矛盾，因此我们不能有任何连续的时间表

#### 2.3 Example about Conflict-Serializable 

![image-20230110163119325](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230110163119325.png)

**<font color=red>找到与之对应的serial schedule</font>**

![image-20230110163232222](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230110163232222.png)

![image-20230110163634775](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230110163634775.png)

![image-20230110163913207](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230110163913207.png)

1. 找到只有输出边的节点
2. 移动相应的T，重复上述操作

![image-20230110163939890](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230110163939890.png)

### 3.  Enforcing Conflict-Serializability Using Locks

#### 3.1 Simple Locking Mechanism

**A transaction has to lock an item before it accesses it.**

**<font color='red'>事务必须在访问项目之前锁定该项目。</font>**

锁由调度程序请求并授予:

1. 每个项目每次最多被一个事务锁定。
2. 事务等待，直到可以授予锁。
3. 每个锁最终都必须释放(解锁)。

![image-20230110164225036](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230110164225036.png)

* Each lock has to be released (unlocked)eventually.
* 每个锁最终都必须被释放(解锁)。



#### 3.2 Schedules With Simple Locks(带有简单锁的时间表)

通过两个操作扩展调度语法:

![image-20221026162110297](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221026162110297.png)

![image-20221026162127442](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221026162127442.png)

1. For each ri(X) / wi(X) there is an earlier li(X) without any ui(X) occurring between li(X) and ri(X) / wi(X).
2. 对于每个ri(X) / wi(X)，都有一个更早的li(X)， li(X)和ri(X) / wi(X)之间没有任何ui(X)。
3. For each li(X) there is a later ui(X).
4. 对于每一个li(X)都有一个后面的ui(X)。
5. If li(X) comes before lj(X), then ui(X) occurs between li(X) and lj(X). 
6. 如果li(X)出现在lj(X)之前，那么ui(X)出现在li(X)和lj(X)之间。

![image-20230110165508644](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230110165508644.png)

**注意这两行是连在一起的，T1中插入了一个T2.很明显不存在一个serial S'可以和S达到相同的目的。**

![image-20230110165521694](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230110165521694.png)

在这种情况下，T2要求对Y的锁定被拒绝。此时，它是Serializable的 比如T1T2就是如此





### 4. Two-Phase Locking

https://zhuanlan.zhihu.com/p/480379228   -- 参考

首先是一个简单的锁的例子：

![image-20221031133510175](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221031133510175.png)

![image-20221031133445168](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221031133445168.png)

首先，两阶段锁强调的是<font color='red'>“加锁（增长阶段，growing phase）</font>和<font color='red'>解锁（缩减阶段，shrinking phase）</font>这两项操作，且每项操作各自为一个阶段，这就是说不管同一个事务内需要在多少个数据项上加锁，那么所有的加锁操作都只能在同一个阶段完成，在这个阶段内，不允许对对已经加锁的数据项进行解锁操作，即加锁和解锁操作不能交叉执行（同一个事务内）。这一条是说在同一个事务内部的事情。

![image-20221031134226489](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221031134226489.png)

现在算是理解了二阶段锁的含义：以下面的图为例子

首先T1进行Growing Pharse, 给自己的各个读写行为附上锁，R(A)施加S-Lock，Write(A)施加X-Lock，总之给自己的每个行为都上锁。然后在T2开始的时候，因为A被锁了，所有T2不能执行，只能在A收缩阶段Shrinking Pharse来释放锁后，才可以继续执行T2.

<font color='red'>一个事项在某一时间获得锁，且只有这一时间可以获得锁，然后在末尾结束锁。</font>

![image-20221031134535836](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221031134535836.png)



<font size=5>二阶段锁的条件</font>

**<font color=red size=5>In each transaction, all lock operations precede all unlocks. 在每个事务中,所有锁操作先于所有解锁。</font>**

![image-20221031131735830](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221031131735830.png)

![image-20230110171900973](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230110171900973.png)

![image-20230110171911594](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230110171911594.png)



**<font color=red size=5>2PL可以保证时间表是冲突可串行化的，但是会导致两个问题</font>**

1. **死锁(DeadLocks)**
2. **Other issues**



#### 4.0 Risk of Deadlocks

![image-20230110204137408](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230110204137408.png)



**这个就属于是死锁了，T1还没有释放X，T2无法要求锁住X**

### 5.如何让2PL更加灵活

换句话说，如何预防死锁Deadlock

**Solution**: <font size=4.5>different lock modes</font>

#### 5.1 Shared & Exclusive Locks 分享锁和排他锁

**Shared Lock("Read Lock"):**

1. 事务请求读取项X
2. **同时授予多个事务**

**Exclusive Lock("Write Lock"):**

1. 事务请求写入项X
2. **一次最多授予一个事务**

Additional rules :

1. 只有当没有其他事务持有X上的独占锁时，才授予X上的共享锁。
2. Shared lock on X is granted only if no other transaction holds an exclusive lock on X.
3. 只有当没有其他事务持有X上的锁(任何类型的)时，才授予X上的独占锁。
4. Exclusive lock on X is granted only if no other transaction holds a lock (of any kind) on X.

![image-20221031165104148](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221031165104148.png)

之后还会有一个Update Locks 操作，简写为u-lock(X)or ul(X)

<font color='red' size=5>Note: 一个独立事项可以同时拥有X的共享锁和排他锁，因为有X和Y</font>

<font color='red'>一个X的分享锁可以被升级为排他锁, 但是可能导致死锁。</font>

#### 5.2 Update Lock 更新锁

简写为u-lock(X)or ul(X)

更新锁定是共享锁定和排他锁定的混合。共享锁是在DML执行之前进行更改之前使用的。**<font color='red'>其他事务可以读取锁定的数据，但不能修改它。一旦修改开始，它就成为一个排他锁，其他事务直到事务结束后才能读取和更新锁定的数据。</font>**因此，更新锁可以避免造成死锁。同一时间只有一个更新锁可以锁定数据，类似于排他锁。但不同之处在于，更新锁只能锁定自身，而不能修改底层数据。在修改数据之前，可以将它转换为排他锁，这可以通过提示UPDLOCK更新锁来实现。
![image-20221031170950725](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221031170950725.png)

![image-20230110210821756](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230110210821756.png)

**<font color='red' size=5>横轴是锁的类型，纵轴是可以分享的锁的类型。比如T1, u-lock(X), T2可以s-lock(X)但是不能使用其他类型的锁</font>**



![image-20230110210350926](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230110210350926.png)

* Straightforward generalisation: In each transaction, all lock operations (i.e., shared, exclusive, or update lock requests) precede all unlocks.
* 简单的泛化:在每个事务中，所有锁操作(即共享、独占或更新锁请求)都先于所有解锁。

![image-20221102194121789](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221102194121789.png)



#### 5.3 Locks With Multiple Granularity(多粒度锁)

DBMS可以在不同的粒度级别上使用锁

* 可锁定关系
* 可锁定磁盘块
* 可锁定元组

![image-20221031172152500](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221031172152500.png)

#### 5.4 Trade-Offs 权衡

权衡该怎么锁

Locking at too coarse granularity: （锁定间距太粗糙）

* 低开销(不需要存储太多信息)
* 较低的并发度:可能造成不必要的延迟



Locking at too fine granularity:（锁定粒度过细）

* 高开销:需要跟踪所有锁定的项
* 高并发度:没有不必要的延迟

需要防止以下问题，以保证(冲突)可序列化性:

* 事务持有元组的共享锁。
* 另一个事务为该关系持有排他锁。

#### 5.5 Intention Locks 意向锁

有意锁定意味着当一个事务通知另一个事务时，它有锁定数据的“意图”，所以它就像名称一样。它确保事务获得要修改的正确数据，防止其他事务获得更高级别的锁。这意味着您打算在获得锁或表上的行之前锁定一个Page。这可以防止其他事务在表上放置排他锁并试图解锁行或页。包含锁定被放置在页和表上，以防止其他事务锁定数据。

![image-20221031174059288](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221031174059288.png)

![image-20221031174109479](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221031174109479.png)

<font color=red>上面这个图非常重要</font>



## Lecture11&12  Some relational DBMS Components

![image-20230110212639631](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230110212639631.png)

**Why Might a Transaction Abort?**

1. **执行事务时出现错误**
   1. **违反完整性约束,其他运行时错误**

比较经典的错误

![image-20221102155930447](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221102155930447.png)

2. Deadlocks
   1. 例如，当使用两相锁时
   2. 并发控制请求终止事务

3. Explicit request

![image-20221102160116616](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221102160116616.png)

Beyond the DBMS`s Control

![image-20221102160244627](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221102160244627.png)

* Media failures: 媒介错误
  * The medium holding the database becomes partially or completely unreadable
  * 保存数据库的介质变得部分或完全不可读
  * Example: changes of bits, head crashes 
* Catastrophic events: 灾变事件
  * The medium holding the database is destroyed
  * 保存数据库的介质被销毁
  * Examples: explosions, fires, etc.
  * 例如：爆炸，火灾
* System failures
  * Information about the active transaction’s state is lost
  * 有关活动事务状态的信息将丢失
  * Examples: power failures, software errors
  * 例如:电源故障，软件错误





### 1. Logging in DBMS

* 想法:将重要的活动写入日志，以便稍后可以恢复所需的数据库状态
* Idea: write important activities to a log so that a desired database state can be recovered later

* 重要活动的例子:
* Examples of important activities:

* **Starts of transactions, commits, aborts 启动事务，提交，终止**

* **Modification of database items 修改数据库项目**

Should work even in case of system failures! 即使在系统故障的情况下也能工作!

![image-20221102160457088](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221102160457088.png)

#### 1.0 Extension of Transaction Syntax 事务语法的扩展

![image-20230110214241180](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230110214241180.png)

![image-20230110214400384](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230110214400384.png)

![image-20230110214408559](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230110214408559.png)

**write(X)操作只写在buffer，通过output(X)把数值从buffer复制到数据库**

![image-20230110214712419](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230110214712419.png)

* flush_log: write log entries that are currently residing in main memory (buffer) to log
* flush_log: 写入当前驻留在主存中的日志项(缓冲区)日志

**画圈的地方为缓冲区**



#### 1.1 Undo Logging 撤销

* Logs activities with the goal of restoring (“undoing”) a previous database state.
* <font color='red'>记录活动，目的是恢复(“撤消”)以前的数据库状态。</font>

![image-20221102160836136](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221102160836136.png)

* If transaction T updates database item X and the old value was v, then <T, X, v> must be written to the log on disk before X is written to disk.
* 如果事务T更新数据库项X，旧值为v，**则<T, X, v>必须在将X写入磁盘之前写入磁盘日志。**
* If transaction T commits, then <COMMIT T> must be written to disk as soon as all database elements changed by T have been written to disk
* 如果事务T提交，那么<COMMIT T>必须在将所有由T更改的数据库元素立即写入磁盘

![image-20230110215544686](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230110215544686.png)

EXAMPLE:
![image-20221102161316172](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221102161316172.png)

* 因为
  * If transaction T updates database item X and the old value was v, then <T, X, v> must be written to the log on disk before X is written to disk.
  * 如果事务T更新数据库项X，旧值为v，**则<T, X, v>必须在将X写入磁盘之前写入磁盘日志。**
* 所以第一个flush_log将数值的变化写入磁盘日志
* 然后将数值变化写入磁盘
* 因为
  * If transaction T commits, then <COMMIT T> must be written to disk as soon as all database elements changed by T have been written to disk
  * 如果事务T提交，那么<COMMIT T>必须在将所有由T更改的数据库元素立即写入磁盘



![image-20221102163220484](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221102163220484.png)

1. flush_log用于更新日志，讲现在local，buffer, database的内容写入日志。
2. output用于更新磁盘，讲buffer写入数据库
3. **<font color=red>这个图是用来和上面的那个一样，根据上面的解释很容易求解</font>**



### 2. The Recovery Manager 恢复管理

![image-20230110221026219](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230110221026219.png)

![image-20230110221036439](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230110221036439.png)

![image-20230110221043660](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230110221043660.png)



#### 2.1 Recovery With Undo Logs

* **<font color='red'>If an error occurs, the recovery manager restores the last consistent database state</font>**

* **<font color=red>如果出现错误,恢复管理器恢复最后一个一致的数据库状态.</font>**

向后遍历撤销日志

![image-20221102163952737](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221102163952737.png)

![image-20230110221625899](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230110221625899.png)

EXAMPLE：

![image-20221102164212116](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221102164212116.png)

![image-20221102164330839](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221102164330839.png)



### 3. What if a transaction aborts? 如果事务中止怎么办?

* Use the undo log to undo all changes made by the transaction.
* 使用undo日志可以撤销事务所做的所有更改。
  * Similar to recovery with undo logs
  * 类似于使用undo日志进行恢复
  * **But focuses on a single transaction**
  * **但只关注单个事务**
* Procedure:
  * Assume T aborts
  * 假设T终止
  * Traverse the undo log from the last to the first item
  * 遍历撤销日志从最后一项到第一项
  * If we see <T, X, v>, change the value of X on disk back to v.
  * 如果我们看到<T, X, v>，将磁盘上X的值改回v。

#### 3.1 Redo Logging 重做

Logs activities with the goal of restoring committed transactions (ignores incomplete transactions).

**<font color='red'>记录活动，目的是恢复已提交的事务(忽略未完成的事务)。</font>**

![image-20221102164612684](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221102164612684.png)

* **<T,X,v>这里的v是新值，不同于之前的旧值**

必须修改日志程序

![image-20221102164754948](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221102164754948.png)

* T first writes all log records for all updates
* T首先写入所有更新的所有日志记录
* T writes <COMMIT T> to the log on disk
* T将<COMMIT T>写入磁盘上的日志
* T writes all committed updates to disk
* T将所有提交的更新写入磁盘

![image-20230110223154391](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230110223154391.png)

![image-20230110223446122](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230110223446122.png)



#### 3.3 Recovery With Redo Logs 使用Redo 进行恢复

![image-20230110223845195](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230110223845195.png)

* Essentially: reverse of undo logging
* 本质上与undo logging相反
* Procedure: 步骤
  * Identify all the transactions with a COMMIT log record.
  * 使用COMMIT日志记录标识所有事务。
  * Traverse the log from first to the last item.
  * 遍历日志从第一个项到最后一个项。
  * If we see <T, X, v> and T has a COMMIT log record, then change the value of X on disk to v.
  * 如果我们看到<T, X, v>并且T有一个COMMIT日志记录，那么将磁盘上X的值更改为v。
  * For each incomplete transaction T, write <ABORT T> into the log on disk.
  * 对于每个未完成的事务T，将<ABORT T>写入磁盘上的日志。

![image-20230110224313390](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230110224313390.png)

![image-20230110224323847](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230110224323847.png)





#### 3.2 Undo and Redo Logging

* **这两句话只是感觉哈，感觉**
* Redo是从已经提交到日志的记录重做数据库
* Undo是为提交的过程，直接ctrl+Z



* **Good properties of undo logging and redo logging**
* **良好的撤销日志和重做日志属性**
* Log records:
  * Same as before, but replace <T, X, v>
  * <T, X, v, w>: “Transaction T has updated the value of database item X, and the old/new value of X is v/w.”
  * Procedure:
    * Write all log records for all updates to database items first
    * 首先写入所有数据库项更新的日志记录
    * Then write updates to disk
    * 然后将更新写入磁盘
    *  <COMMIT T> can be written to disk before or after all changes have been written to disk
    * <COMMIT T>可以在所有更改写入磁盘之前或之后写入磁盘
    * Recovery needs to process log in both directions
    * 恢复需要在两个方向上处理日志

![image-20230110225535062](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230110225535062.png)

![image-20221102170631853](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221102170631853.png)



![image-20230110225542661](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230110225542661.png)

![image-20230110225552234](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230110225552234.png)

##### 3.2.1 Undo without Redo

* Undo essentially ensures Atomicity 撤消实质上确保了原子性
* Can ensure durability using Force 使用力能保证耐久性吗
  * **Force the writing of updates to disk before commit**
  * **在提交之前强制将更新写入磁盘**
  * (No Force is not to require this)
  * (没有力量来要求这个)
  * Force is expensive in disk operations
  * 强制在磁盘操作中代价很高

![image-20230110225611794](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230110225611794.png)

##### 3.2.2 Redo without Undo

* Redo essentially ensures Durability
* 重做本质上保证了持久性
* Can ensure atomicity using No Steal
* 使用No Steal可以确保原子性
  * No Steal means that uncommitted data may not overwrite committed data on disk
  * 无窃取意味着未提交的数据不能覆盖磁盘上已提交的数据
  * (Steal is not to require this)
  * (偷是不需要这个的)
  * No Steal is expensive to ensure
  * 不偷是昂贵的保证

![image-20221102170730556](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221102170730556.png)



<font color='red' size=5>Ensuring atomicity and durability</font>

在没有日志的情况下，使用No Steal/Force可以确保原子性和持久性吗

1. 非常困难和昂贵的保证
2. (必须在执行commit语句时将事务所做的每一个更改写入磁盘!)

![image-20230110230054004](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230110230054004.png)

在实践中:

◦Want Steal/No Force(最便宜的时间)→使用Undo/Redo

![image-20221102172338948](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221102172338948.png)





## Lecture 13 & 14 & 15

https://www.bilibili.com/video/BV1yL4y1H7Kd/?spm_id_from=333.337.search-card.all.click&vd_source=9d046a6203dde4f5f1794bf980388e63

### 1. Checkpoint

检查点往往用于线性恢复程序，在执行时，它会进行以下三个步骤

1. 将当前驻留在主存中的所有日志记录输出到稳定存储器中。
2.  将所有修改过的缓冲区块输出到磁盘。
3. 将日志记录<检查点>写入稳定存储。

![image-20221113171638874](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221113171638874.png)



 举例说明
![image-20221113172032646](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221113172032646.png)

简单来说，检查点是一个数据库的存档点，当到达检测点后，将数据写入数据库，相当于存档保存。而从T2-T4属于是未能保存存档，再下一次游戏失败复活时，T2-T4所获得的金币或装备丢失。而T2-T3因为已经提交到缓存区，事件进行完毕，所以是重做，T4未进行完毕，所以撤销。



* 简单的检查点可以加快恢复速度，但是ARIES检查点却不能



# ---------------------

### 1.Recovery With Simple Checkpoints

![image-20230111200326097](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230111200326097.png)

* 简单来说，检查点是一个数据库的存档点，当到达检测点后，将数据写入数据库，相当于存档保存。
* 在上图中，我们使用undo进行回溯时，当遇到第一个chechkpoint的时候会出现停止，因为之后的内容已经被写入磁盘无法修改。

![image-20230111200941946](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230111200941946.png)

#### 1.1 ARIES Checkpoints

![image-20230111201439081](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230111201439081.png)

* Requirements:
  * Undo/Redo logging
  * Transactions do not write to buffers(!) before they are sure they want to commit
  * 事务在确定要提交之前不会写入缓冲区(!)
* Procedure:
  * Write <CHECKPOINT(T1, T2,...)> in log and flush it
  * 在日志中写入<CHECKPOINT(T1, T2，…)>并刷新
    * T1, T2,... are the transaction in progress (i.e. not committed and not aborted)
    * T1, T2,…事务是否正在进行(即没有提交也没有中止)
  * Write the content of the bufferto disk (i.e. output)
  * 将缓冲区的内容写入磁盘(即输出)
  * Write <END CHECKPOINT> in log and flush it
  * 在日志中写入<END CHECKPOINT>并刷新
* 解释一下：
* 相当于先写开始，然后把在这个节点前的内容从缓冲区写入磁盘，最后写上结束

![image-20230111202001428](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230111202001428.png)

#### 1.2 Conflict-Serialisability vs Recovery

![image-20230111202151045](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230111202151045.png)

* **Conflict-Serialisability**
* Many nice properties:许多性质
  * Equivalent to serial schedules 相当于串行调度
  * Ensure consistency / correctness  确保一致性/正确性
* Can be enforced by two-phase locking (2PL)
* 可以通过两相锁(2PL)强制
* **Logging and Recovery**
  * Suitable logging techniquesensure that we can restore desired database states
  * 合适的日志技术确保我们可以恢复所需的数据库状态
    * Undo incomplete transactions
    * 撤消未完成的事务
    * Redo committed transactions
    * 重做已提交的事务
    * Undo a single or a selected number of transactions
    * 撤消单个或选定数量的事务
* Robust: works even after system failures
* 鲁棒性：即使系统出现故障也能正常工作（系统的抗干扰能力）

![image-20230111202922213](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230111202922213.png)

![image-20230111203020026](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230111203020026.png)

#### 1.3 Dirty Reads 脏读

![image-20230118175400921](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230118175400921.png)

* In practice, the isolation property is often not fully enforced (à“dirty reads” may occur)

* 在实践中，隔离属性通常没有完全强制执行(à可能发生“脏读”)

* Reason: efficiency! 效率

  * Spend less time on preventing ”dirty reads”
  * 少花点时间防止“脏读”
  * Gain ”more parallelism” by executing some transactions that would have to wait to prevent “dirty reads”
  * 通过执行一些必须等待以防止“脏读”的事务来获得“更多的并行性”

  ![image-20230111203438389](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230111203438389.png)

* “Dirty reads” can slow down the system when transactions have to abort
* 当事务必须中止时，“脏读”会降低系统的速度

##### 1.3.1 Read Levels in SQL

1. **Read Uncommitted**
2. **Read Committed**
3. **Repeatable Read**
4. **Serializable**

#### 1.4 Cascading Rollback 连级回滚

* **<font color=red>事务(T1)导致失败，必须执行回滚。依赖于T1操作的其他事务也必须回滚，从而导致级联效应。</font>**

* Find all transactions that have read items written by T.
* 找到所有读过T写的项的事务。
* Recursively abort all transactions that have read itemswritten by an aborted transaction.
* 递归地中止已读取由中止事务写入的项的所有事务。(所有有关的事项都要停止)

![image-20230111203912398](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230111203912398.png)

![image-20230111204108256](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230111204108256.png)

**<font color= red>因为如果不放弃，所有读取T1的T都会出现影响，如果放弃，则会破坏耐久性</font>**

![image-20230111204335748](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230111204335748.png)

### 2.Recoverable Schedules 可恢复时间表

* The problem for Durability in regards to cascading rollbacks occur because a transaction T2reads data from some transaction T1, then T2commits and afterwards T1 aborts.

* 与级联回滚有关的持久性问题的发生是因为事务t2从某个事务T1读取数据，然后提交，然后t1 abort。

  

* **A schedule S is recoverable if the following is true:**

* **当满足以下条件时，计划S是可恢复的:**

  * **if a transaction T1commits and has <font color=red>read</font> an item X that was written before by a different transaction T2, ...**
  * **如果事务t1提交之前<font color=red>读取</font>了由另一个事务T2写入的项X，**
  * **<font color=red>then T2must commit before T1commits.</font>**
  * **那么t2必须在t1commit之前提交。**

![image-20230111210929462](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230111210929462.png)

![image-20230111211235756](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230111211235756.png)

* S1和S2的的可串行化很容易证明

#### 2.1 Recoverable Schedules – implicit assumption 可恢复时间表-隐含假设

* Additional implicit requirement:
* 附加的隐含要求:
* **All log records have to reach disk in the order in which they are written.**
* **所有日志记录必须按照写入的顺序到达磁盘。**
* **谁先写入缓存区谁先到达磁盘**

![image-20230111212220621](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230111212220621.png)

#### 2.2 Recoverable schedules still cascades 可恢复的调度仍然级

![image-20230111212422144](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230111212422144.png)



### 3. Cascadeless Schedules 无联级时间表

* **A schedule is cascadeless if each transaction in it reads only values that were written by transactions that have already committed.**
* **如果调度中的每个事务只<font color=red>读取</font>已经提交的事务写入的值，那么调度就是无级联的。**

![image-20230111212802775](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230111212802775.png)

![image-20230111215707542](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230111215707542.png)

**对于可恢复的时间表:**

**日志记录必须按照正确的顺序到达磁盘。**

![image-20230111215813653](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230111215813653.png)

* S1-S4不是cascadeless
* S5不是串行序列

![image-20230111215944654](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230111215944654.png)

* **<font color=red>Cascadeless schedules are recoverable:</font>**
* **无级联调度是可恢复的**
* **<font color=red>Cascadeless schedules are in general not serialisable.(recall example on previous slide)</font>**
* **无级联调度通常是不可序列化的。**



### 4. Strict Schedules 严格时间表

* **A schedule is strict if each transaction in it <font color=red>reads and writes</font> only values that were written by transactions that have already committed.**
* **如果调度中的每个事务只<font color=red>读写</font> 已经提交的事务写入的值，那么调度就是严格的。**

![image-20230111220630942](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230111220630942.png)

![image-20230111220945937](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230111220945937.png)

#### 4.1 Strict Two-Phase Locking (Strict 2PL) 严格的二阶段锁

![image-20230111221044064](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230111221044064.png)

* Most popular variant of two-phase locking (2PL) 最流行的两相锁(2PL)变体
* Enforces both:
  * Conflict-serialisability
  * Strict schedules
* **Strict locking condition (in addition to 2PL condition):除了2PL以外的条件**
  * **A transaction T must not release any lock (that allows T to write data) until:**
  * **事务T不能释放任何锁(相当于允许T写入数据)，直到:** 
  * **<font color=red>注：其实是允许T写入数据, 所以其实是可以释放分享锁，因为分享锁不允许写入数据</font>**
    * **T has committed or aborted, and**
    * **T已提交或中止，并且**
    * **The commit/abort log record has been written to disk.**
    * **提交/中止日志记录已写入磁盘。**

![image-20230111221456287](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230111221456287.png)

![image-20230111221503810](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230111221503810.png)

**上面这个图就很明确的告诉你了，只有在T被提交后，再释放锁才是满足严格2PL**

![image-20230111221641893](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230111221641893.png)

* **<font color=red size=5>T can release the shared lock on X here (shared locks do not allow T to write data)</font>**
* **<font color=red size=5>T可以在这里释放X上的共享锁(共享锁不允许T写入数据)</font>**

![image-20230111222340607](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230111222340607.png)

* **<font color=red size=5>If S is a schedule consisting of strict 2PL transactions:</font>**
* **<font color=red size=5>S is conflict-serialisable.</font>**
* **<font color=red size=5>S is strict.</font>**

![image-20230111222539961](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230111222539961.png)

## Lecture 15 All of ACID

![image-20230116233850333](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230116233850333.png)

### 1. Strict 2PL and Deadlocks 严格的2PL和死锁

![image-20230116233901784](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230116233901784.png)

![image-20230116233908962](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230116233908962.png)

* Strict 2PL yields conflict-serialisable, strict schedules

* 严格的2PL产生了conflict-serialisable和strict schedules

  

* Two approaches for deadlock prevention:

* 防止死锁的两种方法:

  * **Detect deadlocks & fix them**
  * **检测死锁并修复它们**
  * **Enforce deadlock-free schedules**
  * **强制执行无死锁计划**



#### 1.1 Deadlock Detection: Approaches

![image-20230116234209583](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230116234209583.png)

* **Timeouts  超时设定**
  * Assume a transaction is in a deadlockif it exceeds a given time limit
  * 假设事务超过给定的时间限制就处于死锁状态
* **Wait-for graphs 等待图**
  * Nodes: transactions
  * Edge from T1to T2 if T1waits for T2to release a lock
  * Deadlocks correspond to cycles 
  * 死锁对应于循环
  * 没有循环的图称为DAG
* **Timestamp-based**

![image-20230116234813048](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230116234813048.png)

* Each transaction T is assigned a unique integer TS(T) upon arrival (the timestamp of T). If T1arrived earlier than T2, we require TS(T1) < TS(T2)
* 每个事务T在到达时被分配一个唯一的整数TS(T) (T的时间戳)。**如果T1比T2早到达，我们要求TS(T1) < TS(T2)**
* <font color=blue>Timesstamp只在T到达时才被分配，且不改变(仅限于上述方法)</font>
* <font color=red size=5>Timestamps do not change even after a restart!时间戳即使在重新启动后也不会改变!</font>
* Caution: We will see a differenttimestamp-based method in the next video, where timestamps dochange after restart
* 注意:在下一个视频中，我们将看到一个不同的基于时间戳的方法，其中时间戳在重启后会发生变化

![image-20230116235200064](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230116235200064.png)

* Want to prevent cyclic dependencies such as
* 为了防止如上图所示的循环依赖
* **Use timestamps to decide which transaction can wait further and which must abort to prevent deadlock**
* **使用时间戳来决定哪些事务可以继续等待，哪些事务必须中止以防止死锁**

##### 1.1.1 Wait-Die Scheme

**旧的transactions总是等待解锁**

![image-20230116235450373](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230116235450373.png)

* Case 1: T1is older than T2 
  * T1is allowed to wait further for T2to unlock
* Case 2: T1is younger than T2 
  * T1is rolled back (“dies”)

* **Note: only older transactions are allowed to wait, so no cyclic dependencies created**
* **注意:只有较旧的事务才允许等待，因此不会创建循环依赖关系**



##### 1.1.2 Wound-Wait Scheme

**旧的交易从不等待解锁**

![image-20230116235623832](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230116235623832.png)

* Case 1: T1is older than T2
  * T2is rolled back unless it has finished(it is “wounded”)
* Case 2: T1is younger than T2 
  * T1is allowed to wait further for T2to unlock

* **Note: only younger transactions are allowed to wait, so no cyclic dependencies created**
* **注意:只允许较年轻的事务等待，因此不会创建循环依赖关系**
* 老的T不等待，因为需要item时，年轻的需要直接回滚给它。年轻的需要它的时，等待

![image-20230117000312979](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117000312979.png)

* 最终，任何有限数量的事务在Wound-Wait 下完成

* At all times, the oldest transaction can move 
* 在任何时候，最老的事务都可以移动
* Hence, eventually it finishes and there is one less transaction left and we are still doing Wound-Wait! 
* 因此，最终它完成了，剩下的交易少了一个，我们仍然在做Wound-Wait
* Wait-Die is similar, but we look at the oldest transaction or the transaction it (recursively) waits for 
* Wait-Die类似，但我们查看的是最古老的事务或它(递归地)等待的事务
* <font color=red>其实就是一个递归逐渐解决的过程</font>



* 那么另一种方法呢？

![image-20230117000518376](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117000518376.png)

#### 1.1 Timestamp-based Scheduling

##### 1.1.1 Basic Idea

* Schedule transactions so that the effect is the same as executing **each transaction instantaneously** when it is started.
* **对事务进行调度，使其效果与启动时立即执行每个事务相同。**

![image-20230117090547809](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117090547809.png)

* **Equivalent to serial schedule that has all transactions in the order of their start time.**
* **相当于按开始时间顺序排列所有事务的串行调度。**

![image-20230117090622807](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117090622807.png)

* 基于时间戳的时间表
* Grant Request
* Abort Transaction
* Delay Transaction

![image-20230117090723604](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117090723604.png)

* Each transaction T is assigned a unique integer TS(T) when it starts (the timestamp of T). If T1started earlier than T2, we require TS(T1) < TS(T2)
* 每个事务T在开始时被分配一个唯一的整数TS(T) (T的时间戳)。如果T1**开始**早于T2，我们要求TS(T1) < TS(T2)
* <font color=red size=5>We assign a new timestamp even after a restart!</font>
* <font color=red size=5>即使在重新启动之后，我们也会分配一个新的时间戳!</font>
* **这里就是和detection不一样了，在detection中，重启不会改变时间戳**

![image-20230117092248949](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117092248949.png)

##### 1.1.2 Additional Bokkeeping

* For each database item X, maintain:
  * Read Time of X: **RT(X)**
  * X读取时间:RT(X)
    * **Timestamp of youngest transaction that read X**
    * **读取X的最年轻事务的时间戳**
  * Write Time of X: **WT(X)**
    * **Timestamp of youngest transaction that wrote X**
    * **写入X的最年轻事务的时间戳**

![image-20230117092858504](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117092858504.png)

##### 1.1.3 Read Requests 阅读要求

* If T1requests to read X: 
  * **<font color=red size=5>Abort & restart T1 if WT(X) > TS(T1)</font>**

![image-20230117093501170](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117093501170.png)

##### 1.1.4 Write Requests

* If T1requests to write X:
  * **<font color=red size=5>Abort & restart T1if RT(X) > TS(T1) or WT(X) > TS(T1)</font>**

![image-20230117093607934](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117093607934.png)



##### 1.1.5 解析

![image-20230117094617983](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117094617983.png)

**画个时间表，在在T1处，X被第一次读取**

![image-20230117094626388](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117094626388.png)

![image-20230117094635156](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117094635156.png)

T2 request Read(Y), 在时间表上写入RT(Y)

![image-20230117094644786](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117094644786.png)

![image-20230117094655963](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117094655963.png)

T2 request Write(Y), 在时间表上写入WT(Y)

![image-20230117094706209](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117094706209.png)

**此时，出现问题，T1申请读取Y，但是因为RT(Y) > TS(T1), 所以必须重启T1**

![image-20230117094719473](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117094719473.png)

![image-20230117094726453](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117094726453.png)

T1重启完毕，T1重新分配一个时间戳 TS(T1)=3

![image-20230117094740472](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117094740472.png)

![image-20230117094748820](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117094748820.png)

此时满足条件，不需要重启或者放弃

![image-20230117094812103](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117094812103.png)



![image-20230117094818293](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117094818293.png)

这里的写入也是一样的，满足条件不需要重启

![image-20230117094824508](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117094824508.png)



<font size=5>Example2</font>

* Assume a timestamp-based scheduler
* 假设有一个基于时间戳的调度程序
  * T1starts first
  * T1 首先开始
  * Lines 1-3 of T1 are executed first, then lines 1-3 of T2
  * 首先执行T1的1-3行，然后执行T2的1-3行

![image-20230117095753535](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117095753535.png)

![image-20230117095800325](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117095800325.png)

![image-20230117095807468](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117095807468.png)

![image-20230117095815142](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117095815142.png)

![image-20230117095821881](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117095821881.png)

* 这个就属于是很典型的互相回溯刷新时间戳，因为两个T的read()和write()的操作顺序相同

#### 1.2 Timestamp-based Scheduling

* **Nice properties:**
* **良好的性质**
  * **Enforces conflict-serialisable schedules**
  * **强制冲突序列化的时间表**
  * **Deadlocks don’t occur**
  * **死锁不会发生**
* **Bad properties:** 
  * **Cascading rollbacks**
  * **级联回滚**
  * **Starvation can occur (cyclic aborts & restarts of transactions)**
  * **可能会出现“饥饿”(事务的循环中止和重新启动)**
* Starvation can be prevented using appropriate techniques (not in this module)
* 可以使用适当的技术来防止饥饿(不在本模块中)

![image-20230117100700491](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117100700491.png)

##### 1.2.1 Ensuring Strictness 	确保严格性

* Schedules enforced by timestamp-based schedulers are not strict.
* 基于时间戳的调度程序执行的调度并不严格。
* Additional condition to enforce a strict schedule:
* 强制执行严格时间表的附加条件:

* **<font color=red>Delay read or write requests until the youngest transaction who wrote X before has committed or aborted.</font>**
* **延迟读或写请求，直到<font color=red>之前写</font>X的最年轻的事务提交或中止。**

![image-20230117100954978](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117100954978.png)

#### 1.3 Multiversion concurrency control 多版本并发控制 MVCC

* Many DBMS are implementing a variant of time-stamp based approaches, called multiversionconcurrency control 
* 许多DBMS正在实现一种基于时间戳的方法，称为多版本并发控制
* The idea is the same as time-stamp based approaches to scheduling, but you have multiple versions of the database!
* 这个想法与基于时间戳的调度方法相同，但是您有多个版本的数据库!
  * **Meaning that write operations do not overwrite each other, but instead wi(X) creates makes a new version of X at time TS(Ti)**
  * **这意味着写操作不会相互覆盖，而是wi(X)在TS(Ti)时创建了一个新版本的X**
  * **<font color=red>Whenever you read, you read the latest version before your timestamp</font>** 
  * **无论何时读取，都是在时间戳之前读取最新版本**
* **This means that a transaction only need to restart if it tries to write AND the read timestamp is later than your timestamp**
* **这意味着只有当事务试图写入并且读取时间戳晚于您的时间戳时，才需要重新启动事务**
* Or, written out in full, the rules are:
* 或者，完整地写出来，规则是:
  * **<font color=red size=5>For writes: Abort & restart T1 if RT(X) > TS(T1) and otherwise, grant request</font>**
  * **<font color=red size=5>对于写操作:如果RT(X) > TS(T1)，则中止并重新启动T1，否则，授予请求</font>**
  * **<font color=red size=5>For reads: Always granted</font>**
  * **<font color=red size=5>对于阅读:总是理所当然的</font>**
* There is also a strict variant, where you delay reads until the transaction you read from commits
* 还有一种严格的变体，即延迟读取，直到从事务中读取的事务提交

一开始，数据库中的版本都是10

![image-20230117103517580](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117103517580.png)

T1开始读，然后read(x)为10的版本

![image-20230117103524961](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117103524961.png)

![image-20230117103657318](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117103657318.png)

T2开始，读取read(Y)=10

![image-20230117103711425](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117103711425.png)

![image-20230117103748488](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117103748488.png)

write(Y),则此时创建一个新版本的Y，Timestamp=2，Y=20

![image-20230117103754666](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117103754666.png)

![image-20230117103801044](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117103801044.png)

**无论何时读取，都是读取自己时间戳之前的最新版本，T1=1，之前没有时间戳，所以读T=1的版本**

![image-20230117103808095](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117103808095.png)

![image-20230117103820460](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117103820460.png)

<font color=red>在此T1写入Write(Y), 对于写操作:如果RT(Y) > TS(T1)，则中止并重新启动T1，否则，授予请求</font>

此时RT(Y)>TS(T1), 所以重新启动T1

![image-20230117103827840](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117103827840.png)

![image-20230117103836733](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117103836733.png)

![image-20230117103845485](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117103845485.png)

一样，读取在时间戳之前的最新版本，X的版本是X=10

![image-20230117103902738](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117103902738.png)

![image-20230117103919191](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117103919191.png)

因为是读该时间戳之前的最新版本，T1=3，所以读取Y=20的版本

![image-20230117103932074](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117103932074.png)



![image-20230117103940252](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117103940252.png)

**<font color=red>在此T1写入Write(Y), 对于写操作:如果RT(Y) > TS(T1)，则中止并重新启动T1，否则，授予请求</font>**

此时RT(Y)=TS(T1)满足条件

![image-20230117103949979](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117103949979.png)

![image-20230117103958643](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117103958643.png)



![image-20230117105807953](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117105807953.png)



### 2. DeadLock

#### 2.1 MySQL (with InnoDB) 

* 还使用基于时间戳的方法来确保读操作不会干扰写操作

![image-20230117105855502](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117105855502.png)

* Uses Wait-For graphs 
* 使用等待图
* Except: If transaction has line of length > 200 it is rolled back 
* 除非:如果事务的行长度为> 200，它将被回滚
* E.g. T1is rolled back in this case: 
* 例:t1在本例中被回滚:
* ![image-20230117110034947](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117110034947.png)

* If cycle: rollback the smallest transaction 
* 如果cycle:回滚最小事务
* Deadlock detection can be switched off, in which case time-out is used (on locks) 
* 可以关闭死锁检测，在这种情况下使用超时(对锁)

#### 2.2 Other DBMS

* PostgreSQL
  * Uses timeout on locks followed by Wait-For graphs 
  * Like MySQL: Uses a timestamp based approach for ensuring that reads do not interfere with writes 
* Oracle DB 
  * Uses timeout directly or timeout followed by Wait-For graphs 
  * Does not use locks on read 
* IBM DB2 
  * Uses lock timeout or global time-out followed by Wait-For graphs 
  * Uses update-locks 

![image-20230117110243926](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117110243926.png)



![image-20230117110314036](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117110314036.png)

本章所涉及的技术并不局限于DBMS

每当系统共享资源时，都会出现类似的问题

一些示例场景:

◦操作系统中的进程访问相同的文件，网络资源等。

◦用户在线编辑同一文档

◦文档版本控制系统，如subversion, git等。



## Lecture16&17&18  Intro to query processing & Faster joins and selections

### 1. Review of Transaction Management 事件管理系统的复习

* Dealing with transactionsis a core task of DBMS 处理事务是数据库管理系统的核心任务
  * Many things can go wrong when processing transactions,
    even when executing single SQL statements.
  * 在处理事务时，许多事情都可能出错，甚至在执行单个SQL语句时也是如此。
  * Need to ensure ACID properties
  * 需要确保ACID性能
* Requires careful schedulingof transactions and logging of relevant information 需要仔细安排时间表的事务和记录相关信息
  * Schedules should be conflict-serialisable 计划应该是冲突序列化的
  * Schedules should be strict 时间表应该严格
* Methods for enforcing conflict-serialisability & strictness: 执行冲突序列化和严格性的方法:
  * Strict two-phase locking & deadlock prevention methods 
  * 严格的两阶段锁定和死锁预防方法
  * Timestamping
  * 时间戳 

#### 1.1 ACID Review

* Atomicity原子性：
  * Transactions are fully executed or not at all 事务要么完全执行，要么根本不执行
  * Ensured by Undo logging, Undo/Redo logging or Force **由Undo日志，Undo/Redo日志或Force保证**
* Consistency一致性：
  * Schedule executes transactions equivalent to a serial schedule调度执行与串行调度等价的事务
  * (needs two assumptions for this: non-database operations can be ignored and if a schedule is serial, then it is consistent) (需要两个假设:非数据库操作可以忽略，如果调度是串行的，那么它是一致的)
  * Ensured by Serializability, Conflict-Serializability, 2PL and Timestamp-based Scheduling (also Strict versions of the last two)**由可串行性、冲突可串行性、2PL和基于时间戳的调度保证(也是后两个的严格版本)**
* Isolation 独立性：
  * A serializable schedule satisfies Isolation and vice versa 可序列化的调度满足隔离，反之亦然
  * Has some levels, but none actually precisely corresponds to the definition (because the last level requires the earlier ones) – Isolation would be satisfied by conflict-serializable schedules, while Isolation level 4 would also require a bit more than Cascadeless. 有一些级别，但没有一个级别实际上精确地对应于定义(因为最后一个级别需要较早的级别)——隔离将由冲突序列化的时间表满足，而隔离级别4也需要比无级联的更多一点
  * <font color='red'>**记得各种隔离的等级吗，还有它的判别方法**</font>
  * ![image-20221120233217308](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221120233217308.png)

* Durability 耐久性：
  * If a transaction is committed, it does not disappear 如果事务被提交，它不会消失
  * **<font color=red>Ensured by Redo logging, Undo/Redo logging or No Steal</font>**
  * Recoverable schedules are also required 还需要可恢复时间表

#### 1.2 Types of Schedules in short

![image-20221120233421390](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221120233421390.png)

* **<font color=red size=5>非常重要</font>**
* **Serial: One transaction done fully, then another, then another and so on 串行:一个事务完全完成，然后是另一个，然后是另一个，以此类推**
* **Serializable schedules (aka. good schedules): Equivalent to a serial schedule  可序列化的时间表(又名。好的时间表):相当于串行时间表**
* **Conflict-serializable: a special kind of serializable schedules that can be checked fast using precedence graphs 可冲突序列化:一种特殊的可串行调度，可以使用优先级图快速检查**
* **Recoverable: If reading uncommitted data, must commit after what you read committed 可恢复的:如果读取未提交的数据，必须在读取提交后提交**
* **Cascadeless: Can only read committed data 无级联:只能读取提交的数据**
* **Strict: ... and can only overwrite committed data 严格:…并且只能覆盖提交的数据**
* **Strict 2PL: use locks (must have a - think physical – lock before using a variable and must unlock after), all locks before every unlock (upto here: 2PL), unlocks of locks that can be used to write: first after commit  严格的2PL:使用锁(在使用变量之前必须有一个物理锁，并且在使用变量之后必须解锁)，每次解锁之前都要锁上所有锁(到这里:2PL)，解锁可用于在提交后先写的锁**



#### 1.3 Logs

* Undo/redo logs: must keep track of starts, commits, aborts, writes (incl. what variable and what it was before and after) 撤销/重做日志:必须跟踪启动、提交、中止和写入(包括变量和之前和之后的变量)
  * Undo and redo are similar but only keeping track of before and after respectively 撤消和重做是类似的，但只分别记录前后
* Recovery: Undo: Start from the end and move up while undoing uncommitted writes 恢复:撤消:从末尾开始，在撤消未提交的写操作时向上移动
* Undo/Redo: Start from top and move down, redo committed writes 重做:从上向下移动，重做提交的写入
* Checkpoints: Simple (stop all new transactions and wait until finish) and ARISE (store the current buffer – information to restore from there)检查点:Simple(停止所有新的事务并等待直到完成)和ARISE(存储当前缓冲区-从那里恢复的信息)

#### 1.4 Deadlocks

* Deadlocks can be avoided using:
  * Timeout 超时设定
  * wait-for graphs (keep track of who waits for whom – cycle=deadlock) 等待图(跟踪谁在等待谁- cycle=死锁)
  * timestamp-based approaches (young always dies, but two schemes: Wait/die, they die for asking an old one for a lock, Wound/wait: They die for being asked by an old one for a lock –
    restarts with the same timestamp!) 基于时间戳的方法(年轻的总是死，但有两种方案:等待/死，它们死于向老的请求锁，伤口/等待:它们死于被老的请求锁，重新启动具有相同的时间戳!)

#### 1.5 Timestamp based approaches to scheduling
Lecture15

* Each transaction has a timestamp and we intuitively restarts one whenever they would cause a paradox with having executed in time-stamp order
* 每个事务都有一个时间戳，当它们按照时间戳顺序执行时，我们直观地重新启动一个事务
  * Paradoxes: reading from the future or writing to a variable that has already been read/overwritten in 
    the future (also multi-version variant that only has the writing a variable that has been read in the 
    future - but must keep track of multiple versions of each variable – one for each timestamp written at)
  * 悖论:从未来读取或写入未来已经读取/覆盖的变量(也是多版本变体，只写入未来已读取的变量-但必须跟踪每个变量的多个版本-每个写入的时间戳对应一个版本)

### 2. Work Progress of Sql Queries

* DBMS selects a good sequence of database operations to execute the query.  DBMS选择一个好的数据库操作序列来执行查询

![image-20221104152117015](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221104152117015.png)

![image-20221104152210591](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221104152210591.png)

#### 2.2 Relational Algebra

Set of operations that can be applied to **relations** to **compute new relations** 可以应用于关系来计算新关系的操作集

Basic relational algebra:

* **Selection (𝜎)**
* **Projection (𝜋)**
* **Cartesian product (X)**
* **Union (∪)**
* **Renaming (𝜌)**
* **Natural join (⋈)**
* **Semijoin (⋉) 半连接**
* **Many others can be defined**

![image-20221121122331840](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121122331840.png)



#### 2.1 Query Plans

A relational algebra expressionthat is obtained from an SQL query is also called a (logical) query plan   <font color='red'>从SQL查询中获得的关系代数Relation Algebra表达式也称为(逻辑)查询计划Query Plans</font>

![image-20221104152934000](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221104152934000.png)

Query Plans通常表示为树

##### 2.1.1 Query Plans As Trees

![image-20221104153053361](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221104153053361.png)

* Leaves = input relations
* Inner nodes = operators

Another Example:

![image-20221121122651665](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121122651665.png)

##### 2.2.1  Executing Query Plans

* There are typically many different query plans 为每个节点计算一个中间结果

* DBMSs aim to select a best possible query plan 对于标记了关系R的叶，中间结果为R。

* Relational algebra is better suited than SQL for this

  * **Can use equivalence laws of relational algebra to generate a query plan for the same query that can be executed faster!**

    **可以使用关系代数的等价定律为相同的查询生成一个查询计划，可以更快地执行!**

  ![image-20230117113104764](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117113104764.png)

Query plans tells us exactly how to compute the result to a query 查询计划确切地告诉我们如何计算查询的结果

* **Proceed from bottom to top: 过程从底向上**

  * Compute an intermediate result for each node 为每个节点计算一个中间结果
  * For a leaf labeled with relation R, the intermediate result is R. 对于标记了关系R的叶，中间结果为R
  * For an inner node labeled with operator op, get the intermediate result by applying op to the childrens’ intermediate results. 对于一个带有操作符的内部节点,通过向儿童的中间结果应用op得到中间结果。

  ![image-20221121124658474](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121124658474.png)

* <font color='red'>Result of the query = intermediate result of the root 查询结果=根的中间结果</font>

![image-20221121124933712](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121124933712.png)

![image-20221121124918326](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121124918326.png)

#### 2.3 Naïve Computation of Joins

![image-20230117113333389](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117113333389.png)

![image-20221104165850061](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221104165850061.png)

一个正常的自然连接。没什么太好说的。一行一行比对就行

结果：

![image-20221121125254784](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121125254784.png)

* 慢:对于rin中的每个元组重新读取整个关系S
* **<font color=red size=5>Running Time:𝑂(|R| ×|S|)</font>**

![image-20230117113449845](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117113449845.png)



#### 2.4 Equijoins 等值连接

* 如果R在A上排序并且S在B上排序，那么（R⋈A=B S）的运行时间可以通过R和S的大小+输出值的大小计算
* ![image-20221121125708048](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121125708048.png)

![image-20221104170332933](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221104170332933.png)

**简单来说，节约成本，减少运算量**

![image-20221121125641968](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121125641968.png)

#### 2.5 Merging 混合

![image-20221104165602998](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221104165602998.png)

![image-20230117120611579](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117120611579.png)

![image-20230117120705222](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117120705222.png)

![image-20230117120711503](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117120711503.png)

![image-20230117120717712](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117120717712.png)

![image-20230117120727940](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117120727940.png)

![image-20230117120735123](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117120735123.png)

![image-20230117120740874](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117120740874.png)

![image-20230117120746401](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117120746401.png)

![image-20230117120756094](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117120756094.png)

![image-20230117120802883](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117120802883.png)

![image-20230117120809895](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117120809895.png)

![image-20230117120818452](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117120818452.png)

![image-20230117120825222](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117120825222.png)

![image-20230117120842477](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117120842477.png)

**下面是在A列中有重复的情况**

![image-20221104170819496](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221104170819496.png)

这里的图在PPT16Lecture

### 3. Faster Joins With Sorting 通过排序更快的连接

![image-20221104171928012](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221104171928012.png)

* 运行时取决于输出的大小称为输出敏感output sensitive

![image-20221104172059318](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221104172059318.png)

* Various join algorithms in practice: 实际上往往会使用多种join算法
  * Index joins
  * Hash joins 
  * Multiway joins: join more than two relations at once



### 3. Disk

![image-20221104172534565](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221104172534565.png)

* B = size of a disk block (typically 512→4096 bytes) B =磁盘块大小(一般为512→4096字节)
* M = number of disk blocks that fit into available RAM M =可装入可用RAM的磁盘块的数量

### 4.Index 

Given the values for one or more attributes of a relation R, provides quick access to the tuples with these values 给定关系R的一个或多个属性提供值，提供对具有这些值的元组进行快速访问。

* 简单来说就是利用index进行寻值

![image-20221104173709978](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221104173709978.png)

Type：

1. Secondary：仅指向磁盘上记录的位置
2. Primary：定义如何在磁盘上对数据进行排序

![image-20221104180146810](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221104180146810.png)

**情况1：**

![image-20221104180212218](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221104180212218.png)

* 寻找带有G401的列
* 访问所以G401的列

**情况2**：

![image-20221104180238155](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221104180238155.png)

**情况3：**

![image-20221104180248960](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221104180248960.png)

#### 4.1 Forms Of Indexes 索引的形式

* B+Trees
  * **如果选择条件指定了范围，很好用**
  * E.g., 𝜎programme=‘G401’ AND year
  * 非常广泛的应用
  * ![image-20221104180520425](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221104180520425.png)

* Hash Tables
  * **如果选择只涉及平等，那很好用**
  * E.g., 𝜎programme=‘G401’
  * ![image-20221104180622990](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221104180622990.png)

#### 4.2 多级索引和初级索引

* Single level index：Stored in single List
* Multi-level index: distributed across different layers

![image-20221104180816031](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221104180816031.png)

#### 4.3 B+Tree

![image-20221121153808094](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121153808094.png)

叶子

![image-20221121135528829](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121135528829.png)

![image-20221121135857210](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121135857210.png)

内节点

![image-20221104213324413](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221104213324413.png)

![image-20221121135911556](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121135911556.png)

<font color='red' size=5>这里的数字都是质数</font>

![image-20221104213348599](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221104213348599.png)



##### 4.3.1 Looking Up Values

Example1

找一个具体值

![image-20221104213514744](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221104213514744.png)

Example2

找一个范围值

![image-20221104213545265](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221104213545265.png)

Example3

找B+树内不存在的值

![image-20221104213728450](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221104213728450.png)

<font color='red' size=4.5>Summary：</font>

Goal: find the pointer to the rows with value v 目标:用值v找到指向行的指针

Procedure:

* 从B+树的根开始
* 如果当前节点不是叶子节点
  * v<a1,  继续到节点的第一个子节点
  * 否则，找到ai≤v的最大i并继续到相关的子节点
* 如果当前节点是叶节点:
  * 如果v出现在叶中，则遵循相关的指针
  * 如果v没有出现在叶中，返回" v不存在于索引中"

![image-20221104214512029](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221104214512029.png)

##### 4.3.2 Insertions 插入

**Task: insert value 48**

![image-20221121140249801](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121140249801.png)

**Task: insert value 42**

![image-20221121140322352](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121140322352.png)

* 需要给42创造空间

![image-20221121140520096](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121140520096.png)

![image-20221121140620227](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121140620227.png)

* 拆分节点

![image-20221121140644062](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121140644062.png)

* 创造新的节点

![image-20221121142044079](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121142044079.png)

* 因为要存放42，所以创造新的节点，因为是b+树，所以如图所示

![image-20221121142157556](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121142157556.png)

* <font color='red'>此时不是B+树</font>

![image-20221121142237689](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121142237689.png)

* 如图，23-31-43的节点不能添加新的子节点，所以如下图

![image-20221121142339837](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121142339837.png)

![image-20221121142358664](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121142358664.png)

* 把43和42连接

![image-20221121142422795](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121142422795.png)

* 在把头节点与43连接

######  4.3.2.1 Insertion: Summary

Goal: insert a new value/pointer pair

Procedure:

* Find the leaf that should contain the value 找到应该包含该值的叶

* If the leaf is not full, insert the key value pair at a suitable location 如果叶未满，则将键值对插入到合适的位置

* If the leaf is full: 如果叶子是满的:

  * Split the leaf to make space for the new value/pointer pair and move half of the pointers to the new node 拆分叶节点，为新的值/指针对腾出空间，并将一半指针移动到新节点
  * Insert the value/pointer pair  插入值/指针对
  * Connect the leaf to a suitable parent node (which might incur the creation of a new node etc.)  将叶节点连接到合适的父节点(这可能导致创建新节点等)。

  ![image-20221121142908330](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121142908330.png)

##### 4.3.3 Deletions 删除

https://blog.csdn.net/zsx0728/article/details/114366379?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522166904504016782388035836%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=166904504016782388035836&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~baidu_landing_v2~default-1-114366379-null-null.142

-- 解释不同情况的删除

删除42

![image-20221121152313871](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121152313871.png)

![image-20221121152340544](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121152340544.png)

* 找到42

![image-20221121152458915](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121152458915.png)

* 删除42，然后检测是否满足B+树，满足，没有问题

* **<font color='red'>There may be more than one B+ tree with the same leaves</font>**

**删除48**

![image-20221121152830165](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121152830165.png)

![image-20221121152843705](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121152843705.png)

**删除41**

![image-20221121153234875](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121153234875.png)

* 找到41

![image-20221121153253977](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121153253977.png)

* 删除41

![image-20221121153310535](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121153310535.png)

* 对B+树进行调整

![image-20221121154033198](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121154033198.png)

* 最终结果，这里使用删除47的初始图进行替代



**删除47**

![image-20221121154833100](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121154833100.png)

![image-20221121154841020](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121154841020.png)

![image-20221121154848429](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121154848429.png)

![image-20221121154855565](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121154855565.png)

![image-20221121154911033](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121154911033.png)

![image-20221121154924990](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121154924990.png)

![image-20221121154936011](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121154936011.png)

![image-20221121154948708](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121154948708.png)

![image-20221121154955512](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121154955512.png)

![image-20221121155004470](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121155004470.png)

![image-20221121155025394](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121155025394.png)

#### 4.3.4 Properties of B+ Tree Indexes

![image-20221121155106436](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121155106436.png)

![image-20221121155114757](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121155114757.png)



## Lecture 19  Query optimization 查询优化

### 1.Query optimization 查询优化

因为初始的查询计划可能不是最优的，所以我们需要对查询进行优化

![image-20221121161831768](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121161831768.png)

**Evaluation of query plans:** 

* Bottom-up  自底向上
* **Efficiency depends on size ofintermediate results 效率取决于中间结果的大小**

Rewrite the initial query plan so that intermediate results will be smaller 重写初始查询计划，使中间结果更小

* Based on equivalence laws of relational algebra 基于关系代数的等价定律
  * Many laws (see references for this lecture on Canvas)
  * **比较重点**
  * ![image-20221121170229960](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121170229960.png)

#### 1.1 Heuristics 启发法

* **尽可能在早期执行where等选择语句，这样可以去除许多不相干的模组**
* Intuition: This gets rid of many irrelevant tuplesvery early during execution.
* 这可以在执行的早期去除许多不相关的元组。

1. 将选择尽可能往下推

![image-20221121170435475](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121170435475.png)

2. 尽可能往下“推”**投影**，或者在适当的地方插入投影
2. * 其实可以看出，这一步的目的也是去除无关的组

![image-20221121170557065](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121170557065.png)

3. 如果可能的话，为×引入**等价连接**，后面跟着𝜎

![image-20221121170833231](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121170833231.png)



### 2. Physical query plans 物理查询计划



![image-20221121171101142](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121171101142.png)



#### 2.1 The purpose of a physical query plan

**A physical query plan adds information required to execute the optimised query plan 物理查询计划添加执行优化查询计划所需的信息**

* Which algorithm to use for execution of operators?
* 使用哪种算法执行运算符?
  * Naïve selection or selection with an index?
  * Naïve选择或选择与索引?
  * Nested Block Join or Sort Join or Hash Join etc.?
  * 嵌套块连接或排序连接或散列连接等?
* How to **pass information** from one operator to the other? 如何将信息从一个操作符传递到另一个操作符?
  * Write to disk, keep in memory, pipelining operators, etc.?写入磁盘,保存在内存,流水线操作符等
* Good order for computing joins, unions, etc.? 计算连接、联合等的良好顺序?
* Additional operations such as sorting  其他操作，如排序



#### 2.2 From Logical Plan to Physical Plans 从逻辑计划到物理计划

一般来说一个逻辑计划可以拥有很多物理计划。需要对物理计划进行评估

* Estimate cost of execution for each plan  执行每个计划的花费

  * ![image-20221121172029967](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121172029967.png)
  * Select physical plan with lowest cost estimate 选择最低消耗的物理计划

  ![image-20221121172111063](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121172111063.png)

##### 2.2.1 Estimating the Cost of Execution 评估执行花费

**1.number of disk access operations 访问磁盘的次数**

* Number of disk accesses influenced by many factors: 受多种因素影响的磁盘访问次数:

  * Selection of algorithms for the individual operators 为单个运算符选择算法
  * Method for passing information 传递信息的方法
  * **Size of intermediate results 中间结果的大小**

  

  

  

**2.Estimated from parameters of the database ** 从数据库参数估计

* Important paramters: 重要的参数
  * **Size of relations 关系参数的大小**
  * **Number of distinct items per attribute per relation 每个关系的每个属性的不同项数**
* Computed exactly from the database or use estimates 从数据库精确计算或使用估计(“统计信息收集”)



###### 2.2.1.1 Estimating Intermediate Result Sizes 评估中间结果的大小

**One of the most challenging tasks of a DBMS**

* Difficult even for nodes close to the leaves  即使是靠近叶子的节点也很难
* Cannot afford executing the query 无法承担查询
* Rely on statistics gathered from data 依靠从数据中收集的统计数据



###### 2.2.1.2 Estimating the Size of a Selection 评估一个选择的大小

![image-20221121173417394](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121173417394.png)

![image-20221121173428472](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121173428472.png)

![image-20221121181743734](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121181743734.png)

Example：

![image-20221121181847570](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121181847570.png)



###### 2.2.1.3 Estimating the size of a joins

![image-20221121182016710](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121182016710.png)

###### 2.2.1.4 Other Issues

How to generate physical query plans?

如何生成物理查询计划?

* Explore all?
* More sensible approaches: top-down/bottom-up

![image-20221121182158104](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121182158104.png)

###### 2.2.1.5 Passing Information 信息传递

Materialisation: write intermediate results to disk. 实体化：将中间结果写入磁盘

Pipelining (“stream-based processing”) 流水线(“基于流的处理”)

* Passes the tuples of one operation directly to the next operation without using disk 将一个操作的元组直接传递给下一个操作，而不使用磁盘
* Extra buffer for each pair of adjacent operations to hold tuples passing from one relation to the other 为每一对相邻操作提供额外的缓冲区，用于保存从一个关系传递到另一个关系的元组
* ![image-20221121182459396](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121182459396.png)

* 通过流水，选择的中间结果将被写入内存中的缓冲区，从那里投影操作符将直接读取和处理这些元组

![image-20221121182521069](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221121182521069.png)





## Lecture20 & Lecture21  Query processing and distributed databases 查询式处理和分布式数据库

 查询处理 Query Processing已经在上节课讲完了。直接开始分布式数据库



### 1. Distributed databases 分布式数据库

* Each site stores only data primarily relevant to it
  Distributed DBMS provide access to data at all sites. **每个站点只存储与它主要相关的数据，分布式DBMS提供对所有站点数据的访问**



![image-20221122132820273](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221122132820273.png)

![image-20221122132905900](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221122132905900.png)

#### 1.1 Other Applications 其他应用

* More general: large organisations/companies 更普遍的是:大型组织/公司

  * ..with different branches or offices 有不同的分支机构或办公室
  *  ...with different sub-companies 不同的子公司
  * ...or simply so large that one computer can’t handle all the request 或者只是因为太大，一台计算机无法处理所有的请求

  

* Providing access to large datasets to many users (e.g., for an online store) 为许多用户提供大型数据集。,用于网上商店)

  * Distribute data over several computers – not necessarily identical (in software or hardware)在多台计算机上分布数据—不一定是相同的(在软件或硬件上)
  * Computers could be at geographically separate locations (but also possible that they are the same place)  计算机可能位于地理上不同的位置(但也可能是同一个位置)
  * Possible advantages:(可能的优点)
    * Balance workload & network traffic  平衡工作负载和网络流量
    * Easier to extend capacity or scale to higher number of users. 更容易扩展容量或规模到更多的用户。

![image-20221122134126541](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221122134126541.png)

#### 1.2 Distributed DataBases

**Distributed Database:**

* **Collection of multiple logically interrelated databases 多个逻辑相关数据库的集合**
* Distributed over a computer network 通过计算机网络分布的

![image-20221122134413664](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221122134413664.png)

##### 1.2.1 The Advantage of Distributed Database

* **Performance improvements 性能改进**
  * Answer queries faster by distributing tasks over the nodes 通过在节点上分配任务，可以更快地回答查询
  * Reduces CPU time, disk accesses, communication cost, ... at individual nodes 减少CPU时间、磁盘访问、通信成本……单个节点
* **Scalability 可扩展性**
  * Easier extension of the system: capacity, performance, ... 更容易扩展的系统:容量，性能，…
  * Essentially just add a new node 本质上就是添加一个新节点
* **Resilience 弹性**
  * Data can be replicated at geographically separate sites 数据可以在地理位置不同的站点上复制
  * Catastrophic failures don’t affect the entire system 灾难性的故障不会影响整个系统

### 2. Fragmentation, replication and transparency  碎片化，复制和透明化

#### 2.1 Fragmentation 碎片化

* **Split database into different parts that can then be stored at different nodes 将数据库分成不同的部分,然后可以存储在不同的节点**
* <font color='red'>We use UNION to combine horizontal fragments and NATURAL JOIN for vertical fragments. Not the other way around. 我们使用union来连接水平分割，使用natural Join来连接竖直分割</font>

![image-20221130153301006](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221130153301006.png)

类型：

* Horizontal fragmentation 水平分割 
* union来连接水平分割
* ![image-20221122141704180](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221122141704180.png)
* Vertical fragmentation 竖直分割
* 用natural Join来连接竖直分割
* ![image-20221122141741506](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221122141741506.png)

* Users don’t see fragments, just the full relations 用户不会看到碎片，只有完全的关系

##### 2.1.1 Horizontal Fragmentation Example 水平碎片示例

* The chain of stores from our running example might jointlystore the Transaction relation  
* 我们正在运行的示例中的商店链可能联合存储Transaction关系

![image-20221122142112195](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221122142112195.png)

* Each site stores a relation that contains a subset of the tuples 每个站点存储一个包含元组子集的关系
* Entire relation = union of relations at the different sites 整个关系=在不同地点的关系的联合

![image-20221122142753397](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221122142753397.png)

* Typically, tuples stored at different sites can be distinguished 
* 通常，存储在不同位置的元组是可以区分的
  * by the value of one or a few attributes; or
  * 通过一个或几个属性的值;或
  * by other conditions that are easy to test
  * 通过其他容易测试的条件

##### 2.1.2 Vertical Fragmentation Example 垂直碎片示例

![image-20221122142912260](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221122142912260.png)

**按照列来区分，需要使用时将不同的碎片进行组合**

#### 2.1.3 Redundancy Improves Resilience 冗余提升弹性

![image-20221122143153360](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221122143153360.png)

* Other sites keep copies of fragment stored at Manchester allows us to answer queries involving data from Manchester 
* **其他网站保留存储在曼彻斯特的碎片副本允许我们回答来自曼彻斯特的数据查询。（即使某一个数据库损坏了，依然不影响查询该数据库）**

![image-20221122143506600](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221122143506600.png)

* **Other sites keep copies of data about suppliers**
  **Allows stores to answer queries involving suppliers without establishing a connection to the central office.**  
* **其他网站保留关于供应商的数据副本允许商店回答涉及供应商的查询,而不与中央办公室建立联系**



### 3. Replication 复制

**<font color=red>Controls how many sites keep a copy of a fragment. 控制多少个节点保留fragment的副本。</font>**

**Full replication** 满复制

* Each fragment stored at every site (àthere are no fragments) 每一个fragment存储在每一个节点上（每一个节点都有全套的fragment）
* Faster query answering 快速的查询响应
*  Very slow updates : consider everycopy 较慢的更新速度，需要考虑到每一个副本

**No replication** 不复制

*  Each fragment stored ata unique site 每一个fragment只存储在唯一的节点上。
* Crashes are a big problem... 崩溃是一个大问题

**Wide spectrum of partial replication** 局部复制更加广泛

* Limit number of copies of each fragment  限制每个片段的副本数量
* Replicate only some fragments, ... 仅复制部分fragment



### 4. Transparency 透明化

**<font color=red>DBMSs ensures that users do not need to know certain facts then creating queries dbms确保用户在创建查询时不需要知道某些事实</font>**



Transparency at different levels 透明化的不同等级

* **Fragmentation transparency 分段透明化**
  * Fragmentation is transparent to users 碎片对用户是透明的
  * Users pose queries against the entire database 用户对整个数据库进行查询
  * The distributed DBMS translates this into a query plan that fetches the required information from appropriate nodes. 分布式DBMS将此转换为查询计划，从适当的节点获取所需的信息
* **Replication transparency  复制透明性**
  *  Ability to store copies of data items / fragments at different sites  能够在不同的站点存储数据项/片段的副本
  * Replication is transparent to users 复制对用户是透明的
  * **<font color=red>该透明性会隐藏备份（Backup）</font>**
  * ![image-20221130153025876](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221130153025876.png)
* **Location transparency 位置透明性**
  * The location where data is store is transparent to the user 数据存储的位置对用户是透明的
* **Naming transparency  命名透明**
  * A given name (e.g. of a relation) has the same meaning everywhere in the system 一个给定的名字(例如关系)在系统中的任何地方都具有相同的含义



### 5. Transaction management in DDBMS

#### 5.1 Concurrency control in DBMS  DBMS系统中的并发控制

For full isolation/consistency, often based on locks: 对于完全隔离或者一致性，这往往是**基于锁**

![image-20221122171107548](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221122171107548.png)

#### 5.2 Concurrency control based on voting  基于投票的并发控制

Another approach to locks (instead of having a single designated computer granting them): 其他的方法来赋予锁(而不是一台指定的计算机赋予锁)

* <font size=6>Voting</font>

Idea:

* Each site with a copy of an item has a local lock that it can grant transactions for that item 每个拥有项目副本的站点都有一个本地锁，它可以授予该项目的事务
* If a transaction gets over half the local locks for an item, it has a global lock on the item 如果事务获得了一个项的一半以上的本地锁，那么它就拥有该项的全局锁
  * If so, it must tell the sites with a copy that it has the lock 如果可以，他必须告诉所有有副本的节点它持有锁
  * If it takes too long, it must stop trying to get the lock 如果它执行了太长时间，它必须停止尝试获得锁
* Plus: Much more distributed than the non-voting approach 另外:比不投票的方式更加分散
* Minus: Requires more communication  缺点:需要更多的沟通



### 6. Recovery in DBMS

#### 6.1 Transactions in Distributed Databases 分布式数据库的事物

**At central office: 在中央办公室**

* Determine inventory for product X at each site 
* 确定产品X在每个站点的库存
* Move product X between stores to balance inventory 
* 在商店之间移动产品X以平衡库存

![image-20221122174057256](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221122174057256.png)

**Global transaction T 全局事务T**

* Starts local transaction T0at central office 
* 在中央办公室启动本地事务t0
* T0 instructs other sites to start local transactions 
* T1, T2, T3     T0指示其他站点启动本地事务T1、T2、T3
* T1, T2, T3find out inventory for product X at sites & send it back to T0 
* T1, T2, T3找出X产品在各站点的库存，并将其送回T0
* T0 determines how to move product X between sites 
* t0决定如何在站点之间移动产品X
* T0 instructs T1, T2, T3to move product X accordingly   
* t0指示T1、T2、t3相应移动乘积X

#### 6.2 Violation of Atomicity 原子性破坏

![image-20221122175845335](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221122175845335.png)

**Atomicity:**

* Can assume to be enforced at each node locally 
* 是否可以假设在每个节点强制运行
* Could be violated globally  
* 是否可以在全局范围内被违反

#### 6.3 Problems With Failing Nodes 故障节点的问题

![image-20221122193802479](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221122193802479.png)

* Nodes can fail during execution of T 在执行Node的节点时会失败
  * Should we abort or wait? 
  * 我们应该放弃还是等待?
  * What about the failing node after recovery?
  * 恢复后出现故障的节点怎么办?

### 7. Distributed Commit 分布式提交

#### 7.1 Two-Phase Commit Protocol  2PC 二阶段提交协议

<font color='red'>Not related to 2PL! 和2PL没有关系</font>

![image-20221122194023300](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221122194023300.png)

Coordinator: executed at some node & decides if and when local transactions can commit  协调器:在某些节点上执行，并决定本地事务是否以及何时可以提交

* Logging: at each node locally 
* 日志记录:在本地每个节点上
  * Messages sent to & received from other nodes are logged, too! 
  * 向其他节点发送和从其他节点接收的消息也会被记录下来!

#### 7.2 The Two Phases

##### 7.2.1 Decide when to commit or abort  决定什么时候提交或者放弃

###### 7.2.1.1 Phase 1: When To Commit?

Coordinator: ask nodes if they want to commit 

协调器:询问节点是否需要提交

![image-20221122194809753](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221122194809753.png)

###### 7.2.1.2 Phase 1: Ready to Commit?

![image-20221122194941333](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221122194941333.png)

At each node: decide whether to commit or abort  在每个节点上:决定是否提交或中止

* If commit ->  go into precommitted state & send back “ready T”  如果提交 -> 进入预演期并且返回ready T
* If abort -> send back “don’t commit T” and abort local transaction  如果放弃，返回“don’t commit T”并且放弃本地事件
* Can delay, but must decide eventually 可以拖延,但必须最终决定

##### 7.2.2 Commit or abort 终止或者放弃

###### 7.2.2.1 Phase 2: Let’s Do It

Coordinator: waits for responses of nodes  协调器:等待节点的响应

* Assume nodes who don’t reply before a given timeout wish to abort 在给定的时间没有超出之前，假设没有回复的节点

![image-20221122195541270](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221122195541270.png)

* If all nodes respond “ready T”  如果所有节点都响应" ready T "
  * Send ”commit T” to all nodes -> nodes commit   发送commit给所有节点，节点提交
  * ![image-20230117145802339](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117145802339.png)
* If some node responds “don’t commit T”  如果有的节点返回“don’t commit T” 
  * Send  “abort T” to all nodes -> nodes abort 发送放弃T给所有节点
  * ![image-20230117145817102](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117145817102.png)



#### 7.2.3 Logging: Phase 1 加载语句1

Again, we have to be careful in which order to write to disk and to the log.  再一次将内容仔细的写入磁盘

![image-20221122201148236](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221122201148236.png)

#### 7.2.4 Logging: Phase 2 加载语句2

![image-20221122201517311](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221122201517311.png)



#### 7.2.5 Three-Phase Commit Protocol 三段提交

* Improvement of Two-Phase Commit 改进两阶段提交 

* Can deal with the situation that in phase 2, the coordinator and some transaction crash, while everybody else are in precommited state  能否处理在阶段2中，协调器和一些事务崩溃，而其他所有事务都处于预提交状态的情况

![image-20221122202057729](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221122202057729.png)

* Idea: divide phase 2 into two parts 
* 将phase2分成两个部分
  * Phase 2(a): “Prepare to Commit”
    * Send the decision (commit/abort) to all nodes
    * 将决策(提交/中止)发送到所有节点
    * Nodes go into prepare-to-commit state
    * 节点进入准备提交状态
  * Phase 2(b): “Commit”
    * The old Phase 2

* **Advantage: if the coordinator fails, all nodes know if they should commit/abort a transaction**
* **优点:如果协调器失败,所有节点都知道是否应该提交/中止事务**

## Lecture22&23   Query processing for DDBMS 分布式数据库的查询处理 &XML&XPath

### 1. Query Processing in Distributed DBMS

![image-20221129131810878](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221129131810878.png)

* Try to answer query at site where query is raised  
* 试着在有疑问的地方回答疑问（**在query发起处的数据库对query进行解答**）

* If not possible: request information from other sites  如果不可能:从其他站点请求信息

* Slow —>  design database to reduce this as much as possible   设计数据库时尽可能减少这一点
* Most expensive: joins  Joins方法

#### 1.1 Joins

![image-20221129132245973](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221129132245973.png)

* Goal: Compute Join at site B 计算在B点的添加

* 显然的方法：Obvious approach：

  * Site B asks site A to send R     B要求A发送R

  * Site B computes R ⋈ S   在B点计算R ⋈ S


* **Better: only send data that is actually required**
* **优化：只发送实际需要的数据**

#### 1.2 Semijoins (⋉)

其实就是**自然连接**

![image-20221129132644583](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221129132644583.png)



##### 1.2.1 Semijoin Reduction 自然连接减负

* **Goal: compute join at site B  计算在B处的Join**

![image-20221129132959443](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221129132959443.png)

* **B先将需要进行处理的数据发送给A，然后A再结合自己的数据进行运算算出结果再发送回B，B再进行处理后输出**



##### 1.2.2 Efficiency 

Semijoin Reduction是否更有效率相比于Semijoin？

Depends:

![image-20221129134552711](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221129134552711.png)



Example:

![image-20221129134713571](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221129134713571.png)



### 2. Introduction to Semi-Structured Data 半结构化数据介绍

#### 2.1 Fully Structured Data 完全结构化数据

**Data in the relation model is structured 关系模型中的数据是结构化的**

*  Data has to fit to schema 数据必须符合模式
* Advantage: highly efficient query processing  优点:查询处理效率高

![image-20221130163808863](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221130163808863.png)

### 2.2 Unstructured Data

Dropping the schema yields unstructured data 删除模式将生成非结构化数据

* **Completely free on how to organise data  完全免费地组织数据**
* **No description of structure or data: programs have to know how to read & interpret the data**   
* **不需要对结构或数据进行描述:程序必须知道如何读取和解释数据**

![image-20221130165238317](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221130165238317.png)



#### 2.3 Semistructured Data  半结构化数据模型

**Combines good aspects of both worlds  结合两个的好方面**

![image-20221130165619468](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221130165619468.png)

* **Self-describing: no schema required**
* **自描述:不需要模式**
* **Flexible: e.g., can add & remove attributes on demand**
* **灵活:例如，可以根据需要添加和删除属性**

#### 2.4 Semistructured Data Model   半结构化数据模型

Semistructured databases may be thought of as collections of nodes linked by edges   

半结构化数据库可以被认为是由边连接的节点的集合

Typically a tree or “tree-like”

**Leaf Nodes** have associated data  叶节点具有关联的数据

* Strings, integers, etc.

**Inner nodes** have edgesgoing to other nodes 内部节点有连接到其他节点的边

* Each edge has a label  每条边都有一个标签

**Root:**

* No incoming edges 没有来边
*  Each node reachable from the root 每个节点从根中可到达

![image-20221130170326908](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221130170326908.png)

![image-20221130170337474](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221130170337474.png)

#### 2.5 Applications 应用程序

Popular form for **storing & sharing data on the web  在网上存储和共享数据的流行形式**

* ◦ Text-based (typically)  
* 基于文本(通常)
* ◦ Self-describing (no what is the meaning of this? Etc.)  
* 自我描述
* ◦ Easy to process and manipulate, even for humans  
* 容易处理和操作，甚至对人类
* ◦ Very flexible 
* 极灵活

**Storage of documents** (word processor documents, spreadsheets, vector graphics, etc.)

文档的存储(字处理器文档、电子表格、矢量图形等)
Some database systems popular in data analytics & big data use semistructured data

在数据分析和大数据中流行的一些在数据库系统使用半结构化数据

![image-20221130171524357](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221130171524357.png)

* XML 
  * 树型结构数据
  * 比关系数据库更慢,但可以做的更多
* JSON 
  * 类似于XML
  * 大量与JavaScript结合使用
  * 较慢，但可以比关系数据库做得更多
* 简单的键值关系
  * 对应于非常简单的XML / JSON文档
  * 更快,但比关系数据库少得多
* 图表
  * 半结构化数据的最一般形式之一
  * 较慢，但可以比关系数据库做得更多

### 3. Basics of XML

![image-20230117165441529](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117165441529.png)

#### 3.1 XML

* XML files look similar to HTML files
* XML文件看起来类似于HTML文件
* An XML document representing the example graph:
* 代表示例图的XML文档:

![image-20230117160320241](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117160320241.png)

![image-20230117160352463](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117160352463.png)

![image-20230117160451114](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117160451114.png)

#### 3.2 Nodes with multiple parents

* XML does not actually have these 
* XML实际上没有这些
  * It is only the case in more general semi-structured file types
  * 在更一般的半结构化文件类型中
  * In other words: XML files forms trees
  * 换句话说,XML文件形成树
  * Have a notion of references (think of them as shortcuts in a file system)
  * 了解引用的概念(可以把它们看作文件系统中的快捷方式)

![image-20230117160800699](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117160800699.png)

#### 3.3 Elements & Tags 元素与标签

* An element has the following form:
* 元素的形式如下:

![image-20230117161114760](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117161114760.png)

* Elements may be nested

* 元素可以嵌套

  *  Nestings must be proper
  * 巢必须是合适的
  * The root element is the element not contained in any other element
  * 根元素是不包含在任何其他元素中的元素
  * A well-formed XML document must have exactly one root element

  * 格式良好的XML文档必须只有一个根元素

* Elements may be empty, in which case we combine the opening and the closing tag: <keyword />

* Elements are case sensitive

* 元素可能是空的,在这种情况下,我们将打开和关闭标记结合在一起:<keyword/ >

* 元素是很敏感的

#### 3.4 Attributes 元素

* Elements can have attributes (name-value pairs), which are put into the element’s opening tag
* 元素可以具有属性(名称-值对)，这些属性放在元素的开始标记中

![image-20230117162353236](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117162353236.png)

* Only one attribute of a given name for each element 
* 每个元素只有一个给定名称的属性
* Useful for ”references”

![image-20230117162449305](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117162449305.png)

* Elements in an XML document are ordered as they occur in the document
* XML文档中的元素在文档中被排序
* Part of the data representation!
* 部分数据表示!

![image-20230117162557942](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117162557942.png)



#### 3.5 Other Features

* Optional **document type definition or XML Schema** at start of XML document.
* 可选的文档类型定义或XML文档开头的XML模式。
* **Entity references**: serve various purposes, such as shortcuts to often repeated text or to distinguish reserved characters from content.
* 实体引用:用于各种目的，例如用于经常重复的文本的快捷方式，或用于区分保留字符和内容。
* **Comments:** enclosed in <!-- and --> tags.
* **评论，我咋觉得是注释呢。。。**
* **CDATA Sections/processing instructions:** can also be used to provide information to application.
* CDATA节/处理指令:也可以用来向应用程序提供信息。

### 4. DTD

https://blog.csdn.net/m0_62839141/article/details/124895443?ops_request_misc=%257B%2522request%255Fid%2522%253A%2522167397449116800213044249%2522%252C%2522scm%2522%253A%252220140713.130102334..%2522%257D&request_id=167397449116800213044249&biz_id=0&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduend~default-1-124895443-null-null.142^v71^

![image-20230117165559025](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117165559025.png)

#### 4.1 Document Type Definitions (DTDs) 文档类型定义(dtd)

* Information about the structure of an XML document
* 关于XML文档结构的信息
  * Elements that may occur in the document,
  * 文档中可能出现的元素，
  * Sub-elements that an element may have,
  * 元素的子元素，
  * Attributes that an element may have, etc.
  * 元素可能具有的属性，等等。
* **Included at the beginning the XML document (between <?xml ... standalone=“no”> and root element)**
* **包含在XML文档的开头(<?xml……Standalone = " no " >和根元素)**

![image-20230117164525799](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117164525799.png)

* Good tradeoff between a full schema and flexibility 完整的模式和灵活性之间很好的权衡

![image-20230117165139066](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117165139066.png)

DTD明显和XML不一样，但是有相似之处。

#### 4.2 Element Type Declarations 元素类型声明

* Identify the rules for elements that can occur in the XML document (i.e. inside parenthesis)
* **确定XML文档中可能出现的元素的规则(即在括号内)**
  * Like: (name, phone?, email?, teaches*)
* **Name with no qualifying punctuation must occur exactly once.** 
* **没有限定标点符号的名称必须恰好出现一次。**
  * Options for repetition are:
    * ***indicates zero or more occurrences for an element;**
    * ***表示一个元素的零或更多的事件;**
    * **+indicates one or more occurrences for an element;**
    * **+表示一个元素出现一次或多次;**
    * **? indicates either zero occurrences or exactly one occurrence for an element.**
    * **?指示一个元素零次出现或只出现一次。**

#### 4.3 Defining Attributes 定义属性

* We have previously seen things like:
  				<module code=”COMP105” title=“Programming Paradigms” /> 
* How do we define that?
* First, define module (without the attributes):
  					<!ELEMENT module EMPTY>
* Then, define the attributes. You do that as follows:
* 然后，定义属性。你可以这样做:
  * <!ATTLIST module code CDATA #IMPLIED>
  * <!ATTLIST module title CDATA #IMPLIED>
  * ![image-20230117170253048](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117170253048.png)

![image-20230117170242107](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117170242107.png)

#### 4.4 DTDs –Attribute Data types

* CDATA: character data, containing any text.
* CDATA:字符数据，包含任何文本。
* ID: used to identify individual elements in document (ID is an element name).
* ID:用于标识文档中的单个元素(ID是一个元素名称)。
* IDREF/IDREFS: must correspond to value of ID attribute(s) for some element in document
* IDREF/IDREFS:必须对应于文档中某些元素的ID属性值
  * ◦ (The previously mentioned shortcuts)
  * (前面提到的快捷方式)
  * ◦ Note: You can not define what type you are pointing at exactly, but just that it is some ID for some object
  * 注意:您不能确切地定义您所指向的类型，而只是某个对象的某个ID
* List of names: values that attribute can hold (enumerated type)
* 名称列表:属性可以保存的值(枚举类型)
  * ◦ Format: (en1|en2|...) meaning the value can be either en1 or en2 or ...

![image-20230117172636552](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117172636552.png)

#### 4.5 Element Identity, IDs, IDREFs

* **ID allows unique key to be associated with an element.** 

* **ID允许将唯一键与元素相关联。**

  

* **IDREF allows an element to refer to another element with the designated key, and attribute type** 

* **IDREF允许一个元素引用另一个具有指定键和属性类型的元素**

  

* **IDREFS allows an element to refer to multiple elements.** 

* **IDREFS允许一个元素引用多个元素。**

  

* To loosely model relationship “Department has Lecturers” and “Department has a head who is a Lecturer”: 

* 要松散地建模“部门有讲师”和“部门有一个负责人是讲师”的关系:

![image-20230117172931970](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117172931970.png)

#### 4.6 Document Validity

* Two levels of document processing: **well-formed and valid.** 
* 文档处理的两个层次:格式良好和有效。
* Non-validating processor ensures an XML document is well-formed before passing information on to application. 
* 在将信息传递给应用程序之前，非验证处理器确保XML文档是格式良好的。
* XML document that conforms to structural and notational rules of XML is considered well-formed; e.g.:
  * ◦ all elements must be within one root element
  * ◦ elements must be nested in a tree structure without any overlap
* Validating processor will not only check that an XML document is well-formed but that it also conforms to a DTD (or XML Schema), in which case XML document is considered valid.
* 验证处理程序不仅检查XML文档是否格式良好，而且还检查它是否符合DTD(或XML模式)，在这种情况下，XML文档被认为是有效的。



### 5.XPath

 ![image-20230117174816197](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117174816197.png)

#### 5.1 General Idea 

* XPath allows us to write queries that return a set of values or nodes from an XML document Values
* XPath允许我们编写从XML文档返回一组值或节点的查询
* Values
  * strings, integers, reals, etc.
* Nodes
  * Document “node”: 
  * Represents the entire document
  * Not the root element
* Element node: any element
  * Attributes: found inside opening tags of elements
  * 属性:在元素的开始标记中找到
* ![image-20230117180637024](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117180637024.png)

#### 5.2 Path Expressions

* Format:![image-20230117180805586](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117180805586.png)
* Selects all nodes reachable from the root by following the edges labeled E1, E2, ..., En
* 根据标记为E1, E2，…的边选择从根可达的所有节点。
* Examples:
  ◦ /students: selects the root element
  ◦ /students/student:selects all student elements
* The result is returned in document order
* 结果按文档顺序返回

![image-20230117180712700](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117180712700.png)



![image-20230117181038404](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117181038404.png)



![image-20230117181204581](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117181204581.png)

#### 5.3 Relative Path Expressions 相关路径表达

* Format:![image-20230117191748982](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117191748982.png)
* Don’t evaluate at the root, but relative to another node
* 不要在根节点上求值，而是相对于另一个节点求值
* Examples:
* ◦ student/name: all name elementsof student elements below a given node
* 给定节点下student元素的所有name元素
* **Again, the result is returned in document order**
* **同样，结果按文档顺序返回**

![image-20230117191700707](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117191700707.png)

#### 5.4 Attributes

* Path expressions can be extended so that we can return attribute values
* 路径表达式可以扩展，这样我们就可以返回属性值
* Idea: replace the last tag name by @A **Attribute name**
* 想法:用@A替换最后一个标签名
* Example:
  * ◦ /students/student/@namereturns ”Anna”, “Ben”, “Chloe”
  * ◦ /students/student/module/@codereturns “COMP207”, “COMP219”
  * ◦ student/@name
* Again: document order
* 再次强调:文件顺序

![image-20230117193348359](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117193348359.png)



#### 5.5 Wildcards 万用字符

* **A wildcard (*) can be used to stand for any tag name or attribute name***
* **通配符(*)可以用来表示任何标记名或属性名**
* *Example:
  * *◦ /students/student/*returns all elements directly below student elements
  * ◦ /students/student/module/@*returns all attributes of modules

![image-20230117194013826](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117194013826.png)



#### 5.6 General form of path expression 路径表达式的一般形式

![image-20230117194055287](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117194055287.png)

#### 5.7 Navigation Axis 导航轴

* **An axis determines the next item on the path:**
* **轴决定路径上的下一项:**

![image-20230117195624676](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117195624676.png)

##### 5.7.1 Descendant 后裔

* Descendant is any number of outgoing arrows away (but at least 1)
* 后代是任意数量的外向箭头(但至少1个)指向的节点

![image-20230117200143010](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117200143010.png)

##### 5.7.2 Parent， Ancestor，Child

* Child is 1 outgoing arrow away
* Child是1个向外的箭头指向的节点
* **x is the parent of y ⇔y is the child of x**
* **x is the ancestor of y ⇔y is the descendant of x**

![image-20230117200319891](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117200319891.png)

##### 5.7.3 Self，Preceding-Sibling，Following-Sibling

* preceding-sibling is the same as going to the parent and then to a child before you in document order following-sibling is a child of your parent after you in document orderself is yourself...
* preceding -sibling和在文档顺序上先到父节点，再到你之前的子节点是一样的。
* <font color=red size=5>**preceding文档顺序和正常文档顺序相反**</font>
  * **preceding-sibling::*[1]指的是最靠近self的哥哥节点**
* following-sibling是在你之后的父节点的子节点。self是你自己。
* ![image-20230117200628473](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117200628473.png)

https://blog.csdn.net/ZYX_jber/article/details/120986932?ops_request_misc=&request_id=&biz_id=102&utm_term=Xpath&utm_medium=distribute.pc_search_result.none-task-blog-2~all~sobaiduweb~default-1-120986932.142^v71^control_1,201^v4^add_ask&spm=1018.2226.3001.4187

![image-20230119092103505](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230119092103505.png)

**子孙节点指后代，在此节点后的所有节点**

**@选取的是属性，不是节点**

![image-20230117200813651](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117200813651.png)

**注意：两道杠表示全选**

#### 5.8 Condition of XPath

* **Idea: if the condition is true, follow the path further**
* **想法:如果条件为真，就沿着这条路走下去**
* **Basic form of conditions:**
* **条件的基本形式:**
  * **Comparisons of two values with =, <, >, <=, >=, !=**
  * **A value can be a relative path expression or any constant**
  * **值可以是相对路径表达式或任何常数**
  * **<font color=red>常数即表示在此节点下的第几个item</font>**
  * **“Existential semantics”**
  * **“生存语义”**
* Combinations of such comparisons using ’and’ & ‘or’
* 使用' and ' & ' or '的比较组合

![image-20230117200920867](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117200920867.png)

![image-20230117201257417](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117201257417.png)

![image-20230117201305891](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117201305891.png)

![image-20230117201500233](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117201500233.png)

多种条件嘛，一步步来

![image-20230117201702694](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117201702694.png)

![image-20230117201716295](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117201716295.png)

![image-20230117201722734](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117201722734.png)

![image-20230117201729604](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117201729604.png)

这里没什么太好说的，看图一步步来就行



**<font color=red size=5>这几个条件得好好看看</font>**

![image-20230119103406636](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230119103406636.png)

![image-20230117201914612](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117201914612.png)

**最后一个，ancestor::*[2]  的意思是指父节点的父节点**

![image-20230117203010985](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117203010985.png)

* Red axes: Reverse axes (i.e. nodes are ordered in reverse of document order) for [i] where i is some number... (The nodes are ordered as normal in output)
* 红色轴:[i]的反向轴(即节点的顺序与文档顺序相反)，其中i是某个数字…(节点在输出中按正常顺序排列)

![image-20230117203701297](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117203701297.png)

data()的意思是不为空。

![image-20230117203845296](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117203845296.png)

![image-20230117203901454](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117203901454.png)



#### 5.9  The Role of XPath

* Not used as a query language itself
* 本身不用作查询语言
  * Used for other languages
  * Examples: XQuery, XMLSchema, ...
* **Purpose: select items in an XML document**
* **目的:在XML文档中选择项**
* Compare with attributes in relational databases, which select items in relations
* 与关系数据库中的属性进行比较，关系数据库选择关系中的项

![image-20230117203932243](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117203932243.png)





## Lecture25 XQuery

### 1. XML Schema

这会在课程最后显示

![image-20230117205131646](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117205131646.png)

### 2. XQuery

* Extension of Xpath by SQL-Like features  通过类似sql的特性扩展XPath
* <font color=blue>XPath是一门XML和HTML文档中查找信息的语言，可用来在XML和HTML文档中对元素和属性进行遍历，这里使用sql的特性来扩展XPath</font>
  *  Every XPath expression is an XQuery expression  每个XPath表达式都是一个XQuery表达式
* More general XQueries: FLWR expressions   更通用的xquery: **FLWR表达式**

![image-20221125093837324](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221125093837324.png)

![image-20221125093911567](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221125093911567.png)

#### 2.1 FLWR Expressions FLWR表达式

![image-20221125094115474](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221125094115474.png)

感觉格式就按照这个来 必须有一个Let 和一个return



#### 2.2 Let Clauses Let条款

![image-20221125094441798](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221125094441798.png)

* Assigns the result of XQuery expression to variable  
* 将XQuery表达式的结果赋值给变量
* Examples:
  * ![image-20221125094542471](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221125094542471.png)
* Variable names: 变量的命名
  * Start with $ (e.g., $doc, $x, $student) 

#### 2.3 For Clauses    For 条款

![image-20221125094721266](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221125094721266.png)

* Execution: 执行
  * Consider each item in the result of XQuery expression in turn (same order as in the result)      依次考虑XQuery表达式结果中的每个项(与结果的顺序相同)
  * For each item, assign it to variable & execute whatever follows the forclause   对于每一项，将其赋值给变量并执行for子句后面的任何内容
  * **For** - selects a sequence of nodes
  * <font color=blue>选择一系列的节点, s有点类似于sql中的选择图表</font>
  
* Examples:
  * ◦ for $s in $doc/students/student
    ◦ for $name in $doc//student[module="COMP207"]/name
  
* ![image-20221207165106913](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221207165106913.png)

#### 2.4 Where Clauses Where 条款

![image-20221125142018703](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221125142018703.png)

* Execution:
  * Evaluate all the conditions   评估所有条件
  * <font color=blue>筛选节点</font>
  * If the conditions are true, then execute the return clause   如果条件为真，则执行return子句
* Conditions：条件
  * e.g. comparison between XPath and constant   比较Xpath和内容
* Example:
  * where $s/module = “COMP207”
  * where $s/year > 2
  
  ![image-20221207165655628](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221207165655628.png)

![image-20221125142315093](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221125142315093.png)

##### 2.4.1 Cafeful With Conditions  仔细的条件

conditions of the form expression * constant  形式表达式*常量的条件

* Example：
  * $s/module = “COMP207”
  * $s/year >= 2
* Existential semantics：e.g., $s/module = “COMP207” is true.  if and only if there exists an item returned by $s/module whose text is equal to “COMP207”  当且仅当$s/module返回一个文本等于" COMP207 "的项

![image-20221207165750739](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221207165750739.png)

##### 2.4.2 Other Types of Conditions

![image-20221207170058183](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221207170058183.png)

<font color=blue>以最后的例子来举例：</font>

![image-20221207170203279](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221207170203279.png)

这个的意思就是在$l/teaches的每个变量$m都需要满足$m/year <= 2

![image-20221207171716870](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221207171716870.png)



![image-20221207171750676](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221207171750676.png)

**<font color=red>返回多个元素时需要返回一个链表</font>**

![image-20221207171842004](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221207171842004.png)

![image-20221207171957487](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221207171957487.png)



![image-20221207172327249](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221207172327249.png)

![image-20221207172402081](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221207172402081.png)

#### 2.5 Order By

在where语句后添加order by，**默认为升序**

![image-20221207172539303](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221207172539303.png)

![image-20221207172651077](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221207172651077.png)



#### 2.6 Group By

![image-20221207172735669](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221207172735669.png)

![image-20221207173636266](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221207173636266.png)

![image-20221207173645563](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221207173645563.png)



#### 2.7 Distinct Values

* In SQL it was a key word (DISTINCT)
* 在SQL中，它是一个关键字(DISTINCT)
* **In XQuery, it is a function, called <font color=red size=5>distinct-values</font>**
* 在XQuery中,它是一个叫做区别值的函数
  *  Converts elements to strings 
    转换元素到字符串

![image-20221207174444286](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221207174444286.png)

<font color='blue'>这种结构不太对，需要用另外一个结构</font>

![image-20221207174600518](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221207174600518.png)

<font color='blue'>需要用函数把整个全部包围起来</font>

![image-20221207174651181](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221207174651181.png)

![image-20230117215013054](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117215013054.png)



### 3. XML in SQL

#### 3.1 SQL in XML

* We will represent the following relational database by an XML document:
* 我们将用XML文档表示以下关系数据库:

![image-20221207175010496](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221207175010496.png)

Bonus: will add a<font color='red'> **DTD Schema**</font> so that the following are in 1-to-1 correspondence

将添加DTD模式,以便在1到1的通信中

* **XML documents conforming to the DTD**
* **符合DTD的XML文档**
* Relational databases with the above schema
* 使用上述模式的关系数据库

![image-20221207200919226](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221207200919226.png)

* Write black part (without ... and with standalone=“yes” instead) gives you a well-formed XML document
* **写黑色部分(没有…而用standalone= " yes "代替)会给你一个格式良好的XML文档**
* Also write the orange part gives you a valid XML document
* 另外，编写橙色部分将为您提供一个有效的XML文档

* 两者的差别在于是否遵守DTD规范。我们认为符合
* ![image-20230117220115695](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117220115695.png)

#### 3.2 XML in SQL

* Three general approaches to storing XML documents in a relational database:
* 在相关数据库中，三种常用的存储XML文件的方式
  * Store XML documents as entries of a table
  * 将XML文档存储为表的条目
  * Store XML documents in schema-independent form
  * 以独立于模式的形式存储XML文档
  * Store XML documents in shredded form across a number of attributes and relations
  * 将XML文档存储在多个属性和关系中

##### 3.2.1 Storing XML in an Attribute

![image-20230117220204414](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117220204414.png)

![image-20221210215938610](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221210215938610.png)

![image-20221210220000914](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221210220000914.png)

##### 3.2.2 Schema-Independent Representation Schema的独立表示

**Since XML is a tree structure, each node may have only one parent. The rootID attribute allows a query on a particular node to be linked back to its document node.**

**由于XML是树结构，每个节点可能只有一个父节点。rootID属性允许将特定节点上的查询链接回其文档节点。**

While this is schema independent, recursive nature of structure can cause performance problems when searching for specific paths. 

虽然这与模式无关，但在搜索特定路径时，结构的递归性质可能会导致性能问题。

To overcome this, create denormalized index containing combinations of path expressions and a link to node and parent node.

要克服这个问题，可以创建非规范化索引，其中包含路径表达式的组合以及到节点和父节点的链接。

![image-20221210220523594](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221210220523594.png)

##### 3.2.3 Storing XML in Shredded Form 以粉碎模式存储XML

* **XML decomposed (shredded) into its constituent elements and data distributed over number of attributes in one or more relations.**
* **XML分解(分解)成它的组成元素和数据，分布在一个或多个关系中的多个属性上。**
*  Storing shredded documents may make it easier to index values of some elements, provided these elements are placed into their own attributes. 
* 存储切碎的文档可能会使一些元素的索引值变得更容易,如果这些元素被放置在它们自己的属性中。
* Also possible to add some additional data relating to hierarchical nature of the XML, making it possible to recompose original structure and ordering, and to allow the XML to be updated.
* 还可以添加一些与XML的层次性质有关的额外数据,使其能够重新构建原始的结构和排序,并允许更新XML。
* With this approach also have to create an appropriate database structure.
* 用这种方法还得创建一个合适的数据库结构。

### 4. Introduction to NoSQL

#### 4.1 NoSQL Databases 不只是数据库

* **NoSQL: “Not Only SQL” or “Not Relational”  不仅只是SQL**

* **Cater to requirements for typical web applications**
* **满足典型web应用程序的需求**
  * **Very fast access to data, with millions of users in parallel**
  * **非常快速地访问数据，与数百万用户并行**
  * **Fault-tolerance**
  * **容错系统**
  * **Flexibility in the type of data stored (semi-structured)**
  * **存储数据类型的灵活性(半结构化)**
  * **Full ACID compliance can sometimes be relaxed**
  * **完全遵守ACID有时可以放松**
* Not restricted to such applications 不限于这样的应用程序
  * E.g., popular for big data analytics projects
* Not a replacement for relational databases
* 不是关系数据库的替代品

![image-20221210223025603](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221210223025603.png)

##### 4.1.1 NoSQL Database Characteristics NoSql 数据库的性质

* NoSQL databases are often distributed NoSQL数据库通常是分布式的
  * Nodes run on commodity hardware
  * 节点运行在商用硬件上
  * Standard network
  * 标准的网络
  
* Designed to Guarantee:
  * **Availability: every non-failing node always executes queries**
  * **可用性:每个不失败的节点总是执行查询**
  * **Consistency: every read receives the most recent write or an error**
  * **一致性:每次读都接收最近一次写或错误**
  * **Scalability: more capacity (users, storage, ...) by adding new nodes**
  * **可伸缩性:通过添加新节点获得更大的容量(用户、存储等等)**
  * **High performance: often achieved by very simple interface(e.g., support lookups/inserts of keys, but do this fast)**
  * **高性能:通常通过非常简单的界面(例如。，支持查找/插入键，但要快)**
  * **Partition-tolerance: even if nodes (or messages) fail, the remaining subnetworks can continue their work**
  * **部分-公差:即使节点(或消息)失败,其余的子网络可以继续他们的工作**
* **<font color=red size=5>Often give up ACID to improve performance</font>**
* **经常放弃ACID来提高性能**

![image-20221210223848384](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221210223848384.png)

##### 4.1.2 The Cap Theorem 茶杯理论

* We cannot achieve all three of these properties:
* 我们不可能同时达到这三个特性

![image-20221210223942967](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221210223942967.png)

##### 4.1.3 From ACID to Base

NoSQL databases drop ACID and often provide the weaker guarantees of BASE:

NoSQL数据库放弃ACID，通常提供较弱的BASE保证:

* **Basically Available,  基本上能用就行**

* **Soft state & eventual consistency:  软状态和最终一致性:**
  * **the database state might occasionally be inconsistent...**
  * **数据库状态可能偶尔不一致**
  * **but it will eventually be made consistent**
  * **但是他们最终将一致**

![image-20221210224238631](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221210224238631.png)

##### 4.1.4 NoSQL Database Classification

Common Classification:

* Key-value stores:
* 键值对存储
  * Efficient lookups and insertions of key-value pairs
  * 高效的键值对查找和插入
* Document stores:
*  文件存储 
  * Similar to key-value stores (values = semi-structured data, represented e.g. in XML/JSON)
  * 类似于键值存储(值=半结构化数据，例如用XML/JSON表示)
  * Lookups can involve values from documents
  * 查找可能涉及文档中的值
* Column stores
* 列存储
* Graph databases
* 图像存储

![image-20221210225316605](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221210225316605.png)







### 5. Key-Value Stores

#### 5.1 Key-Value Stores

Key-value stores are a type of database that uses a unique key to retrieve a corresponding value. They are often used for simple data storage and retrieval, as they provide fast and efficient access to data. Key-value stores are also known as key-value databases, key-value stores, or simply key-value systems. They are commonly used in distributed systems and cloud computing environments, where they provide a scalable and fault-tolerant way to store and retrieve data. Key-value stores typically support operations such as inserting, updating, and deleting key-value pairs, as well as searching for keys and retrieving their corresponding values.

**Key-value存储是一种数据库，它使用唯一的键来检索相应的值。**它们通常用于简单的数据存储和检索，因为它们提供了快速高效的数据访问。Key-value存储也被称为键值数据库、键值存储或简单的键值系统。它们通常用于分布式系统和云计算环境，提供了一种可扩展和容错的方法来存储和检索数据。Key-value存储通常支持插入、更新和删除键值对，以及搜索键并检索它们的对应值的操作。

![image-20221210231118730](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221210231118730.png)

![image-20221210231143355](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221210231143355.png)



#### 5.2 Distributed Storage

Each key-value pair (k,v) is stored at some node

* Step 1: Assign values vfor key kto integer between 0 and 2n-1
* 在0和2n-1之间分配关键的kto整数值
* Step 2:Distribute nodes to some of the integers(typically randomly)
* 将节点分配给某些整数(通常是随机的)

* **If (k,v) is assigned to integer i, it is stored at the node following i on the ring**

* **如果(k,v)赋值给整数i，则它存储在环的下一个节点上**

![image-20221210232453566](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221210232453566.png)



##### 5.2.1 Scalability Via Horizontal Fragmentation 通过水平碎片实现可扩展性

New nodes can be added easily:

* Add node to free range(s) and move key-value pairs appropriately
* 将节点添加到自由范围，并适当移动键-值对
* Automatic horizontal fragmentation
* 自动水平分段

![image-20221210232558744](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221210232558744.png)

##### 5.2.2 Replication 复制

* Replication is used to ensure availability

* 复制用于确保可用性

* Replicas (copies of key-value pairs) are stored on consecutive nodes on the ring in clock-wise order

* 副本(键-值对的副本)按顺时针顺序存储在环上的连续节点上

![image-20221210232829555](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221210232829555.png)

##### 5.2.3 Properties

![image-20230117222115806](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117222115806.png)

![image-20221210232915819](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221210232915819.png)

![image-20221210232957962](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221210232957962.png)

![image-20221210232951734](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221210232951734.png)







### 6.  Other NoSql DataDases

#### 6.1 Document Stores

* Databases that store collections of “documents”
* 存储“文档”集合的数据库
  * Document = semistructured data associated with an object ID
  * 文档=与对象ID相关联的半结构化数据

![image-20230117223749881](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117223749881.png)

![image-20230117223811716](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117223811716.png)

![image-20230117223820359](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117223820359.png)

##### 6.1.1 Typical Use Case 典型用例

* Restaurant information web service
* 食肆资讯网页服务
  * Filter collection of restaurants by location, ratings, etc.
  * 过滤集合餐厅的位置，评级等。
  * Data associated with restaurants might vary
  * 与餐厅相关的数据可能有所不同
  * User requests typically require all data associated with a restaurant, but do not need to join data from different restaurants
  * 用户请求通常需要与餐厅相关的所有数据，但不需要连接来自不同餐厅的数据

![image-20230117223914879](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117223914879.png)

![image-20230117224218675](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117224218675.png)

![image-20230117224340737](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117224340737.png)

![image-20230117224347466](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117224347466.png)

![image-20230117224405043](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117224405043.png)





#### 6.2 Column Stores 列存储

![image-20230117224526469](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117224526469.png)

![image-20230117224540460](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117224540460.png)

![image-20230117224602958](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117224602958.png)

#### 6.3 Graph Databases

![image-20230117224614353](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117224614353.png)



## Lecture 27&28&29 Introduction to data-analysis


### 1. The Final Part

* Return to relational databases
* 返回关系数据库
  * ◦ So, again relational databases, SQL, ...
* **Different use cases: data analysis**
* **不同的用例:数据分析**
* **Different technology: data warehouses**
* **不同的技术:数据仓库**

![image-20230117225544175](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117225544175.png)



#### 1.1 A Data Analysis Scenario 一个数据分析场景

![](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117225626758.png)

![image-20230117230040521](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117230040521.png)

![image-20230117230316503](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117230316503.png)

#### 1.2 Data WareHouses 数据仓库

* Database systems designed to support data analysis
* 数据库系统设计用于支持数据分析
  * ◦ ...to answer queries like those in the previous scenarios
* Typically integrate different data sources
* 通常集成不同的数据源

![image-20230117230605505](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117230605505.png)

#### 1.3 OLAP vs OLTP

* **OLAP (Online Analytic Processing): refers to the process of analysingcomplex data stored in a data warehouse**
* **OLAP(在线分析处理):指对存储在数据仓库中的复杂数据进行分析的过程**
* OLAP query: a query used in OLAP
* OLAP查询:用于OLAP的查询
  * ◦ Typical OLAP query:
  * ![image-20230117230839718](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117230839718.png)
* **OLTP (Online Transaction Processing): traditional DBMS tasks**
* **OLTP(在线事务处理):传统的DBMS任务**
  * ◦ queries and updates that can be executed fast
  * 可以快速执行的查询和更新
  * ◦ affect a small portion of a database
  * 影响数据库的一小部分

![image-20230117231014227](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117231014227.png)

##### 1.3.1 Fact Tables & Data Cubes 事实表和数据立方体

* In OLAP applications, there is typically a unique **fact table**
* 在OLAP应用程序中，通常有一个唯一的事实表
  * **Represents events & objects of interest for the analysis**
  * **表示对分析感兴趣的事件和对象**
* Example fact table: Sales(productNo, date, store, price)
* 示例事实表:Sales(productNo，日期，商店，价格)
* May be thought of as representing a data cube
* 可以被认为代表一个数据立方体

![image-20230117231143770](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117231143770.png)

#### 1.4 Star Schemas 星策略

* One of the most common data warehouse architectures
* 最常见的数据仓库架构之一
  * ◦ Unique fact table: contains points in the data cube
  * 唯一事实表:包含数据多维数据集中的点
  * ◦ Dimension tables: describe values along each axis
  * 维度表:描述沿每个轴的值

![image-20230117231513642](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117231513642.png)



### 2. Market-basket model  市场购物篮模型

* Data that can be described by:
  * A set of items I
  * 一套项目I
  * A set of baskets B: each basket b∈Bis a subset of I
  * 一组篮子B:每个篮子B∈Bis是I的子集

![image-20230117232623474](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117232623474.png)



![image-20230117232633898](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117232633898.png)

![image-20230117232933673](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117232933673.png)

![image-20230117232940316](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117232940316.png)

![image-20230117232947420](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117232947420.png)

![image-20230117232954995](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117232954995.png)

![image-20230117233004088](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117233004088.png)

![image-20230117233010884](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117233010884.png)

![image-20230117233026492](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117233026492.png)

![image-20230117233042733](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117233042733.png)

![image-20230117233048957](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117233048957.png)

![image-20230117233055763](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117233055763.png)

![image-20230117233102323](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230117233102323.png)







Atomicity

在commit之前，数据库都没有被更改，所以如果中途出现错误，执行会被撤销返回到执行前的状态。

Isolation



不太明白。



我们听说了ACID:答:

原子性——要么拥有一切，要么一无所有C:

一致性——满足约束之间的某个地方，直到与现实世界相匹配我:

隔离——该效果与以某种顺序单独执行的每个事务相匹配D:

持久性——已提交的事务以后不会被撤消



 ## Problems

### Week1

![image-20221013222152212](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221013222152212.png)

当B =1时，只删除的工作原理。注意，从B中删除东西不会打破外键约束，但插入可能会。此外，添加A可能会打破主键约束，从A中删除可能会打破外键约束。

<font color='red'>外键是另一个表的主键或唯一约束，且外键可以为空或者重复。但主键不能为空或重复</font>

## Week2

![image-20221018230511923](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221018230511923.png)

因为有R和S分别有5rows 和6rows，且我们不确定它们是否有名称相同的列，如果没有，则自然连接的结果是30.如果有，则结果可能是[0,30)。

![image-20221018231307827](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221018231307827.png)

自己试一试就看的出来。。。



![image-20221018231342348](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221018231342348.png)

![image-20221018231357704](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221018231357704.png)

![image-20221018231428891](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221018231428891.png)

除了模块和代码是两个不同的词(<font color='red' size=5>**因此自然连接默认为笛卡尔积**</font>)之外，如果它是固定的，这甚至不会是正确的输出(因为在这种情况下Sebastian应该匹配COMP201, John应该匹配COMP105)。

![image-20221018233045040](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20221018233045040.png)

......实话实说，我不理解















![image-20230118112013114](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230118112013114.png)

![image-20230118114102096](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230118114102096.png)



![image-20230118144812969](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230118144812969.png)

![image-20230118151148732](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230118151148732.png)

![image-20230118151201547](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230118151201547.png)

![image-20230118153125319](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230118153125319.png)

![image-20230118153437570](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230118153437570.png)

![image-20230118155251483](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230118155251483.png)

![image-20230118155303215](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230118155303215.png)

![image-20230118160813117](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230118160813117.png)

![image-20230118160821296](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230118160821296.png)

![image-20230118162646580](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230118162646580.png)

![image-20230118162916567](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230118162916567.png)



![image-20230118171522812](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230118171522812.png)



![image-20230118171556498](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230118171556498.png)

![image-20230118171604498](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230118171604498.png)



![image-20230118173733303](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230118173733303.png)



![image-20230118174235406](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230118174235406.png)



![image-20230118215952922](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230118215952922.png)



![image-20230118224353247](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230118224353247.png)















