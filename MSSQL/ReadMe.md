# MS SQL Server Processor

Once you have `mssql.zip` contents extracted in the folder where `SpotAssist.exe` is running, you have the ability to work with any MSSQL databases and from any place which allows you to type the following commands/queries and execute. Here execute means, just select and copy. That's it.

The following code sample having 4 lines will show you the SQL objects that are available in the `AdventureWorksLT2019` database.

```
~>process-mssql
=>your_connection_string_here
USE AdventureWorksLT2019;
SELECT * FROM sys.objects;
```

When you copy the above code, you will see the following output.

![image](https://user-images.githubusercontent.com/109056087/217724237-b332b1db-24be-45c9-8666-463472b46ae8.png)


## What are they?
1. First line is instruction for what type of application we are invoking.
2. Second line is your connection string. This could be your template recalling as done here. `=>your_connection_string_here` will automatically replace with the connection string that was created as template.
3. From line 3 onwards, you start with actual SQL queries just like SSMS.
4. Once you copy, you will see the output in your default browser.

Note: Check the console for any errors, if its' not working for you.
