P42 2-GROUP BY子句 | The GROUP BY Clause





​	Group By最主要的作用是分组！ ！！！

在一些数据库里，如：得出每日的交易额。

每天的每一笔订单储存在库里，用日期进行分组，并将每日的费用储存进去，从而得到答案。  如果有两个或多个列来进行分组，就相当于把这两个列进行排列组合来得出所有的情况。

* Group By 不可以用Desc表现降序。

单列分组

​	

**Use sql_invoicing;**

**Select**
	**client_id,**
	**Sum(invoice_total) As total_sales**
**From invoices**
**Where invoice_date > '2019-07-01'** 
**Group By client_id**
**Order BY invoice_total Desc**

