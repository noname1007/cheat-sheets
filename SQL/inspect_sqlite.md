# SQLite

[SQLite](https://www.sqlite.org/) is a database engine written in the C programming language.

## Inspect a database

To access a database type
```sql
sqlite3 [DATABASE]
```
See the tables in the database by using the tables command.
```sql
sqlite> .tables
```
At this point we can dump all of the data from the table.
```sql
PRAGMA table_info(tablename);
SELECT * FROM tablename;
```