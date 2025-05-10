# Experiment 4: Aggregate Functions, Group By and Having Clause

## AIM
To study and implement aggregate functions, GROUP BY, and HAVING clause with suitable examples.

## THEORY

### Aggregate Functions
These perform calculations on a set of values and return a single value.

- **MIN()** – Smallest value  
- **MAX()** – Largest value  
- **COUNT()** – Number of rows  
- **SUM()** – Total of values  
- **AVG()** – Average of values

**Syntax:**
```sql
SELECT AGG_FUNC(column_name) FROM table_name WHERE condition;
```
### GROUP BY
Groups records with the same values in specified columns.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name;
```
### HAVING
Filters the grouped records based on aggregate conditions.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name
HAVING condition;
```

**Question 1**
--
-- Paste Question 1 here
![Screenshot 2025-05-10 121710(1)](https://github.com/user-attachments/assets/d7445d5b-bb99-4dae-9985-4638dd9daf86)

```sql
-- Paste your SQL code below for Question 1

select DoctorID,count(*) as TotalAppointments
from Appointments
group by DoctorID 
```

**Output:**

![Screenshot 2025-05-10 121851(1)](https://github.com/user-attachments/assets/95c0fe95-449f-4703-8667-2697b0c04d0f)


**Question 2**
---
-- Paste Question 2 here
![Screenshot 2025-05-10 121941(1)](https://github.com/user-attachments/assets/a9b0524f-495f-4b36-9b5b-b550873d6a30)

```sql
-- Paste your SQL code below for Question 2
select Diagnosis,count(*)as DiagnosisCount 
from MedicalRecords
group by Diagnosis 
order by DiagnosisCount desc
limit 1;
```

**Output:**
![Screenshot 2025-05-10 122042(1)](https://github.com/user-attachments/assets/c8e402ec-f89e-4867-8ed5-9e31eaf38b70)


**Question 3**
---
-- Paste Question 3 here
![Screenshot 2025-05-10 122149(1)](https://github.com/user-attachments/assets/ef8d6b93-65da-465d-8cd6-2ee6ab36bc4c)

```sql
-- Paste your SQL code below for Question 3
select PatientID,count(*)as TotalMedications
from Prescriptions
group by PatientID
```

**Output:**

![Screenshot 2025-05-10 122457(1)](https://github.com/user-attachments/assets/bb3f161b-7314-4617-9f39-06bdf61566ba)


**Question 4**
---
-- Paste Question 4 here
![Screenshot 2025-05-10 122559(1)](https://github.com/user-attachments/assets/7772ab76-ef12-4732-afd9-7ba7cef4231e)

```sql
-- Paste your SQL code below for Question 4
select count(*)as"COUNT"
from customer
where grade>1
```

**Output:**

![Screenshot 2025-05-10 122705(1)](https://github.com/user-attachments/assets/7d45e259-d082-469a-b90e-84a43a5fc7ca)


**Question 5**
---
-- Paste Question 5 here
![Screenshot 2025-05-10 122851(1)](https://github.com/user-attachments/assets/5ab55deb-5fcc-434e-9e24-2b9a6ba28510)

```sql
-- Paste your SQL code below for Question 5
select count(*)as "employees_in_california"
from employee
where city='California';
```

**Output:**

![Screenshot 2025-05-10 123008(1)](https://github.com/user-attachments/assets/3c06c919-98f6-4295-abb3-5da5d2edb0ac)


**Question 6**
---
-- Paste Question 6 here
![Screenshot 2025-05-10 123107(1)](https://github.com/user-attachments/assets/1bcf2537-f16f-43a7-8d0e-051607f83497)

```sql
-- Paste your SQL code below for Question 6
select name,email,length(email)as"min_email_length"
from customer
order by length(email) asc limit 1;


```

**Output:**
![Screenshot 2025-05-10 123305(1)](https://github.com/user-attachments/assets/039548fb-dd78-4f93-955a-2395705c9bc1)


**Question 7**
---
-- Paste Question 7 here
![Screenshot 2025-05-10 123428(1)](https://github.com/user-attachments/assets/e48dba7c-dd2b-43d8-aa2e-c5c0919b99ce)
```sql
-- Paste your SQL code below for Question 7
select min(purch_amt)as"MINIMUM"
from orders
```

**Output:**
![Screenshot 2025-05-10 123740(1)](https://github.com/user-attachments/assets/0ec8afb0-018a-482f-8ec8-e1fba30740b5)


**Question 8**
---
-- Paste Question 8 here
![Screenshot 2025-05-10 123908(1)](https://github.com/user-attachments/assets/a78fa818-f928-48bc-8a61-6310cb5fea0f)

```sql
-- Paste your SQL code below for Question 8
select jdate,MAX(workhour)as"MAX(workhour)"
from employee1
group by jdate
having MAX(workhour)>12

```

**Output:**
![Screenshot 2025-05-10 124002(1)](https://github.com/user-attachments/assets/a9520215-e8ea-4ca9-8efe-b76af04a7905)


**Question 9**
---
-- Paste Question 9 here

```sql
-- Paste your SQL code below for Question 9
select jdate,MIN(workhour) as "MIN(workhour)"
from employee1
group by jdate
having MIN(workhour)<10
```

**Output:**

![Screenshot 2025-05-10 124746(1)](https://github.com/user-attachments/assets/e5d3aca0-7858-4d88-b321-c1b44589e0e5)


**Question 10**
---
-- Paste Question 10 here
![Screenshot 2025-05-10 124955(1)](https://github.com/user-attachments/assets/3049671f-7700-453f-b900-e7485d2509a5)

```sql
-- Paste your SQL code below for Question 10
select age,min(income) as "Income"
from employee
group by age
having Income < 1000000;

```

**Output:**

![Screenshot 2025-05-10 125057(1)](https://github.com/user-attachments/assets/309e6420-2919-4109-b294-4ac45f3aa126)



## RESULT
Thus, the SQL queries to implement aggregate functions, GROUP BY, and HAVING clause have been executed successfully.
