---
layout: post
title:  "Docker Philosophy"
date:   2015-04-07 18:41:32
categories: devops
description: Features & Commands
---

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

* __Advanced Topics__
  * Functional Types of Containers - Service, Data, Helpers
  * Container Linking
  * Source & Recepient Containers using environment variables without any port connections
  * Compose still in beta can help with multi container linking

* __Questions__
  * Can docker be used as a build server?
  * Is that a good idea? ( Depends on the application I guess )
  * Cloud Provider - AWS ( digital ocean is an option)
  * How do you manage content, configuration & logging on a nginx docker container?