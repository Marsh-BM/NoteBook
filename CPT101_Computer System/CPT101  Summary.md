# CPT101_Computer Systems



## Lecture1

## Lecture2

## Lecture3

Compilers(编译器)

translating HLL instructions into machine code (sequence of instructions) before the code can be run on the machine.

Assemblers(组译器，汇编程序)

translating mnemonic form of machine instructions (like MOV, ADD, etc) into their binary codes.

Interpreters(解释器)

translating HLL instructions into machine code on-the-fly (while the program is running).

## **lecture4**

### Data, Information and Knowledge

Data:  raw facts, fifigures, measurements.

(数据可以是图形，数字等)

Information: Data organized into useful representation

（有逻辑的将数据排列。）

Knowledge: Application of reasoned analysis of information

(推理分析应用信息)

‘Data are in increasing order’, ‘data can be derived based of Fibonacci 

sequencing’, etc

### **Information entropy（信息熵）**

解决了对信息的量化度量（Measurement of Information）问题。

### Data codes — numeric and character

一般我们需要将如图像，代码等数据转化为二进制储存到电脑，再让电脑将二进制重新转化为代码。

### **Bit**

A bit is the most basic unit of information possible; it contains the information necessary to  distinguish two alternatives (1 or 0, yes or no, etc.

### Binary number system（二进制）

![微信图片_20220107161127](C:\Users\白木-泽\Desktop\屏幕截图\微信图片_20220107161127.jpg)

### Binary vs. Decimal notation

Decimal notation is more compact than binary, generally uses less digit to represent the same number.

Decimal is more convenient for humans.

Binary is more “convenient” for computers due to two-state, ON/OF technology employed

### Hexadecimal notation(16进制)

Hexadecimal notation uses 16 as a base.

Convenient shorthand for binary numbers.

Every hexadecimal digit exactly represents 4 binary bits.

![微信图片_20220107163643](C:\Users\白木-泽\Desktop\屏幕截图\微信图片_20220107163643.jpg)

![image-20220107163723265](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220107163723265.png)



### Octal notation(八进制)

### ASCII制

![image-20220107164120175](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220107164120175.png)

![image-20220107164139988](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220107164139988.png)



## **Lecture5**

### Alphanumeric codes（字母数字代码）

  **ASCII code** (American Standard Code for Information Interchange)  

(7bit code) and its extensions (8-bit code). (Well-established)

  **EBCDIC code** (Extended Binary Coded Decimal Interchange Code) 

8-bit code. (IBM mainframe computer)

  **Unicode**

Recent 160bit standard (Up to characters can be encoded)

#### Limitation of ASCII code

The limitations of the well-established 8 bit ASCII codes.

Too limited for the display requirements of modern Windows-based word

processors.

（只有7位，难以满足需求，即使扩充到8位也一样）

![image-20220107172742809](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220107172742809.png)

#### Unicode

有超过65000个词汇。

Standard includes the European alphabetic scripts, Middle Eastern right-to-left scripts, 

and scripts of Asia, Africa and America, ideographic characters of China, Japan, etc.

Standard includes punctuation marks, mathematical symbols, geometric shapes, etc.

It is ok to use Unicode in Java programming

*To show Chinese characters in a java program unicode must be used*

### Representation of numbers

#### Integer

![image-20220107171922987](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220107171922987.png)

#### Real Number

The most widely-used standard for flfloating-point computation.

Defifines format for representing flfloating-point numbers, special values, and a set of  flfloating-point operations that operates on these values.

![image-20220107172337947](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220107172337947.png)

## Lecture6_Operating Systems

![image-20220107191900634](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220107191900634.png)

### Functions

Functions of OS — to interpret and carry out commands issued by: Users of the computer or, Application programs running on the computer.

### Purpose

![image-20220107181934625](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220107181934625.png)

### Onion Ring Model（洋葱圈模型）

![image-20220107182248767](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220107182248767.png)

### Modern Operating Systems

Allow for the simultaneous processing of multiple programs.

![image-20220107192611927](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220107192611927.png)

DOS ( Disk Operating System )磁盘操作系统

![image-20220107183227602](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220107183227602.png)

Windows

![image-20220107183328994](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220107183328994.png)

### Interaction with operating system

![image-20220107190736962](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220107190736962.png)

### Simplifified picture of OS services

![image-20220107191204274](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220107191204274.png)

### Computer Networks

Computer network is an interconnected collection of autonomous computers to facilitate fast information exchange.

#### Computer Networks purpose

![image-20220107191617282](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220107191617282.png)

![image-20220107192716917](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220107192716917.png)



## Lecture7

### The von Neumann model

![image-20220107222034744](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220107222034744.png)



### The principal components of a computer(电脑的组成)

![image-20220107222158128](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220107222158128.png)

### Mother Board（主板）

CPU, Main memory, and input-output units.

### Processor(处理器)

![image-20220107222728816](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220107222728816.png)

### Registers(寄存器)

![image-20220107222848677](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220107222848677.png)

### Coprocessors: Assistants to the CPU（协处理器）

Coprocessors: microprocessors performing specialized functions that CPU cannot perform or cannot perform as well and as quickly Math, Graphics.

(用来处理CPU无法处理或者处理的不是这么好的微处理器)

### Board and Chips

![image-20220107224918008](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220107224918008.png)



### Bus(总线)

An alternative scheme is point-to point connection

The number of pathways needed to link even possible pair of *n* units *n*(*n* − 1)/2

Each pathway will still require a full-width data highway.

Could be 32 datelines, an

d say 6 control lines/.

The result will be a huge number of wires.

The number of wires required for a bus is much smaller than that for point-to-point connections.

However, a bus can only transfer one item at a time, like a railway line.

Which leads to limit of performance — Bus Bottleneck

It cannot be solved by simply increasing the speed of a processor.

### Registers（寄存器）

![image-20220108003137002](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20220108003137002.png)



## Lecture8















