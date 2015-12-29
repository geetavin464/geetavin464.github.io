---
layout: post
title:  "Principles of Single Page Apps"
date:   2015-09-26 19:08:44
categories: ui
description: Front End Dev & Deployment
published: true
---

* Node.js ~ Originally intended to build server side js apps. Used to build automation tools and packages
* npm ~ Package manager for node
* bower ~ node package ~ Package manager for the web
* gulp ~ node package ~ task runner

* Resources
* [Node & npm](http://www.sitepoint.com/beginners-guide-node-package-manager)
* [Bower](https://blog.engineyard.com/2014/frontend-dependencies-management-part-1)
* [Gulp](https://blog.engineyard.com/2014/frontend-dependencies-management-part-2)
* [Yeoman](https://blog.engineyard.com/2014/frontend-dependencies-management-part-3)

* __Useful Node/npm Commands__
  * `node --version`
  * `npm -v`
  * Installation
  * `curl -sL https://deb.nodesource.com/setup_0.12 | sudo bash -`
  * `sudo apt-get install -y nodejs`
  * `npm config list`
  * `npm list --global --depth=0`
  * `npm list --local --depth=0`
  * `npm uninstall package`
  * `npm install pkg@ver`
  * `npm update pkg`
  * `npm cache clean`
  * `npm init` - creates package.json in the root folder

* __Dealing with older versions of ubuntu__
  * [article](http://stackoverflow.com/questions/30316812/ubuntu-apt-get-unable-to-fetch-packages)
  * Global search and replace `%s/pattern/replace` - did not work - why?
  * 'iptables -I INPUT -p tcp --dport 1022 -j ACCEPT'
  * sudo chown -R grockit:grockit grockit
  * sudo chown -R grockit:grockit .

* __Mac Installation__
  * https://nodejs.org/en/
  * pkg manager - install versionn 4.2.2
  * node & npm are installed
