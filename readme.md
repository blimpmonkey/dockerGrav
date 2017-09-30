# documentation`
run docker-compose up and copy the contents of Grav.zip into the app/ folder

## setup
runnin the app in your browser
```
localhost
```

## shell into container
```
$ docker-compose exec php sh
```

## install grav
```
# composer create-project getgrav/grav .
```

## docker-compose
list of commands
#### list running containers
note different outputs
```
$ docker ps
$ docker-compose ps
```
#### build
```
$ docker-compose build
```
#### kill
```
$ docker-compose kill
```
#### remove
```
$ docker-compose rm
```
#### list containers
```
$ docker ps
```
output
```
CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS                NAMES
b14230bc9c67        gravserver_php      "docker-php-entryp..."   25 minutes ago      Up 5 seconds        9000/tcp             gravserver_php_1
5c50ce29cb5f        nginx:alpine        "nginx -g 'daemon ..."   25 minutes ago      Up 5 seconds        0.0.0.0:80->80/tcp   gravserver_web_1
```
#### list images
```
$ docker images
```
#### remove images
force remove images
```
$ docker rmi a2 75 b1 a27 9e --force
```
#### start
start docker in detached mode
```
$ docker-compose up -d
```
#### execute bash
```
$ docker-compose exec php sh
```
## bash
commands need to be executed from the /app folder
#### update
```
/app # bin/gpm update
```
#### versions
```
/app # bin/gpm -v
```
## steps
compose docker file
```
$ docker-compose up --build -d
```
launch bash from container (unused, see apline shell command)
```
$ docker-compose exec php bash
bash-4.3#
```
launch (alpine) shell from container
```
$ docker-compose exec php sh
```
navigate to app folder
```
/var/www/html # cd /app
```
run grav command(s)
```
/app # bin/gpm selfupdate
```