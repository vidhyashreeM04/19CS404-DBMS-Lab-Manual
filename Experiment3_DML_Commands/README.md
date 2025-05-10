# Experiment 3: DML Commands

## AIM
To study and implement DML (Data Manipulation Language) commands.

## THEORY

### 1. INSERT INTO
Used to add records into a relation.
These are three type of INSERT INTO queries which are as
A)Inserting a single record
**Syntax (Single Row):**
```sql
INSERT INTO table_name (field_1, field_2, ...) VALUES (value_1, value_2, ...);
```
**Syntax (Multiple Rows):**
```sql
INSERT INTO table_name (field_1, field_2, ...) VALUES
(value_1, value_2, ...),
(value_3, value_4, ...);
```
**Syntax (Insert from another table):**
```sql
INSERT INTO table_name SELECT * FROM other_table WHERE condition;
```
### 2. UPDATE
Used to modify records in a relation.
Syntax:
```sql
UPDATE table_name SET column1 = value1, column2 = value2 WHERE condition;
```
### 3. DELETE
Used to delete records from a relation.
**Syntax (All rows):**
```sql
DELETE FROM table_name;
```
**Syntax (Specific condition):**
```sql
DELETE FROM table_name WHERE condition;
```
### 4. SELECT
Used to retrieve records from a table.
**Syntax:**
```sql
SELECT column1, column2 FROM table_name WHERE condition;
```
**Question 1**
--
-- Paste Question 1 here
![Screenshot 2025-05-10 113354(1)](https://github.com/user-attachments/assets/4b6cf70d-ff19-45cf-8f97-622640c8b1a1)


```sql
INSERT INTO Student_details(RollNo,Name,Gender,Subject,MARKS)
VALUES
('202','Ella King','F','Chemistry','87'),
('203','James Bond','M','Literature','78');

```

**Output:**

![Screenshot 2025-05-10 113532(1)](https://github.com/user-attachments/assets/d8db1b5b-debb-4dc8-a582-4fdd72077264)


**Question 2**
---
-- Paste Question 2 here
![Screenshot 2025-05-10 113725(1)](https://github.com/user-attachments/assets/68165199-e79a-474c-8092-6b06552726ab)

```sql
-- Paste your SQL code below for Question 2
update products
set reorder_lvl=20
where quantity < 10 and category like 'Snacks';
```

**Output:**
![Screenshot 2025-05-10 114007(1)](https://github.com/user-attachments/assets/6684524a-4d51-49ed-9526-2d146c24d951)


**Question 3**
---
-- Paste Question 3 here
![Screenshot 2025-05-10 114117(1)](https://github.com/user-attachments/assets/67c4c44a-1df8-4ef4-bed3-e54d144bf60f)

```sql
-- Paste your SQL code below for Question 3
delete from customer
where grade=2;
```

**Output:**

![Output3](output.png)

**Question 4**
---
-- Paste Question 4 here
![Screenshot 2025-05-10 114440(1)](https://github.com/user-attachments/assets/8aaf4463-f1c9-4b37-bf92-b8c9051e0494)

```sql
-- Paste your SQL code below for Question 4
delete from doctors
where doctor_id >= 2 and doctor_id <= 4
```

**Output:**
![Screenshot 2025-05-10 114553](https://github.com/user-attachments/assets/fb83bd28-2af7-4ec8-9e16-b23fc5e6f3a7)


**Question 5**
---
-- Paste Question 5 here
![Screenshot 2025-05-10 114739(1)](https://github.com/user-attachments/assets/0f557db1-cdba-4507-b755-2dff619aa956)

```sql
-- Paste your SQL code below for Question 5
select *
from patients
where first_name like 'A%';
```

**Output:**

![Screenshot 2025-05-10 114838(1)](https://github.com/user-attachments/assets/f265babc-fa0a-4b7f-b8cb-7ac4d2b1677a)


**Question 6**
---
-- Paste Question 6 here
![Screenshot 2025-05-10 115019(1)](https://github.com/user-attachments/assets/4c224096-d037-4a47-840c-5a6f3f49ae78)

```sql
-- Paste your SQL code below for Question 6
insert into Products(ProductID, ProductName, Price, Stock)
select ProductID, ProductName, Price, Stock
from Discontinued_products;

```

**Output:**
![Screenshot 2025-05-10 115110(1)](https://github.com/user-attachments/assets/1355897d-0549-4859-b964-020c9c38fe8b)


**Question 7**
---
-- Paste Question 7 here


![Screenshot 2025-05-10 115212(1)](https://github.com/user-attachments/assets/41351080-6aac-4adb-a200-4ceec0d9a1fb)

```sql
-- Paste your SQL code below for Question 7
update products
set category = 'Household'
where product_name like '%Detergent%';
```

**Output:**
![Screenshot 2025-05-10 115256(1)](https://github.com/user-attachments/assets/d0097265-27ca-4ba4-8368-e5634a279d20)


**Question 8**
---
-- Paste Question 8 here

![Screenshot 2025-05-10 115402(1)](https://github.com/user-attachments/assets/e465529d-dda6-433d-b853-29c834ca5452)

```sql
-- Paste your SQL code below for Question 8
update products
set sell_price=cast(sell_price*1.10 as int)
where supplier_id=6;
```

**Output:**
![Screenshot 2025-05-10 115448(1)](https://github.com/user-attachments/assets/2199d864-e1da-4664-8c91-9e95addfbed6)


**Question 9**
---
-- Paste Question 9 here

![Screenshot 2025-05-10 115551(1)](https://github.com/user-attachments/assets/51ff10ad-1434-4871-be0f-1ff0fb05d8e6)

```sql
-- Paste your SQL code below for Question 9
delete from customer
where grade < 2;
```

**Output:**
![Screenshot 2025-05-10 115648(1)](https://github.com/user-attachments/assets/87401184-1755-4259-990d-07c931c8f300)


**Question 10**
---
-- Paste Question 10 here

![Screenshot 2025-05-10 115749(1)](https://github.com/user-attachments/assets/2d6202ca-c0f2-4698-a446-d62a5ff8a10b)

```sql
-- Paste your SQL code below for Question 10
delete from customer
where grade != 3;
```

**Output:**
![Screenshot 2025-05-10 115848(1)](https://github.com/user-attachments/assets/4c055b92-bfaf-47cc-aeba-d8ab1709c249)


## RESULT
Thus, the SQL queries to implement DML commands have been executed successfully.
