P46 2- 子查询 | Subqueries



Where unit_price > (
	Select unit_price
    From products
    Where product_id = 3
)



在子查询中，会优先对括号内的进行查询，之后再对外部条件进行筛选。