---
layout: post
title:  "Programming Techniques"
date:   2015-04-16 18:41:32
categories: programming
published: false
---

<table class="responsive-table striped">
  <tr>
    <th>  </th>
    <th> Recursive Implementation  </th>
    <th> Iterative Implementation </th>
  </tr>
  <tr>
    <td> Factorial </td>
    <td>   </td>
    <td>   </td>
  </tr>
  <tr>
    <td> Fibonacci </td>
    <td>   </td>
    <td>   </td>
  </tr>
</table>

* Terminology
  * Recursive Function
  * Recursive Call
  * Base Condition/Termination Condition
  * Pause/Resume
  * Factorial
  * Fibonacci
  * Iteration
  * Complexity Analysis
  * Time Complexity Analysis
  * Space Complexity Analysis
  * Runtime Efficiency
  * Memory Efficiency
  * Recurrence Function

* __Recursive Function__
  * If a function can be written as a simpler form of itself
  * The call to itself is called a recurive call
  * Without a base or termination condition, the recursive call might have gone on endlessly
  * The function is passed, then resumed

* __Examples__
  * Factorial
  * Fibonacci

* __Fibonacci__
  * is a mathematical sequence
  * First two elements are 0,1
  * Iterative is better than recursive
  * because you compute each only once
  * lot of redundancy
  * Run time grows exponentially because of this redundancy
  * To calculate F(40) you computer F(2) 63245986 times
  * Expensive in time and space

* __Complexity__
  * Time Complexity - How time taken grows with input
  * Space Complexity - How memory grows with input
  * Each simple operation takes 1 unit of time
  * `T(0) = 1`
  * For recursive functions
  * `T(n) = T(n-1)+3`
  * Multiplication, Substraction, Comparison
  * `T(k) = T(n-k)+3k`
  * n-k = 0
  * n=k
  * `T(k)= T(0)+3k`
  * T(k) = 3k+1
  * T(n)=3n+1
  * O(n)
  * Write a recurrence interms of its base condition
  * Both time & space complexity of factorial is O(n)

* __Recursion__
  * Factorial - Recursive Implementation
  * Time complexity - O(n); Space Complexity - O(n)
  * Fibonacci - Recursive Implementation
  * Time Complexity - Lower Bound - 2^(n/2)
  * Upper bound - 2^n
  * O(2^n) - worst time complexity
  * Fib-Iterative.

* __Recursion with Memoization__
  * Time Complexity - O(n)
  * Memory Complexity - 

* __Terminology__
  * Time Complexity or Runtime Complexity
  * Space Complexity or Memory Complexity
  * Recursion Tree
  * Function Call stack
  * push & pop from memory stack
  * Maximum space consumed in the memory stack
  * Depth of the recursion tree - length of the longest path in the tree