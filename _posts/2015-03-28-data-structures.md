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
  3. Cost of operations, which determines the chief application for that data structure

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
  * | Operation          |        Array          |    Linked List      |
    |:------------------:|:---------------------:|:-------------------:|
    | Access an element  |        O(1)           |     O(n)            |
    | Insert at begin    |        O(n)           |     O(1)            |
    | Insert at end      |        O(n)           |     O(n)            |
    | Insert at middle   |        O(n)           |     O(n)            |

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
  * Applications: Organization Structure, File System
  * Recursive Data Structure because of sub trees

* __Tree Glossary__
  * Root
  * Node - contains data and references to other nodes
  * Children
  * Parent
  * Sibling
  * Leaf - has no children
  * Links/Edges
  * Internal Node - has atleast 1 child
  * Ancestor, Descendent - If you can walk a tree from A to B, A - ancestor B - descendent

* __Tree Properties__
  * Every node has only 1 parent, but zero or more children
  * N nodes, n-1 edges
  * Depth of node x - # of edges from root to node x
  * Height of node x - # of edges from node x to a leaf
  * Height of a tree - height of the root node
  * Cost of operations are measured in terms of the height of the tree

* __Binary Search Tree__
  * Cost of inserting, deleting, searching - logn
  * We want the height to be minimum
  * With n nodes, the maximum height is n-1
  * Minimum height is logn
  * Worst Case O(n)
  * Average Case O(logn)
  * A binary tree is balanced when the difference between the height of left and right subtree is not more than 1

* __Graph__
  * There is no root. Only nodes and edges
  * Edges can be directed/undirected, weighted/unweighted
  * Applications: Social Network like Facebook is a undirected graph
  * Twitter - Directed Graph
  * Highway network - weighted graph, since some edges/paths might be more expensive. Weight could be the length or traffic along that edge. Minimize the total cost
  * Lot of problems like friend recommendations become easy, when we model data as a graph, like 
  * Standard Problem - Find all the nodes at with shortest path from node x=2

* __Heap__
  * is a tree with a special heap property.
  * There are 2 types of heaps. Max heap and Min heap
  * Max heap - parent nodes are always greater than or equal to the children
  * Root is the highest


