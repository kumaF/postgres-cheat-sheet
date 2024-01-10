## PostgreSQL ORDER BY

### Overview 
Learn how to sort the result set returned from the `SELECT` statement by using the PostgreSQL `ORDER BY` clause. 

### Syntax

```
SELECT
	select_column_list
FROM
	schema_name.table_name
ORDER BY
	sort_expression1 [ASC | DESC] [NULLS FIRST | NULLS LAST],
        ...
	sort_expressionN [ASC | DESC] [NULLS FIRST | NULLS LAST];
```

### Examples

1) Sort rows by one column
    ```
    SELECT first_name, last_name
    FROM public.customer
    ORDER BY first_name ASC;
    ```
2) Sort rows by multiple columns
    ```
    SELECT first_name, last_name
    FROM public.customer
    ORDER BY first_name ASC, last_name DESC;
    ```
3) Sort rows with NULL values
    ```
    SELECT first_name, last_name
    FROM public.customer
    ORDER BY first_name ASC NULLS FIRST
    ```

### Summary
- Use the `ORDER BY` clause to sort rows.
- Use the `ASC` option to sort rows in ascending order and `DESC` option to sort rows in descending order.
- The `ORDER BY` clause uses the `ASC` option by default.
- Use `NULLS FIRST` and `NULLS LAST` options to explicitly specify the order of nulls with other non-null values.