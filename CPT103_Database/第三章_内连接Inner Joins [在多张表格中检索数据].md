第三章_内连接|Inner Joins [在多张表格中检索数据]



一，格式

Join + 表名 （+ on + 不同表中相同的列名）

【join products p on oi.product_id = p.product_id】

**use sql_store;**
**select order_id, oi.product_id, quantity, oi.unit_price**
**from order_items oi**
**join products p on oi.product_id=p.product_id**

*在表名后可以加缩写，但是之后都必须用缩写表示。

*不同数据库之间的表只要加上前缀就好。





二，跨数据库连接

1.定义：如字面意思般，需要使用两个在不同数据库下的表。

2.格式：数据库名.表名

[**select ***
**from order_items oi**
**join sql_inventory.products p**
	**on oi.product_id = p.product_id**]



三，自连接

1.定义：将一张表与它自己连接。





四、多表连接|Joining Multiple Tables

**use sql_invoicing;**

**select p.payment_id, p.client_id, p.invoice_id, p.date, p.amount,  pm.name**
**from payments	p**
**join clients	c**
	**on p.client_id = c.client_id**
**join payment_methods	pm**
	**on pm.payment_method_id = p.payment_method**



五. 复合连接条件|Compound Join Condiation

就是当主键是复合主键时，如何连接两个表。或者说用更加多个的条件去连接两个表。

**use sql_store;**

**select ***
**from order_items oi**
**join order_item_notes oin**
	**on oi.order_id = oin.order_id**
    **and oi.product_id = oin.product_id**

 //

​	1.主键的含义：指的是一个列或多列的组合，其值能唯一地标识表中的每一行，通过它可强制表的实体完整性。

​	2.主键主要作用：

（1）、保证实体的完整性。

（2）、加快数据库的操作速度。

（3）、在表中添加新记录时，DBMS会自动检查新记录的主键值，不允许该值与其他记录的主键值重复。

（4）、DBMS自动按主键值的顺序显示表中的记录；如果没有定义主键，则按输入记录的顺序显示表中的记录。

//
