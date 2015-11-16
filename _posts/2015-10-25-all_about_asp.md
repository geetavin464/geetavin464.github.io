---
layout: post
title:  "All about ASP"
date:   2015-10-25 19:08:44
categories: microsoft
description: asp
published: false
---

* __Views__
  * are in the `Views` folder
  * Layouts are present in the `shared` folder
  * Views use razor syntax to combine code & markup
  * Create a View - Right click on controller action

* __Razor Syntax__
  * Combines code & markup
  * @ - Code snippet
  * @()
  * @{} - Code block
  * @: - Content/Text
  * @* *@ - Comment block

* __Controllers__
  * Every public method in a controller class is an action
  * Request data from model & send it to the view
  * When you create controller, several templates to chose from, MVC or Entity etc
  * You create model objects in the controller

* __Sharing data between controllers & views__
  * `ViewData` is dictionary/hash that is shared between controllers & views
  * Store the data that you want to share in this
  * `ViewBag` 

* __Model__
  * Class that contains data & may be some behavior
  * Right click -> Add class
  * Generates scaffold
  * Filename is the same as the classname
  * You can have models that are not associated with data
  * attributes - access modifier, data type & constructor
  * Models have data annotations to maintain integrity
  * Required, DisplayType, StringLength, Display, EmailAddress

* __Methods__
  * Similar to data, methods also have access modifier, type declaration and name
  * Constructor Methods - have the same name as the class
  * By default, there is a no argument constructor method
  * Access Modifier - public, private
  * Errors - Methods do not exist in the current context
  * To call the method, add the name of the class with a . as the prefix
  * Static Methods - Methods you can call from anywhere in your application
  * POCO class - focus is on data

* __Build the solution__
  * To make sure there are no errors

* __Types__
  * Commonly Used Types - string, list, DateTime, bool, IEnumerable
  * Lists - List<Instructor> Instructors
  * [Required] - Attributes are required
  * Data Annotations ~ Data Validations
  * They belong in the model ofcourse

* __Request Routing__
  * `App_start` folder
  * `RouteConfig.cs`
  * `routes.mapRoute` 
  * Breaks the url in 3 segments - controller, action & id
  * provide defaults

* __database files__
  * mdf
