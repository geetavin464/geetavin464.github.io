---
layout: post
title:  "Entity Framework"
date:   2015-10-14 19:08:44
categories: microsoft
description: entity Framework
published: false
---

* __Basics__ 
  * EF6 is the stable release
  * Open Source
  * Microsoft
  * New vs Existing Database

* __Entity Data Model__
  * Generate ADO.net Entity Model
  * Generate from database 
  * Options do not show up in the Genesis project

* __Entity SQL__
  * LINQ - preferred way to work with EF
  * take the grunt work out of it & lets you focus on the creative parts
  * tables -> classes
  * columns -> properties
  * relationships -> collections
  * stored procedures -> functions
  * Not always 1:1
  * Col names may not map to property names

* __Terms__
  * Conventional ADO.net
  * Manage connections, create objects, track objects
  * Create POCO classes
  * Officially recommended by Microsoft for ORM
  * EF6 is full featured
  * EDM - hear of EF - schema mapping - Entity Data Model
  * Query the EDM

* __Features__
  * Table splitting
  * Inheritance
  * Many to Many - joining table

* __Model Creation__
  * Right click
  * Entity Model
  * Type - EF Designer with Database
  * Connection string
  * meta data
  * edm file - 1 large xml file
  * Where is the model browser?
  