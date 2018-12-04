1. What is the target of Azure SQL Databases.

Azure SQL Database provides a relational database as a service, targeted at online transaction processing (OLTP; that is, data entry and retrieval transactions) workloads.

2. By default, how many logical SQL Database servers can you have per Azure subscription?

By default, you can have up to six logical SQL Database servers per Azure subscription.

3. Why does the connection string set the TrustServerCertificate property to False and the Encrypt
property to True?

This is to provide additional protection while accessing SQL Database over the Internet. Doing so helps thwart potential man-in the-middle attacks.

4. What are transient errors?

Transient errors are errors that are intermittent and likely will be resolved if the command is retried.

5. What three things contribute to the total cost for running a SQL Server deployment on Azure Virtual
Machines?

First is the cost of the Windows VM itself. Recall that Azure VMs are charged on a per-minute usage model. Second is the SQL Server license cost. When using a SQL Server image from the Azure Marketplace, you will pay an additional per-minute SQL Server license cost, which varies according to the version of SQL Server (Web, Standard, or Enterprise) and the target size of the VM. Finally, you’ll also pay for the Azure Storage cost.

6. Why do you need to be concerned about high availability and disaster recovery for SQL Server in Azure
Virtual Machines?

Azure provides high-availability features for the VMs, but not necessarily for SQL Server running on the VM. It is possible for the VM to be online but the SQL Server instance to be offline, unhealthy, or both. Additionally, it is possible for the VM to unavailable due to hardware failure or software upgrades. Therefore, a practiced HADR strategy should be considered.

7. What are six SQL Server features that are not currently supported in SQL Database (according to the
book)?

Windows authentication. FILESTREAM data. Database mirroring. Extended stored procedures. SQL Server Agent/Jobs. SQL Server Reporting Services (SSRS) and SQL Server Integration Services (SSIS) are not supported.

8. Name four factors to consider when choosing between SQL Database and SQL Server in Azure Virtual
Machines.

Database size, existing application versus new application, level of administrative control (including hardware infrastructure), business continuity strategy, and hybrid scenarios.

9. Who did Microsoft collaborate with to bring their ClearDb database as a service for MySQL to the
Azure platform?

SuccessBrick.

10. What two options exist in Azure if you don't need a relational database management system (RDBMS) based
data storage solution such as SQL Database or SQL Server in Azure Virtual Machines?

Using a NoSQL service such as DocumentDB or Azure Table storage is also an option. 
