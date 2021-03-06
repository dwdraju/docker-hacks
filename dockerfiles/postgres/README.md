1. Build image from Dockerfile with a name 'postgres':
```
$ docker build -t my_postgres .
```

2. Run PostgreSQL server container of name 'db_postgres':
```
$ docker run --rm -P -d --name db_postgres my_postgres
```

3. Connect from host system:
```
$ psql -h localhost -p 49153 -d docker -U docker --password
```

4. Access container volumes:
```
$ docker run --rm --volumes-from db_postgres -it busybox sh
```

5. Create backup of volumes:
```
$ docker run --rm --volumes-from db_postgres -v $(pwd):/backup busybox tar cvzf /backup/backup.tar.gz /etc/postgresql /var/log/postgresql /var/lib/postgresql
```