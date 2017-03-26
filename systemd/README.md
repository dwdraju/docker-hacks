Copy service file to /etc/systemd:
```
$ cp postgres.service /etc/systemd/system
```

Enable service:
```
$ systemctl enable /etc/systemd/system/postgres.service
```

Start service:
```
$ systemctl start postgres.service
```