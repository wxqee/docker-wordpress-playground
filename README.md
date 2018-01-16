# Reference

1. [wxqee/docker-wordpress-playground](https://github.com/wxqee/docker-wordpress-playground)
1. [QuickStart: Compose and WordPress](https://docs.docker.com/compose/wordpress/)

# Run Example

Go into directory *local-example*

``` bash
cd local-example/
```

You can keep or update *docker-compose.yml* as you wish, and then start docker.

``` bash
docker-compose up -d
```

After *mysql* and *wordpress* container starting done, check the container.

``` bash
docker ps
```

and you can see something like below:

```
CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS                  NAMES
86fa6d60469d        wordpress:latest    "docker-entrypoint..."   3 minutes ago       Up 3 minutes        0.0.0.0:8000->80/tcp   localexample_wordpress_1
d7575c796542        mysql:5.7           "docker-entrypoint..."   3 minutes ago       Up 3 minutes        3306/tcp               localexample_db_1
```

Oepn [http://localhost:8000](http://localhost:8000) from your browser.

*Start Your Wordpress Life* from here.

# Something Addition

Any changes to the shared folders are about to take effects to your WordPress
environment.

1. *db_data/* folder is for mounting container *mysql* data folder.
1. *wordpress/* folder is for mounting container *wordpress* as source tree.

