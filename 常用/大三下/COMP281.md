# COMP281 

# C

## 1. 打印

### 1.1 转义字符

![image-20230201162921953](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230201162921953.png)

### 1.2 数据类型

![image-20230201165247949](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20230201165247949.png)

* 字符使用单引号，字符串使用双引号



## 1. Compiling and Running C Programs

### 1.1. 4 kinds of files to work with

![image-20230214163332399](D:\笔记\笔记图片\image-20230214163332399.png)

![image-20230214163351106](D:\笔记\笔记图片\image-20230214163351106.png)

![image-20230214163400400](D:\笔记\笔记图片\image-20230214163400400.png)

![image-20230214163409188](D:\笔记\笔记图片\image-20230214163409188.png)

### 1.2. The Preprocessor 预处理器

* It is a separate program, normally called “cpp” for “c preprocessor”. 
* 它是一个独立的程序,通常被称为“cpp”,用于“c预处理”
* It is invoked automatically by the compiler before compilation proper begins. 
* 它在编译开始之前由编译器自动调用。
* It converts source code (*.c) files, which may exist as a real file or be stored in memory for a short time before being sent to the Compiler. 
* 它将源代码(* . c)文件转换为一个真实的文件,或者在发送到编译器之前的短时间内存储在内存中
* Preprocessor commands start with “#”. There are several preprocessor commands; the most important ones are:
* Preprocessor命令以“#”开头。有几个预处理命令;最重要的是:

#### 2.1 #include

* #include
* ![image-20230214164908075](D:\笔记\笔记图片\image-20230214164908075.png)

* To access function definitions defined outside of a source code file, e.g.,
* 要访问在源代码文件之外定义的函数定义，例如，

![image-20230214164940778](D:\笔记\笔记图片\image-20230214164940778.png)



* C compilers do not allow using a function unless it has previously been declared or defined in the file. #include statements are thus the way to re-use previouslywritten code in C programs.
* C编译器不允许使用函数，除非它之前已经在文件中声明或定义过。因此，#include语句是在C程序中重用之前编写的代码的方法。

#### 2.2 \#define

![image-20230214165330478](D:\笔记\笔记图片\image-20230214165330478.png)

![image-20230214165357058](D:\笔记\笔记图片\image-20230214165357058.png)

* To avoid having to explicitly write out some constant value in many different places in a source code file.
* 为了避免在源代码文件中显式地在许多不同的地方写一些常量值。
* This is important if the constant value needs to be changed later; it's much less bug-prone to change it once, in the #define, than to have to change it in multiple places scattered all over the source code.
* 如果以后需要更改常量值，这一点很重要;在#define中更改一次比在散布在源代码中的多个地方更改更不容易出现错误。

![image-20230214165457475](D:\笔记\笔记图片\image-20230214165457475.png)



### 1.3.The Compiler

* After the Preprocessor has included all header files and expanded out all the #define and #include statements (and any other preprocessor commands that may be in the original file), the compiler compiles the program.
* 在预处理器包含所有头文件之后,并扩展了所有#定义和# include语句(以及其他可能在原始文件中的其他预处理命令),编译器编译程序。
* It turns the source code into an object code file, which contains the binary version of the source code (not executable yet).
* 它将源代码转换为目标代码文件，其中包含源代码的二进制版本(还不能执行)。

![image-20230214165752616](D:\笔记\笔记图片\image-20230214165752616.png)

![image-20230214165758991](D:\笔记\笔记图片\image-20230214165758991.png)

### 1.4 The Linker

![image-20230214165954446](D:\笔记\笔记图片\image-20230214165954446.png)



![image-20230214170003373](D:\笔记\笔记图片\image-20230214170003373.png)



## 2. C Language Basics

![image-20230214170034929](D:\笔记\笔记图片\image-20230214170034929.png)

![image-20230214170136822](D:\笔记\笔记图片\image-20230214170136822.png)



![image-20230214170143134](D:\笔记\笔记图片\image-20230214170143134.png)



![image-20230214170210287](D:\笔记\笔记图片\image-20230214170210287.png)



![image-20230214170233047](D:\笔记\笔记图片\image-20230214170233047.png)

![image-20230214170309222](D:\笔记\笔记图片\image-20230214170309222.png)

![image-20230214170349960](D:\笔记\笔记图片\image-20230214170349960.png)

![image-20230214170358733](D:\笔记\笔记图片\image-20230214170358733.png)





## 3. 指针

### 3.1 指针变量和指针

![image-20230302205943674](D:\笔记\笔记图片\image-20230302205943674.png)

* 不同类型的数据所占用的内存是不一样的

### 3.2 取地址运算符和取值运算符



![image-20230302210150074](D:\笔记\笔记图片\image-20230302210150074.png)

* **也就是说，同样的*pb其实是可以代表完全不同的东西，取地址或者取值**

* <font color=blue>注意：地址的类型与数据的类型相等</font>
* <font color = blue>地址一般都是四个字节</font>
* **<font color=blue>注意指针必须初始化，否则非常危险</font>**

```
char a = 'F';
int b = 123;

char *pa = &a;
int *pd = &b;

printf("a= %c\n", *pa);
printf("b = %d\n", *pd);

*pa = 'C';
*pd = *pd+1;

printf("a= %c\n", *pa);
printf("b = %d\n", *pd);

//打印地址占字节的大小
printf("size of a = %d\n", sizeof (pa));
printf("size of b = %d\n", sizeof(pd));

// %p表示打印地址
printf("address of a = %p\n", pa);
printf("address of b = %p\n", pd);
```

 ### 3.3 指针和数组

#### 3.3.1 指向数组的指针

![image-20230302215449942](D:\笔记\笔记图片\image-20230302215449942.png)

##### 3.3.1.1 指针的运算

![image-20230302215756542](D:\笔记\笔记图片\image-20230302215756542.png)

# C++

## Lecture1 

## 1. Introduction of C++

* C++ is one more than C 

  * Very serious and powerful language 
  * C++ = C + object-oriented features (while keeping things fast) 
  * **c++ = c+面向对象的特性(同时保持速度)**
  * Very similar syntax between C, Java, C++ and C# since they all belong to the same family

* Designed with efficiency in mind 

  * By default, C++ is unmanaged and used in low-level programming 
  * 默认情况下，c++是非托管的，用于低级编程
  * Unmanaged = compiles and is then run directly on the underlying system 
  * Unmanaged =编译，然后直接在底层系统上运行
  * Managed = compiles to an intermediate level that are then run
  * Managed =编译到中间级别，然后运行该级别
  * The advantages is that (typically) the intermediate level provide memory management, such as garbage collection ◦ Most C programs are valid in C++ and can be compiled with a C++ compiler 
  * 优点是(通常)中间层提供内存管理，如垃圾收集◦大多数C程序在c++中是有效的，可以用c++编译器编译
  * But C++ does help to prevent some of the errors that are common in C
  * 但c++确实有助于防止C中常见的一些错误

  ![image-20230306091200542](D:\笔记\笔记图片\image-20230306091200542.png)

  ![image-20230306091236472](D:\笔记\笔记图片\image-20230306091236472.png)

## 2. Hello World!

![image-20230306091558144](D:\笔记\笔记图片\image-20230306091558144.png)

* 在std是命名空间的关键字，用于将一组相关的标识符封装在一个命名空间里，避免与其他库或用户定义的标识符发送冲突。

![image-20230320224421135](D:\笔记\笔记图片\image-20230320224421135.png)

* The  library provides the std::string class, with behaviour like Java 
* 标准库提供了std::string类，其行为类似于Java
  * The string can be initialised via a constructor 
  * 字符串可以通过构造函数初始化
  * The class has some built-in methods, such as size() 
  * 该类有一些内置方法，比如size()
  *  Memory allocation is done for you
  * 内存分配已为您完成

### 2.1 Output Syntax

![image-20230320224923155](D:\笔记\笔记图片\image-20230320224923155.png)



* **<font color=red>std::count 的意思是标准输入函数</font>**
* <font color=red><< 与 >>的作用是赋值，区别是前者是将后面的值赋给前面的, 后者是将前面的值赋给后面的</font>

### 2.2 Namespaces 命名空间

* **<font color=red>目的是解决全局变量和函数名称冲突的问题</font>**

* std::bla says that bla is in the standard namespace

* Std::bla表示bla在标准名称空间中

  *  Namespace is like packages in Java 
  * 命名空间就像Java中的包
  * E.g. std::cout means cout as it is defined in the std namespace and std::endl means endl as it is defined in the std namespace
  * 例如，std::cout表示在std命名空间中定义的cout, std::endl表示在std命名空间中定义的endl

  ![image-20230320230505586](D:\笔记\笔记图片\image-20230320230505586.png)

  

![image-20230320230305310](D:\笔记\笔记图片\image-20230320230305310.png)

![image-20230320231128452](D:\笔记\笔记图片\image-20230320231128452.png)





## Lecture2

## 3. C++ Classes

* Classes in C++ is an option – not a requirement
* c++中的类是一个选项，而不是必须的
* If you do not like classes, you can simply not write any in C++
  * You can still get things like nicer strings and/or nicer input in/output
  * Some small programs are written like that...
  * Take the features you like, avoid the features you do not...
* That said, there are good reasons for using classes and object-oriented design:
  * Encapsulate code - Later, design patterns will make that even stronger...
  * Easier names (variables are not global)
  * ... many other reasons

![image-20230320231953926](D:\笔记\笔记图片\image-20230320231953926.png)

![image-20230320232013186](D:\笔记\笔记图片\image-20230320232013186.png)







## 4.Acess modifies in C++

* Public: You can access these from anywhere 
* 公共:你可以在任何地方访问这些
* Private: You can only access them from this class ◦ you can also be friends with a class – that will also let you access their private variables 
* 私有:你只能访问他们从这个类◦你也可以成为一个类的朋友-这也会让你访问他们的私有变量
* Protected: You can only access them from this class, sub-classes or from friends
* 受保护:你只能从这个类，子类或从朋友访问他们

```
using namespace std;
class Animal {
private:
    int weight;
    string name;
public:
    void setWeight(int value) { weight = value; }
    int getWeight(void) { return weight; }
}; // Don’t forget the semi-colon
int main()
{
    Animal example; // Creates the object (unlike Java)
    example.setWeight(55);
    cout << example.getWeight();
}
```

![image-20230320232614152](D:\笔记\笔记图片\image-20230320232614152.png)

​                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              

## 5. Getters && Setters

* Generally we don’t want to expose internal variables to the outside world, so
* 通常我们不想把内部变量暴露给外界，所以
* we keep them private and define getters and setters
* 我们保持它们为私有，并定义getter和setter
* We do not actually want to expose getters and setters either, except for cases (like here), where we are using the class directly for data storage
* 实际上，我们也不想公开getter和setter，除非我们直接将类用于数据存储的情况(例如这里)

* <font color=red>通过Getters和Setters方法来访问类内部的变量或者函数</font>

![image-20230320232934923](D:\笔记\笔记图片\image-20230320232934923.png)

## 6. Split between .h and .cpp

* **The class definition is in .h and implementation of methods and similar in .cpp**
* **类定义在.h中，方法实现在.cpp中类似**
* It is considered bad form to do the following:
* 以下行为被认为是不礼貌的:
  * Classes and such outside namespace
  * Define longer functions in the .h file
  * Assigning variables that are not constants in a .h file
  * Using using namespace in a .h file
    * The issue with the last one is that it will spread to all files that includes the .h file

![image-20230320233451365](D:\笔记\笔记图片\image-20230320233451365.png)

### 6.1 Fixed Version 不可编辑的版本

![image-20230320235915652](D:\笔记\笔记图片\image-20230320235915652.png)

**<font color=red>就这么想想, 一个Basic文件来运行，一个.h文件用来存储类，一个.cpp文件用来存储方法</font>**

### 6.2 Constructors and Destructors 构造函数和析构函数

* Constructors in C++ behave the same as they do in Java
* c++中的构造函数与Java中的构造函数的行为相同
  * Called whenever an object is created
  * 每当创建对象时调用
  * Has no return type and must have the same name as the class
  * 没有返回类型，必须与类具有相同的名称
  * Performs any setup required by the class (such as memory allocation)
  * 执行类所需的任何设置(例如内存分配)
  * If you don’t declare a constructor then a default one will be used
  * 如果您没有声明构造函数，则将使用默认构造函数
  * If you do declare one, the default one will get removed
  * 如果你声明了一个，默认的将被删除

* **Java does not have destructors because it uses garbage collection**
* **Java没有析构函数，因为它使用垃圾收集**
  * Objects are automatically deleted when no longer in use
  * 对象在不再使用时自动删除
  * Memory is freed and tidied up automatically
  * 自动释放和清理内存
* In C++ the destructor is called whenever an object is deleted
* 在c++中，每当删除一个对象时，就会调用析构函数
  * Has the same name as the class with a tilde in front of it
  * 与前面带有波浪号的类名称相同
  * Should free up any memory and resources allocated by the constructor
  * 是否应该释放构造函数分配的内存和资源

![image-20230321000747963](D:\笔记\笔记图片\image-20230321000747963.png)

**<font color=red>注意上述的代码结构</font>**

## 7. Memory Management in C++  C++的内存管理

* Memory management is a bit easier in C++ than it is in C
* 内存管理在c++中要比在C中简单一些
  * Don’t need to worry about malloc and free
  * 不需要担心malloc和free
  * Constructor allocates enough memory for class variables
  * 构造函数为类变量分配了足够的内存
  * Destructor will free memory used by class variables
  * 析构函数将释放类变量所使用的内存
  * Local variables are deleted automatically when they go out of scope (also triggers a call to their destructor)
  * 局部变量超出作用域时自动删除(还触发对其析构函数的调用)
* Use constructors to perform set-up and allocate any extra resources
* 使用构造函数来执行设置和分配任何额外的资源
* Use destructors to perform clean-up and free all resources
* 使用析构函数执行清理并释放所有资源
  * Delete memory for permanent objects you created (see later)
  * 删除您创建的永久对象的内存(参见后面的内容)
  * Flush data buffers
  * 刷新数据缓冲区
  * Close any open files, network streams, etc.
  * 关闭所有打开的文件、网络流等。

### 7.1 Member Initialisation

* This feature was introduced in the C++11 standard
* 该特性是在c++ 11标准中引入的
* A shortcut way to initialise variables from incoming parameters without having to explicitly write assignment statements
* 一种从传入参数初始化变量的快捷方法，无需显式地编写赋值语句
* A list of initialisations is inserted before the constructor body
* 在构造函数体之前插入一个初始化列表

![image-20230321003915588](D:\笔记\笔记图片\image-20230321003915588.png)

## 8. Inheritence 继承

![image-20230321004007571](D:\笔记\笔记图片\image-20230321004007571.png)

### 8.1 多态

![image-20230321005321251](D:\笔记\笔记图片\image-20230321005321251.png)

![image-20230321005544449](D:\笔记\笔记图片\image-20230321005544449.png)

#### 8.2.1  多态的初始化Initialisation

* Memory for parent class is always initialised before the memory for child
* 父类的内存总是在子类的内存之前初始化
* The way to pass data from child to parent constructor is as follows:
* 将数据从子构造函数传递给父构造函数的方法如下:

![image-20230321005812788](D:\笔记\笔记图片\image-20230321005812788.png)

![image-20230321005851528](D:\笔记\笔记图片\image-20230321005851528.png)

### 8.2 Slicing

![image-20230321010155028](D:\笔记\笔记图片\image-20230321010155028.png)

![image-20230321010245557](D:\笔记\笔记图片\image-20230321010245557.png)

* <font color=red>子类继承了父类的属性，但同时自己也有一部分属于自己的属性</font>

![image-20230321010544397](D:\笔记\笔记图片\image-20230321010544397.png)

![image-20230321010732075](D:\笔记\笔记图片\image-20230321010732075.png)

* **<font color=red>父类不能调用子类中的属性和方法</font>**



### 8.3 The three ways to pass objects to functions 将对象传递给函数的三种方法
![image-20230321010825747](D:\笔记\笔记图片\image-20230321010825747.png)



* 按引用传递是按指针传递方法的简化
  * 参考不能被接收方法重新分配
  * 语法看起来更好，因为它使用点符号
  * 有效地传递一个指针到一个对象
  * 不复制原始对象
  * 它的内容可以通过方法改变，因此任何其他指针到同一对象将看到改变的版本

![image-20230321011149460](D:\笔记\笔记图片\image-20230321011149460.png)

![image-20230321011204354](D:\笔记\笔记图片\image-20230321011204354.png)

![image-20230321011335245](D:\笔记\笔记图片\image-20230321011335245.png)



## Lecture 3 inheritence and operator overloading

## 9.Overloading 过载

* You can overload functions in C++ like in Java
  * Two functions can have the same name if they have different parameters
  * 如果两个函数的形参不同，则它们可以具有相同的名称
  * The compiler will use the one whose parameters match the ones you pass in
  * 编译器将使用参数与传入的参数匹配的那个
    * This is picked at compile time – an example of what this means is on the next slide
    * 这是在编译时选择的——下一张幻灯片中有一个例子说明这意味着什么
  * Allows us to keep our code clean and use meaningful names
  * 允许我们保持代码干净并使用有意义的名称
* Most commonly used with constructors (but can be used with any functions)
* 最常用于构造函数(但也可以用于任何函数)
  * Construct an object differently depending on incoming parameters
  * 根据传入参数构造不同的对象
    * Remember the default constructor will no longer exist if you define your own, so include one if you need it (otherwise you must use one you wrote)
    * 请记住，如果您定义了自己的默认构造函数，那么默认构造函数将不再存在，因此如果需要的话，请包含一个默认构造函数(否则必须使用自己编写的构造函数)。

![image-20230321011816415](D:\笔记\笔记图片\image-20230321011816415.png)

### 9.1 Overview of overloading operators

![image-20230321011932263](D:\笔记\笔记图片\image-20230321011932263.png)

* C++ also allows you to overload almost any operator
* c++还允许重载几乎任何操作符
  * Make it do something completely different if you want to (not advisable!)
  * 如果你想让它做一些完全不同的事情(不可取!)
  * Usually, we overload maths and I/O operators to work with our classes
  * 通常，我们会重载数学和I/O操作符来处理类
  * To be precise, you can overload:
  * 准确地说，你可以重载:
    * There are some corner cases with the red ones though, which you might want to look into if you consider overloading those
    * 有一些红色的极端情况，如果你考虑重载它们，你可能想看看
    * Overloading the blue ones can lead to very unreadable code very fast
    * 重载蓝色部分会导致代码很快变得难以读懂

![image-20230321012516896](D:\笔记\笔记图片\image-20230321012516896.png)

![image-20230321012606188](D:\笔记\笔记图片\image-20230321012606188.png)

### 9.2 Constructor Overloading 过载的构造方法

* The class definition needs private variables for its internal data, plus a way to construct an object from incoming values

* 类定义需要内部数据的私有变量，以及从传入值构造对象的方法

  * There are two overloaded constructors
  * 有两个重载构造函数
    * Create object given values for feet and inches
    * 创建给定英尺和英寸值的对象
    * Create object given value for inches (automatic conversion to feet)
    * 创建对象的英寸值(自动转换为英尺)
  * This gives the user some flexibility in how they create Ruler objects
  * 这为用户创建Ruler对象提供了一定的灵活性

  ![image-20230321012859106](D:\笔记\笔记图片\image-20230321012859106.png)

#### 9.2.1 Constructor Implementation 构造方法的应用

* The two constructors are implemented as follows:
* 这两个构造函数的实现如下:
* We need to make sure the internal model is consistent
* 我们需要确保内部模型是一致的
  * Convert incoming inches into feet if the number is too big
  * 如果数字太大，将输入的英寸转换为英尺
    * Remember that / performs integer division (ignoring remainder)
    * And % gives us the remainder after integer division (modulus operator)

![image-20230321013025063](D:\笔记\笔记图片\image-20230321013025063.png)

![image-20230321013547940](D:\笔记\笔记图片\image-20230321013547940.png)



![image-20230321112223925](D:\笔记\笔记图片\image-20230321112223925.png)

![image-20230412163038889](D:\笔记\笔记图片\image-20230412163038889.png)



## Lecture4 Operator overloading

### 1. Unary and binary operators 一元运算符和二元运算符

* There are 3 types of operators:
* 有3种类型的操作符:
  * Prefix-unary, postfix-unary and binary
  * 前缀一元，后缀一元和二进制

![image-20230412163453956](D:\笔记\笔记图片\image-20230412163453956.png)

![image-20230412163511678](D:\笔记\笔记图片\image-20230412163511678.png)

* You just write int as the parameter – it is to distinguish from the prefix version
* 您只需将int作为形参—这是为了区别于前缀version

* **`prefix-unary` 运算符是一元运算符，它位于运算对象的前面，例如 `++x`，其中 `++` 是前置自增运算符，它将 `x` 的值增加 1，并返回新的值。**
* **`postfix-unary` 运算符也是一元运算符，它位于运算对象的后面，例如 `x++`，其中 `++` 是后置自增运算符，它将 `x` 的值增加 1，并返回旧的值。**
* **`binary` 运算符是二元运算符，它需要两个运算对象，例如 `x + y`，其中 `+` 是加法运算符，它将 `x` 和 `y` 相加，并返回结果。**

![image-20230412163749538](D:\笔记\笔记图片\image-20230412163749538.png)

#### 1.1 Binary Operators

![image-20230412165327903](D:\笔记\笔记图片\image-20230412165327903.png)

* The issue is that we have seen how to overload things, both unary and binary, from inside the class that is on the left (or right for postfix-unary)
* 问题是,我们已经看到了如何从左边的类中从左边(或者是postfix-unary)中过载的东西来过载。
* We want to overload << outside cout!
  * (More precisely, outside ostream – the class for output streams)
* The way to do so we need to define the free function (we will get back to how it can do it for Ruler – which was not defined in std – later today/next week, when we get to templates)

![image-20230412170031322](D:\笔记\笔记图片\image-20230412170031322.png)

* 解释一下，类似于java的toString方法
* ![image-20230412172253723](D:\笔记\笔记图片\image-20230412172253723.png)

![image-20230413235408390](D:\笔记\笔记图片\image-20230413235408390.png)



#### 1.2 Friendship is magic 友元

![image-20230413235447585](D:\笔记\笔记图片\image-20230413235447585.png)

* 在上面的例子里，我们发现直接在头文件中声明会出现问题，因为找不到相应重载的函数定义。友元就是为了解决这个问题出现的。
* ![image-20230413235758191](D:\笔记\笔记图片\image-20230413235758191.png)

#### 1.3 Summary about Unary and Binary

![image-20230414000006174](D:\笔记\笔记图片\image-20230414000006174.png)

![image-20230414000013463](D:\笔记\笔记图片\image-20230414000013463.png)



### 2. Templates 模板

* 函数模板：<font color=red>一个不规定函数中参数类型的特殊函数，根据实际传入的参数，编译器可以自动生成实际的函数代码</font>
* 类模板：<font color=red>在一个类模板中，某些成员或者参数的类型是未知的，同样的，在实例化时指定这些参数的类型，编译可以生成的实际代码</font>

![image-20230414000657434](D:\笔记\笔记图片\image-20230414000657434.png)

![image-20230414000729464](D:\笔记\笔记图片\image-20230414000729464.png)

#### 2.1 Problems

* As it also the case in Java and C, in C++, a method can only return 1 object
  Say you are writing a method, but want it to return 2 objects, like an animal and an integer

* 在Java和C中也是如此，在c++中，一个方法只能返回一个对象

  假设您正在编写一个方法，但希望它返回2个对象，比如动物和整数



* 1. You can make a global variable for the animal (or integer) and then return the integer (or animal)您可以为动物(或整数)创建一个全局变量，然后返回整数(或动物)
     1. This is ugly and not proper OO design 这是丑陋的，不合适的OO设计
  2. The proper way is to have an object for storing both of these, e.g正确的方法是有一个对象来存储这两个，例如

![image-20230414001029193](D:\笔记\笔记图片\image-20230414001029193.png)

* However, you might do this many times and end up with lots of such classes

* 但是，您可能多次这样做，最终会得到许多这样的类

  * Like before, this takes time to write, creates bugs and here you also have to remember the name of the variables
  * 像以前一样，这需要时间来编写，产生bug，这里你还必须记住变量的名称

* One could get around that using a common supertype and then casts or polymorphisms

* 可以使用公共超类型，然后使用类型强制转换或多态性来解决这个问题

  * The former is somewhat ugly and the latter adds bloat to the code (the former does too) – remember, this is why we need virtual
  * 前者有点丑陋，后者会增加代码的臃肿(前者也是如此)——记住，这就是我们需要virtual的原因

  ![image-20230414001356441](D:\笔记\笔记图片\image-20230414001356441.png)

  ![image-20230414001348148](D:\笔记\笔记图片\image-20230414001348148.png)



## Lecture 5 &&6 Standard template library: Containers and
iterators && stl algorithms
### 1. Overview over standard template library 标准模板库概述

* Consists of 3 main parts (+ Pair from last time as an additional part):
* 由三个主要部分组成(+配对从上次作为附加部分):
  *  Containers: standard data structures
  * 容器:标准数据结构
    * vectors, arrays, deque, set* (and multiset*), map* (and multimap*), list*, forward_list
  * Iterators: standard ways to move through the standard data structures
  * 迭代器:在标准数据结构中移动的标准方法
    * Multiple levels of them: Random access, bidirectional, forward, input = output
    * 它们的多个层次:随机访问，双向，向前，输入=输出
      * (Input and output are at the same level)
      * (输入和输出处于同一水平)
      * The first 3 data structures can use any level while set, map and list can use bidirectional and below and forward_list can only use forward and below
      * 前3个数据结构可以使用任何级别，而set、map和list可以使用双向及以下，forward_list只能使用正向及以下
* Algorithms: uses iterator(s) (usually 2 and often some method as parameters) to give their results
* 算法:使用迭代器(通常是2和一些方法作为参数)来给出结果
  * Sorting, searching, various modifying and non-modifying algorithms, numeric algorithms and min/max algorithms
  * 排序，搜索，各种修改和非修改算法，数值算法和最小/最大算法

![image-20230414151818659](D:\笔记\笔记图片\image-20230414151818659.png)

* <font color=red>在这方面，我在想container大概就是各自不同的数据结构</font>

#### 1.1 Container



##### 1.1.1 Vectors

![image-20230414151951590](D:\笔记\笔记图片\image-20230414151951590.png)

* Automatic resizing = just think of it as always having (roughly) the size of whatever you have put in and expands whenever you need it to 
* 自动调整大小=只要认为它总是(粗略地)拥有您所输入的大小，并在需要时进行扩展
* vector<int> is roughly equal to ArrayList<Integer> in Java
* vector<int>在Java中大致等于ArrayList<Integer>

![image-20230414152650456](D:\笔记\笔记图片\image-20230414152650456.png)

![image-20230414152830094](D:\笔记\笔记图片\image-20230414152830094.png)

##### 1.1.2 Multiset

![image-20230414153000097](D:\笔记\笔记图片\image-20230414153000097.png)

* Things are stored in ascending order (based on <) by default
* 默认情况下，内容以升序(基于<)存储
  * You can do it with other orderings, but it looks a bit ugly...
  * 你可以用其他订单做，但是看起来有点难看…

![image-20230414153146308](D:\笔记\笔记图片\image-20230414153146308.png)

#### 1.2 Iterators 迭代器

* An iterator is associated with a container, but the code for them looks similar between containers Iterators are objects for accessing/manipulating the data in their container
* 迭代器与容器相关联，但它们的代码在容器之间看起来很相似。**迭代器是用于访问/操作容器中的数据的对象**
  * Multiple levels of them: Random access, bidirectional, forward, input = output
  * 它们的多个层次:随机访问，双向，向前，输入=输出
    *  (Input and output are at the same level
    * 输入和输出处于同一水平

![image-20230414155532047](D:\笔记\笔记图片\image-20230414155532047.png)

* Syntax looks a little strange so we need to explain it
* 语法看起来有点奇怪，所以我们需要解释一下
  * Multiset/vector class has a member object called iterator
  * Multiset/vector类有一个名为iterator的成员对象
  * In this example, the multiset/vector template is using integers
  * 在本例中，multiset/vector模板使用的是整数
  * So the iterator will point to an integer within the multiset/vector
  * 因此迭代器将指向multiset/vector中的一个整数





* 在 C++ 中，迭代器（iterator）是一种广义指针，用于指向容器中的元素，并支持对容器进行遍历、访问和修改操作。迭代器的定义和作用如下：

  定义：迭代器是一种能够遍历容器中元素的对象，类似于指针。

  作用：

  - 提供了一种统一的访问容器中元素的方式，无需了解容器内部的数据结构和实现细节。
  - 支持对容器进行遍历、访问和修改操作，实现了对容器的抽象和封装。
  - 可以作为泛型算法的输入参数，从而实现通用的算法模板。

![image-20230414155414315](D:\笔记\笔记图片\image-20230414155414315.png)



![image-20230414160031979](D:\笔记\笔记图片\image-20230414160031979.png)

![image-20230414160141012](D:\笔记\笔记图片\image-20230414160141012.png)

![image-20230414161419448](D:\笔记\笔记图片\image-20230414161419448.png)



![image-20230414161428397](D:\笔记\笔记图片\image-20230414161428397.png)

![image-20230414162912577](D:\笔记\笔记图片\image-20230414162912577.png)

#### 1.3 STL Arrays

* You might have asked yourself why we have an array container when we already have arrays
* 您可能会问自己，既然已经有数组了，为什么还要使用数组容器 
* Two reasons:
  * We can use iterators (and standard functions, such as size, insert or erase) on them so the code will look similar to other containers
  * 我们可以对它们使用迭代器(以及标准函数，如size、insert或erase)，这样代码看起来就类似于其他容器
  * We can use algorithms (see Thursday) on them
  * 我们可以对它们使用算法

![image-20230414163327645](D:\笔记\笔记图片\image-20230414163327645.png)

* 这里的c是一个变量，而一个数组的长度不可以是变量

![image-20230414165547169](D:\笔记\笔记图片\image-20230414165547169.png)

* 解释一下这张ppt
*  `--store2.end()` 返回指向容器 `store2` 最后一个元素的迭代器
* `store2.end()` 返回指向容器 `store2` 最后一个元素后一个位置的迭代器
* These ranges are always including the start, but excluding the end
* 这些范围总是包括开始，但不包括结束

#### 1.4 Algorithm Types



![image-20230414165812839](D:\笔记\笔记图片\image-20230414165812839.png)



##### 1.4.1 Min

![image-20230414171047963](D:\笔记\笔记图片\image-20230414171047963.png)

* min:

![image-20230414171123654](D:\笔记\笔记图片\image-20230414171123654.png)

* min_element

  * 具体来说，`min_element` 用于在一个容器（比如 `vector` 或者 `array`）中寻找最小的元素。它接受三个参数：容器的起始迭代器，容器的结束迭代器和一个可选的比较函数。

  

  ![image-20230414171241187](D:\笔记\笔记图片\image-20230414171241187.png)

  

![image-20230414171331296](D:\笔记\笔记图片\image-20230414171331296.png)

![image-20230414171323561](D:\笔记\笔记图片\image-20230414171323561.png)

![image-20230414171514147](D:\笔记\笔记图片\image-20230414171514147.png)

* abs()用于求绝对值

![image-20230414171726170](D:\笔记\笔记图片\image-20230414171726170.png)

* 更换了固定的42值，可以根据需要任意替换

![image-20230414171803585](D:\笔记\笔记图片\image-20230414171803585.png)

* 但必须是一个准确的值而不是一个变量



#### 1.5 Functor（函数对象）

* Functor（函数对象）是 C++ 中的一种编程技术，它是指实现了函数调用操作符（operator()）的类对象。它可以像普通函数一样被调用，这个过程被称为函数对象的“仿函数”（function-like）行为。
* <font color=red>似乎是这么一回事。一个类在合适的加工后，可以 像一个类一样被调用</font>

![image-20230414172620558](D:\笔记\笔记图片\image-20230414172620558.png)



![image-20230414173903471](D:\笔记\笔记图片\image-20230414173903471.png)

![image-20230414173945719](D:\笔记\笔记图片\image-20230414173945719.png)





![image-20230414174013760](D:\笔记\笔记图片\image-20230414174013760.png)

![image-20230414174053608](D:\笔记\笔记图片\image-20230414174053608.png)

![image-20230414174124828](D:\笔记\笔记图片\image-20230414174124828.png)

* 这行代码的作用是去除容器 `arr` 中连续重复的元素，保留第一个。去重后的元素会在容器前面连续存放，返回值是指向去重后容器中不重复部分的最后一个元素的迭代器，可以用来确定新的结尾位置。



![image-20230414174909206](D:\笔记\笔记图片\image-20230414174909206.png)































