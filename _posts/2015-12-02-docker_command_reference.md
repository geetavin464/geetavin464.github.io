---
layout: post
title:  "Docker  Command Reference"
date:   2015-12-02 18:41:32
categories: devops
description: Features & Commands
---

* __Installation & Setup on Ubuntu__
  * `sudo apt-get update`
  * `curl -sSL https://get.docker.com/ | sh`
  * `docker -v`
  * `sudo usermod -aG docker ubuntu`
  * `docker ps -a`

* __Info Commands__
  * `docker info`
  * `docker history`

* __nginx Reference__
  * https://hub.docker.com/_/nginx/

* __Image Commands__
  * `docker build -t repo_name/img_name:tag .` - 
  * `docker tag img_id user_name/img_name:latest` - Tag & push image
  * `docker login --username=uname --password=pw --email=email`
  * `docker push`
  * `docker rmi -f img_id`
  * `docker rmi -f img_name`
  * `docker pull uname/iname:tag` - pull image
  * `docker images`
  * `docker search -s 10 ubuntu` - search for image with more than 10 stars
  * `docker inspect img_name`
  * `docker tag local_repo:tag docker_hub_repo:tag` - rename local repo& image
  * `docker tag img_id docker_hub_repo:tag` - also rename
  * Name of repository ~ username/image_name

* __Container Commands__
  * Container is a basic linux os
  * `docker run --name docker-nginx -p 80:80 -d nginx`
  * creates a container with the name `docker-nginx`
  * `-d` in the background as a daemon; detached mode; keeps running until manually stopped;
  * `80:80` - local_machine_port:container_port
  * `nginx` - name of the image
  * `docker ps -a` - list containers including those that are stopped
  * `docker stop $cid`
  * `docker rm container_name`
  * `-v` - link volume
  * `docker top c_id`
  * `docker run -it -v vol1 /john1 myimg`
  * `docker exec -it c_id bash` - takes you inside the container
  * `docker inspect c_id | grep IpAddress`
  * `docker commit c_id repo_name/app_name:tag` - commits the container as an image
  * Push must have same repository and tag as the docker hub repo

* __Container Troubleshooting__
  * `docker logs c_id`
  * `docker logs -f c_id` - follow the log
  * `docker logs -f --tail 1 c_id` - follow from the last line
  * The logs are output from the pid 1 process
  * Map a volume to look at the logs on the host. These logs are available, even if the container is shut down
  * Volume mounting is best approach to view logs.
  * If you make changes to docker engine, eg: logging, you restart the service

* __Docker run Reference__
  * `-w=""` - Override working directory
  * `-u=""` - username or uid
  * `-v=[]` - volume

* __Dockerfile Instructions__
  * Instructions are traditionally uppercase
  * `FROM` - Mandatory. First instruction is always a `FROM`
  * `#` indicates a comment
  * $variable_name
  * A series of commands a user could call on the command line to assemble an image
  * `PATH` - A local directory, which defines the context
  * Traditionally dockerfile belongs in the root folder. You can use -f flag to point to it elsewhere
  * `CMD` - There can be only 1 CMD in a dockerfile. Only the last will take effect
  * `URL` - A git repo location
  * `.dockerignore` - to exclude files from the context
  * `MAINTAINER` - author
  * `LABEL` - add meta data to the image
  * `EXPOSE` - expose ports. Used to interconnect containers using links
  * `USER` - sets the username
  * `ENV` - set shell variables
  * `WORKDIR` - sets the work directory for RUN, CMD, ENTRYPOINT, ADD, COPY
  * `VOLUME` - Creates a mount point with the specified name. Marks it as holding volumes from native host or other containers
  * `RUN` vs `CMD` vs `ENTRYPOINT`
  * `ADD` vs `COPY`
