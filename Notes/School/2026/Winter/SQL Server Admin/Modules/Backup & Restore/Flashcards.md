```flashy
Which of the following is a reason that transaction logs must be backed up frequently?
so you don’t have to spend time backing up data files
frequent backups increase the likelihood of a corrupt active transaction log
=when the log is backed up, it is truncated
the tail of the log increases each time the log is backed up
---
How are full and differential database backups used?

a differential backup is followed by one or more full backups
full backups copy data that has changed since the last differential backup
=differential backups are usually performed more often than full backups
differential backups are more resource intensive than full backups
---
A Backup device is a logical storage device that references a physical location.
=True
False
---
Which of the following is true about log shipping?

=Allows you to have a warm standby Server
Log shipping supports automatic failover
Log Shipping does not provide redundancy
Log shipping is much like Raid 0
---
Which backup scheme reduces the amount of downtime to perform a restore but creates additional IT management and physical resource overhead?
=Full database backup plus differential database backup plus multiple transaction log backups
Single transaction log backup plus full database backup
Full database backup plus multiple transaction log backups
Single transaction log backup plus simple recovery model
---
Which of the following is NOT a commonly used type of backup plan?
Full database backup, simple recovery model
=Single transaction log backup plus simple recovery model
Single transaction log backup plus full database backup
Full database backup plus multiple transaction log backups
---
Which recovery model causes all operations to be written to the transaction log?

simple recovery model
=full recovery model
bulk logged recovery model
truncated recovery model
---
What SQL command do you use when restoring transaction logs if you want to do a point-in-time restore?
TIMELOG
TRANSACT
=STOPAT
NOTAFTER
---
The four Recover Models are: Full, Bulk-logged, BCP logged, and Simple.
True
=False
---
The AlwaysOn capabilities of SQL Server effectively replace the need to perform traditional backups.
True
=False
---
Which of the following is true about the factors that should be considered when evaluating database business requirements and the associated risk assessments?
mission-critical systems provide administrators with a large time window for performing maintenance
=databases that have a high change rate require more frequent backups
for best performance, backups should be done when the system is under peak load
a single large database is usually easier to maintain than several smaller databases
---
Which two ways can you back up and restore a database?
=Using Transact SQL
Using Windows restore option
=SSMS
the sp_bckup system stored procedure
---
Data loss caused by environmental events has the greatest possibility of occurrence.
True
=False
---
Which of the following is true about backup sets?
backup sets are usually stored to the same media as the database log
when the expiration date on a backup set passes, the data is no longer usable
backups made to tape are preferable to using disks due to better performance
=a backup device references a physical location where backup sets are stored
---
If you experience database corruption, what should you do before performing a restore operation?
=backup the transaction log tail
restore the head of the transaction log
perform a fresh full backup
check the physical integrity of the database
---
Which category of risk has the highest probability of occurrence?
=user error
hardware failure
system software failure
environmental events
---
Which of the following SQL commands should you perform in a database recovery operation when you have recovered the last transaction log?

RESTORE DATABASE <DatabaseName> FROM <BackupDevice> WITH NORECOVERY;
RESTORE LOG <LogFileName> FROM <BackupDevice> WITH FILE = n WITH NORECOVERY;
RESTORE DATABASE <DatabaseName> FROM <BackupDevice> WITH NORECOVERY;
=RESTORE DATABASE <DatabaseName> WITH RECOVERY;
---
Which of the following is true about the recovery point objective?
they should be the same for each database
the RTO is usually the same whether the recovery scenario involves one or many databases
the RTO is the maximum amount of data that may be lost
=the recovery point objective is expressed as a time frame
---
Transaction logs are required in the event that a database needs to be restored back to a specific point in time.
=True
False
---
Which of the following is NOT among the three primary factors that should be considered for each risk scenario identified?
probability of occurrence
=personnel involved in the scenario
magnitude of the impact
difficulty of timely detection
```