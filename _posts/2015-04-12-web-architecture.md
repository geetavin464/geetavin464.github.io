---
layout: post
title:  "SPA & AngularJS"
date:   2015-04-12 06:08:44
categories: architecture
published: true
---

* __Single Page Application__
  * Heavily dependent on javascript
  * 1 web page or 1 url
  * Fragment Hash - the bit after the #
  * Use of fragment hash retains bookmarkability and back/fwd buttons
  * Loads all other content using javascript
  * Example: Gmail
  * UI is not reloaded
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

* __AngularJS Philosophy__
  * Front End Web Application Framework/Javascript Framework
  * Tag Line - HTML for web applications
  * Can create dynamic SPA
  * Philosophy: Declarative programming is better than imperative programming

* __AngularJS Trivia__
  * `ng-app` - Adding this attribute to the html tag - instantiates an angular app on the page
  * Angular looks through the DOM for {{}} double curly braces and swaps them with the value of the model
  * Model is nothing but a piece of data within the application
  * Model can be array, string, number, object..
  * Controller is a javascript function, that add business logic to the application
  * Controller defines scope and has access to all data or models in that scope
  * keyword - `ng-controller`
  * Everything in the div is inside the controller scope
  * scope keyword - `$scope`

* __Architecture__
  * Web Frontend
  * Mobile frontend
  * Services, also need to talk to each other
