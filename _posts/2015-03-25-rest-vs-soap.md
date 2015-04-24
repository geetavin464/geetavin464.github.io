---
layout: post
title:  "REST vs SOAP"
date:   2015-03-24 16:38:44
categories: architecture
---
<table class="responsive-table striped">
    <tr>
      <th> REST </th>
      <th> SOAP </th>
    </tr>
    <tr>
      <td> Representational State Transfer </td>
      <td> Simple Object Access Protocol </td>
    </tr>
    <tr>
      <td> Focussed on data (resources) <br/>
           Performs CRUD operations on data <br/>
      </td>
      <td> Focussed on operations (services) </td>
    </tr>
    <tr>
      <td> Example: getUser(id) </td>
      <td> Example: switchCategory(id) </td>
    </tr>
    <tr>
      <td> Rest permits different data formats including JSON. <br/> THis allows support for browser clients </td>
      <td> SOAP permits only XML </td>
    </tr>
    <tr>
      <td> Rest reads can be cached </td>
      <td> SOAP reads cannot be cached </td>
    </tr>
    <tr>
      <td>  </td>
      <td> Supports enterprise security features <br/>
            ACID transactions <br/> 
            Reliable Messaging <br/>
      </td>
    </tr>
  </table>

* __What makes an API Restful__
  * Resource Identification Per Request: Each request that modifies the database should act on one row of one table
  * Requests that fetch information should fetch zero or more rows from one table
  * Client state is not stored. Each request uniquely identifies itself and have no context of the requests that came before it

* __Rest API Best Practices__
  * Use the right verb for the right CRUD action - POST for create, PUT for update
  * Never change an existing API. Add a new version. 
  * Simplify resource lookup by providing id to the client
  * Require re-authentication on a per-request basis
  * Return status codes that make sense
  * Request level specs or Controller Tests

* __Resources__
  * [Rest vs SOAP](http://spf13.com/post/soap-vs-rest)
  * [Restful API](https://www.airpair.com/ruby-on-rails/posts/building-a-restful-api-in-a-rails-application)