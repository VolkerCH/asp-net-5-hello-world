# asp-net-5-hello-world
First Example for ASP.NET and with in a docker environment. To install docker look to [Boot2Docker](http://boot2docker.io/) URL. Once installed you can start the docker command line with the 'Boot2Docker Start' link on the desktop or start menu.

``` cmd
connecting...
                        ##        .
                  ## ## ##       ==
               ## ## ## ##      ===
           /""""""""""""""""\___/ ===
      ~~~ {~~ ~~~~ ~~~ ~~~~ ~~ ~ /  ===- ~~~
           \______ o          __/
             \    \        __/
              \____\______/
 _                 _   ____     _            _
| |__   ___   ___ | |_|___ \ __| | ___   ___| | _____ _ __
| '_ \ / _ \ / _ \| __| __) / _` |/ _ \ / __| |/ / _ \ '__|
| |_) | (_) | (_) | |_ / __/ (_| | (_) | (__|   <  __/ |
|_.__/ \___/ \___/ \__|_____\__,_|\___/ \___|_|\_\___|_|
Boot2Docker version 1.5.0, build master : a66bce5 - Tue Feb 10 23:31:27 UTC 2015

Docker version 1.5.0, build a8a31ef
docker@boot2docker:~$ docker -v
```

Use for tests with docker images based on the docker image

Use the following steps:

Copy solution and Dockerfile to Docker VM:
``` bash
git clone https://github.com/VolkerCH/asp-net-5-hello-world.git hello-world
```

Run the Docker build command in project directory to create the Docker image:
``` bash
cd hello-world/src/HelloWorld
docker build -t hello-mvc .
```

Start the container based on the new image:
``` bash
docker run -t -d -p 80:5004 hello-mvc
```

Run `docker images` to find out the ID of the container to go to command line:
``` bash
docker exec -it <<id of running container>> /bin/bash
```

Missing programms in the images (nodejs, grunt):
``` bash
curl -sL https://deb.nodesource.com/setup | bash -
apt-get install -y nodejs
npm install -g grunt-cli

kpm restore
```
