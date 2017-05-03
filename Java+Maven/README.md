# Debian-MySQL

### Running

Exposed:

```shell  nom container mysql ==> [mysql]:mysql
docker run -it --rm --name my-maven-project --link mysql:mysql -v "/home/capaldi/GitHub/training-java:/usr/src/mymaven" -w /usr/src/mymaven javamaven mvn clean package
```
