### Volume cleanup

List volumes:
```
$ docker volume ls
```

Clean volumes:
```
$ docker volume rm $(docker volume ls -qf dangling=true)
```

### Container cleanup

Remove stopped containers:
```
$ docker rm $(docker ps -a -q)
```

Remove container and its volumes
```
$ docker rm -v container
```

### Image cleanup

Remove all images:
```
$ docker rmi $(docker images -q)
```

Remove images of same IMAGE ID:
```
$ docker rmi -f [ID]
```