This comprehensive PostgreSQL cheat sheet offers a quick reference to essential commands and concepts for database management, querying, and optimization. From basic data manipulation and table management to advanced querying with joins and aggregate functions, it provides valuable insights for both beginners and experienced users. Enhance your PostgreSQL skills with examples, explanations, and external resources for further learning.

## The Basics

### Transactions
Transactions ensure data integrity by grouping multiple operations into a single, all-or-nothing operation. The key commands are:

- Start a transaction:
  ```sql
  BEGIN;
  ```

- Commit changes made during a transaction:
  ```sql
  COMMIT;
  ```

- Rollback changes if an error occurs:
  ```sql
  ROLLBACK;
  ```

### Data Types
PostgreSQL supports a wide range of data types. Here are a few commonly used ones:

- Integer types: `SMALLINT`, `INTEGER`, `BIGINT`
- Decimal numbers: `DECIMAL`, `NUMERIC`
- Floating-point numbers: `REAL`, `DOUBLE PRECISION`
- Character types: `CHAR(n)`, `VARCHAR(n)`, `TEXT`
- Boolean type: `BOOLEAN`
- Date and Time types: `DATE`, `TIME`, `TIMESTAMP`

### Common Table Expressions (CTEs)
CTEs provide a way to write more readable and modular SQL queries:

- Basic CTE structure:
  ```sql
  WITH cte_name AS (
    SELECT * FROM table_name WHERE condition
  )
  SELECT * FROM cte_name;
  ```

### Performance Optimization
Understanding how to analyze and improve query performance is crucial:

- Use `EXPLAIN` to analyze query plans:
  ```sql
  EXPLAIN SELECT * FROM table_name;
  ```

- Indexes are critical for improving query performance. Ensure frequently queried columns are indexed.

### Permissions and Security
Managing user roles and permissions is key for database security:

- Create a new user role with login capabilities:
  ```sql
  CREATE ROLE user_name WITH LOGIN PASSWORD 'password';
  ```

- Grant SELECT permissions on a table to a user:
  ```sql
  GRANT SELECT ON table_name TO user_name;
  ```

### Backup and Restore
Basic commands for backing up and restoring your database:

- Backup a database to a file:
  ```shell
  pg_dump database_name > backup_file.sql
  ```

- Restore a database from a file:
  ```shell
  psql database_name < backup_file.sql
  ```

### Useful links

1. [**PostgreSQL Documentation**](https://www.postgresql.org/docs/) - The go-to resource for all PostgreSQL features and functionalities.
2. [**SQLZoo**](https://sqlzoo.net/wiki/PostgreSQL) - Interactive SQL tutorials with a focus on PostgreSQL. Great for hands-on learning.
3. [**PostgreSQL Tutorial**](https://www.postgresqltutorial.com/) - Easy-to-follow tutorials for PostgreSQL beginners.
4. [**DB Fiddle**](https://dbfiddle.uk/?rdbms=postgres_13) - Test and share SQL queries online. Supports PostgreSQL.
5. [**pgExercises**](https://pgexercises.com/) - Practice real-world SQL queries with PostgreSQL exercises.


## Example Commands
### QUERYING DATA FROM A TABLE

- Query data in columns c1, c2 from a table:
  ```sql
  SELECT c1, c2 FROM t;
  ```

- Query all rows and columns from a table:
  ```sql
  SELECT * FROM t;
  ```

- Query data and filter rows with a condition:
  ```sql
  SELECT c1, c2 FROM t WHERE condition;
  ```

- Query distinct rows from a table:
  ```sql
  SELECT DISTINCT c1 FROM t WHERE condition;
  ```

- Sort the result set in ascending or descending order:
  ```sql
  SELECT c1, c2 FROM t ORDER BY c1 ASC [DESC];
  ```

- Skip offset of rows and return the next n rows:
  ```sql
  SELECT c1, c2 FROM t ORDER BY c1 LIMIT n OFFSET offset;
  ```

- Group rows using an aggregate function:
  ```sql
  SELECT c1, aggregate(c2) FROM t GROUP BY c1;
  ```

- Filter groups using HAVING clause:
  ```sql
  SELECT c1, aggregate(c2) FROM t GROUP BY c1 HAVING condition;
  ```


### QUERYING FROM MULTIPLE TABLES

- Inner join `t1` and `t2`:
  ```sql
  SELECT c1, c2 FROM t1 INNER JOIN t2 ON condition;
  ```

- Left join `t1` and `t2`:
  ```sql
  SELECT c1, c2 FROM t1 LEFT JOIN t2 ON condition;
  ```

- Right join `t1` and `t2`:
  ```sql
  SELECT c1, c2 FROM t1 RIGHT JOIN t2 ON condition;
  ```

- Perform a full outer join:
  ```sql
  SELECT c1, c2 FROM t1 FULL OUTER JOIN t2 ON condition;
  ```

- Produce a Cartesian product of rows in tables (cross join):
  ```sql
  SELECT c1, c2 FROM t1 CROSS JOIN t2;
  ```

- Another way to perform a cross join:
  ```sql
  SELECT c1, c2 FROM t1, t2;
  ```

- Join `t1` to itself using an INNER JOIN clause:
  ```sql
  SELECT c1, c2 FROM t1 A INNER JOIN t2 B ON condition;
  ```
	
### USING SQL OPERATORS

- Combine rows from two queries with UNION or UNION ALL:
  ```sql
  SELECT c1, c2 FROM t1 UNION [ALL] SELECT c1, c2 FROM t2;
  ```

- Return the intersection of two queries with INTERSECT:
  ```sql
  SELECT c1, c2 FROM t1 INTERSECT SELECT c1, c2 FROM t2;
  ```

- Subtract a result set from another result set with EXCEPT:
  ```sql
  SELECT c1, c2 FROM t1 EXCEPT SELECT c1, c2 FROM t2;
  ```

- Query rows using pattern matching % _ with LIKE or NOT LIKE:
  ```sql
  SELECT c1, c2 FROM t1 WHERE c1 [NOT] LIKE pattern;
  ```

- Query rows in a list with IN or NOT IN:
  ```sql
  SELECT c1, c2 FROM t WHERE c1 [NOT] IN value_list;
  ```

- Query rows between two values with BETWEEN:
  ```sql
  SELECT c1, c2 FROM t WHERE c1 BETWEEN low AND high;
  ```

- Check if values in a table are NULL or not with IS NULL or IS NOT NULL:
  ```sql
  SELECT c1, c2 FROM t WHERE c1 IS [NOT] NULL;
  ```
	
### MANAGING TABLES

- Create a new table with three columns:
  ```sql
  CREATE TABLE t (
    id SERIAL PRIMARY KEY,
    name VARCHAR NOT NULL,
    price NUMERIC(10, 2) DEFAULT 0
  );
  ```

- Delete the table from the database:
  ```sql
  DROP TABLE t CASCADE;
  ```

- Add a new column to the table:
  ```sql
  ALTER TABLE t ADD column_name data_type;
  ```

- Drop column `c` from the table:
  ```sql
  ALTER TABLE t DROP COLUMN c;
  ```

- Add a constraint:
  ```sql
  ALTER TABLE t ADD CONSTRAINT constraint_name constraint_type;
  ```

- Drop a constraint:
  ```sql
  ALTER TABLE t DROP CONSTRAINT constraint_name;
  ```

- Rename a table from `t1` to `t2`:
  ```sql
  ALTER TABLE t1 RENAME TO t2;
  ```

- Rename column `c1` to `c2`:
  ```sql
  ALTER TABLE t1 RENAME COLUMN c1 TO c2;
  ```

- Remove all data in a table:
  ```sql
  TRUNCATE TABLE t CASCADE;
  ```


### USING SQL CONSTRAINTS

- Set `c1` and `c2` as a composite primary key:
  ```sql
  CREATE TABLE t (
    c1 INT, 
    c2 INT, 
    c3 VARCHAR, 
    PRIMARY KEY (c1, c2)
  );
  ```

- Set `c2` column as a foreign key:
  ```sql
  CREATE TABLE t1 (
    c1 SERIAL PRIMARY KEY, 
    c2 INT, 
    FOREIGN KEY (c2) REFERENCES t2(c2)
  );
  ```

- Make the values in `c1` and `c2` unique:
  ```sql
  CREATE TABLE t (
    c1 INT, 
    c2 INT, 
    UNIQUE(c1, c2)
  );
  ```

- Ensure `c1` > 0 and values in `c1` >= `c2`:
  ```sql
  CREATE TABLE t (
    c1 INT, 
    c2 INT, 
    CHECK (c1 > 0 AND c1 >= c2)
  );
  ```

- Set values in `c2` column not NULL:
  ```sql
  CREATE TABLE t (
    c1 SERIAL PRIMARY KEY, 
    c2 VARCHAR NOT NULL
  );
  ```
	

### MODIFYING DATA

- Insert one row into a table:
  ```sql
  INSERT INTO t(column_list) VALUES(value_list);
  ```

- Insert multiple rows into a table:
  ```sql
  INSERT INTO t(column_list) VALUES (value_list), (value_list), ...;
  ```

- Insert rows from `t2` into `t1`:
  ```sql
  INSERT INTO t1(column_list) SELECT column_list FROM t2;
  ```

- Update new value in the column `c1` for all rows:
  ```sql
  UPDATE t SET c1 = new_value;
  ```

- Update values in the column `c1`, `c2` that match the condition:
  ```sql
  UPDATE t SET c1 = new_value, c2 = new_value WHERE condition;
  ```

- Delete all data in a table:
  ```sql
  DELETE FROM t;
  ```

- Delete subset of rows in a table:
  ```sql
  DELETE FROM t WHERE condition;
  ```
	
	
### MANAGING VIEWS

- Create a new view that consists of `c1` and `c2`:
  ```sql
  CREATE VIEW v(c1, c2) AS SELECT c1, c2 FROM t;
  ```

- Create a new view with a check option:
  ```sql
  CREATE VIEW v(c1, c2) AS SELECT c1, c2 FROM t WITH [CASCADED | LOCAL] CHECK OPTION;
  ```

- Create a recursive view:
  ```sql
  CREATE RECURSIVE VIEW v AS select-statement -- anchor part UNION [ALL] select-statement; -- recursive part
  ```

- Create a temporary view:
  ```sql
  CREATE TEMPORARY VIEW v AS SELECT c1, c2 FROM t;
  ```

- Delete a view:
  ```sql
  DROP VIEW view_name;
  ```
	

### MANAGING INDEXES

- Create an index on `c1` and `c2` of the table `t`:
  ```sql
  CREATE INDEX idx_name ON t(c1, c2);
  ```

- Create a unique index on `c3` and `c4` of the table `t`:
  ```sql
  CREATE UNIQUE INDEX idx_name ON t(c3, c4);
  ```

- Drop an index:
  ```sql
  DROP INDEX idx_name;
  ```


### SQL AGGREGATE FUNCTIONS

- `AVG` returns the average of a list:
  ```sql
  SELECT AVG(column_name) FROM table_name;
  ```

- `COUNT` returns the number of elements in a list:
  ```sql
  SELECT COUNT(column_name) FROM table_name;
  ```

- `SUM` returns the total sum of a list:
  ```sql
  SELECT SUM(column_name) FROM table_name;
  ```

- `MAX` returns the maximum value in a list:
  ```sql
  SELECT MAX(column_name) FROM table_name;
  ```

- `MIN` returns the minimum value in a list:
  ```sql
  SELECT MIN(column_name) FROM table_name;
  ```
	

### MANAGING TRIGGERS

- Create or modify a trigger:
  ```sql
  CREATE OR MODIFY TRIGGER trigger_name
  WHEN EVENT
  ON table_name FOR EACH ROW|STATEMENT
  EXECUTE FUNCTION stored_procedure_name(arguments);
  ```

- Events and Trigger Types:
  - `BEFORE` – invoke before the event occurs.
  - `AFTER` – invoke after the event occurs.
  - `EVENT` can be `INSERT`, `UPDATE`, or `DELETE`.
  - `TRIGGER_TYPE` can be `FOR EACH ROW` or `FOR EACH STATEMENT`.

- Example of creating a trigger invoked before a new row is inserted:
  ```sql
  CREATE TRIGGER before_insert_person
  BEFORE INSERT ON person
  FOR EACH ROW
  EXECUTE FUNCTION stored_procedure_name();
  ```

- Delete a specific trigger:
  ```sql
  DROP TRIGGER trigger_name ON table_name;
  ```
