---
layout: post
title:  "Design Patterns"
date:   2015-03-29 07:24:32
categories: architecture
published: true
description: template strategy singleton factory
---

* __Purpose__
  * To prevent reinventing the wheel
  * To avoid ad hoc programming
  * When you read code, you would be able to identify the design pattern being used and easily work with it

* __Types__
  * Creational
  * Structural
  * Behavioral
  * Concurrency

* __Template Method__
  * This is a behavioral pattern that relies heavily on inheritance
  * If you see multiple if/else statements in your code, then it might be time to use this pattern
  * Example: You are building a TicTacToe game between human and computer
  * You have multiple snippets like this in you code - `if human do this else do that`
  * You have an abstract class `Player`
  * Then you create subclasses `Human` and `AI` with details of implementation
  * The generic Player class contains Template methods which defer specific logic to subclasses

* __Strategy__
  * Lets behavior to be selected at run-time
  * Used in authentication, twitter, facebook
  * Strategy
  * Context
  * Runtime Flexibility

* __Singleton__
  * A class has only a single object
  * You cannot instantiate a new object since the `new` method is private
  * You cannot access the object of the class using `Klass.instance`
  * To use this pattern do a `include Singleton` in your class
  * Example: Rails controllers use the singleton pattern. You cannot instantiate a new controller instance

* __Factory__
  * The factory class determines which class to be instantiated