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
  * `~` - Home Directory
  * `~/.ssh` - Contains known_hosts, Authentication keys id_rsa
  * `~/.bash_profile` - Defines the aliases and configuration. Startup File. 

* __Environment Variables__*
  * `env` - view all environment variables
  * `env | grep PATH`
  * `echo $PATH`
  * `lsb_release -a` - Prints the ubuntu version

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
  * `mv f1 f2` Renames file f1 to f2
  * `cp f1 f2` Copies file f1 to f2
  * `ls -l` Lists files with permissions
  * `scp foobar.txt your_username@remotehost.edu:/some/remote/directory` securely copy a file to remote destination. also works the other way.

* __Compression & Decompression__
  * `tar -zcvf filename.tar.gz input_folder` Compress the input folder & archive
  * `tar -zxvf filename.tar.gz` Decompress the archive into the folder

* Links 
  * `ln -s abc.txt abc_soft.txt` 
  * Soft link points to the file in its current location. Just a hyperlink. Does not work if the file is moved.
  * `ln abc.txt abc_hard.txt`
  * Hard link points to the file wherever it is. They have the same inode value.

* User Management
  * `sudo` Run commands as the root user
  * A normal user can have sudo privileges

* Scripts
  * #! /bin/bash - Hash Bang. Tells the script to use the bash interpreter

* Network Management
  * `netstat -ntlp` - List of ports listening
  * `telnet host port` - Check if the port on the host is listening`

* Command Enhancements
  * `time cmd` - Prints the time taken to execute the cmd
  * `|` - Passes the output of the previous command to the input of the next command
  * `&` - Execute a command in the background and return
  * `./cmd` - Bypass an alias
  * 




