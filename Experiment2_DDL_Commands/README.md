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
<img width="1072" height="462" alt="image" src="https://github.com/user-attachments/assets/a3979eae-3ab5-4027-8644-a0c3e65630eb" />


```
CREATE TABLE Reviews(
ReviewID INTEGER,
ProductID INTEGER,
Rating REAL,
ReviewText TEXT);
```

**Output:**

<img width="1342" height="468" alt="image" src="https://github.com/user-attachments/assets/38fab69c-987f-4e62-92aa-535eeaf87421" />


**Question 2**
---
<img width="1240" height="383" alt="image" src="https://github.com/user-attachments/assets/3eb534b5-312b-4e7d-8702-513c813fcd58" />


```
INSERT INTO Employee(EmployeeID,Name,Position)
VALUES(4,"Emily White","Analyst");
```

**Output:**

<img width="1213" height="300" alt="image" src="https://github.com/user-attachments/assets/d2151b46-c430-40b9-b05a-aa8426080ab8" />


**Question 3**
---
<img width="1233" height="378" alt="image" src="https://github.com/user-attachments/assets/265d5c1c-ffbe-48e6-b3f7-ba3c8c6a97a2" />


```
CREATE TABLE Orders(
OrderID INTEGER PRIMARY KEY,
OrderDate Date NOT NULL,
CustomerID INTEGER REFERENCES Customers(CustomerID));
```

**Output:**

<img width="1237" height="367" alt="image" src="https://github.com/user-attachments/assets/5ac9ba00-dd38-49cb-9d63-edd0098418df" />


**Question 4**
---
<img width="1218" height="442" alt="image" src="https://github.com/user-attachments/assets/3bdd348c-50fa-4681-8a16-ba4f2674c5cd" />


```
CREATE TABLE Bonuses(
BonusID INTEGER PRIMARY KEY,
EmployeeID INTEGER REFERENCES Employees(EmployeeID),
BonusAmount REAL CHECK(BonusAmount>0),
BonusDate Date,
Reason TEXT NOT NULL);
```

**Output:**

<img width="1231" height="358" alt="image" src="https://github.com/user-attachments/assets/0485a9e9-5aa0-4779-b8ee-8fbf34a70879" />


**Question 5**
---
<img width="1205" height="391" alt="image" src="https://github.com/user-attachments/assets/275950da-340a-48b1-8c05-8643507486bd" />


```
ALTER TABLE Student_details ADD COLUMN MobileNumber NUMBER;
ALTER TABLE Student_details ADD COLUMN Address VARCHAR(100);
```

**Output:**

<img width="1238" height="405" alt="image" src="https://github.com/user-attachments/assets/09247942-317d-45d1-8d5d-f12068bf3a1d" />


**Question 6**
---
<img width="1066" height="606" alt="image" src="https://github.com/user-attachments/assets/a6ac78b5-9223-4ab1-94d9-24155e3a9c50" />


```
ALTER TABLE Student_details ADD COLUMN mobilenumber number;
```

**Output:**
<img width="1223" height="447" alt="image" src="https://github.com/user-attachments/assets/6d4b2e5d-2541-4007-95fe-d6873894a415" />


**Question 7**
---
<img width="1050" height="362" alt="image" src="https://github.com/user-attachments/assets/f4339a80-6383-4c29-9005-34539a57f4a0" />


```
<img width="1050" height="362" alt="image" src="https://github.com/user-attachments/assets/a9d880e4-8d25-47c1-a833-e1b38fc7721a" />

```

**Output:**

<img width="1251" height="357" alt="image" src="https://github.com/user-attachments/assets/6c4f1950-c6e8-4577-bcec-fa705c4395b5" />


**Question 8**
---
<img width="1077" height="467" alt="image" src="https://github.com/user-attachments/assets/dd173c39-f89c-4d1c-9cbb-b1fd9fd30489" />


```
<img width="615" height="257" alt="image" src="https://github.com/user-attachments/assets/7f137739-2e7f-460c-9348-488dea83cdc9" />

```

**Output:**

<img width="1223" height="431" alt="image" src="https://github.com/user-attachments/assets/e9d3a81b-c1ed-4917-a085-cd9d55c1338f" />


**Question 9**
---
<img width="907" height="382" alt="image" src="https://github.com/user-attachments/assets/17e6a217-8a33-46b1-9b03-cc3017deca16" />


```
INSERT INTO Employee SELECT EmployeeID,Name,Department,Salary FROM Former_employees;
```

**Output:**

<img width="1268" height="302" alt="image" src="https://github.com/user-attachments/assets/09e1d089-1428-4dd4-8736-8b5d5943bf7b" />


**Question 10**
---
<img width="1192" height="501" alt="image" src="https://github.com/user-attachments/assets/a587b8d7-39d9-4258-acf0-5ada0f39e1da" />


```
INSERT INTO Customers(CustomerID,Name,Address) VALUES (306,"Diana Prince","Themyscira");
INSERT INTO Customers(CustomerID,Name,Address,City,ZipCode) VALUES (307,"Bruce Wayne","Wayne Manor","Gotham",10007);
INSERT INTO Customers(CustomerID,Name,Address,ZipCode) VALUES (308,"Peter Parker","Queens",11375);


```

**Output:**

<img width="1240" height="322" alt="image" src="https://github.com/user-attachments/assets/44a65984-2a31-4db2-ac29-595578dc4938" />

## RESULT
Thus, the SQL queries to implement different types of constraints and DDL commands have been executed successfully.
