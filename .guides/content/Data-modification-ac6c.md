The reason why we set up the `trips` table with the data type definition we displayed by using the `SHOW COLUMNS FROM trips;` statement is because the user follows this process whenever he/she takes a car:

1. The user requests the vehicle and the driver gets notified
2. The user starts the trip and a new `trip_datetime_start` value is created which cannot be `NULL`
3. The user finishes the trip and the app registers an ending datetime

As you can see, some data may not exist in the table only after the user finishes the trip. 

In this case, even though some data has been inserted into the table, specific table rows must be updated later on. 

### Introducing the `UPDATE` SQL keyword

The `UPDATE` SQL keyword let us update the records from existing database tables.

Let's inspect the data from the `trips` table: 

```
mysql> SELECT * FROM trips;
```

You should see this output:

```

```