P24 7-外连接|Outer Joins



​		外连接分为左连接和右连接

左连接（left join）

：不管是否满足条件，返回全部的值。

右连接（right join）

：只会返回满足on条件的值。

**use sql_store;**
**select** 
		**c.customer_id,**
        **c.first_name,**
        **o.order_id**
        
**from customers c**
***left/right* join orders o**
	**on o.customer_id = c.customer_id**
**order by c.customer_id**

进行进一步的解释就是

left会返回左边表的所有值，right会返回右边表的所有值。





注意：

内连接：指连接结果仅包含符合连接条件的行，参与连接的两个表都应该符合连接条件。



外连接：连接结果不仅包含符合连接条件的，也包含不符合条件的行。左，右，全就是包含左表或右表或左右两表中未匹配的数据。





*连接的对象取决于条件，并不一定都是和from后的表相连。