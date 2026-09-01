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
<img width="1302" height="808" alt="image" src="https://github.com/user-attachments/assets/06e9a6a1-c0f8-4a34-a794-b57c466fa9e0" />

```sql
SELECT p.admission_date,s.surgery_date FROM PATIENTS p
JOIN SURGERIES s
ON p.patient_id=s.patient_id;
```

**Output:**
<img width="983" height="521" alt="image" src="https://github.com/user-attachments/assets/a3344c68-f147-45d9-8574-7a0f5a1e07a6" />


**Question 2**
---
<img width="1247" height="862" alt="image" src="https://github.com/user-attachments/assets/00ddadec-d872-4fbd-96a5-ef84e0de94d2" />

```sql
SELECT c.cust_name,c.city,c.grade,s.name AS Salesman,s.city FROM customer c
JOIN salesman s
ON c.salesman_id=s.salesman_id
WHERE c.grade<300
ORDER BY c.customer_id;
```

**Output:**
<img width="1227" height="730" alt="image" src="https://github.com/user-attachments/assets/5662769d-e9a3-4876-abad-8f1b18283b2e" />


**Question 3**
---
<img width="1205" height="768" alt="image" src="https://github.com/user-attachments/assets/7e6910f9-c2b8-414a-9194-af8374c60255" />

```sql
SELECT p.* FROM PATIENTS p 
INNER JOIN DOCTORS d
ON p.doctor_id=d.doctor_id
WHERE d.first_name="John" AND d.last_name="Smith";
```

**Output:**

<img width="1237" height="408" alt="image" src="https://github.com/user-attachments/assets/a47795b2-c38a-45de-b41f-dfcf9f8cf388" />

**Question 4**
---
<img width="1212" height="857" alt="image" src="https://github.com/user-attachments/assets/e1dbae30-5649-43a2-9d81-754e716ff234" />


```sql
SELECT c.cust_name AS 'Customer Name',c.city,s.name AS Salesman,s.commission FROM customer c
JOIN salesman s
ON c.salesman_id=s.salesman_id;
```

**Output:**

<img width="1237" height="832" alt="image" src="https://github.com/user-attachments/assets/1a749469-0afd-4440-b9f0-832b8e662ac6" />

**Question 5**
---
<img width="1260" height="790" alt="image" src="https://github.com/user-attachments/assets/c86e87e5-e935-4e9e-8872-a425c40be257" />

```sql
SELECT p.first_name,s.* FROM PATIENTS p
INNER JOIN SURGERIES s
ON p.patient_id=s.patient_id
WHERE discharge_date BETWEEN '2024-03-01' AND '2024-03-31' AND admission_date NOT BETWEEN '2024-03-01' AND '2024-03-31';
```

**Output:**
<img width="1282" height="418" alt="image" src="https://github.com/user-attachments/assets/f77aa4d8-d531-49d5-8ce3-172b456289fd" />

**Question 6**
---

<img width="1257" height="403" alt="image" src="https://github.com/user-attachments/assets/9a34e65f-08a3-4766-803d-decd445689fe" />

```sql
SELECT s.name,c.cust_name,c.city,c.grade,c.salesman_id FROM Salesman s
LEFT JOIN Customer c
ON c.salesman_id=s.salesman_id
WHERE c.grade<=100;
```

**Output:**
<img width="1207" height="493" alt="image" src="https://github.com/user-attachments/assets/c2ff6db0-80f0-4b1a-b7dd-3db6f71bfcf5" />

**Question 7**
---
-- Paste Question 7 here

```sql
-- Paste your SQL code below for Question 7
```

**Output:**

![Output7](output.png)

**Question 8**
---
-- Paste Question 8 here

```sql
-- Paste your SQL code below for Question 8
```

**Output:**

![Output8](output.png)

**Question 9**
---
-- Paste Question 9 here

```sql
-- Paste your SQL code below for Question 9
```

**Output:**

![Output9](output.png)

**Question 10**
---
-- Paste Question 10 here

```sql
-- Paste your SQL code below for Question 10
```

**Output:**

![Output10](output.png)


## RESULT
Thus, the SQL queries to implement different types of joins have been executed successfully.
