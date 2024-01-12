## PostgreSQL `IS NULL`

### Overview 
Learn how to use the PostgreSQL `IS NULL` operator to check if a value is NULL or not.

### Syntax

```
SELECT
    select_column_list
FROM
    schema_name.table_name
WHERE
    column_value IS NULL;
```

### Examples

1) `IS NULL` operator in `WHERE` clause
    
    ```
    SELECT first_name, last_name
    FROM public.customer
    WHERE phone IS NULL;
    ```
2) `IS NOT NULL` operator in `WHERE` clause
    
    ```
    SELECT first_name, last_name
    FROM public.customer
    WHERE phone IS NOT NULL;
    ```

### Summary
- The expression NULL = NULL returns false. This is because NULL is not equal to any value even itself.
- To check whether a value is NULL or not, you use the `IS NULL` operator instead.