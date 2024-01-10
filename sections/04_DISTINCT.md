## PostgreSQL `DISTINCT`

### Overview 
Learn how to use the PostgreSQL `SELECT` `DISTINCT` clause to remove duplicate rows from a result set returned by a query.

### Syntax

```
SELECT
   DISTINCT select_column_list
FROM
   schema_name.table_name;
```

```
SELECT
   DISTINCT ON (distinct_column_list) select_column_list
FROM
   schema_name.table_name;
```

### Examples

1) `DISTINCT` one column
   
   ```
   SELECT DISTINCT district
   FROM public.address
   ORDER BY district ASC;
   ```
2) `DISTINCT` multiple columns
   
   ```
   SELECT DISTINCT district, city_id
   FROM public.address
   ORDER BY district ASC, city_id ASC;
   ```
3) `DISTINCT` on columns
   
   ```
   SELECT DISTINCT ON (district) district, city_id
   FROM public.address
   ORDER BY district ASC, city_id ASC;
   ```

### Summary
- Use `DISTINCT` clause to remove duplicate rows from a result set.
- Use `DISTINCT ON (expression)` to keep the **first** row of each group of duplicates.