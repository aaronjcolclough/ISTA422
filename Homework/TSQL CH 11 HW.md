1. **Why do we use variables in T-SQL? How do you declare and initialize T-SQL variables?**

You use variables to temporarily store data values for later use in the same batch in which they were declared. Use a DECLARE statement to declare one or more variables, and use a SET statement to assign a value to a single variable.
DECLARE @i AS INT;
SET @i = 10;


2. **Describe what is meant by a batch file in T-SQL? What is the difference between batches and transactions?**

A batch is one or more T-SQL statements sent by a client application to SQL Server for execution as a single unit. A transaction is an atomic unit of work. A batch can have multiple transactions, and a transaction can be submitted in parts as multiple batches.

3. **What is the scope of variables with respect to T-SQL batches?**

A variable is local to the batch in which it’s defined.

4. **Write a T-SQL code snippet that returns a data element stating whether the current person can legally purchase alcohol, that is, has reached his 21st birthday.**



5. **(Not in book) Does T-SQL have a for loop construction?**

no but a while loop can be constructed

6. **What is a cursor? What is the difference between a relation and a cursor?**

cursor—a nonrelational result with order guaranteed among rows.

7. **How do you declare a temporary table? Why would you declare a temporary table?**

Most common scenario for using temporary tables is from within a stored procedure.
If there is logic inside a stored procedure which involves manipulation of data that cannot be done within a single query, then in such cases, the output of one query / intermediate results can be stored in a temporary table which then participates in further manipulation via joins etc to achieve the final result.
create table #Temp ( EventID int, EventTitle Varchar(50), EventStartDate DateTime, EventEndDate DatetIme, EventEnumDays int, EventStartTime Datetime, EventEndTime DateTime, EventRecurring Bit, EventType int )

8. **What is the difference between a stored procedure, a user defined function, and a trigger?**

A stored procedure is a user defined piece of code written in the local version of PL/SQL, which may return a value (making it a function) that is invoked by calling it explicitly.
User-defined functions are routines that accept parameters, perform an action, such as a complex calculation, and return the result of that action as a value. The return value can either be a single scalar value or a result set.
A trigger is a stored procedure that runs automatically when various events happen (eg update, insert, delete).

9. **Write a user defined function that returns a Boolean as to whether a customer may purchase alcohol as of the instant that the function runs.**



10. **Write a trigger that places a customer in the OFF LIMITS table if he attempt to purchase alcohol when he is underage.**



11. **Write a stored procedure that deletes customers from the OFF LIMITS table when they have reached their 21st birthday.**
