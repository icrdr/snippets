### Create new user
`mysql > CREATE USER 'newuser'@'localhost' IDENTIFIED BY 'password';`

#### Set privileges
`mysql > GRANT ALL PRIVILEGES ON * . * TO 'newuser'@'localhost';`

`mysql > FLUSH PRIVILEGES;';`

### Bakeup
#### all DB
`mysqldump -uroot -proot --all-databases --single-transaction > [.sql file path]`
#### single DB
`mysqldump -uroot -proot --single-transaction [DB name] > [.sql file path]`

### Recovery
#### all DB
`mysql -uroot -proot < 20190201-1325_all_backup.sql`
#### single DB
`mysql > CREATE DATABASE test;` create DB first

`mysqldump -uroot -proot [DB name] < [.sql file path]`

### Fix 'invalid default value for date'
```
show variables like 'sql_mode' ; 
set global sql_mode = 'ONLY_FULL_GROUP_BY,STRICT_TRANS_TABLES,ERROR_FOR_DIVISION_BY_ZERO,NO_ENGINE_SUBSTITUTION';
```


