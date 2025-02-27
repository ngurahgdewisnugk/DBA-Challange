# Challenge : Query Data
Image : 

![image](https://github.com/user-attachments/assets/502fcd65-f8fc-4620-9b87-f6d42ebd830f)

Text : 
```
/*
Answer a few questions about the data stored in the Two Trees database:

1. Product sizes are in US fluid ounces, What are the sizes in milliliters? 1 ounce = 29.57353 milliliters

2. How many different product SKUs are available in each size?

3. What is the highest priced product in the cosmetics product line?
*/
```

## Answer 
```
--Answer 1 ounce to milliliters (correct)
SELECT p.ProductName "Product Name",
	p.Size "Size (Ounces)",
    p.Size * 29.57353"Size (milliliters)"
FROM products.products p
    JOIN products.categories c
        ON p.CategoryID = c.CategoryID
;
``` 

**Result** : 

![image](https://github.com/user-attachments/assets/b793ef55-c140-49ef-9b07-8b8fb743901a)

```
--Answer 2: how many products are in each size 
SELECT
	p.Size AS "SKU SIZE",
    COUNT(p.SKU) AS "Count of SKU Size"
FROM products.products p  
GROUP BY p.Size 
;
```

**Result** :

![image](https://github.com/user-attachments/assets/9bca107a-87d3-473d-871c-c39dbc3bc7fd)

```
--Answer 3 Highest product in comestic productline
SELECT p.ProductName, p.SKU, p.Price, c.ProductLine as "ProductLine"
FROM products.products p 
	 JOIN products.categories c
	 ON p.CategoryID = c.CategoryID 
WHERE p.Price =
		(select MAX(p1.Price)
		 from products.products p1 
		 where p1.CategoryID = 3);
;
```

**Result** :

![image](https://github.com/user-attachments/assets/f6bf67d5-7c47-4c18-a621-074bb5ee4ca6)

# Code Challenge : Query Summary Statistics 
![image](https://github.com/user-attachments/assets/c3adb0b9-3b82-4be0-8e9f-6b5cbc65e02d)

![image](https://github.com/user-attachments/assets/907e325d-46a8-41e3-81a2-54065f498538)

![image](https://github.com/user-attachments/assets/bb743ea2-8d25-4bc2-b285-5268a71544ad)

## Answer : 
```
-- SQL request(s)‌‌‌‌‌‌‌‌‌‌‌‌‌‌ below 
SELECT 
Genre, 
count(*) as Total_Tracks, 
sum(PLAYCOUNT) as Total_Plays, 
avg(PLAYCOUNT) as Average_Plays 
FROM MusicTracks 
WHERE ReleaseDate > '2021-01-01' 
GROUP BY Genre 
HAVING SUM(PLAYCOUNT) > 500 
ORDER BY sum(playcount) desc 
;
```

## Result 
```
Correct output
4 rows
----------------------------------------------------------
| GENRE     | TOTAL_TRACKS | TOTAL_PLAYS | AVERAGE_PLAYS |
----------------------------------------------------------
| Pop       | 6            | 1265        | 210           |
| EDM       | 4            | 1115        | 278           |
| Synthwave | 6            | 965         | 160           |
| Rock      | 4            | 545         | 136           |
----------------------------------------------------------
```
