---
backward: "[[SQL Server Admin]]"
parent: "[[SQL Server Admin]]"
forward: "[[SSMS, System DBs & Physical Structure]]"
order: 1
tags:
  - test
---
> *Created: <%+ tp.file.creation_date("M/D/YYYY @ h:mm A") %>*
> *Modified: <%+ tp.file.last_modified_date("M/D/YYYY @ h:mm A") %>*

```flashy
Which is NOT a database property?
Every single data item in the table must be single valued
Columns in a table do not have any particular order
In a table, there are never two identical rows
=Rows in a table must have a particular order.
---
SQL is:
Language for network databases
Structured Language
=Structured Query Language
Structured Qualified Language
---
What is DML?
Data Modification Language
=Data Manipulation Language
Defined Modification Language
None of the above
---
SQL Servers flavor of SQL is:
=Transact SQL
PL/SQL
SparkSQL
PostgreSQL
---
What are the SQL Server Authentication modes?
Windows
Server
=Mixed Mode
high availability
---
Which of the following is the core component within a database that control data storage and access requests from client applications?
replication server
query handler
control module
=database engine
---
SQL Server 2019 can be installed on a 32 bit system.
True
=False
---
Which of the following SQL Server editions is not a good choice if you want to use Business Intelligence on your production server?
=Web
Developer
Standard
Enterprise
---
Which of the following can be described as an isolated guest operating system installed on top of a normal operating system?
=virtual machine
physical server
host computer
emulated PC
---
Which SQL Server Edition offers all functionality of Enterprise edition but can not be used on a Production Server?
Enterprise
Web
=Developer
Express
---
What type of Windows Server should you NOT install SQL Server for security reasons?
file server
application server
=domain controller
authentication controller
---
A common reason that SQL Server installation might fail is because the Windows OS is not up to date with service packs or security updates.
=True
False
---
An install of SQL Server is called:
CAL
SQL
domain controller
virtual machine
multicore processor
=an instance
---
An isolated guest operating system installed on top of a normal operating system is called:
CAL
SQL
domain controller
=virtual machine
multicore processor
an instance
---
A user-centric licensing model is called:
=CAL
SQL
domain controller
virtual machine
multicore processor
an instance
---
A database programming language is called:
CAL
=SQL
domain controller
virtual machine
multicore processor
an instance
---
A server running a version of the Windows Server operating system, with Active Directory Domain Services (AD DS) installed is called:
CAL
SQL
=domain controller
virtual machine
multicore processor
an instance
---
A processor with more than one core processing unit is called:
CAL
SQL
domain controller
virtual machine
=multicore processor
an instance
---
Which of the following ultimately determines which SQL Server edition is most suited for a particular application?
=business requirements
application version
product cost
system requirements
---
What feature of SQL Server provides high end datacenter capabilities with fast performance, unlimited virtualization, and end to end business intelligence for a production environment?
Standard
Developer
Web
=Enterprise
---
Which of the following is a portal that hosts online documentation, tutorials, and user forums for Microsoft products?
=TechNet
MSN
MicroForums
NetInfo
---
Which of the following is an edition of SQL Server?
Datacenter
Public
=Enterprise
Essential
---
Which SQL Server edition is targeted at hosted, Internet-facing deployments?
Developer
Standard
Express
=Web
---
Which of the following is NOT a recommended minimum requirement for running SQL Server 2019 Standard?
1 GB memory
=500 MHz processor
6 GB hard-disk space
IE 7
---
Mixed Mode allows for:
mixed users to log in
Only windows users to log in
Only SQL users to log in
=Windows and SQL users to log in
---
Which SQL Server edition is a free entry level database?
=Express Edition
Datacenter
Business Intelligence
Standard
---
You can install SQL Server 2019 on:
Windows
Linux
Mac
=All the above
---
SQL Server 2012 is only available in 64-bit versions.
True
=False
---
Which of the following is true about the physical file structure of a SQL Server database?
=it must have at least one log and one data file
only a data file is required
there are two data files for every log file
log files organize data in tables and indexes
---
Which system database is recreated each time SQL Server starts?
Master
Model
=tempdb
resource
---
Data Discovery and Classification was introduced in:
SQL Server 2016
=SSMS 17.5
SSMS 2019
SQL Server 2018
---
Which of the following is NOT a system database on a SQL Server system?
model
master
=directory
resource
---
What are int, date, and bit examples of in a SQL database?
=data type
condition
column name
record
---
Which of the following is true about naming objects?
the database management system provides strict rules
=Camel case does not use special characters to link words
tables should always be named with a character prefix
A column name of Last Name is preferable to LastName
---
What should you always do before creating a new database?
=backup the master system database
install a fresh instance of SQL Server 2012
delete all existing temporary databases
stop and restart the SQL Server service
---
Which system database stores information on the structure of other databases and their components?
model
=master
msdb
tempdb
---
Which of the following is a way of organizing data, with defined rules for storing, manipulating, and retrieving data?
modeling format
virtual instance
physical architecture
=logical structure
---
Since it is easy to make configuration changes after a database is created, it’s best to get the database created and make changes as necessary afterward.
True
=False
---
Many tasks can be performed with SQL Server Management Studio, but to delete a database, you need to use a SQL statement in the SQLCMD command prompt.
True
=False
---
Which of the following is true about log files?
=they aid in database roll back
log files are optional for each database
there can be only one log file per database
they should be stored on the same physical disk as data files
---
It is best to store the data files in the default location.
True
=False
---
The column or combination of columns that uniquely identify each record within a table:
Object Explorer
table
constraint
extent
=primary key
foreign Key
---
A physical storage unit that is a collection of eight pages:
Object Explorer
table
constraint
=extent
primary key
foreign Key
---
A condition that imposes a limitation on a value or action:
Object Explorer
table
=constraint
extent
primary key
foreign Key
---
Organized as a two-dimensional structure consisting of rows and columns:
Object Explorer
=table
constraint
extent
primary key
foreign Key
---
Provides a tree view of the different database schema objects organized as a series of folders:
=Object Explorer
table
constraint
extent
primary key
foreign Key
---
Constructed based on a common field, and enforces Referential Integrity:
Object Explorer
table
constraint
extent
primary key
=foreign Key
---
Which of the following is a file extension used in the physical structure of a SQL database?
=.ldf
.mdb
.txt
.dbf
---
Which tool allows you to create SQL queries to be executed against a database?
Object Explorer
=Query Editor
Analysis Services
View Compiler
---
Which system database stores information related to jobs, schedules, and database backups?
tempdb
=msdb
model
master
---
Which of the following is a required setting that must be supplied when creating a database?
the SQL Server name
=a unique database name
the master database configuration
the user credentials
---
The master system database stores a database template that is used as a blueprint when creating a new user database.
True
=False
---
Which data format represents data as a series of ones and zeros?
=binary
octal
decimal
hex
---
Which of the following allows for importing and exporting of data?
=bcp
DBCC
sqlcmd
sqlservr
---
Log files:
are stored in pages
are deleted when the database restarts
=should not be stored on the same disk as the data files
store pointers to the data
---
Select the types of Extents.
Mixed Extent
Logical Extent
=Uniform Extent
Page Extent
---
Determining the correct datatype isn't important in SQL Server.
True
=False
---
Which of the following is commonly referred to as a record?
constraint
column
=row
attribute
---
The two main physical file types in an SQL Server database are data files and log files.
=True
False
---
Which of the following is true about the Autogrowth setting?
by default, it doubles the size of the log file when it becomes full
the data file is affected by it but log files are not
you should keep this value as small as possible
=you should configure it so that file growth occurs infrequently
---
Data is stored in a _________.
Row Header
Mixed Extent
Uniform Extent
=Page
---
Which of the following is true about the model database template?
it cannot be customized
changes to it will affect existing databases
=new databases will inherit settings from it
modifying model database settings requires different steps than user databases
---
Which of the following is true about filegroups?
filegroups are only used when there is more than one data file
there can be only one data file per filegroup
=each database must have a primary filegroup
multiple data files should be of different sizes for best performance
---
The primary purpose of a database is to organize and store data in a secure manner.
=True
False
---
sqlcmd ____.
is a cross platform interactive command-line tool
must have Python installed
is used to start an instance
=is used to enter TSQL statements from the prompt
---
Which command returns all the columns for records in which the value of Col1 is greater than 10 but has a value less than Col2?
::
=%sql SELECT * FROM Table1 WHERE Col1 < Col2 AND Col1 > 10%
%sql SELECT ALL FROM Table1 WHEN Col1 < Col2 OR Col1 > 10%
%sql SELECT * FROM Table1 IF Col1 > 10 BUT Col1 < Col2%
%sql SELECT ALL FROM Table1 LIKE Col1 > 10 NOT Col1 < Col2%
---
A database operation that can be used to merge and retrieve data stored in more than one table view is called a SELECT.
True
=False
---
Which type of join returns all columns from both tables and only returns rows where the join column values are equal?
=inner
left outer
right outer
full outer
---
Which syntax should you use to sort the result set in reverse alphabetic order.
%sql ORDER ON [Column Name] Z-A%
%sql SORT REVERSE BY [Column Name]%
%sql SORT ON [Column Name] REVERSE%
=%sql ORDER BY [Column Name] DESC%
---
Which clause do you use with a join operation to specify which columns from each table should be used as the matching key?
FROM
=ON
BY
WITH
---
What type of functions are used to summarize data in a grouped column or for all records in a table?
Summary procedures
=Aggregate functions
Grouping statements
Totaling processes
---
Which of the following best describes the IntelliSense feature in Query Editor?
it is a database building wizard
=it is a text AutoComplete feature
it is a visual query builder
it is used to create tables
---
What are the keywords %sql CHECK%, %sql UNIQUE%, and %sql NOT NULL% referred to as?
limits
keys
=constraints
references
---
The most widely used component of the SQL language; provides the means to query data:
Check
DEFAULT
database context
=data manipulation language
REVOKE
EXCEPT
AND
OR
GRANT
---
An operator that returns rows from the first query that do not exist in the second query:
Check
DEFAULT
database context
data manipulation language
REVOKE
=EXCEPT
AND
OR
GRANT
---
A logical operator that specifies that all conditions must be true:
Check
DEFAULT
database context
data manipulation language
REVOKE
EXCEPT
=AND
OR
GRANT
---
A logical operator that specifies that any condition must be true:
Check
DEFAULT
database context
data manipulation language
REVOKE
EXCEPT
AND
=OR
GRANT
---
A constraint that causes the value of a field to be autopopulated on insertion of a record if the value is not specified:
Check
=DEFAULT
database context
data manipulation language
REVOKE
EXCEPT
AND
OR
GRANT
---
A constraint used to limit values of a column before a change is committed to the database:
=Check
DEFAULT
database context
data manipulation language
REVOKE
EXCEPT
AND
OR
GRANT
---
A SQL statement used to remove permissions directly from a database user or from a role:
Check
DEFAULT
database context
data manipulation language
=REVOKE
EXCEPT
AND
OR
GRANT
---
The database that is used by the database engine to resolve object names:
Check
DEFAULT
=database context
data manipulation language
REVOKE
EXCEPT
AND
OR
GRANT
---
A SQL statement used to assign permissions directly to a database user or via a role:
Check
DEFAULT
database context
data manipulation language
REVOKE
EXCEPT
AND
OR
=GRANT
---
Which command selects all columns in a table?
%sql SELECT #%
%sql SELECT ;%
=%sql SELECT *%
%sql SELECT @%
---
What keyword can you include in a SELECT statement to create a column alias for the column returned in the result set?
FROM
FOR
ALIAS
=AS
---
What is the name for the type of query where a SQL query is embedded within another SQL query?
nested query
embedded query
=subquery
inner query
---
Which of the following is true about the SQL language?
it is case sensitive
keywords must be written in uppercase
=the semicolon is a statement terminator
statement terminators are required at the end of a statement
---
If you want to remove duplicates from a result set, which command should you use?
%sql SELECT AS%
%sql SELECT UNIQUE%
%sql SELECT ONLY%
=%sql SELECT DISTINCT%
---
Which statement is used to modify column values of an existing row in a table?
ALTER
CHANGE
MODIFY
=UPDATE
---
If you want to compare a value in a column against a list of values, which syntax would you use?
::
%sql WHERE [Column Name] LIKE ([Value1], [Value2], [Value3])%
%sql WHERE [Column Name] = ([Value1], [Value2], [Value3])%
=%sql WHERE [Column Name] IN ([Value1], [Value2], [Value3])%
%sql WHERE [Column Name] EXISTS ([Value1], [Value2], [Value3])%
---
If Col1 contains the string “Hello” and Col2 is Null, what is the result of %sql SELECT Col1 + Col2%?
“Hello”
Error
=Null
“HelloNull”
---
Which of the following represents correct syntax for a SELECT statement?
::
=%sql SELECT [Column Name] FROM [Table Name]%
%sql SELECT [Object Name] FOR [Column Name];%
%sql SELECT [Database Name] From [Column Name];%
%sql SELECT [Table Name] FROM [Row Name]%
---
Transact-SQL is the variant of SQL developed by Microsoft and Sybase.
=True
False
---
A string concatenation operation evaluates to null if all of the input columns have a value.
True
=False
---
The database schema is defined by the DDL components in the SQL programming language.
=True
False
---
Which command will result in records that have a Col1 value greater than 100?
::
%sql SELECT Col1 FROM Table1 IF Col1 GT 100%
=%sql SELECT Col1 FROM Table1 WHERE Col1 > 100%
%sql SELECT Col1 > 100 FROM Table1%
%sql IF Col1 > 100 SELECT * FROM Table1%
---
SQL is an imperative programming language.
True
=False
---
Which type of merge statement only combines rows that exist in two result sets?
UNION
EXCEPT
=INTERSECT
JOIN
---
Which command returns the product of two columns returned in a column named ProdC1C2?
::
=%sql SELECT Col1 * Col2 AS ProdC1C2%
%sql SELECT AS ProdC1C2 Col1 x Col2%
%sql SELECT FROM Col1 * Col2 TOTAL ProdC1C2%
%sql SELECT (Col1, Col2) PRODUCT ProdC1C2%
---
Which command changes the database context?
%sql OPEN [Database Name]%
=%sql USE [Database Name];%
%sql SELECT [Database Name];%
%sql SWITCH [Database Name]%
---
SQL injection can allow the deletion of tables.
=True
False
---
The statement
%sql
CREATE VIEW Example1
AS
SELECT VendorName, SUM(InvoiceTotal) AS SumOfInvoices
FROM Vendors JOIN Invoices ON Vendors.VendorID = Invoices.VendorID
GROUP BY VendorName
ORDER BY VendorName;
%
::
will fail because the GROUP BY clause isn’t allowed in this view
will fail because the column alias SumOfInvoices is invalid
=will fail because the ORDER BY clause isn’t allowed in this view
will succeed
---
The %sql WITH SCHEMABINDING% clause of the %sql CREATE VIEW% statement:
protects the view by binding it to the database schema
prevents the tables that the view is based on from being deleted
=prevents the tables that the view is based on from being modified in a way that affects the view
all of the above
---
What is the correct code that calls the following stored procedure, passes the value ‘2011-12-01’ to its input parameter, and stores the value of its output parameter in a variable named @MyInvoiceTotal.
%sql
CREATE PROC spInvoiceTotal2
       @DateVar smalldatetime,
       @InvoiceTotal money OUTPUT
AS
SELECT @InvoiceTotal = SUM(InvoiceTotal)
FROM Invoices
WHERE InvoiceDate >= @DateVar;
%
::
%sql spInvoiceTotal2 '2011-12-01', @MyInvoiceTotal OUTPUT;%
=%sql EXEC spInvoiceTotal2 '2011-12-01', @MyInvoiceTotal OUTPUT%
%sql @MyInvoiceTotal =EXEC spInvoiceTotal2 '2011-12-01',%
---
The %sql WITH ENCRYPTION% clause of the %sql CREATE VIEW% statement:
prevents users from modifying the view
=prevents users from seeing the code that defines the view
prevents users from using the view without the appropriate authorization
causes the data that’s returned by the view to be encrypted
---
Parameters for stored procedures and functions can be of any valid SQL Server data type except:
date/time
=table
xml
numeric
---
Stored procedures should use dynamic sql statements.
True
=False
---
Stored procedures execute faster than an equivalent SQL script because stored procedures are ______________________________.
=precompiled
created by the system
scalar
encrypted
---
Data validation is the process of:
using the THROW statement to raise a custom error message
preventing errors due to incorrect Transact-SQL syntax
=preventing errors due to invalid data
trapping SQL Server errors so the user doesn’t see the system error message
---
A user-defined function:
=can return a single scalar value or a single table value
can return multiple scalar values or a single table value
can return multiple scalar values or multiple table values
can’t accept input parameters
---
If you delete a stored procedure, function, or trigger and then create it again:
you should use the %sql ALTER% statement
you delete the tables on
```