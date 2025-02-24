# Challenge : Add data to a table 
![image](https://github.com/user-attachments/assets/35a569c6-3a6c-4adf-96ba-8c671988e067)

# Answer
## Add New Employees to KinetEco Database 
```
--- add three new employees
INSERT INTO HumanResources.Employees 
	(EmployeeID, FirstName, LastName, Department,HireDate)
VALUES
	(202501, 'Ni Kadek', 'Ajeng Hardinityas', 'Medical', '20250224'),
	(202502, 'Ngurah Gede', 'Wisnu Gudakesa','IT', '20250225'),
	(202503, 'Putu' , 'Wibowo' ,'Call Center', '20250226')
;
```
**Result** :

![image](https://github.com/user-attachments/assets/3d193609-6ece-44c5-935a-539e363cb208)

## Promoted to New Department for `Putu Wibowo`
```
--- Modify an employee's department for Putu Wibowo
UPDATE HumanResources.Employees 
SET Department = 'Human Resource'
WHERE EmployeeID = 202503;
```
**Result** :

![image](https://github.com/user-attachments/assets/deedbb31-b272-465f-9d60-539548dff858)

## Retired Kadek Ajeng Employee from KinetEco
```
--- Remove an employee's record
DELETE FROM HumanResources.Employees 
WHERE EmployeeID = 202501;
```
**Result** : 

![image](https://github.com/user-attachments/assets/37fd3f46-28fb-4c01-90aa-49f99666bc40)

# Code Challenge : Correct recorded information 
![image](https://github.com/user-attachments/assets/f9b0f718-dac8-4309-97ec-20dfc698d1e9)
![image](https://github.com/user-attachments/assets/f6dd3e8d-6c81-431b-9d03-f09a50b84c81)
![image](https://github.com/user-attachments/assets/cf2162c5-8fd6-4902-acc2-6ae09f8dec88)

## Answer 
```
-- SQL request(s)‌‌‌‌‌‌‌‌‌‌‌‌‌ below
-- Write your SQL code here
INSERT INTO BookReadingLog
    (BookID, BookTitle, Author, Genre, Rating, IsCompleted, DateStarted, DateCompleted)
VALUES
    (11, 'The Crimson Moon', 'Charlie Woods', 'Fantasy', 8, false, '2024-08-01', null)
;

UPDATE BookReadingLog 
SET DateStarted = '2024-07-01', DateCompleted = '2024-07-15'
Where BookTitle = 'Echoes of the Past';

DELETE FROM BookReadingLog 
Where BookTitle = 'Beneath the Waves';

------------------------------
-- Do not edit below this line
-- Include this select statement in your final solution to verify the changes made above.

SELECT * FROM BookReadingLog;
```

## Result 
```
Correct output
10 rows
----------------------------------------------------------------------------------------------------------------------------
| BOOKID | BOOKTITLE             | AUTHOR        | GENRE              | RATING | ISCOMPLETED | DATESTARTED | DATECOMPLETED |
----------------------------------------------------------------------------------------------------------------------------
| 1      | The Lost Kingdom      | Avery Stone   | Fantasy            | 9      | true        | 2024-01-10  | 2024-01-25    |
| 2      | Shadows of the Night  | Harper Quinn  | Thriller           | 8      | true        | 2024-02-01  | 2024-02-18    |
| 4      | The Final Hour        | Morgan Blake  | Science Fiction    | 10     | true        | 2024-03-20  | 2024-04-10    |
| 5      | Echoes of the Past    | Riley Cross   | Historical Fiction | 9      | false       | 2024-07-01  | 2024-07-15    |
| 6      | The Silent Truth      | Emery Lane    | Mystery            | 8      | false       | 2024-06-10  | null          |
| 7      | Whispers in the Wind  | Jordan Vale   | Romance            | 7      | true        | 2024-06-20  | 2024-07-05    |
| 8      | The Forgotten Journey | Peyton Reed   | Fantasy            | 9      | true        | 2024-07-01  | 2024-07-15    |
| 9      | Rise of the Fallen    | Casey Frost   | Dystopian          | 8      | false       | 2024-07-10  | null          |
| 10     | Beyond the Horizon    | Sage Rivers   | Adventure          | 10     | true        | 2024-07-15  | 2024-07-25    |
| 11     | The Crimson Moon      | Charlie Woods | Fantasy            | 8      | false       | 2024-08-01  | null          |
----------------------------------------------------------------------------------------------------------------------------
```
