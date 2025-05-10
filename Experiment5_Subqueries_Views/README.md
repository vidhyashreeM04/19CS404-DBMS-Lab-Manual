# Experiment 5: Subqueries and Views

## AIM
To study and implement subqueries and views.

## THEORY

### Subqueries
A subquery is a query inside another SQL query and is embedded in:
- WHERE clause
- HAVING clause
- FROM clause

**Types:**
- **Single-row subquery**:
  Sub queries can also return more than one value. Such results should be made use along with the operators in and any.
- **Multiple-row subquery**:
  Here more than one subquery is used. These multiple sub queries are combined by means of ‘and’ & ‘or’ keywords.
- **Correlated subquery**:
  A subquery is evaluated once for the entire parent statement whereas a correlated Sub query is evaluated once per row processed by the parent statement.

**Example:**
```sql
SELECT * FROM employees
WHERE salary > (SELECT AVG(salary) FROM employees);
```
### Views
A view is a virtual table based on the result of an SQL SELECT query.
**Create View:**
```sql
CREATE VIEW view_name AS
SELECT column1, column2 FROM table_name WHERE condition;
```
**Drop View:**
```sql
DROP VIEW view_name;
```

**Question 1**
--
-- Paste Question 1 here
![Screenshot 2025-05-10 213915(1)](https://github.com/user-attachments/assets/c13f8e05-6b0a-46b0-8060-9d213b7ad896)


```sql
-- Paste your SQL code below for Question 1
select name,city
from customer
where city IN (
      select city
      from customer
      where id IN (3,7)
      );
```

**Output:**

![Screenshot 2025-05-10 214030(1)](https://github.com/user-attachments/assets/419cc6ea-9d00-4cc7-8d96-abbec188d0cb)


**Question 2**
---
-- Paste Question 2 here
![Screenshot 2025-05-10 214120(1)](https://github.com/user-attachments/assets/3ca7d377-be8a-435f-af05-47426da955b3)

```sql
-- Paste your SQL code below for Question 2
select id,name,age,address,salary
from customers
where salary < 2500;

```

**Output:**
![Screenshot 2025-05-10 214219(1)](https://github.com/user-attachments/assets/2ec20a85-6319-4401-9020-8fbb8b9dfc97)


**Question 3**
---
-- Paste Question 3 here
![Screenshot 2025-05-10 214313(1)](https://github.com/user-attachments/assets/667b9599-ff70-481c-8c0f-d00c37e073d9)

       
```sql
-- Paste your SQL code below for Question 3
select  student_name, grade
from Grades g1
where grade  = (
    select min(grade) 
    from Grades g2
    where g1.subject=g2.subject
    );
       
```

**Output:**
![Screenshot 2025-05-10 214521(1)](https://github.com/user-attachments/assets/4fd4fa20-29b4-4c5e-8fa4-b8dcfa1288cb)


**Question 4**
---
-- Paste Question 4 here
![Screenshot 2025-05-10 214635(1)](https://github.com/user-attachments/assets/69245d71-2a41-479a-b264-005a54d54b14)

```sql
-- Paste your SQL code below for Question 4
select id,name,age,city,income
from employee
where age < (
    select avg(age)
    from employee
    where income > 250000
    );
```

**Output:**
![Screenshot 2025-05-10 214753(1)](https://github.com/user-attachments/assets/2167d31f-d28d-4b9f-b248-088545cb3dfc)


**Question 5**
---
-- Paste Question 5 here
![Screenshot 2025-05-10 214845(1)](https://github.com/user-attachments/assets/2aaa0e79-986e-41b6-b85f-c7ba7d4b196a)

```sql
-- Paste your SQL code below for Question 5
select id,name,age,address,salary
from customers
where age < 30;
```

**Output:**
![Screenshot 2025-05-10 214958(1)](https://github.com/user-attachments/assets/e354f4eb-3764-4bff-8c04-e0ca52f6a562)


**Question 6**
---
-- Paste Question 6 here
![Screenshot 2025-05-10 215059(1)](https://github.com/user-attachments/assets/4f1daaed-5826-46ee-84c1-2ebb1dff0e12)

```sql
-- Paste your SQL code below for Question 6
select id,name,city,email,phone
from customer
where city<>(
    select city
    from customer
    order by id desc
    limit 1
    );
```

**Output:**

![Screenshot 2025-05-10 215210(1)](https://github.com/user-attachments/assets/e35777a9-6d9a-4e84-af3a-2158c1a26418)


**Question 7**
---
-- Paste Question 7 here
![Screenshot 2025-05-10 215259(1)](https://github.com/user-attachments/assets/984a02a8-6595-44d7-b8cd-f602fc9b73b1)

```sql
-- Paste your SQL code below for Question 7
SELECT *
FROM Employee
WHERE age < (
    SELECT AVG(age)
    FROM Employee
    WHERE income > 1000000
);

```

**Output:**

![Screenshot 2025-05-10 215410(1)](https://github.com/user-attachments/assets/e9970940-bd15-4cd5-bc92-b8ab6b9ec8b6)


**Question 8**
---
-- Paste Question 8 here
![Screenshot 2025-05-10 215537(1)](https://github.com/user-attachments/assets/cafe7400-931a-4afc-8dc2-55c126fbbd04)

```sql
-- Paste your SQL code below for Question 8
select o.ord_no, o.purch_amt, o.ord_date, o.customer_id,o.salesman_id
from orders o
join salesman s on o.salesman_id=s.salesman_id
where s.name='Paul Adam';
```

**Output:**

![Screenshot 2025-05-10 215641(1)](https://github.com/user-attachments/assets/00550219-2f91-412e-ab39-103b3405fabb)


**Question 9**
---
-- Paste Question 9 here
![Screenshot 2025-05-10 215741(1)](https://github.com/user-attachments/assets/eeaa6494-fbe5-4cd4-8f26-7d2b04500715)

```sql
-- Paste your SQL code below for Question 9
select medication_id as "medic",medication_name,dosage
from Medications
where dosage = (
    select Max(dosage) 
    from Medications
    );
```

**Output:**
![Screenshot 2025-05-10 215920(1)](https://github.com/user-attachments/assets/d8eea743-c783-478f-ad1d-86e6113cc41e)



**Question 10**
---
-- Paste Question 10 here
![Screenshot 2025-05-10 220004(1)](https://github.com/user-attachments/assets/59079e15-f15c-4700-98b7-259bdb8369d3)

```sql
-- Paste your SQL code below for Question 10
select id,name,age,address,salary
from customers
where salary = 1500;
```

**Output:**

![Screenshot 2025-05-10 220056(1)](https://github.com/user-attachments/assets/5605a1e6-6520-4b1b-a8a1-ac4684d76453)


## RESULT
Thus, the SQL queries to implement subqueries and views have been executed successfully.
