Simple Bank application with basic crud operation which will use RDS postgres database.

1. Create basic java application
2. Create RDS postgres database
   1. Create custom database name
3. Update application.properties
   1. Get Endpoint from RDS and replace it with localhost:5432
   2. Update credentials
4. Go to RDS database-> Connection&Security ->Open Security Group-> Edit inbound rules
   i) Add protocol - TCP , Port - 5432, Source - Anywhere IPV4 - save changes
5. Connect with PgAdmin
   1. Register -> Server -> provide custom name -> provide endpoint & credential -> save
   2. Insert some rows or made some changes and check through endpoints
6. Delete database
   1. Select Create snapshot while deleting if backup is required
Note: You cannot see the RDS data (tables, rows) in the AWS Management Console. In this case connect with PgAdmin and see

-----------------------------------------------------

Creating database instance using snapshot:
AWS RDS -> Snapshots -> Select snapshot -> Actions -> Restore snapshot -> It gives all the options as before and restores the database
Delete snapshot as well if not required
# SpringBoot-RDS
