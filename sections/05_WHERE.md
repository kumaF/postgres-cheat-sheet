## PostgreSQL WHERE

### Overview 
Learn how to use PostgreSQL `WHERE` clause to filter rows returned by a `SELECT` statement.

### Syntax

```
SELECT
    select_column_list
FROM
    schema_name.table_name
WHERE
    condition
```

### Examples

1) `WHERE` clause with the equal `(=)` operator
    ```
    SELECT first_name, last_name
	FROM public.customer
    WHERE first_name = 'Jamie';
    ```

2) `WHERE` clause with the `AND` operator
    ```
    SELECT first_name, last_name
	FROM public.customer
    WHERE first_name = 'Jamie' AND last_name = 'Rice';
    ```

3) `WHERE` clause with the `OR` operator
    ```
    SELECT first_name, last_name
	FROM public.customer
    WHERE first_name = 'Adam' OR last_name = 'Rodriguez';
    ```

4) `WHERE` clause with the `IN` operator
    ```
    SELECT first_name, last_name
	FROM public.customer
    WHERE first_name IN ('Ann', 'Anne', 'Annie');
    ```

5) `WHERE` clause with the `LIKE` operator
    ```
    SELECT first_name, last_name
	FROM public.customer
    WHERE first_name LIKE 'Ann%';
    ```

6) `WHERE` clause with the `BETWEEN` operator
    ```
    SELECT first_name, LENGTH(first_name) AS name_length
	FROM public.customer
    WHERE first_name LIKE 'A%' AND LENGTH(first_name) BETWEEN 3 AND 5
    ORDER BY name_length;
    ```

7) `WHERE` clause with the not equal `(<>)`, `(!=)` operator
    ```
    SELECT first_name, last_name
	FROM public.customer
    WHERE first_name LIKE 'Ann%' AND last_name != 'Hill';
    ```

### Summary
- It's possible to use `WHERE` clause in the `SELECT`, `UPDATE` and `DELETE` statements to specify rows.
- To form the condition in the `WHERE` clause, use comparison and logical operators such as,
  - Equal `(=)`
  - Greater than `(>)`
  - Less than `(<)`
  - Greater than or equal `(>=)`
  - Less than or equal `(<=)`
  - Not equal `(<>)` or `(!=)`
  - `AND` operator
  - `OR` operator
  - `IN` operator
  - `BETWEEN` operator
  - `LIKE` operator
  - `IS NULL` operator
  - `NOT` operator
- If you use column aliases in the `SELECT` clause, you cannot use them in the `WHERE` clause.