### Debug Docker Containers



Logs:
```
$ docker run -d --name=logtest alpine /bin/sh -c “while true; do sleep 2; df -h; done”
```
```
$ docker logs logtest
```