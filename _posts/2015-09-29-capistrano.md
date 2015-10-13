---
layout: post
title:  "How capistrano works"
date:   2015-09-29 19:08:44
categories: devops
description: How capistrano works
published: true
---

* __Basics__
  * capistrano is a task runner for web just like gulp
  * recipe is a script for a particular task
  * Common tasks - downloading code, maintaining version, updating symlinks
  * Servers - name the servers and assign roles
  * When you specify a server or role on command line, while running the recipes, they are run only on that particular server
  * Purpose - To be able to run scripts/tasks on remote servers without logging in
  * Common Error - Running cap tasks directly on the remote server rather from the gateway server

* __Capfile__
  * Ruby script
  * Capistrano reads instructions from capfile
  * You also define the servers in the capfile
  * Do not have a file extension
  * `cap taskname`
  * [Docs](https://github.com/leehambley/capistrano-handbook/blob/master/index.markdown)
  * [Docs](https://github.com/capistrano/capistrano/wiki/2.x-Getting-Started)

* __Commands__
  * `bundle exec cap -T` - Lists all available tasks

  


