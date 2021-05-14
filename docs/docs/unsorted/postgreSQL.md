install

https://www.digitalocean.com/community/tutorials/how-to-install-postgresql-on-ubuntu-20-04-quickstart
https://www.youtube.com/watch?v=qw--VYLpxG4

sudo systemctl status postgresql



### commands
```
sudo -i -u postgres

psql

sudo -u postgres psql
psql -U postgres -d dvdrental
```

https://www.postgresqltutorial.com/postgresql-show-tables/
```

\l — list of databases

\c blog — change the database

show tables
```
\d
\dt 
\dt+

```
```
\q — quit

\h — help
```

create new database
```
create database dvdrental;

createdb -T template0 new_database
```

restore db
https://www.postgresqltutorial.com/postgresql-restore-database/

```

```
```

user
https://medium.com/coding-blocks/creating-user-database-and-adding-access-on-postgresql-8bfcd2f4a91e
```
sudo -u postgres psql
postgres=# create database mydb;
postgres=# create user myuser with encrypted password 'mypass';
postgres=# grant all privileges on database mydb to myuser;
```


show users
\du

To login without a password:

sudo -u user_name psql db_name

To reset the password if you have forgotten:
ALTER USER orlovkn WITH PASSWORD '12345';