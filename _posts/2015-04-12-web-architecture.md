---
layout: post
title:  "Web Architecture"
date:   2015-04-12 06:08:44
categories: Cheatsheets
published: false
---

* __Single Page Application__
  * Heavily dependent on javascript
  * 1 web page or 1 url
  * Fragment Hash - the bit after the #
  * Use of fragment hash retains bookmarkability and back/fwd buttons
  * Loads all other content using javascript
  * Example: Gmail
  * UI is not reloaded
  * 2.0 client is an SPA
  * They don't directly connect to the DB. But rather send restful requests to the API


* __Advantages__
  * Less page load time
  * Assets are loaded only once
  * Use fake JSON to test SPA
  * Offline processing
  * Reduced number of requests to the server
  * Flexibility of UI design
  * API & UI can be independently developed and tested
  * Use caching and local storage

* __Disadvantages__
  * Analytics
  * Back button issue 

* __AngularJS Philosophy__
  * Front End Web Application Framework
  * Tag Line - HTML for web applications
  * Javascript Framework
  * Can create dynamic SPA
  * Philosophy: Declarative programming is better than imperative programming

* __AngularJS Trivia__
  * `ng-app` - Adding this attribut to the html tag - instantiates an angular app on the page
  * Angular looks through the DOM for {{}} double curly braces and swaps them with the value of the model
  * Model is nothing but a piece of data within the application
  * Model can be array, string, number, object..
  * Controller
  * Scope is defined by a controller
  * Controller has access to all data and models in a scope and can operate on it using javascript
  * `ng-controller`
  * Everything in the div is inside the controller scope
  * Controllers are javascript functions
  * Use controllers to add business logic for the application
  * `$scope`

* __MVC vs MVVM__
  * 