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
<img width="1217" height="333" alt="image" src="https://github.com/user-attachments/assets/66631534-818b-41be-897e-3eb1a3782b89" />


```
UPDATE products 
SET quantity=quantity*1.10;
```

**Output:**

<img width="1237" height="588" alt="image" src="https://github.com/user-attachments/assets/7811d764-6e9c-4a21-852d-dd47aa12dcf3" />


**Question 2**
---
<img width="1042" height="225" alt="image" src="https://github.com/user-attachments/assets/7212f586-4d8b-477d-b0fe-4940b5b71def" />


```
update products set product_name='Grapefruit'
where product_id=4;
```

**Output:**

<img width="1217" height="270" alt="image" src="https://github.com/user-attachments/assets/4d83d4e3-924e-4120-b3d5-e2d78f87ef8b" />


**Question 3**
---
<img width="1233" height="747" alt="image" src="https://github.com/user-attachments/assets/1e45e4ad-2a2f-4f1c-954c-470bc4e26ff2" />


```sql
UPDATE products
SET sell_price=CAST(cost_price*1.35 AS INT)
WHERE (sell_price-cost_price)*1.0/cost_price<30;
```

**Output:**

<img width="1245" height="520" alt="image" src="https://github.com/user-attachments/assets/3646a928-65d7-484e-9f66-531a22897fd7" />


**Question 4**
---
<img width="1037" height="817" alt="image" src="https://github.com/user-attachments/assets/17524b13-5dde-4099-835f-a15075e249f6" />


```sql
update sales set sell_price=sell_price+3
where product_id IN(
    select product_id
    from products
    where supplier_id=4
);
```

**Output:**

<img width="1190" height="426" alt="image" src="https://github.com/user-attachments/assets/e53d0de9-cc33-4620-a0ae-059bd3254e56" />


**Question 5**
---
<img width="1047" height="322" alt="image" src="https://github.com/user-attachments/assets/eb11b4d9-473e-4174-94d7-bc9a0974f362" />



```sql
update products set product_name='Premium Bread'
where product_id=5;
```

**Output:**

<img width="1228" height="372" alt="image" src="https://github.com/user-attachments/assets/ac50fb4c-9451-4ebc-bd67-281039798dd7" />

**Question 6**
---
<img width="1133" height="160" alt="image" src="https://github.com/user-attachments/assets/11b9ac4e-2fc8-4f94-bc90-65d810bb2fc5" />


```sql
delete from Doctors where specialization='Cardiology';
```

**Output:**
<img width="1187" height="360" alt="image" src="https://github.com/user-attachments/assets/171c0bb1-1f59-4cb5-a40a-768a35498e2f" />


**Question 7**
---

<img width="1196" height="717" alt="image" src="https://github.com/user-attachments/assets/9388283d-ba0f-4e87-950e-30cc240f8ce7" />

```sql
delete from customer where OPENING_AMT between 4000 and 6000;
```

**Output:**

<img width="1210" height="575" alt="image" src="https://github.com/user-attachments/assets/78134fd8-f3b1-46d3-89d6-6967f082c04c" />


**Question 8**
---
<img width="1183" height="577" alt="image" src="https://github.com/user-attachments/assets/b766f163-c400-4cc8-9db1-0bca7c76a8e6" />

```sql
delete from Doctors where last_name is NULL;

```

**Output:**

<img width="1196" height="672" alt="image" src="https://github.com/user-attachments/assets/fbb3bfaf-674c-42a0-88d0-f1e86b8c291c" />


**Question 9**
---
<img width="1230" height="672" alt="image" src="https://github.com/user-attachments/assets/c43db78c-076c-46ee-9a22-a045e92a44bf" />


```sql
delete from Customer where Length(Cust_Name)=6;
```

**Output:**
<img width="1220" height="667" alt="image" src="https://github.com/user-attachments/assets/49d107d3-55dc-4cba-abd8-f7d038732e38" />


**Question 10**
---
<img width="1207" height="660" alt="image" src="https://github.com/user-attachments/assets/74565b60-6dae-4904-bbb5-027f98f29eee" />


```sql
delete from Customer where Grade >= 2;
```

**Output:**
<img width="875" height="522" alt="image" src="https://github.com/user-attachments/assets/03c91b89-1c4b-4750-9e31-a352d239f369" />



<img width="1413" height="605" alt="image" src="https://github.com/user-attachments/assets/6823b29a-6d2b-49dd-a630-45191aeeeec4" />




## RESULT
Thus, the SQL queries to implement DML commands have been executed successfully.
