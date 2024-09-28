# Join (SQL)

A join in the Structured Query Language combines columns from one or more tables into a new table. Informally, a join stitches two tables and puts on the same row records with matching fields : `INNER`, `LEFT OUTER`, `RIGHT OUTER`, `FULL OUTER` and `CROSS`.

![This represents a full join SQL statement between tables A and B](Square_join.png)

This represents a full join SQL statement between tables A and B

# Example

The example uses the following tables:

**Department Table**

| DepartmentID | DepartmentName |
| --- | --- |
| 31 | Sales |
| 33 | Engineering |
| 34 | Clerical |
| 35 | Marketing |

**Employee table**

| LastName | DepartmentID |
| --- | --- |
| Rafferty | 31 |
| Jones | 33 |
| Heisenberg | 33 |
| Robinson | 34 |
| Smith | 34 |
| Williams | `NULL` |

`Department.DepartmentID` is the primary key of the `Department` table, whereas `Employee.DepartmentID` is a foreign key.

Note that in `Employee`, "Williams" has not yet been assigned to a department. Also, no employees have been assigned to the "Marketing" department.
These are the SQL statements to create the above tables: 

```sql
CREATE TABLE department(
    DepartmentID INT PRIMARY KEY NOT NULL,
    DepartmentName VARCHAR(20)
);

CREATE TABLE employee (
    LastName VARCHAR(20),
    DepartmentID INT REFERENCES department(DepartmentID)
);

INSERT INTO department
VALUES (31, 'Sales'),
       (33, 'Engineering'),
       (34, 'Clerical'),
       (35, 'Marketing');

INSERT INTO employee
VALUES ('Rafferty', 31),
       ('Jones', 33),
       ('Heisenberg', 33),
       ('Robinson', 34),
       ('Smith', 34),
       ('Williams', NULL);
```

## Cross join

`CROSS JOIN` returns the Cartesian product of rows from tables in the join. In other words, it will produce rows which combine each row from the first table with each row from the second table.

| Employee.LastName | Employee.DepartmentID | Department.DepartmentName | Department.DepartmentID |
| --- | --- | --- | --- |
| Rafferty | 31 | Sales | 31 |
| Jones | 33 | Sales | 31 |
| Heisenberg | 33 | Sales | 31 |
| Smith | 34 | Sales | 31 |
| Robinson | 34 | Sales | 31 |
| Williams | `NULL` | Sales | 31 |
| Rafferty | 31 | Engineering | 33 |
| Jones | 33 | Engineering | 33 |
| Heisenberg | 33 | Engineering | 33 |
| Smith | 34 | Engineering | 33 |
| Robinson | 34 | Engineering | 33 |
| Williams | `NULL` | Engineering | 33 |
| Rafferty | 31 | Clerical | 34 |
| Jones | 33 | Clerical | 34 |
| Heisenberg | 33 | Clerical | 34 |
| Smith | 34 | Clerical | 34 |
| Robinson | 34 | Clerical | 34 |
| Williams | `NULL` | Clerical | 34 |
| Rafferty | 31 | Marketing | 35 |
| Jones | 33 | Marketing | 35 |
| Heisenberg | 33 | Marketing | 35 |
| Smith | 34 | Marketing | 35 |
| Robinson | 34 | Marketing | 35 |
| Williams | `NULL` | Marketing | 35 |