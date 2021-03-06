|||info
### Reset section database
If you make a mistake while editing the `EPDriver` database in this set of sections or just want to reset the database back to its original state, return to this page and click the “Reset Section Database” button below.

{Reset Section Database}(node .guides/sqltests/fw-sql-reset-epdriver.js)
|||
---

In order to illustrate the SQL `UPDATE` functionality, we created an __*Easy Private Driver App*__ schema, `EPDriver` for short, that represents the storage of some of the data from an app that enables users to hire private drivers.

Click on the `mysql>` prompt in the left pane and verify that the `EPDriver` database exists by executing the `SHOW DATABASES;` statement.

You should see this: 

```
+--------------------+
| Database           |
+--------------------+
| information_schema |
| EPDriver           |
| ... more db's      |
+--------------------+
```

Use the `EPDriver` schema and display its tables:

```
mysql> USE EPDriver;
```

```
mysql> SHOW TABLES;
```

This is the result:

```
+--------------------+ 
| Tables_in_EPDriver | 
+--------------------+ 
| drivers            |
| trips              |
| users              |
+--------------------+
3 rows in set (0.00 sec)
```

--- 
Let's evaluate the `table` columns' data types in the next section.