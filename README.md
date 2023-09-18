# Dump & Restore :tractor:

### Dump Command :arrow_down_small:
    pg_dump --host portals-db-1-0-pg.cmmuo3lde4yu.us-east-1.rds.amazonaws.com(server) --port 5432 --username "master"(user) --schema "practicinglogs"(scheme name) -Fc  --blobs --verbose --file "practicinglogs.dump"(databasename.dump) "practicinglogs"(databasename)
##
### Restore Command :arrow_down_small:
    pg_restore --host "portals-db-1-0-pg.cmmuo3lde4yu.us-east-1.rds.amazonaws.com"(server) -U master(user)  -d "practicinglogs"(databasename) --schema "practicinglogs_demo"(scheme name)  "practicinglogs.dump"(the file created in the step before)
##
### Steps :arrow_down_small:
1. create databases in target by its name in source
2. users in source should be created in target
3. ssh into databasemanager2 ec2 and securitygroup should have your ip (the user should be ubuntu not root)
4. run the commands
