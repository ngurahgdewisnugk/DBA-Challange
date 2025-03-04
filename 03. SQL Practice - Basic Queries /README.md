# What Should You Know
## Relation Dabatase Schema
![image](https://github.com/user-attachments/assets/a628b33c-4efc-46ac-9b1a-c91438f4d330)

# Code Challanges
## Code Challange: Get Sorted data from a Table
![image](https://github.com/user-attachments/assets/938b9408-4c0e-4651-b929-4fd5aca33ed8)
![image](https://github.com/user-attachments/assets/c2806f66-ec51-4b57-b516-d19a5b2dbaf7)
![image](https://github.com/user-attachments/assets/73be85a4-6478-474c-9795-cfd1e077b82d)
![image](https://github.com/user-attachments/assets/805ad042-f1dd-474c-b4c6-d0ad096f4cca)

### Queries :
```
-- SQL request(s)​​​​​​‌‌​​​‌​‌‌‌‌​​​​​‌‌‌‌​​​‌‌ below
SELECT firstname, lastname, email
FROM Customers order by lastname, firstname asc;
```

## Code Challange: Get Sorted data from a Table
![image](https://github.com/user-attachments/assets/2105c82a-cd57-4949-b6aa-5627270e2ec9)
![image](https://github.com/user-attachments/assets/364d0356-d13c-477c-b1bb-87eaa688aaab)
![image](https://github.com/user-attachments/assets/1d5f2ba3-cb6a-449f-8bb9-0740b68f0b7d)

### Queries :
```
-- SQL request(s)​​​​​​‌‌​​​‌​‌‌‌‌​​​​‌​​‌‌​​​‌​ below
SELECT top 2 r.date , r.PartySize, c.FirstName, c.LastName, c.Email 
FROM Reservations r 
inner join Customers c on r.CustomerID = c.CustomerID   
order by Date desc;
```

### Result : 
![image](https://github.com/user-attachments/assets/4ee48c15-4171-45b7-8ee2-a309b48dd686)

## Code Challange: Retrieve data filtered on a range
![image](https://github.com/user-attachments/assets/ca4abec2-2015-47e3-bd6b-b9b79bc6bd94)
![image](https://github.com/user-attachments/assets/a005b2ce-5303-4396-a09d-f18933045a3c)
![image](https://github.com/user-attachments/assets/bbbe8605-f566-492f-9acf-4689091ec73c)
![image](https://github.com/user-attachments/assets/e2ba5a6b-a567-4136-afd6-22715eb7a315)

### Queries : 
```
-- SQL request(s)​​​​​​‌‌​​​‌​‌‌‌‌​​​‌​​​​​‌​​‌‌ below
SELECT DishID, Name, Price
FROM Dishes
where price >= 8.00 and price <= 9.00
order by name asc;
```

### Result :
![image](https://github.com/user-attachments/assets/1fba878f-f9de-4232-b7b4-887e9ae13b58)

## Code Challange: Retrieve aggregated data
![image](https://github.com/user-attachments/assets/08edf2b8-c2c3-43d1-afb8-77f65f372b05)
![image](https://github.com/user-attachments/assets/bd5abb8c-945c-4cbf-acd8-0c8ff05130c9)
![image](https://github.com/user-attachments/assets/6dc079f8-d0c3-4820-bdde-621ae72af639)

### Queries : 
```
-- SQL request(s)​​​​​​‌‌​​​‌​‌‌‌‌​​​‌​​‌‌​‌​‌​‌ below
select top 3 c.CustomerID, c.FirstName, c.LastName, count(O.CustomerID) as CustomerOrderCount
from Customers c join Orders o on C.CustomerID = o.CustomerID
group by c.CustomerID, c.FirstName, c.LastName
order by count(O.CustomerID) desc;
```

### Result : 
![image](https://github.com/user-attachments/assets/c1c02ff2-219a-4e91-8e4f-ac3d92fa283e)

## Code Challange: Filter data using a string pattern
![image](https://github.com/user-attachments/assets/e85e331f-e357-4f28-82ca-7ace7d2b77c3)
![image](https://github.com/user-attachments/assets/90e08597-18a3-41cf-a0ab-a13adde92f3f)
![image](https://github.com/user-attachments/assets/7819f8b0-8fcb-4939-950e-96ae7ffc99cd)

### Queries : 
```
-- SQL request(s)​​​​​​‌‌​​​‌​‌‌‌‌​​​‌​‌​‌‌‌‌​‌​ below
SELECT FirstName, LastName, City 
FROM Customers
WHERE City like 'R%'
ORDER BY City;
```

### Result : 
![image](https://github.com/user-attachments/assets/2d12e79c-91fe-41e1-bad7-f5d7e806ac2b)

## Code Challange: Find the most expensive restaurant order
![image](https://github.com/user-attachments/assets/a36e9a6d-424d-409a-8941-974c9dfd1607)
![image](https://github.com/user-attachments/assets/96a5fbfa-770e-4fb1-97c5-8cb83847434e)
![image](https://github.com/user-attachments/assets/6fefb5eb-11de-4ee2-a8a6-72c4dec3c27f)
![image](https://github.com/user-attachments/assets/43ced23f-8740-4896-b242-118865b8bb95)

### Queries : 
```
-- SQL request(s)​​​​​​‌‌​​​‌​‌‌‌‌​​​‌​‌‌‌​​​​​​ below
SELECT top 1 o.orderID, c.FirstName, c.LastName, sum(d.price) as ordertotal
FROM Orders o join OrdersDishes od on o.OrderID = od.OrderID
join Dishes d on d.DishID = od.DishID
join Customers c on o.CustomerID = c.CustomerID
group by o.orderID
order by ordertotal desc;
```

### Result : 
![image](https://github.com/user-attachments/assets/695d1b7f-a446-4699-8505-13b49cd58bde)

## Code Challange: Find the average of all restaurant orders
![image](https://github.com/user-attachments/assets/1f1ee6e9-b667-43d8-92ef-621b2ce54a81)
![image](https://github.com/user-attachments/assets/dafce2f3-ede8-42f6-bda7-1c42991b0875)
![image](https://github.com/user-attachments/assets/da57d2c6-2322-4e34-9845-9d28f567e1bb)

### Queries : 
```
-- SQL request(s)​​​​​​‌‌​​​‌​‌‌‌‌‌​‌‌​​‌‌​‌​‌​‌ below
SELECT sum(d.price) / count(distinct o.OrderID) as orderaverage 
FROM Dishes d join OrdersDishes od on d.DishID = od.DishID
join orders o on o.OrderID = od.OrderID;

/*I solved this without needing a subquery. I joined the ordersdishes table, and summed prices using order id as a base. and then after that I divided the sum by count(distinct order id).

SELECT sum(Price) / count(distinct orders.orderid)
FROM Dishes
inner join ordersdishes on Dishes.DISHID = ordersdishes.DISHID
inner join orders on ordersdishes.orderid = orders.ORDERID
*/
```

### Result : 
![image](https://github.com/user-attachments/assets/89562e64-e690-4386-bde4-e35fa4409bf4)
