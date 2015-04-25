---
layout: post
title:  "Regular Expressions"
date:   2015-04-18 07:24:32
categories: programming
description: basics characters filters metacharacters use in ruby
---

* __What is a regular expression__
  * A regular expression is also called a pattern or regex
  * Sequence of characters 
  * Forms a search pattern
  * Normally written between forward slashes `/pattern/`
  * Used to check if a string contains the pattern and also to extract portions that match

* __Characters__
  * A regex has 2 types of characters
  * regular character - with literal meaning
  * meta character - special meaning

* __Use Cases & Examples__
  * `seriali[sz]e` - To locate the same word with different spellings
  * To locate email addresses in the text
  * Syntax Highlighting
  * Search engines

* __Quantification/Repetition__
  * Quantifier - is a construct that specifies how often the preceeding element is allowed to occur. 
  * `a?` - zero or one occurence of a
  * `a*` - zero or more of a
  * `a+` - one or more of a
  * `a{3} - exactly 3 occurrences of a
  * `a{3,} - 3 or more occurences of a
  * `a{3,6} - between 3 and 6 occurences of a

* __Grouping__
  * Grouping constructs specify a group
  * [abc] - a single character of a,b or c
  * [^abc] - a single character except a, b or c
  * [a-zA-Z] - a single character in the range of a-z or A-Z
  * (..) - everything enclosed

* __Metacharacters__
  * `^` - Start of line
  * `$` - end of line
  * `\A` - start of string
  * `\z` - end of string
  * `.` - any single character
  * `\s` - any whitespace character
  * `\S` - any non whitespace character
  * `\d` - any digit
  * `\D` - any non digit
  * `\w` - any word character
  * `\W` - any non word character 
  * 

* __Logical__
  * (a|b) - a or b

* __Ruby Examples__
  * Ruby has built in support for regex
  * `=~` operator is used to match a regex and a string. Order does not matter
  * If match is found, the operator returns index of first match in string.
  * Returns nil otherwise
  * `"apple" =~ /ap/ #=> 0` 
  * `"apple" =~ /fruit/ #=> nil` 
  * `match` method returns a match data object
  * `"apple".match(/ap/) #<MatchData "ap">`

* __Resources__
  * [Here](rubular.com)