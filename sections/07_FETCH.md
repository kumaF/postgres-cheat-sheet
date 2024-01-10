## PostgreSQL `FETCH`

### Overview 
Learn how to use the PostgreSQL `FETCH` clause to retrieve a portion of rows returned by a query.

### Syntax

```
SELECT
    select_column_list
FROM
    schema_name.table_name
OFFSET
    start { ROW | ROWS }
FETCH
    { FIRST | NEXT } [ row_count ] { ROW | ROWS } ONLY
```

### Examples

1) `FETCH` clause to select first customer
    
    ```
    SELECT first_name, last_name
	FROM public.customer
    ORDER BY customer_id ASC
    FETCH FIRST ROW ONLY;
    ```
    is equivalent to

    ```
    SELECT first_name, last_name
	FROM public.customer
    ORDER BY customer_id ASC
    FETCH FIRST 1 ROW ONLY;
    ```
2) `FETCH` clause to select first five customers
    
    ```
    SELECT first_name, last_name
	FROM public.customer
    ORDER BY customer_id ASC
    FETCH FIRST 5 ROWS ONLY;
    ```
3) `FETCH` `OFFSSET` to get top / bottom N rows
    
    ```
    SELECT first_name, last_name
	FROM public.customer
    ORDER BY customer_id ASC
    OFFSET 5 ROWS
    FETCH NEXT 5 ROWS ONLY;
    ```

### Summary
- `ROW` is the synonym for `ROWS`, `FIRST` is the synonym for `NEXT`. So you can use them interchangeably.
- The `OFFSET` value is an integer that must be zero or positive. By default, it is zero if the `OFFSET` clause is not specified.
- The `FETCH` value is an integer that must be one or greater. By default, it is 1 if you do not specify it explicitly.