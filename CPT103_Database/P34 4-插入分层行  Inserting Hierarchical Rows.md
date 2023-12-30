P34 4-插入分层行 | Inserting Hierarchical Rows





数据库中存在一个表中的一条数据可以对应另一表中的多条数据，类似于一笔订单可以有多个项目，也就是表之间的亲子关系，插入分层行也就是在亲子关系表单中插入数据。例如

INSERT INTO orders (customer_id, order_date, status)

VALUES (1, '2020-01-01', 1);

INSERT INTO order_items

VALUES(LAST_INSERT_ID(), 1, 1, 2.95)

(LAST_INSERT_ID(), 2, 1, 3.95)

\\ 为了获取新插入的列的id来在子表中插入数据，使用函数**LAST_INSERT_ID()**，就能获得刚刚插入的新列的id。

上面的例子展示了如何在母表中插入数据，又在对应子表中插入多行数据





*其实就是因为有些时候母表中的一行对应子表中的多行，（比如订单10同时购买了产品1和9）子表不能用AI递增来直接增加数量，需要接受目标中增加的订单11，用11来创建新的行的order_id。*

**Insert Into orders (**
					**customer_id,** 
                    **order_date,** 
                    **status**
                    **)**
**Values (1, '2019-01-02', 1)**

**Insert Into order_items**
**Values (Last_Insert_ID(), 1, 1, 2.95),**
	   **(Last_Insert_ID(), 2, 1, 3.98)**

上述情况就是新的订单买了两个物品，所以只能这样写。