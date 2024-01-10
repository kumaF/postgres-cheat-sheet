## PostgreSQL Column Alias

### Overview 
Learn about PostgreSQL column aliases and how to use column aliases to assign temporary names to columns in queries.

### Syntax

```
SELECT
    column_name AS alias_name
FROM
    schema_name.table_name;
```

```
SELECT
    column_name alias_name
FROM
    schema_name.table_name;
```

```
SELECT
    expression alias_name
FROM
    schema_name.table_name;
```

### Examples

1) Assigning a column alias to a column
    ```
    SELECT first_name, last_name as surname
    FROM public.customer;
    ```
2) Assigning a column alias to an expression
    ```
    SELECT first_name || ' ' || last_name as full_name
    FROM public.customer;
    ```
3) Column aliases that contain spaces
   ```
    SELECT first_name || ' ' || last_name as "Full Name"
    FROM public.customer;
    ```

### Summary
- Assign a column or an expression a column alias using the syntax `column_name AS alias_name` or `expression AS alias_name`.
- The `AS` keyword is optional.
- Use double quotes `(“)` to surround a column alias that contains spaces.