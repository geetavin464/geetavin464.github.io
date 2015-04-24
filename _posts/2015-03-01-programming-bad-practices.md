---
layout: post
title:  "Programming Bad Practices"
date:   2015-03-01 21:05:44
categories: programming
published: true
---

* __Bad Practices__
  * Duplicate Code
  * Long Methods (more than 6 or 8 lines of code). If you cannot break it apart there might be a flaw in the design
  * Feature Envy - When a class B is constantly requesting methods from class A, then perhaps the method needs to be defined in class A
  * Data Clumps - Instead of having multiple dependent variables as parameters, have a single data structure 
  * Comments - Prefer clean and self-explanatory code over comments
  * Divergent Change - When a class or method has more than one responsibility
  * Conditionals - You can usually avoid conditional daze through object oriented design and patterns like strategy
  
* __Primer__
  * Is the code unit tested?
  * Is it human readable?
  * Is it machine readable? aka Is it semantically correct?
  * Is it extensible? aka Is it scalable?
  * Does the business logic belong in the models?
  * Does the presentation logic belong in the controllers?
  * Is the reusable code extracted out of models & controllers?
  * Are edge/boundary cases appropriately handled?

* __Rules of Thumb__
  * DRY - Don't repeat yourself

