Detailed Steps:

Setup VPC 1 Advantage RDS
1) RDS managed services
2) Automated provisioning, OS patching
3) Continuous backups and restore to specific timestamp (point in time restore)
4) Monitoring dashboards
5) Read replicas for improved read performance
6) Mutli AZ setup for DR (Disaster Recovery)
7) Maintenance windows for upgrades
8) scaling capability (Vertical and horizontal)
9) storage backed by EBS (gp2 or iol)
10) You can't SSH into your instances.

RDS Backups

Automated Backups:
1) Backup are automatically enabled in RSA
2) Daily full backup of the database (during the maintenace windows)
3) Transaction logs are backed-up RDS every 5 minutes
4) Ability to restore to any point in time (from oldest backup to 5 min ago)
5) 7 days retention (can be increased to 35 days)

DB Snapshots:

1) Manullay triggered by user
2) Retention of backup for as long as you want 

Storage Auto Scaling:

1) Helps you increase storgae on your RDS DB instance dynamically
2) When RDS detects you are running out of free databse storage, its scales automatically.
3) Aviod manually scaling your DB storage.
4) You have to set maximum storage Threshold (maxium limit for DB storage)
5) Automatically Modify storage if:
   1) Free storage is less than 10 % of allocated storage
   2) Low-storage lasts at least 5 minutes
   3) 6 hours have passed since last modification
6) Supports all RDS (MariaDB, MySQL, PostgresSQL, SQL SERVER, Oracle)

![image](https://user-images.githubusercontent.com/6921037/184113298-abb64e4f-4a4f-40d0-adb1-2cc7f80a11ae.png)

Create RDS:

1) RDS - create Database - Standared create
2) MYSQL - select version - templates production
3) set DB instance identifier default value database-1
4) Master username value=admin
5) Master password value=admin
6) DB instance class - Burstable class db.t2.miceo
7) storage type = SSd(gp2)
8) Allocated storage (20) GB
9) Enable auto Scaling
10) Maxium storage threshold 1000
11) connectivity select VPC for your RDS
12) Subnet group
13) VPC security group
14) Availabilty zone - no perference
15) Database port 3305
16) Database Autentication - password and IAM database
17) Create database name
18) Enable automated backup
19) Backup retention period 
20) backup windows
21) Monitoring logs
22) Enable auto minor version upgrade
23) Enable database deletion protection
24) 

