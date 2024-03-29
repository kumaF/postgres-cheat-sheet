## PostgreSQL `LIMIT`

### Overview 
Learn how to use the PostgreSQL `LIMIT` clause to get a subset of rows generated by a query.

### Syntax

```
SELECT
    select_column_list
FROM
    schema_name.table_name
LIMIT
    row_count
OFFSET
    rows_to_skip
```

### Examples

1) `LIMIT` to constrain the number of returned rows
    
    ```
    SELECT first_name, last_name
    FROM public.customer
    LIMIT 5;
    ```
2) `LIMIT` with `OFFSET`
   
    ```
    SELECT first_name, last_name
	FROM public.customer
    LIMIT 5 OFFSET 3;
    ```
3) `LIMIT` `OFFSSET` to get top / bottom N rows
    
    ```
    SELECT first_name, last_name
	FROM public.customer
    ORDER BY customer_id DESC
    LIMIT 5 OFFSET 3;
    ``````

### Summary
- `LIMIT` is an optional clause.
- Use `OFFSET` clause to skip number of rows.
- Make sure to use the `ORDER BY` clause to control the row order