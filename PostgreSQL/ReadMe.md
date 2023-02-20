# PostgreSQL Processor

Once you have `postgres.zip` contents extracted in the folder where `SpotAssist.exe` is running, you have the ability to work with any PostgreSQL databases and from any place which allows you to type the following commands/queries and execute. Here execute means, just select and copy. That's it.

The following code sample having 3 lines will show you the SQL objects that are available in the connected database.

```
~>process-postgres
=>your_connection_string_here
SELECT * FROM sqlite_schema;
```

## What are they?
1. First line is instruction for what type of application we are invoking.
2. Second line is your connection string. This could be your template recalling as done here. `=>your_connection_string_here` will automatically replace with the connection string that was created as template.
3. From line 3 onwards, you start with actual SQL queries.
4. Once you copy, you will see the output in your default browser.

Note: Check the console for any errors, if its' not working for you.
