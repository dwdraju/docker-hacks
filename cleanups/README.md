### Volume cleanup

List volumes:
```
$ docker volume ls
```

Clean volumes:
```
$ docker volume rm $(docker volume ls -qf dangling=true)
```