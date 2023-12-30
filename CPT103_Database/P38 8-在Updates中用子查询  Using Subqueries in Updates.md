P38 8-在Updates中用子查询 | Using Subqueries in Updates



*：子查询是在另一段SQL语句中的选择语句。

Mysql会优先执行（）内的语句





**Use sql_invoicing;**

**Update invoices**
**Set**
	**payment_total = invoice_total * 0.5,** 
    **payment_date = due_date**
**Where invoice_id In**
					**(Select client_id**
					**From clients**
					**Where state In ('CA', 'NY'))**

Exercise：

**Use sql_store;**

**Update customers**
**Set**
	**comments = 'Gold Customer'**
**Where customer_id In**
					**(Select customer_id**
					**From customers**
					**Where points > 3000)**

