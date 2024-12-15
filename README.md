# SQL Query Error: WHERE Clause Subquery/Function Returning Multiple Rows
This repository demonstrates a common SQL error where a subquery or a user-defined function in the WHERE clause returns multiple rows instead of a single boolean value, leading to a query failure. The error is explained in detail with examples in the bug.sql file, and a corrected version of the query is provided in bugSolution.sql.  This showcases an important aspect of relational database querying and how to ensure subqueries or functions operate as intended when used in WHERE clauses.

## Setup
To test the examples, you will need a database system that supports SQL. Create a database and the necessary tables (employees, departments, products) with sample data as needed.

## Bug Explanation
The bug occurs when a subquery or function used in the WHERE clause returns more than one row.  The database engine is expecting a scalar result (a single TRUE or FALSE value) for each row being evaluated, and receives multiple rows causing an unexpected outcome.

## Solution
The solution involves modifying the subquery or function to return a single boolean value. This might require using aggregate functions (like EXISTS), joins, or restructuring the logic of the user-defined function to ensure it always returns a single value.