---
layout: post
title:  "Linux File Structure & Commands"
date:   2015-02-22 19:08:44
categories: Cheatsheets
---

* __Philosophy of Linux__: 
  * Linux does not assume anything. Lets you install what you need rather than give you a bunch of things you may not need. All commands are case sensitive.

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
  * daemon - is a background process
  * `ps aux | grep ruby` - prints the process information

* __Scheduled Jobs__
  * `crontab -l` - lists all the scheduled background processes
  * `crontab -e` - edit the crontab 

* __htop__
  * Interactive List of processes ordered by CPU usage
  * Prints CPU & Memory Utilization
  * `space` tags a process. colors it yellow.

* __Files & Directories__
  * `cat filename` prints the file contents in the terminal for reading.
  * `less filename` paginate the file. space to advance
  * `touch filename` creates a new file
  * `tail -f filename -n 100` Prints the last 100 lines of the file
  * `mv f1 f2` Renames file f1 to f2
  * `cp f1 f2` Copies file f1 to f2
  * `ls -l` Lists files with permissions
  * `scp foobar.txt your_username@remotehost.edu:/some/remote/directory` securely copy a file to remote destination. also works the other way.
  * `mkdir -p /some/dir/` - Creates the parent directories along the way

* __Pattern Search__
  * `egrep -c 'update_user' file1.txt` - Counts the number of lines with the pattern
  * `egrep -iB 120 "There were errors with the information" unicorn.log | tail -12`
  * `-i` ignore case
  * `-l` print name of files matched
  * `-w` search for words
  * `-A 3` 3 lines after the match
  * `-B 3` 3 lines before the match
  * `-C 3` 3 lines around the match
  * `-r` Search recursively
  * `-n` show line number
  * `-v` invert the match
  * `-s` returns if the patter is matched 


* __Compression & Decompression__
  * `tar -zcvf filename.tar.gz input_folder` Compress the input folder & archive
  * `tar -zxvf filename.tar.gz` Decompress the archive into the folder

* __Links__
  * `ln -s abc.txt abc_soft.txt` 
  * Soft link points to the file in its current location. Just a hyperlink. Does not work if the file is moved.
  * `ln abc.txt abc_hard.txt`
  * `rm abc_hard.txt` 
  * Hard link points to the file wherever it is. They have the same inode value.

* __User Management__
  * `sudo` Run commands as the root user
  * A normal user can have sudo privileges

* __Scripts__
  * `#! /bin/bash` - Hash Bang. Tells the script to use the bash interpreter

* __Network Management__
  * `netstat -ntlp` - List of ports listening
  * `telnet host port` - Check if the port on the host is listening`
  * `iostat` - 
  * `host google.com` - DNS lookup
  * `ping google.com` - Tells if a machine is active
  * `du` - Disk Usage Statistics
  * `ifconfig` - Print or Configure network interface parameters

* __Command Enhancements__
  * `time cmd` - Prints the time taken to execute the cmd
  * `|` - Passes the output of the previous command to the input of the next command
  * `&` - Execute a command in the background and return
  * `./cmd` - Bypass an alias
  * `man cmd` - Manual Entry for command
  * `whatis cmd` - Also documentation
  * `screen -x` - Screen Sharing between users

* __Aliases__
  * Aliases help replace one string with another while execution. Aliases are usually defined in the configuration file like .bash_profile 
  * `alias ll="ls -l"` - Creates an alias
  * `alias ll` - Gets the alias for the string

* __Terminal__
  * `cmd + R` - clears the terminals
  * `ctrl + R` - search through history

* __Vi Editor__
  * `vi +89 filename` - Opens the file from line 89
  * Modes - Command Mode- esc & Insert Mode- i
  * `dd` - Deletes line in command mode
  * `yy` - Copy line
  * `p` - Paste
  * `:n` - Goto line
  * `$` - Go to end of line
  * `^` - Go to beginning of line
  * `:q :q! :wq` - Quit , Quit without saving , Save & Quit




