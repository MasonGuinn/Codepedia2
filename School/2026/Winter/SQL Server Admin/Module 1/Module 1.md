---
backward: "[[Area Template]]"
parent: "[[Development]]"
forward: "[[Topic Template]]"
order: 99
tags:
  - topic
---
> *Created: <%+ tp.file.creation_date("M/D/YYYY @ h:mm A") %>*
> *Modified: <%+ tp.file.last_modified_date("M/D/YYYY @ h:mm A") %>*

# Lecture 1 Quiz
```flashy
Which language is used for inserting, updating, deleting, and selecting data in a database?
Data Definition Language (DDL)
=Data Manipulation Language (DML)
Data Control Language (DCL)
Structured Query Language (SQL)
---
Which phase of the database lifecycle involves creating an Entity Relationship Diagram (ERD)?
Normalization
=Database design
Query optimization
Authentication and authorization
---
What is the main purpose of the normalization process in database design?
To increase data duplication
=To prevent data anomalies
To simplify the database structure
To remove all tables from the database
---
What is the purpose of a query optimizer in a database system?
To create graphical user interfaces
To manage database security
To optimize data integrity
=To make queries faster and more efficient
---
What is SQL Server primarily used for?
Graphic design
Video editing
=Relational database management
Web development
```

# Lecture 2 Quiz
```flashy
Which edition of SQL Server offers high-end data center capabilities, unlimited virtualization, and end-to-end business intelligence?
SQL Server Standard Edition
SQL Server Web Edition
SQL Server Developer Edition
=SQL Server Enterprise Edition
---
Which SQL Server management tool is primarily used for interacting with SQL Server?
SQL Server Configuration Manager
SQL Server Profiler
SQL Server Data Tools
=SQL Server Management Studio
---
What is the primary purpose of SQL Server Profiler?
To manage services and network protocols.
To automate the physical design of databases.
=To record database and server activities for performance analysis.
To create SQL Server Relational Databases.
---
What is the primary use of a Docker container when installing SQL Server on a Mac?
To run SQL Server directly on the OS.
To install SQL Server on a domain controller.
=To provide lightweight and standalone packages for SQL Server.
To install SQL Server on a Linux machine.
---
What is the minimum number of cores for core-based licensing?
Two cores
=Four cores
Six cores
Eight cores
```

# Lecture 3 Quiz

```flashy
What should you consider when deciding which features to install?
Install all available features for better performance
=Minimize the footprint of the SQL Server instance based on business requirements
Install features randomly and adjust later
Features cannot be added or removed after installation
---
What is the purpose of creating multiple Active Directory accounts for services in a production environment?
To complicate the installation process
To avoid creating any accounts
To simplify account management
=To enhance security by isolating service accounts
---
Which authentication mode provides both Windows authentication and SQL Server authentication?
Single authentication mode
=Mixed mode authentication
Dual authentication mode
Hybrid authentication mode
---
What should you consider when assigning permissions to users during SQL Server installation?
Give permissions to all users by default
=Assign permissions to users with the least privileges necessary
Assign permissions only to administrators
Permissions cannot be modified after installation
---
What is the purpose of setting Active Directory accounts for services during installation?
It’s not necessary, as services can use default accounts
To increase the installation speed
To ensure SQL Server can connect to the internet
=To allow services to run with appropriate permissions and security
```

# Lecture 4 Quiz
```flashy
Why is it recommended to avoid giving the administrator full control over the database server?
It slows down the server performance
It limits the administrator’s capabilities
=It increases the risk of unauthorized access
It interferes with SQL Server integration
---
What are the different startup types for services mentioned in the video?
Instant, automatic, and delayed
Immediate, delayed, and suspended
=Manual, automatic, and disabled
On-demand, scheduled, and adaptive
---
What is the purpose of the SQL Server Integration Services (SSIS)?
To manage database engine services
To perform analysis on data
To manage integration with Active Directory
=To get data in and out of SQL Server
---
What type of permissions should be assigned to users during SQL Server installation?
Full control permissions for all users
=Minimal permissions required for their tasks
Administrator-level permissions for all users
No permissions, as they can be assigned later
---
What type of SQL Server instance is being installed in the video?
Clustered instance
Default instance
=Named instance
Virtual instance
```


# Module 1 Quiz
```flashy
SQL is:
Language for network databases 
Structured Language 
=Structured Query Language 
Structured Qualified Language 
---
Which is NOT a database property?
Every single data item in the table must be single valued 
Columns in a table do not have any particular order 
In a table, there are never two identical rows 
=Rows in a table must have a particular order. 
---
SQL Servers flavor of SQL is:
=Transact SQL 
PL/SQL 
SparkSQL 
PostgreSQL 
---
What is DML?
Data Modification Language 
=Data Manipulation Language 
Defined Modification Language 
None of the above 
---
A common reason that SQL Server installation might fail is because the Windows OS is not up to date with service packs or security updates.
=True 
False 
---
Which of the following is a portal that hosts online documentation, tutorials, and user forums for Microsoft products?
=TechNet 
MSN 
MicroForums 
NetInfo 
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
Which of the following is the core component within a database that control data storage and access requests from client applications?
replication server 
query handler 
control module 
=database engine 
---
What type of Windows Server should you NOT install SQL Server for security reasons?
file server 
application server 
=domain controller 
authentication controller 
---
SQL Server 2019 can be installed on a 32 bit system.
True 
=False 
---
What feature of SQL Server provides high end datacenter capabilities with fast performance, unlimited virtualization, and end to end business intelligence for a production environment?
Standard 
Developer 
Web 
=Enterprise 
---
An install of SQL Server is called:
A database
=An instance
A cluster
A service
---
An isolated guest operating system installed on top of a normal operating system:
Container
Docker
=Virtual machine
Hypervisor
---
A user-centric licensing model:
=CAL
Core-based
Open Source
Per-processor
---
A processor with more than one core processing unit:
Hyper-threaded
=Multicore processor
Virtual processor
Unit-core
---
What are the SQL Server Authentication modes?
Windows 
Server 
=Mixed Mode 
high availability 
---
Which of the following is an edition of SQL Server?
Datacenter 
Public 
=Enterprise 
Essential 
---
Which of the following is NOT a recommended minimum requirement for running SQL Server 2019 Standard?
1 GB memory 
=500 MHz processor 
6 GB hard-disk space 
IE 7 
---
Which SQL Server Edition offers all functionality of Enterprise edition but can not be used on a Production Server?
Enterprise 
Web 
=Developer 
Express 
---
Which SQL Server edition is targeted at hosted, Internet-facing deployments?
Developer 
Standard 
Express 
=Web 
---
Mixed Mode allows for:
mixed users to log in 
Only windows users to log in 
Only SQL users to log in 
=Windows and SQL users to log in 
---
Which of the following SQL Server editions is not a good choice if you want to use Business Intelligence on your production server?
=Web 
Developer 
Standard 
Enterprise
```