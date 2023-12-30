P41 1- 聚合函数 | Aggregate Function [汇总数据]



1.一些常用的聚合函数类型：

MAX()

MIN()

AVG()		平均值

SUM()		合计数

COUNT()	

​			订单数（数据有几条），该聚合函数不会返回空值。可以使用Count（*）来确保返回每一行的值。



*1.注意上述聚合函数的取值范围是在限制条件之下的值，而并非整个表。

  2.在默认情况下，这些所有的值都会取重复值。如果想要去除唯一值，那么就要加入Distinct语句。

​	**eg： Count(Distinct client_id) As total_records**

