P30 13- 联合 | Unions



作用：合并两段查询的数据。可以是同一张表，也可以是不同的表。但是两次返回值的列数必须相同。然后列名由第一段决定。



语法：

Select 
	order_id,
    order_date,
    'Archived' As status
From orders
Where order_date >= '2019-01-01'
**Union**
Select 
	order_id,
    order_date,
    'Archived' As status
From orders
Where order_date < '2019-01-01'



*Order by 放在最后。

