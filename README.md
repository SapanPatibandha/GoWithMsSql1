# GoWithMsSql1
https://blog.logrocket.com/using-sql-database-golang/

<br></br>


# install sql on docker. 
```sh
docker pull mcr.microsoft.com/mssql/server:2019-latest
```

<p></p>

```sh
docker run -e "ACCEPT_EULA=Y" -e "SA_PASSWORD=INSTANCE_PASSWORD" -p 1433:1433 --name sql1 -h sql1 -d mcr.microsoft.com/mssql/server:2019-latest
```

<p></p>

```sh
docker exec -it sql1 "bash"
```

<p></p>

```sh
/opt/mssql-tools/bin/sqlcmd -S localhost -U SA -P "INSTANCE_PASSWORD"
```

```sql
CREATE DATABASE goTrial
GO
```


```sql
SELECT Name from sys.Databases
GO
```


```sql
USE goTrial
GO
```



```sql
CREATE TABLE Reminders ( ID int IDENTITY(1, 1), title varchar(75), description varchar(175), alias varchar(70))
GO 
```

```sh

go get github.com/denisenkom/go-mssqldb github.com/joho/godotenv/cmd/godotenv

```

