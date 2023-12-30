P32 2-插入单行 | Inserting a Row





格式（直接上实例了）

**Insert Into customers 
Values (
	****default,**
    **'John',**
    **'Smith',**
    **'1990-01-01',**
    **default,**
    **'adress',**
    **'city',**
    **'CA',**
    **default**
    )



第二种方法（省去了default和null的填写）

**In**sert Into customers (**
	**first_name,**
    **last_name,**
    **birth_date,**
    **address,**
    **city,**
    **state)**
**Values (**
    **'John',**
    **'Smith',**
    **'1990-01-01',**
    **'adress',**
    **'city',**
    'CA')**