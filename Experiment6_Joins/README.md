# Experiment 6: Joins

## AIM
To study and implement different types of joins.

## THEORY

SQL Joins are used to combine records from two or more tables based on a related column.

### 1. INNER JOIN
Returns records with matching values in both tables.

**Syntax:**
```sql
SELECT columns
FROM table1
INNER JOIN table2
ON table1.column = table2.column;
```

### 2. LEFT JOIN
Returns all records from the left table, and matched records from the right.

**Syntax:**

```sql
SELECT columns
FROM table1
LEFT JOIN table2
ON table1.column = table2.column;
```
### 3. RIGHT JOIN
Returns all records from the right table, and matched records from the left.

**Syntax:**

```sql
SELECT columns
FROM table1
RIGHT JOIN table2
ON table1.column = table2.column;
```
### 4. FULL OUTER JOIN
Returns all records when there is a match in either left or right table.

**Syntax:**

```sql
SELECT columns
FROM table1
FULL OUTER JOIN table2
ON table1.column = table2.column;
```

**Question 1**
--
-- Paste Question 1 here
![Screenshot 2025-05-10 220916(1)](https://github.com/user-attachments/assets/b4d9bea9-3ace-4845-abf9-cdbd8cd95685)

```sql
-- Paste your SQL code below for Question 1
select p.first_name as "patient_name",a.*
from patients p
inner join appointments a on p.patient_id = a.patient_id;
```

**Output:**

![Screenshot 2025-05-10 221026(1)](https://github.com/user-attachments/assets/017c38c2-e0a9-46d6-ab09-f255389f3efc)


**Question 2**
---
-- Paste Question 2 here
![Screenshot 2025-05-10 221132(1)](https://github.com/user-attachments/assets/57ffe60a-b256-47a0-91c4-1ca1a3aeb057)

```sql
-- Paste your SQL code below for Question 2
select c.cust_name as "Customer Name",c.city as "city",s.name as "Salesman",s.commission as "commission"
from customer c
inner join salesman s on c.salesman_id = s.salesman_id;
```

**Output:**

![Screenshot 2025-05-10 221229(1)](https://github.com/user-attachments/assets/afb09fd5-c1e9-426f-a659-7b8ca34173dd)


**Question 3**
---
-- Paste Question 3 here
![Screenshot 2025-05-10 221405(1)](https://github.com/user-attachments/assets/2818f377-1111-46a1-ae95-102c76070989)

```sql
-- Paste your SQL code below for Question 3
select o.ord_no,o.purch_amt,o.ord_date,c.cust_name,c.city as "customer_city",c.grade,s.name as "salesman_name",s.city as "salesman_city",s.commission
from orders o
inner join customer c on o.customer_id = c.customer_id
inner join salesman s on c.salesman_id = s.salesman_id;
```

**Output:**

![Screenshot 2025-05-10 221520(1)](https://github.com/user-attachments/assets/fdadb3c4-234b-4de6-825a-15fbb40e37b8)


**Question 4**
---
-- Paste Question 4 here
![Screenshot 2025-05-10 221625(1)](https://github.com/user-attachments/assets/25447611-2562-4dcf-bae4-37fa4b5ed06b)

```sql
-- Paste your SQL code below for Question 4
select s.*
from customer c
join salesman s on c.salesman_id = s.salesman_id
where c.cust_name = 'Fabian Johns';
```

**Output:**
![Screenshot 2025-05-10 221738(1)](https://github.com/user-attachments/assets/cb7e8475-74fa-4243-8841-a2c4dacccc7c)


**Question 5**
---
-- Paste Question 5 here
![Screenshot 2025-05-10 221840(1)](https://github.com/user-attachments/assets/17b6838d-b92a-40ef-bab8-8af238897d71)

```sql
-- Paste your SQL code below for Question 5
select p.*
from patients p
inner join appointments a on p.patient_id = a.patient_id
where a.appointment_date BETWEEN '2024-01-01' and '2024-01-31';
```

**Output:**

![Screenshot 2025-05-10 221949(1)](https://github.com/user-attachments/assets/adcc0bb7-29ec-4d01-acba-367250c7bae8)


**Question 6**
---
-- Paste Question 6 here
![Screenshot 2025-05-10 222221(1)](https://github.com/user-attachments/assets/b0df7a2a-3a05-4d19-b8fd-4a5f0523a8e1)


```sql
-- Paste your SQL code below for Question 6
select c.cust_name,s.commission
from customer c
left join salesman s on c.salesman_id = s.salesman_id;

```

**Output:**

![Screenshot 2025-05-10 222344(1)](https://github.com/user-attachments/assets/652b2d14-301e-4a7b-a2c0-9a9a88054a67)


**Question 7**
---
-- Paste Question 7 here
![Screenshot 2025-05-10 222515(1)](https://github.com/user-attachments/assets/5d673988-ea8a-4890-ba3c-891d24d3a9c0)

```sql
-- Paste your SQL code below for Question 7
select s.name as "Salesman",c.cust_name,c.city
from salesman s
join customer c on s.city=c.city;
```

**Output:**

![Screenshot 2025-05-10 222703(1)](https://github.com/user-attachments/assets/8f42dbaf-c3b8-4bf7-98d9-f31120bb0f26)


**Question 8**
---
-- Paste Question 8 here
![Screenshot 2025-05-10 222859(1)](https://github.com/user-attachments/assets/a0b4239b-f4a2-4855-93c7-d6e1f8cfb183)

```sql
-- Paste your SQL code below for Question 8
select p.first_name as "patient_name",t.*
from patients p
join test_results t on p.patient_id = t.patient_id
where p.admission_date BETWEEN '2024-01-01' and '2024-01-31';

```

**Output:**
![Screenshot 2025-05-10 222944(1)](https://github.com/user-attachments/assets/727c9400-afbd-413c-8f88-a23063bcbd24)


**Question 9**
---
-- Paste Question 9 here
![Screenshot 2025-05-10 223041(1)](https://github.com/user-attachments/assets/1a2a66bc-35e8-4f11-b1d3-01fe1d526a17)

```sql
-- Paste your SQL code below for Question 9
select o.ord_no,o.purch_amt,c.cust_name,c.city
from customer c
join orders o on c.customer_id=o.customer_id
where o.purch_amt BETWEEN 500 and 2000;

```

**Output:**

![Screenshot 2025-05-10 223141(1)](https://github.com/user-attachments/assets/b67f4600-1635-458d-ae62-e813ca917dfc)


**Question 10**
---
-- Paste Question 10 here
![Screenshot 2025-05-10 223911(1)](https://github.com/user-attachments/assets/c2509b17-61b5-4d28-ab72-affa78387e14)

```sql
-- Paste your SQL code below for Question 10
SELECT 
    t.*
FROM 
    test_results t
INNER JOIN 
    patients p ON t.patient_id = p.patient_id
WHERE 
    p.first_name = 'Alice';

```

**Output:**

![Screenshot 2025-05-10 224002(1)](https://github.com/user-attachments/assets/b50c5c10-c431-4f5c-a0b9-c465538c2c23)



## RESULT
Thus, the SQL queries to implement different types of joins have been executed successfully.
