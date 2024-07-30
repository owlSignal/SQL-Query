### INNER JOIN

#### Query 1: Retrieve order items and customer names
~~~
SELECT o.itemid, c.customername
FROM orderinfo AS o
INNER JOIN customer AS c ON o.customerid=c.customerid;
~~~

#### Query 2: Get book titles and author names

~~~
SELECT i.booktitle, a.authorname
FROM item AS i
INNER JOIN author AS a ON i.authorid=a.authorid;
~~~

### LEFT JOIN

Query 1: Get all book titles with author names (if available)
~~~
SELECT i.booktitle, a.authorname
FROM item AS i
LEFT JOIN author AS a ON i.authorid=a.authorid
ORDER BY i.booktitle;
~~~

Query 2: Get all customers with their order items (if any)

~~~
SELECT c.customername, o.itemid
FROM customer AS c
LEFT JOIN orderinfo AS o ON c.customerid=o.customerid
ORDER BY c.customername;
~~~

### RIGHT JOIN

#### Query 1: Get all customers with their order items (if any)

~~~
SELECT o.itemid, c.customername
FROM orderinfo AS o
RIGHT JOIN customer AS c ON o.customerid=c.customerid
ORDER BY c.customername;
~~~

#### Query 2: Get all book titles with author names (if available)

~~~
SELECT a.authorname, i.booktitle
FROM author AS a 
RIGHT JOIN item AS i ON a.authorid=i.authorid
ORDER BY a.authorname;
~~~

### SELF JOIN and CROSS JOIN

#### Query 1: Get employee names and their manager names
~~~
SELECT e.firstname AS EmployeeName, em.firstname AS ManagerName
FROM employees e
INNER JOIN employees em
ON e.managerid=em.managerid;
~~~

#### Query 2: Cross join between item and author tables
~~~
SELECT *
FROM item
CROSS JOIN author;
~~~

#### Query 3: Get matching author names and book titles

~~~
SELECT a.authorname, i.booktitle
FROM author AS a
INNER JOIN item AS i ON a.authorid=i.authorid;
~~~

### UNION and UNION ALL

#### Query 1: Combine customer names and employee first names
~~~
SELECT customername FROM customer
UNION
SELECT firstname FROM employees
ORDER BY customername;
~~~

#### Query 2: Combine cities from customer and supplier tables
~~~
SELECT city FROM customer
UNION ALL
SELECT city FROM supplier
ORDER BY city;
~~~
