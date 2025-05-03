# Experiment 2: DDL Commands

## AIM
To study and implement DDL commands and different types of constraints.

## THEORY

### 1. CREATE
Used to create a new relation (table).

**Syntax:**
```sql
CREATE TABLE (
  field_1 data_type(size),
  field_2 data_type(size),
  ...
);
```
### 2. ALTER
Used to add, modify, drop, or rename fields in an existing relation.
(a) ADD
```sql
ALTER TABLE std ADD (Address CHAR(10));
```
(b) MODIFY
```sql
ALTER TABLE relation_name MODIFY (field_1 new_data_type(size));
```
(c) DROP
```sql
ALTER TABLE relation_name DROP COLUMN field_name;
```
(d) RENAME
```sql
ALTER TABLE relation_name RENAME COLUMN old_field_name TO new_field_name;
```
### 3. DROP TABLE
Used to permanently delete the structure and data of a table.
```sql
DROP TABLE relation_name;
```
### 4. RENAME
Used to rename an existing database object.
```sql
RENAME TABLE old_relation_name TO new_relation_name;
```
### CONSTRAINTS
Constraints are used to specify rules for the data in a table. If there is any violation between the constraint and the data action, the action is aborted by the constraint. It can be specified when the table is created (using CREATE TABLE) or after it is created (using ALTER TABLE).
### 1. NOT NULL
When a column is defined as NOT NULL, it becomes mandatory to enter a value in that column.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) NOT NULL
);
```
### 2. UNIQUE
Ensures that values in a column are unique.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) UNIQUE
);
```
### 3. CHECK
Specifies a condition that each row must satisfy.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) CHECK (logical_expression)
);
```
### 4. PRIMARY KEY
Used to uniquely identify each record in a table.
Properties:
Must contain unique values.
Cannot be null.
Should contain minimal fields.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) PRIMARY KEY
);
```
### 5. FOREIGN KEY
Used to reference the primary key of another table.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size),
  FOREIGN KEY (column_name) REFERENCES other_table(column)
);
```
### 6. DEFAULT
Used to insert a default value into a column if no value is specified.

Syntax:
```sql
CREATE TABLE Table_Name (
  col_name1 data_type,
  col_name2 data_type,
  col_name3 data_type DEFAULT 'default_value'
);
```

**Question 1**
--
-- Paste Question 1 here        
```sql
-- Paste your SQL code below for Question 1
```
![Screenshot 2025-05-03 112823](https://github.com/user-attachments/assets/b665ba87-5784-42b2-964a-377be8223f40)


**Output:**
![Screenshot 2025-05-03 112932](https://github.com/user-attachments/assets/97faab22-bd5f-4949-a66b-2af943ab6ea0)



**Question 2**
---
-- Paste Question 2 here

```sql
-- Paste your SQL code below for Question 2
![Screenshot 2025-05-03 113019](https://github.com/user-attachments/assets/ecc5a2e2-8a7f-42f2-a73f-bb6e2602a5b4)



**Output:**
![Screenshot 2025-05-03 113110](https://github.com/user-attachments/assets/5a06389c-ff45-44d8-94e5-2733c14d0ca1)




**Question 3**
---
-- Paste Question 3 here

```sql
-- Paste your SQL code below for Question 3
```

![Screenshot 2025-05-03 113209](https://github.com/user-attachments/assets/b7259ad0-cfbf-4947-bc1a-1de81634fe7a)



**Output:**
![Screenshot 2025-05-03 113227](https://github.com/user-attachments/assets/874e1b6e-a4c2-47b4-ad0b-e84389d5bb8c)

**Question 4**
---
-- Paste Question 4 here

```sql
-- Paste your SQL code below for Question 4
```

![Screenshot 2025-05-03 113446](https://github.com/user-attachments/assets/55f1888e-df62-48de-9232-2e7dd02671c5)

**Output:**
![Screenshot 2025-05-03 113505](https://github.com/user-attachments/assets/8760dd6e-d87d-414e-a8c0-460f22fb6bba)






**Question 5**
---
-- Paste Question 5 here

```sql
-- Paste your SQL code below for Question 5
```
![Screenshot 2025-05-03 113615](https://github.com/user-attachments/assets/b62d1b1a-e6d7-4fe7-b490-531f4706e8b7)


**Output:**

![Screenshot 2025-05-03 113632](https://github.com/user-attachments/assets/186dc460-bafa-4cd4-800d-05da1befdf42)


**Question 6**
---
-- Paste Question 6 here

```sql
-- Paste your SQL code below for Question 6
```
![Screenshot 2025-05-03 114223](https://github.com/user-attachments/assets/d3f03aa5-25fd-4688-af5b-3871b470ce91)

**Output:**


**Question 7**
---
-- Paste Question 7 here

```sql
-- Paste your SQL code below for Question 7
```
![Screenshot 2025-05-03 113911](https://github.com/user-attachments/assets/182fd346-7ce0-4c03-bfa7-c9b364a444a7)


**Output:**


![Screenshot 2025-05-03 113925](https://github.com/user-attachments/assets/922edf92-e5fd-4619-a44d-5c01738080fe)


**Question 8**
---
-- Paste Question 8 here

```sql
-- Paste your SQL code below for Question 8
```

![Screenshot 2025-05-03 114101](https://github.com/user-attachments/assets/6dd56983-0e5c-4bab-9d04-8ac9fa5c37a3)



**Output:**

![Screenshot 2025-05-03 114113](https://github.com/user-attachments/assets/49aeb441-f1bf-4a19-ac69-933a7e7c7669)


**Question 9**
---
-- Paste Question 9 here

```sql
-- Paste your SQL code below for Question 9
```
![Screenshot 2025-05-03 112617](https://github.com/user-attachments/assets/b818adb5-932d-4f63-a1eb-091934485809)


**Output:**
![Screenshot 2025-05-03 112650](https://github.com/user-attachments/assets/f6610ea1-7ffa-4452-a191-5649880d7de8)



**Question 10**
---
![Screenshot 2025-05-03 112341](https://github.com/user-attachments/assets/8ef26b70-7606-4855-9b53-0fcd0bcef256)


**Output:**
![Screenshot 2025-05-03 112523](https://github.com/user-attachments/assets/e3f585fd-fbe5-4116-9564-8d43d51b82ba)





## RESULT
Thus, the SQL queries to implement different types of constraints and DDL commands have been executed successfully.
