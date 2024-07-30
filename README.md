# BOOKSTORE Database Structure and SQL Queries

## Database Schema

### Tables and Columns

1. **Author**
   - authorid
   - authorname

2. **Customer**
   - customerid
   - customername
   - address
   - city

3. **Employees**
   - employeeid
   - firstname
   - lastname
   - employeerole

4. **Item**
   - itemid
   - booktitle
   - authorid

5. **Orderinfo**
   - id
   - itemid
   - customerid

6. **Supplier**
   - supplierid
   - suppliername
   - city

## SQL Queries

### Table of Contents
1. [INNER JOIN](#inner-join)
2. [LEFT JOIN](#left-join)
3. [RIGHT JOIN](#right-join)
4. [SELF JOIN and CROSS JOIN](#self-join-and-cross-join)
5. [UNION and UNION ALL](#union-and-union-all)
