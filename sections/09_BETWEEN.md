## PostgreSQL `BETWEEN`

### Overview 
Learn how to use the PostgreSQL `BETWEEN` operator to match a value against a range of values.

### Syntax

```
SELECT
    select_column_list
FROM
    schema_name.table_name
WHERE
    column_value BETWEEN low AND high;
```

### Examples

1) `BETWEEN` operator in `WHERE` clause
    
    ```
    SELECT customer_id, payment_id, amount
    FROM public.payment
    WHERE amount BETWEEN 8 AND 10;
    ```
    is equivalent to

    ```
    SELECT customer_id, payment_id, amount
    FROM public.payment
    WHERE amount >= 9 AND amount <= 10;
    ```
2) `NOT BETWEEN` operator in `WHERE` clause
    
    ```
    SELECT customer_id, payment_id, amount
    FROM public.payment
    WHERE amount NOT BETWEEN 8 AND 10;
    ```
    is equivalent to

    ```
    SELECT customer_id, payment_id, amount
    FROM public.payment
    WHERE amount < 9 AND amount > 10;
    ```

### Summary
- Use `BETWEEN` operator to match a value against a range of values.
- `value BETWEEN low AND high` is equivalent to `value >= low and value <= high`.
- `value NOT BETWEEN low AND high` is equivalent to `value < low OR value > high`.
- Often use the `BETWEEN` operator in the `WHERE` clause of a `SELECT`, `INSERT`, `UPDATE` or `DELETE` statement.