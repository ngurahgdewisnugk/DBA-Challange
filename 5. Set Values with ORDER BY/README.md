# Code Challange: Write A SQL SELECT query 
![image](https://github.com/user-attachments/assets/46d6a723-e47d-488c-a657-c96c24913b34)
![image](https://github.com/user-attachments/assets/7f178bea-7d61-439a-aec6-dbd783ed31bd)

## Answer : 
```
select top 3 r.recipeid, r.recipename, i.ingredientname, r.preptime 
from cooking.recipes r join cooking.ingredients i
on r.PRIMARYINGREDIENT = i.INGREDIENTID
where i.ingredientid = 2
order by r.preptime asc;
```

## Result : 
```
Correct output
3 rows
-------------------------------------------------------------------
| RECIPEID | RECIPENAME               | INGREDIENTNAME | PREPTIME |
-------------------------------------------------------------------
| 12       | Grilled Chicken Sandwich | Chicken        | 20       |
| 7        | Chicken Caesar Salad     | Chicken        | 20       |
| 22       | Chicken Stir Fry         | Chicken        | 25       |
-------------------------------------------------------------------
```
