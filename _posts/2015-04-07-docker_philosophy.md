---
layout: post
title:  "Docker Philosophy"
date:   2015-04-07 18:41:32
categories: devops
description: Features & Commands
---

* Topics
  * Engine, Images, Dockerfile, Containers, Volumes, Networking, Troubleshooting, CI flow

* __Containers vs Virtual Machines__
  * Containers look and operate like a VM
  * They are not VM
  * They are lightweight. Spin up faster. 
  * A host can accomadate more containers than VMs
  * Containers run on top of docker engine

* __Usecases__
  * Deploy web front end applications
  * Deploy web API's
  * Maintenance scripts
  * Do not use containers to store persistent data

* __Container__
  * Containers should allow stopping, destroying and recreating. Containers are ephemeral.
  * Run a single process in a container
  * -y indicates yes to prompts
  * Container is run, only as long as the default command is running
  * Container itself is a process in the host machine. Any command run by the container is a child process
  * Containers have internal IP address
  * Specify a name to avoid strange auto generated names
  * Do not run ssh servers on containers unless needed. Use docker commands to check logs, restart processes, tweak configuration, run upgrades

* __Images__
  * An image is a template for a container
  * It could be a simple command or complex 
  * Docker hub is a registry for images
  * If the image's source is changed on the hub, it is downloaded again
  * Images are read-only
  * An image layer is a file system which is readonly
  * A R-W filesystem is installed on top the image layers
  * After each RUN, docker looks for a matching image in the cache
  * Docker logo represents official images in the registry(hub)
  * prefix of library denotes official image
  * build cache
  * Trivia: 70+ official, 100K+ regular, 300M+ downloads

* __Dockerfile__
  * A dockerfile lets you create your own image
  * `touch Dockerfile`
  * `FROM docker/nginx:latest` - tells which image to base off of. Always the First instruction in the dockerfile
  * `RUN apt-get prog1` - creates a image layer. Minimize image layers by combining multiple RUNs to avoid multiple intermediate images keeping readability in mind
  * `CMD service nginx start` - run after the image is loaded
  * Files & patterns listed in .dockerignore will ignored
  * Split long commands with backslashes
  * COPY is preferred over ADD though they are functionally similar
  * needs a context. Everything in .dockerignore is avoided
  * Send build context to docker engine
  * You can specify CMD for the container. Only one is accepted. If multiple, the last one is picked.
  * Can be over-ridden at runtime
  * CMD can be shell form or json array form
  * If no CMD is mentioned the default CMD associated with the base image is run

* __Volumes__
  * Volumes are mounted when creating or executing a container
  * The data in this volume is persistent, even if you delete the container
  * Volumes are independent of the containers lifecycle
  * Volumes can be shared between containers
  * I understand sharing volumes between host & container. 
  * You can specify volumes in the dockerfile using the VOLUME instruction
  * You cannot map volumes from host using the dockerfile. coz it is intended to work on any host.
  * You can store data (for eg logs in a volume, which can be accessed even after the container is shut down)
  * Mounting folders from host is not recommended. Because it binds you to that host. Not good for production use.
  * I do not understand from the examples how volumes are persistent

* __Networking__
  * Containers have their own IP address
  * You can specify container ports in the EXPOSE instruction
  * Linking: Container connection without any network ports
  * You first create the source container. Then the recepient with the link to the source. name followed by an alias
  * It creates an entry in the recepient container with an alias & IP of the source container
  * Linking is useful when you have separate web & database containers
  * Containers can be on the same host or different hosts

* __Continuous Integration__
  * How to integrate docker in your CI workflow?
  * Traditional Flow: User commits->CI runs testcases, triggers build-> sends to app server
  * Docker flow: Have CI server also build image after it built application. 
  * Image is pushed to docker hub. From the hub, it is deployed to the host machine
  * Alternate Flow(Auto Build): No CI server. git -> hub -> host machine
  * 2 possible workflows. I guess the former is better. Since we already have teamcity setup
  * How to automatically pull image into the host

* __Troubleshooting__
  * 1: Container shuts down unexpectedly? 
  * The main application or process it is running has shut down

* __Advanced Topics__
  * Functional Types of Containers - Service, Data, Helpers
  * Compose still in beta can help with multi container linking
  * Swarm - to scale the container

* __Questions__
  * Can docker be used as a build server?
  * Is that a good idea? ( Depends on the application I guess )
  * Cloud Provider - AWS ( digital ocean is an option)
  * How do you manage content, configuration & logging on a nginx docker container?