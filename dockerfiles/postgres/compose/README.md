Start container:
```
$ docker-compose up --build -d
```

Login to postgres:
```
psql -h localhost -p 5432 -d docker -U docker --password
```