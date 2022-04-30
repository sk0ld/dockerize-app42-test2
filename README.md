Example of Java app move to docker containers with docker compose
=========

Short info
------------

Tested on Ubuntu 20.04

Services:
1) dev-maven - to build war artifact
2) db - MySQL DB for Java app
3) prod-tomcat - Apache Tomcat webserver to publish Java app

Based on : https://github.com/sk0ld/clone-app42-test


Original : https://github.com/shephertz/App42PaaS-Java-MySQL-Sample


To install docker:

```
apt update && apt install -y git docker.io
```


To install docker compose: follow https://docs.docker.com/compose/install/ or https://docs.docker.com.zh.xy2401.com/v17.12/compose/install/#install-compose

Cloning repository & preparing docker image:

```
git clone https://github.com/sk0ld/dockerize-app42-test2.git

cd dockerize-app42-test2/ && docker-compose up -d
```

Access Java app hosted on tomcat:
```
http://your_ip_or_hostname:8080/app42-1.0
```

To stop docker container:

```
docker-compose stop
```
