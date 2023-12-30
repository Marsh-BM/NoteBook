P29 12- 交叉连接 | Cross Joins



 用法：

使用交叉连接结合或者连接第一个表的每条记录和第二个表的每条记录。



一般使用情况：

你有一件产品，他有着红黄蓝三种颜色，和大中小三种型号，你想要得到所有产品的类型组合，使用交叉连接。



显示语法：

**Select ***
**From customers 	c**
**Cross Join products	p**



隐式语法：

**Select ***
**From customers 	c, orders o**

二者查询结果相同。