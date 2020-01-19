## Postgres Indexes

You can read good tutors [here](https://www.postgresqltutorial.com/postgresql-indexes/)

---

First read [open and setup PSQL](https://github.com/alexyndr/alexyndr.github.io/blob/master/postgres-cheatsheet.md)

### - Create Index

`CREATE INDEX simple_index ON table_name (column_name);`

Duplicate values are allowed

### - Show created Indexes

`=# \d table_name`

Indexes:
"table_name_pkey" PRIMARY KEY, btree (id)
"simple_index" btree (column_name)  # previous created index

---

### - Show all indexes of your database_name

`SELECT * FROM pg_indexes;`

You will see all available indexes of your database_name

---

### - Also you can modifine output of indexes

`SELECT indexname,indexdef FROM pg_indexes WHERE tablename = 'table_name';`

| indexname       | indexdef |
|-----------------|:--------:|
| table_name_pkey | CREATE UNIQUE INDEX table_name_pkey ON public.table_name USING btree (id) |
| simple_index    | CREATE INDEX simple_index ON public.table_name USING btree (column_name)  |

(2 rows)

---

### - Create Multicolumn Index

`CREATE INDEX multiply_index_name ON table_name (column1, column2);`

Duplicate values are allowed

You can read more [here](https://www.postgresqltutorial.com/postgresql-indexes/postgresql-multicolumn-indexes/)

---

### - Create UNIQUE index

`CREATE UNIQUE INDEX unique_index_name ON table_name (column1, column2);`

Duplicate values are not allowed

---

### - Drop Index

`DROP INDEX title_index;`

---

### - PostgreSQL Index Types

Read about types [here](https://www.postgresqltutorial.com/postgresql-indexes/postgresql-index-types/)
