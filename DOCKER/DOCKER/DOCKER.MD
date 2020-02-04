
---

###### [改善](https://github.com/ttltrk/0C/blob/master/README.MD) - [.co.](https://github.com/ttltrk/PRG/blob/master/CODING.MD) - [manuals](https://github.com/ttltrk/PRG/blob/master/MAN.MD)

###### [PY](https://github.com/ttltrk/PRG/blob/master/PY/DOC/PYF/PYF.MD) - [JV](https://github.com/ttltrk/PRG/blob/master/JAVA/JAVA.MD) - [C](https://github.com/ttltrk/PRG/blob/master/C/C.MD) - [SQL](https://github.com/ttltrk/DB/blob/master/SQL/DOC/OSM/OSQLM/SQLM/SQLM.MD) - [SH](https://github.com/ttltrk/ELSE/blob/master/M/UX/UX.MD) - [PL](https://github.com/ttltrk/PRG/blob/master/PERL/PL.MD) - [DS](https://github.com/ttltrk/ELSE/blob/master/DATA/DS/DS.MD) - [DO](https://github.com/ttltrk/ELSE/blob/master/DOCKER/DOCKER/DOCKER.MD) || [ENG](https://github.com/ttltrk/ELSE/blob/master/LAN/ENG/LE.MD) - [DE](https://github.com/ttltrk/ELSE/blob/master/LAN/GER/DUO_GER.MD) - [SP](https://github.com/ttltrk/ELSE/blob/master/LAN/SP/SP.MD) - [FR](https://github.com/ttltrk/ELSE/blob/master/LAN/FR/FR.MD) - [TR](https://github.com/ttltrk/ELSE/blob/master/LAN/TR/TR.MD) - [LA](https://github.com/ttltrk/ELSE/blob/master/LAN/LATIN/LATIN.MD) - [ESP](https://github.com/ttltrk/ELSE/blob/master/LAN/ESP/ESP.MD) || [Tools](https://github.com/ttltrk/ELSE/blob/master/M/TOOLS/TOOLS.MD)

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

mongo handling

```
C:\Users\AttilaTorok>docker run --name mongo -d mongo
Unable to find image 'mongo:latest' locally
latest: Pulling from library/mongo
5c939e3a4d10: Pull complete                                                                                             c63719cdbe7a: Pull complete                                                                                             19a861ea6baf: Pull complete                                                                                             651c9d2d6c4f: Pull complete                                                                                             85155c6d5fac: Pull complete                                                                                             85fb0780fd97: Pull complete                                                                                             85b3b1a901f5: Pull complete                                                                                             6a882e007bb6: Pull complete                                                                                             f7806503a70f: Pull complete                                                                                             5732cde4308d: Pull complete                                                                                             8f892a804391: Pull complete                                                                                             afc61ce39de5: Pull complete                                                                                             ffc30d4b370e: Pull complete                                                                                             Digest: sha256:48a59166d81b41da82cedc8e57223cfc7b6314dc34e8a571dc12f2fc35ac9258
Status: Downloaded newer image for mongo:latest
57f58f39a3c8ec35fb0cd1d18c21c536a48a889d3409d71f4f1bbdfae633238e

C:\Users\AttilaTorok>docker ps
CONTAINER ID        IMAGE               COMMAND                  CREATED              STATUS              PORTS               NAMES
57f58f39a3c8        mongo               "docker-entrypoint.s…"   About a minute ago   Up About a minute   27017/tcp           mongo

C:\Users\AttilaTorok>docker top mongo
PID                 USER                TIME                COMMAND
2414                999                 0:01                mongod --bind_ip_all

C:\Users\AttilaTorok>ps -ef | grep mongod
       0   4352      1  0   Feb 03 con  0:45 mongod
AttilaTo   8436  12848  0 13:23:38 con  0:00 grep  mongod

C:\Users\AttilaTorok>docker stop mongo
mongo

C:\Users\AttilaTorok>docker ps
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES

C:\Users\AttilaTorok>
```

---
