杂记：关于IO流



定义：当不同的介质之间有数据交互的时候，JAVA就使用流来实现。 数据源可以是文件，还可以是数据库，网络甚至是其他的程序。 比如读取文件的数据到程序中，站在程序的角度来看，就叫做输入流。 输入流： InputStream 输出流：OutputStream

InputStream and Outsteam 即为IO，流即为数据，故全称IO流。**（感觉就是给数据的读写换了个高大上的名字）**



1.IO流的四点明确

**（1）：明确要操作的数据是数据源还是数据目的(要读还是要写)**

InputSteam	Reader  数据源

OutputStream	Writer	数据目的

**（2）：明确1要操作的设备上的数据是字节还是文本。**

（3）**明确数据所在的具体设备**

源设备：

硬盘：文件 `File`开头

内存：数组，字符串

键盘：`System.in`

网络：`Socket`



对应目的设备：

硬盘：文件 `File`开头

内存：数组，字符串

屏幕：`System.out`

网络：`Socket`



（4）明确是否需要额外功能

需要转换—— 转换流 InputStreamReader 、OutputStreamWriter

**（InputStreamReader用于将字节输入流转换为字符输入流，OutputStreamWriter用于将字节输出流转换为字符输出流。）*



需要高效—— 缓冲流Bufferedxxx

（分为输入\输出和字节\字符的 四种方式，如：BufferedInputStream）



多个源—— 序列流 SequenceInputStream



对象序列化—— ObjectInputStream、ObjectOutputStream



保证数据的输出形式—— 打印流PrintStream 、Printwriter



操作基本数据，保证字节原样性——DataOutputStream，DataInputStream



![image-20211204215907412](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20211204215907412.png)













