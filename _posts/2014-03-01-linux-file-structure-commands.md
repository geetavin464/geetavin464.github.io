---
layout: post
title:  "Linux CheatSheet"
date:   2015-02-22 19:08:44
categories: Essentials
---

* __Philosophy of Linux__: 
  * Linux does not assume anything. Lets you install what you need rather than give you a bunch of things you may not need.

* __Kernel__
  * Takes care of resource allocation. 

* __Shell__
  * Accepts commands and passes it to the kernel

* __Service__
  * Service is an application that runs in the background

* __Important Folders__
  * `/var/run` - pids for the important processes
  * `/var/log` - Logs
  * `/etc/init` - Configuration Files
  * `/etc/init.d` - Scripts that respond to start and stop
  * `/etc/hosts` - DNS
  * `/etc/passwd` - User Database

* __Processes__
  * Processes are the core of a linux OS. A process is an instance of a running command. 
  * init - is the first process with id 1. Cannot be killed. Every other process is the child of init. 

* __htop__
  * Interactive List of processes ordered by CPU usage

* __Files & Directories__
  * `cat filename` prints the file contents in the terminal for reading.
  * `less filename` paginate the file. space to advance
  * `touch filename` creates a new file
  * `tail -f filename -n 100` Prints the last 100 lines of the file




