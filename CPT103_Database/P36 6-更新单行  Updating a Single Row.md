P36 6-更新单行 | Updating a Single Row



一，实例1：

**Use sql_invoicing;**

**Update invoices**
**Set payment_total = 10, payment_date = '2019-03-01'		-- 设置修改数值**
**Where invoice_id = 1		-- 设置修改位置**
    

​	实例2：

**Update invoices****
**Set** 
	**payment_total = invoice_total * 0.5,** 
    **payment_date = due_date**
**Where invoice_id =3**** 

