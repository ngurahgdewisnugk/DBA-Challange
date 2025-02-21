# Challenge : Create a Table 
![image](https://github.com/user-attachments/assets/60df3e6a-54ec-4be7-9f2a-1595e5ac10af)

## Answer
1. Connect to Database KinetEco with **Dbeaver**
   ![image](https://github.com/user-attachments/assets/69f2856e-332a-497a-b11b-f6c2088db912)
2. Open new SQL Script
   ![image](https://github.com/user-attachments/assets/7a2f0d85-6d10-44d7-a8ee-71fbc14d804a)
3. Make A query create schema and table for Database **KinetEco**.
   - Schema
     ```
     CREATE SCHEMA HumanResources;	
     ```
     ![image](https://github.com/user-attachments/assets/dd92dfcf-aadc-46c7-806e-1c18affa69d0)
   - Table
     ```
     CREATE TABLE HumanResources.Employees (
		EmployeeID INT NOT NULL PRIMARY KEY,
		FirstName CHAR(50) NOT NULL,
		LastName CHAR(50) NOT NULL,
		Department CHAR(50) NOT NULL,
		HireDate DATE NOT NULL
		);
     ```
     ![image](https://github.com/user-attachments/assets/cc531a25-73a1-4b52-a361-0791d0238fa5)

# Code Challenge : Tables and Data Type  
![image](https://github.com/user-attachments/assets/69a79cf4-a45d-48c4-94b1-448c852b6617)
![image](https://github.com/user-attachments/assets/0f88b9fc-ae3c-4b90-9d91-c474bc771de5)
![image](https://github.com/user-attachments/assets/1a18f858-fdea-4334-a021-8aa1871b8686)

## Answer 
```
-- SQL request(s)‌‌‌‌‌‌‌‌‌‌‌‌‌‌‌‌ below 
-- Create your schema and table here
CREATE SCHEMA Pets; 
CREATE TABLE Pets.Grooming ( 
GroomingID INT NOT NULL PRIMARY KEY, 
PetName CHAR(50) NOT NULL, 
LastGroomingDate DATE NOT NULL, 
GroomingService CHAR(50) NOT NULL, 
NextAppointmentDate DATE NOT NULL ); 
------------------------------ 
-- Do not edit below this line 
-- Include this insert and select statement in your final solution to test the table you've created above. 
INSERT INTO Pets.Grooming (GroomingID, PetName, LastGroomingDate, GroomingService, NextAppointmentDate) VALUES 
(1, 'Buddy', '2023-06-10', 'Full Groom', '2024-08-10'), 
(2, 'Whiskers', '2023-07-01', 'Nail Trim', '2024-09-01'), 
(3, 'Max', '2023-06-15', 'Bath and Brush', '2024-08-15'), 
(4, 'Bella', '2023-07-05', 'Ear Cleaning', '2024-09-05'), 
(5, 'Luna', '2023-07-10', 'Nail Trim', '2024-08-10'); 

SELECT * FROM Pets.Grooming;
```
## Result
![image](https://github.com/user-attachments/assets/e8498db1-9148-46da-844c-85cc83571b17)
