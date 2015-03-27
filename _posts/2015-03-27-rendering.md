---
layout: post
title:  "Server vs Client Side Rendering"
date:   2015-03-27 06:08:44
categories: Cheatsheets
---

* __Server Side Rendering__
  * The browser recieves html directly over http
  * html is cached by google

* __Client Side Rendering__
  * The browser receives the rendering code(javascript) and data
  * Run the javasript to generate html
  * is important for mobile applications to support functionality in offline mode
  * However client can handle simple UI tasks, but for heavy logic rely on the server

* __Applications__
  * Most applications typically use a mix of server and client side rendering