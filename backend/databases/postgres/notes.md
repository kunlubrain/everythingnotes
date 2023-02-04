## useful commands


```
brew services stop postgresql
brew services start postgresql
createuser -s user		::create a new user
psql -U postgres postgres	:: login as <user> to <database>

\du	:: display all users
\l	:: list databases
\c	:: change database
\dt	:: display tables

::see tables
\dt+
SELECT * FROM pg_catalog.pg_tables WHERE schemaname != 'pg_catalog' AND schemaname != 'information_schema';

::see rows in table
SELECT * FROM seats LIMIT 10 ;
SELECT * FROM bookings.seats LIMIT 10 ;
```

Show all tables:

- https://www.sqltutorial.org/sql-list-all-tables/

## PgAdmin

* Run Query

Tools > Query Tool -> Open Query Window

## Data LOAD and DUMP

### Sample Data

[Sample Data List](https://wiki.postgresql.org/wiki/Sample_Databases)

[Film Store](https://github.com/jOOQ/sakila)

### Dump Python DataFrame to PG

[pandas to_sql](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.to_sql.html#pandas-dataframe-to-sql)
[df to csv to pg](https://towardsdatascience.com/upload-your-pandas-dataframe-to-your-database-10x-faster-eb6dc6609ddf)
[simple df to csv](https://www.geeksforgeeks.org/how-to-insert-a-pandas-dataframe-to-an-existing-postgresql-table/)

## Trouble Shooting

> psql: error: connection to server at "localhost" (::1), port 5432 failed: FATAL:  database "..." does not exist

<
$`reatedb <mydb>
$ psql -h localhost


python - set search path
        self.cur.execute("SET search_path TO schema_xyz")
https://stackoverflow.com/questions/32812463/setting-schema-for-all-queries-of-a-connection-in-psycopg2-getting-race-conditi

## Ref

[install-digitalocean](https://www.digitalocean.com/community/tutorials/how-to-install-postgresql-on-ubuntu-20-04-quickstart)
[install-aws-linux](http://howto.philippkeller.com/2022/05/03/How-to-install-postgres-on-amazon-linux-2/)
[stackoverflow](https://stackoverflow.com/questions/17633422/psql-fatal-database-user-does-not-exist)
