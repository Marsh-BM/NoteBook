CPT111 IO流

//</font size=3 color="red">字体颜色为红色，大小为3</font>

**<font size=5 color="blue">File reading</font>**

​	**Paths** - a Class that contains static methods.

​	**Path** - an object that is used to navigate to a particular region.

​				*Created from the Paths class

​	**Files** - a class taht consists exclusively of static methods.

​				*operates on files, directories, or other types of files.

​	**BufferedReader(缓冲流)**- 

​				*Reads text from a character-input stream, buffering characters so as to provide for the efficient reading of characters, arrays, and lines. 

​				*Buffered, so stored in memory.

​			

​	**<font size=5 color="blue">File Reading - Opening a File</font>**![image-20211216220644936](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20211216220644936.png)



**<font size=5 color="blue">File Reading - Reading Content</font>**

![image-20211216220940886](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20211216220940886.png)

​	**Method: 	readLine(): a method of buffered reader to read the content and reads one line of file.**



**<font size=5 color="blue">File Reading - Close File</font>**

![image-20211216221155167](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20211216221155167.png)



**<font size=5 color="blue">File Reading - Exceptions</font>**

![image-20211216221302910](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20211216221302910.png)

可以尝试用try-catch-finally的方法或者直接抛出。



**<font size=5 color="blue">Paths-Absolute and Relative</font>**

***RealPath**

一种真正的绝对路径。并不是简单的将工作路径和相对路径相加，而是公正的，只要表达的是同一路径，realPath都是一样的。

对象名.getRealPath

**Absolute**

Assume that a base path is E:\home\ 

● A relative path: “Documents\Test.txt” 

获得绝对路径的方法：

对象名.getAbsolutePath();





**Relative**

 Assume that a base path is E:\home\ 

● A relative path: “Documents\Test.txt” 

**当你在java中创建文件而没有指定绝对路径时，文件将相对于您的工作路径被创建。

获取相对路径的方法：

对象名.getPath();



**<font size=5 color="blue">BufferedWriter - options</font>**

在函数： BufferedWriter writer = Files.newBufferedWriter(Path); 存在时，我们对其添加一些后缀。

例如：

![image-20211216224354330](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20211216224354330.png)

![image-20211216224451479](C:\Users\白木-泽\AppData\Roaming\Typora\typora-user-images\image-20211216224451479.png)









