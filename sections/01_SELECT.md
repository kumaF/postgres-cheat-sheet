## PostgreSQL SELECT

### Overview 
Learn how to use the basic PostgreSQL `SELECT` statement to query data from a table.

### Syntax

```
SELECT
   select_column_list
FROM
   schema_name.table_name;
```

### Examples

1) `SELECT` one column from the table
   
   ```
   SELECT first_name
   FROM public.customer;
   ```
2) `SELECT` multiple columns from the table
   
   ```
   SELECT first_name, last_name
   FROM public.customer;
   ```
3) `SELECT` all columns from the table
   
   ```
   SELECT *first_name*
   FROM public.customer;
   ```
4) `SELECT` data with an expression
   
   ```
    SELECT 5 * 3;
   ```

### Summary

- If you specify a list of columns, you need to place a comma `(,)` between them.
- If you want to select data from all the columns, you can use an asterisk `(*)`.
- The select list may also contain expressions or literal values.
- specify the name of the table from which you want to query data after the `FROM` keyword.
- The `FROM` clause is optional. If you do not query data from any table, you can omit it.
- PostgreSQL evaluates the `FROM` clause before the `SELECT` clause.