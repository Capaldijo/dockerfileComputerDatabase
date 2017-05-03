# Debian-MySQL

### Running

Simple:

```shell
docker run -d --name="mysql-run" -e MYSQL_PASSWORD=password capaldi/mysql
```

Exposed:

```shell
docker run -d --name="mysql-run" -e MYSQL_PASSWORD=password -p 3307:3306 capaldi/mysql
```
