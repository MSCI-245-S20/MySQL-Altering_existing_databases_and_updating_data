### Introducing the `UPDATE` SQL keyword

The `UPDATE` SQL keyword lets us __update the records from existing database tables__.

Let's inspect the data from the `trips` table.

First, do a `USE EPDriver;` to _use_ the appropriate database and then:

```
mysql> SELECT * FROM trips;
```

You should see this output:

```
+----+---------------------+---------------------+-----------------+
| id | trip_datetime_start | trip_datetime_end   | trip_total_fare |
+----+---------------------+---------------------+-----------------+
|  1 | 2015-09-15 03:20:59 | 2015-09-15 03:54:08 |           79.40 |
|  2 | 2015-09-15 20:44:17 | 2015-09-15 21:18:58 |           91.79 |
|  3 | 2015-09-15 04:01:04 | 2015-09-15 04:20:18 |           17.67 |
|  4 | 2015-09-15 22:56:33 | NULL                |            0.00 |
|  5 | 2015-09-15 21:12:33 | 2015-09-15 22:00:00 |           92.33 |
|  6 | 2015-09-15 07:14:59 | 2015-09-15 08:24:19 |           85.38 |
|  7 | 2015-09-15 15:48:41 | NULL                |            0.00 |
|  8 | 2015-09-15 09:40:55 | 2015-09-15 10:05:32 |           43.73 |
|  9 | 2015-09-15 10:00:08 | NULL                |            0.00 |
| 10 | 2015-09-15 14:57:24 | 2015-09-15 15:11:26 |            4.50 |
+----+---------------------+---------------------+-----------------+
10 rows in set (0.00 sec)
```

We'll keep an eye on the `id`'s where the user hasn't finished the trip yet. 
Can you guess which `id`'s these are?