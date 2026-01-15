---
backward: "[[Module 1]]"
parent: "[[SQL Server Admin]]"
forward: "[[Module 3]]"
order: 2
tags:
  - topic
---
> *Created: <%+ tp.file.creation_date("M/D/YYYY @ h:mm A") %>*
> *Modified: <%+ tp.file.last_modified_date("M/D/YYYY @ h:mm A") %>*

# Lecture 1 Quiz
```flashy
What is the main difference between MDF and LDF files in SQL Server databases?
=MDF files store data, while LDF files store log information
LDF files store data, while MDF files store log information
Both MDF and LDF files store data
MDF files store data, while LDF files store metadata
---
What is the recommended authentication mode to connect to SQL Server instances?
SQL Server Authentication
Mixed Mode Authentication
=Windows Authentication
Azure Authentication
---
Which classification level represents data with no risk to sensitive information?
=Public
General
Confidential
Highly Confidential
---
How can you create a new database using SQL Server Management Studio?
=Right-click the Databases folder, select New Database, and fill in the details
Use the Windows Command Prompt and enter a specific command
Download a pre-configured database template from the internet
Manually create new database files using a text editor
---
Which tool is used to create and execute Transact-SQL queries in SQL Server Management Studio?
Azure Data Studio
SQL Server Data Tools
SQL Server Query Analyzer
=Query Editor
```

# Lecture 2 Quiz
```flashy
What type of authentication is used to connect to the SQL Server instances in the video?
SQL Server Authentication 
Mixed Mode Authentication 
=Windows Authentication 
Azure Authentication 
---
What additional tool is installed along with SQL Server Management Studio in this release?
Microsoft Office Suite 
Microsoft Visual Studio 
SQL Server Data Tools 
=Azure Data Studio 
---
What is the primary purpose of SQL Server Management Studio?
To download SQL Server instances 
To manage Microsoft Office applications 
=To interact with SQL Server instances 
To create Windows authentication accounts 
---
What is the main advantage of using SQL Server Management Studio for database management?
It supports only SQL Server instances 
It has a limited set of features 
=It provides a graphical interface for tasks 
It requires advanced coding skills 
---
What SQL Server tool allows you to view and manage your SQL Server services?
Server Manager 
Administration Services 
Active Directory Manager 
=Configuration Manager
```

# Lecture 3 Quiz
```flashy
Which database is responsible for storing temporary tables and objects?
Master 
=TempDB 
Model 
Resource 
---
Which utility can be used for bulk copying data into or out of SQL Server?
SQL Server Management Studio 
SQL Server Agent 
SQL Command 
=BCP 
---
What is an extent in SQL Server’s storage architecture?
A unit of storage equal to 8 KB 
=A set of continuous 8 KB pages 
A database file 
A table partition 
---
What is the primary purpose of the master database in SQL Server?
It stores temporary data 
It stores user data 
=It contains system-level information about the SQL Server instance 
It maintains log records for transactions 
---
What is the purpose of the Model database in SQL Server?
It stores system tables and procedures 
It stores temporary data 
=It acts as a template for user-defined databases 
It maintains log records for transactions
```

# Lecture 4 Quiz
```flashy
If you get an error connecting to the Administrator’s desktop
Close the virtual machine 
=Click continue or OK 
Log in as Administrator 
None of the above 
---
Which data files do I attach first in the video?
Adventureworks 
=NwindSQL 
WorldWideImporters 
Defaultdatabase 
---
Which instance do I attach Nwindsql and restore Adventureworks to?
=The Default Instance 
The Named Instance 
Nwindsql Instance 
Adventureworks Instance 
---
Which account should I be logged into when attaching the databases?
=Administrator 
My user account 
The local user account 
Any account, doesn't really matter 
---
Which utility is used in the video to attach a database to a SQL Server instance?
SQL Server Configuration Manager 
SQL Server Profiler 
=SQL Server Management Studio 
SQL Server Data Tools
```

# Lecture 5 Quiz
```flashy
Should the foreign key be an identity column?
Yes, if the primary key it is referring to is an identity column.
=No, if the primary key it is referring to is an identity column it should be the int datatype
It doesn’t matter as long as the primary key column and the foreign key column have the same name.
No, it should be a varchar if the primary key it is referring to is an identity column.
---
Do I want you creating identity columns in the homework for this chapter?
Yes
=No
---
In the video I create the foreign key with the following specifications. (Choose 2)
The Primary key table is Products
=The Primary key table is Supplier and the Primary key is SupplierID
The foreign key table is Supplier and the foreign key field is SupplierID
=The foreign key table is Products and the foreign key is SupplierId
---
Which option determines the behavior of the transaction log in SQL Server?
Auto growth
=Recovery model
Collation setting
Page compression
---
What is the purpose of specifying a default filegroup for a data file?
=It determines the location of the data file
It ensures that the data file is encrypted
It determines the primary key for the data file
It determines the foreign key relationships in the data file
```