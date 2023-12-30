P35 5-创建表复制 | Creating a Copy of a Table



方法一：

**Create Table order_archived As**
**Select * From orders**		-- 子查询

利用这种方法可以创造出一个与orders相同的表，但是新创造的表没有主键且没有勾选AI，无法自己递增。





方法二：

**Use sql_store;**
**Insert Intoorder_archived**
**Select ***
**From orders**
**Where order_date < '2019-01-01'**

这种方法可以避免方法一出现的问题，但是相对来说语法更加复杂，而且可以指定复制的范**围。但这个的前提是先创造一个表。**



 **Use sql_invoicing;**
 **Create Table invoices_archived**
 **Select** 
	**i.invoice_id,**
    **i.number,**
    **c.name as client,**
    **i.invoice_total,**
    **i.payment_total,**
    **i.invoice_date,**
    **i.payment_date,**
    **i.due_date**
 **From invoices	i**
 **Join clients	c**
	**Using(client_id)**
 **Where payment_total > 0**
 **-- == Where payment_date Is Not Null**