Create volume container:
```
$ docker create -v /hello --name data busybox
```

Create application container with volume link:
```
docker run --volumes-from data --name main busybox
```