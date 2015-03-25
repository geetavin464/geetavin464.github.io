---
layout: post
title:  "REST vs SOAP"
date:   2015-03-24 16:38:44
categories: Cheatsheets
---

* __REST__
  * Representational State Transfer
  * Rest is focussed on data(resources)
  * Performs CRUD operations on data(resources)
  * ex: getUser(id)
  * Rest permits different data formats including JSON, which allows support for browser clients
  * Rest reads can be cached

* __SOAP__
  * Simple Object Access Protocol
  * SAOP is focussed on operations(services)
  * ex: switchCategory(id)
  * SOAP permits only XML
  * SOAP reads cannot be cached

* __Why SOAP__
  * Supports some enterprise security features
  * ACID transactions
  * Reliable Messaging

* __What makes an API Restful__
  * Resource Identification Per Request: Each request that modifies the database should act on one row of one table
  * Requests that fetch information should fetch zero or more rows from one table
  * Resource is represented as data usually JSON
  * Client state is not stored. Each request uniquely identifies itself and have no context of the requests that came before it

* __Rest API Best Practices__
  * Use the right verb for the right CRUD action - POST for create, PUT for update
  * Never change an existing API. Add a new version. 
  * Simplify resource lookup by providing id to the client
  * Require re-authentication on a per-request basis
  * Return status codes that make sense
  * Request level specs or Controller Tests

* __Resources__
  * [Rest vs SOAP](http://spf13.com/post/soap-vs-rest)
  * [Restful API](https://www.airpair.com/ruby-on-rails/posts/building-a-restful-api-in-a-rails-application)