1. **What is a temporal table?**

A type of user table designed to keep a full history of data changes and allow easy point-in-time analysis.

2. **Under what circumstances would you use a temporal table? Temporal tables are in widespread use in certain kinds of businesses.**

When you need to keep track of relevant changes.

3. **What are the semantics of a temporal table? There are seven of them.**

■ A primary key
■ Two columns defined as DATETIME2 with any precision, which are non-nullable and represent the start and end of the row’s validity period in the UTC time zone
■ A start column that should be marked with the option GENERATED ALWAYS AS ROW START
■ An end column that should be marked with the option GENERATED ALWAYS AS ROW END
■ A designation of the period columns with the option PERIOD FOR SYSTEM_TIME (<startcol>, <endcol>)
■ The table option SYSTEM_VERSIONING, which should be set to ON
■ A linked history table (which SQL Server can create for you) to hold the past states of modified rows

4. **How do you search a history table?**

SELECT ... FROM <table_or_view> FOR SYSTEM_TIME <subclause> AS <alias>;

5. **How do you modify a history table?**

Using INSERT, UPDATE, DELETE, and MERGE but they can only be done on the current table.

6. **How do you delete date from a history table? Why would you want to delete data from a history table?**

you don't

7. **How do you search a history table?**

SELECT ... FROM <table_or_view> FOR SYSTEM_TIME <subclause> AS <alias>;

8. **How do you query all data from both a history ﬁle and the current data?**

SELECT empid, empname, department, salary, sysstart, sysend FROM dbo.Employees FOR SYSTEM_TIME ALL;

9. **How do you drop a temporal table?**

Using ALTER TABLE and SET (system_versioning = off) to change the history table to a normal table, then DROP TABLE
