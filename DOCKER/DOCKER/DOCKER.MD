
---

###### [改善](https://github.com/ttltrk/0C/blob/master/README.MD) - [.co.](https://github.com/ttltrk/PRG/blob/master/CODING.MD) - [manuals](https://github.com/ttltrk/PRG/blob/master/MAN.MD) - [most used manuals](https://github.com/ttltrk/PRG/blob/master/MUM.MD)

###### [PRG](https://github.com/ttltrk/PRG)

---

### Docker

---

```
docker version
docker info
docker //list of commands
```

---

```
if using docker toolbox type in the IP addreess >> http://192.168.99.100
```

---

```
docker container run --publish 80:80 nginx //starting the nginx webserver
ctr+c //stop

docker container run --publish 80:80 --detach nginx //starting the nginx webserver in the background
docker container run --publish 80:80 --detach --name webhost nginx //starting the nginx webserver in the background and specify name

docker container ls //list out your containers
docker container stop <CONTAINER ID> // stop the server
```

---

```
C:\Users\AttilaTorok>docker container ls
CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS                NAMES
d60c2c5e5ed0        nginx               "nginx -g 'daemon of…"   8 minutes ago       Up 8 minutes        0.0.0.0:80->80/tcp   wonderful_tu

C:\Users\AttilaTorok>docker container stop d60c2c5e5ed0
d60c2c5e5ed0

C:\Users\AttilaTorok>docker container ls
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES

C:\Users\AttilaTorok>
```

---

```
C:\Users\AttilaTorok>docker container run --publish 80:80 --detach --name webhost nginx
bbee64f442ffe6aa2486a3ae9460bba631918e6ba11cdbe6975703b44a3a6668

C:\Users\AttilaTorok>docker container ls -a
CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS                         PORTS                NAMES
bbee64f442ff        nginx               "nginx -g 'daemon of…"   5 seconds ago       Up 4 seconds                   0.0.0.0:80->80/tcp   webhost
b5278e85d261        nginx               "nginx -g 'daemon of…"   About an hour ago   Created                                             elegant_wing
d60c2c5e5ed0        nginx               "nginx -g 'daemon of…"   About an hour ago   Exited (0) About an hour ago                        wonderful_tu

C:\Users\AttilaTorok>
```

---

```
docker container logs webhost //logfile

C:\Users\AttilaTorok>docker container logs webhost
172.17.0.1 - - [04/Feb/2020:11:49:06 +0000] "GET / HTTP/1.1" 304 0 "-" "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/79.0.3945.130 Safari/537.36" "-"
172.17.0.1 - - [04/Feb/2020:11:49:06 +0000] "GET / HTTP/1.1" 304 0 "-" "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/79.0.3945.130 Safari/537.36" "-"
172.17.0.1 - - [04/Feb/2020:11:49:07 +0000] "GET / HTTP/1.1" 304 0 "-" "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/79.0.3945.130 Safari/537.36" "-"
172.17.0.1 - - [04/Feb/2020:11:49:07 +0000] "GET / HTTP/1.1" 304 0 "-" "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/79.0.3945.130 Safari/537.36" "-"
172.17.0.1 - - [04/Feb/2020:11:49:08 +0000] "GET / HTTP/1.1" 304 0 "-" "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/79.0.3945.130 Safari/537.36" "-"
172.17.0.1 - - [04/Feb/2020:11:49:08 +0000] "GET / HTTP/1.1" 304 0 "-" "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/79.0.3945.130 Safari/537.36" "-"
172.17.0.1 - - [04/Feb/2020:11:49:08 +0000] "GET / HTTP/1.1" 304 0 "-" "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/79.0.3945.130 Safari/537.36" "-"
172.17.0.1 - - [04/Feb/2020:11:49:08 +0000] "GET / HTTP/1.1" 304 0 "-" "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/79.0.3945.130 Safari/537.36" "-"
172.17.0.1 - - [04/Feb/2020:11:49:09 +0000] "GET / HTTP/1.1" 304 0 "-" "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/79.0.3945.130 Safari/537.36" "-"
172.17.0.1 - - [04/Feb/2020:11:49:09 +0000] "GET / HTTP/1.1" 304 0 "-" "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/79.0.3945.130 Safari/537.36" "-"
172.17.0.1 - - [04/Feb/2020:11:49:09 +0000] "GET / HTTP/1.1" 304 0 "-" "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/79.0.3945.130 Safari/537.36" "-"
172.17.0.1 - - [04/Feb/2020:11:49:10 +0000] "GET / HTTP/1.1" 304 0 "-" "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/79.0.3945.130 Safari/537.36" "-"

C:\Users\AttilaTorok>
```

---

```
docker container top webhost //process running inside the container 

C:\Users\AttilaTorok>docker container top webhost
PID                 USER                TIME                COMMAND
2089                root                0:00                nginx: master process nginx -g daemon off;
2127                101                 0:00                nginx: worker process

C:\Users\AttilaTorok>
```

---

```
docker container rm -f bbe //remove running container

C:\Users\AttilaTorok>docker container ls -a
CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS                         PORTS                NAMES
bbee64f442ff        nginx               "nginx -g 'daemon of…"   6 minutes ago       Up 6 minutes                   0.0.0.0:80->80/tcp   webhost
b5278e85d261        nginx               "nginx -g 'daemon of…"   About an hour ago   Created                                             elegant_wing
d60c2c5e5ed0        nginx               "nginx -g 'daemon of…"   About an hour ago   Exited (0) About an hour ago                        wonderful_tu

C:\Users\AttilaTorok>
C:\Users\AttilaTorok>
C:\Users\AttilaTorok>docker container rm bbe b52 d60
b52
d60
Error response from daemon: You cannot remove a running container bbee64f442ffe6aa2486a3ae9460bba631918e6ba11cdbe6975703b44a3a6668. Stop the container before attempting removal or force remove

C:\Users\AttilaTorok>docker container rm -f bbe
bbe

C:\Users\AttilaTorok>docker container ls
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES

C:\Users\AttilaTorok>  
```

---
