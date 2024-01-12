## PostgreSQL `LIKE`

### Overview 
Learn how to use the PostgreSQL `LIKE` and `ILIKE` operators to query data using pattern matchings.

### Syntax

```
SELECT
    select_column_list
FROM
    schema_name.table_name
WHERE
    column_value LIKE pattern;
```

### Examples

1) `LIKE` operator in `WHERE` clause
    
    ```
    SELECT first_name, last_name
    FROM public.customer
    WHERE first_name LIKE '_her%';
    ```
2) `NOT LIKE` operator in `WHERE` clause
    
    ```
    SELECT first_name, last_name
    FROM public.customer
    WHERE first_name NOT LIKE '_her%';
    ```
3) `ILIKE` operator in `WHERE` clause

    ```
    SELECT first_name, last_name
    FROM public.customer
    WHERE first_name ILIKE '_her%';
    ```
4) `NOT ILIKE` operator in `WHERE` clause
    
    ```
    SELECT first_name, last_name
    FROM public.customer
    WHERE first_name NOT ILIKE '_her%';
    ```

### Summary
- Construct a pattern by combining literal values with wildcard characters and use the `LIKE` or `NOT LIKE` operator to find the matches.
- Percent sign `(%)` matches any sequence of zero or more characters.
- Underscore sign `(_)`  matches any single character.
- `ILIKE` operator matches value case-insensitively.