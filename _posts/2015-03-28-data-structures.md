---
layout: post
title:  "Data Structures"
date:   2015-03-28 06:08:44
categories: Cheatsheets
---

* __Data Structure__
  * Way of storing and organizing data
  * Array, Linked List, Stack, Queue - Linear Data Structures
  * Tree, Graph - Non Linear Data Structures

* __Study of Data Structures__
  * has 3 components
  1. Abstract Data Structure - Defining the data and operations at a top level abstraction with no details of implementation
  2. Implementation
  3. Cost of operations

* __How to chose a data structure__
  * Determine What needs to be stored
  * Minimize the cost of frequently used operations
  * Minimize the most expensive resource - processing power or memory usage or difficulty of implementation
  * Memory is getting cheaper by the day

* __List/Static List__
  * Data: Collection of objects, not necessarily the same type
  * Operations: Write/Modify at a position. Read at a position
  * Implementation: Array
  * When a static array is full, a new array is created double the size and elements are copied from the old. Memory is freed from the old.
  * Programming Languages like Ruby implement dynamic arrays

* __Dynamic List__
  * Operations: Insert/Remove/Read/Modify/Count/EmptyCheck

* __Linked List__
  * Data: head pointer, node(data,next)
  * Collection of nodes with data & next elements. Defined by head pointer

* __Array vs Linked List__
  * | Operation          | Efficiency Array      | Efficiency Linked List |
    | :-----------------:| :--------------------:|:----------------------:|
    | Access an element  |      O(1)             |     O(n)               |
    | Insert at begin    |      O(n)             |     O(1)               |
    | Insert at end      |      O(n)             |     O(n)               |
    | Insert at middle   |      O(n)             |     O(n)               |

* __Double Linked List__
  * Data: head pointer, node(data, next, prev)
  * Operations: Insert(start, middle, end) Delete(start, middle, end) Print(curr, next)

* __Stack__
  * A list with a constraint. Insertion and deletion must be performed from the same end. ie the top
  * Also called LIFO
  * Operations: Insert(push), Delete(pop), top, is_empty, 
  * All operations are O(1)
  * Application: Execution of Function Calls/Recursion. Undo in an editor.

* __Queue__
  * A list with a constraint. Insertion must be performed at one end (head). Deletion must be performed at the other end (tail).
  * Also called FIFO
  * Operations: insert/enqueue/push, delete/dequeue/pop, is_empty, size, 
  * All operations are O(1)
  * Application: Shared Service that can serve one request at a time - Network Printer
  * Computer Processor

* __Tree__
  * Com