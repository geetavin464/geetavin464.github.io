---
layout: post
title:  "Networking Protocols"
date:   2015-03-02 18:41:32
categories: devops
description: Networking protocols, their purpose, features and commands
---

* __Frequently Used Networking Protocols__
  * HTTP, HTTPS, SSH, DNS, SMTP, POP3/IMAP

* __IP Address__
  * public ip or dns - external - reachable over the internet
  * private ip or dns - internal - reachable in the private network
  * ipv4 4 octets ie 8 bits each

* __Ports__
  * An IP address has multiple ports for various servers
  * Each server binds to a port and listens for incoming connections
  * `http - 80`
  * `https - 443`
  * `dns - 53`
  * `ssh - 22`
  * `smtp - 25`
  * Port ~ Apartment Number. Socket ~ Door of Apartment. IP address ~ street address
  * Port Forwarding

* __https__
  * When you use https protocol to make a connection from a browser, you see a green lock icon to the left
  * All data transfer between the client and server is encrypted
  * The server should know how to handle this connection
  * The server needs a certificate - .crt and a private key - .key 

* __Generating an SSL certificate__
  * Popular Implementation - openssl
  * Use openssl to generate a certificate signing request .csr
  * You can use these files to generate a self-sign certificate for local environment
  * You can submit these to a dns provider and request for a .crt and .key
  * Normally expires in 365 days
  * `openssl x509 -enddate -noout -in certif.crt` To check the expiration of a .crt
  * `openssl x509 -in server.crt -text` - prints info of ssl cert

* __Securing a website__
  * `openssl req -newkey rsa:2048 -nodes -keyout domain.key -out domain.csr`
  * Above command creates a csr and key
  * Use them to generate a crt from provider like Comodo
  
* __Using an ssl Certificate__
  * Turn on the ssl config option in nginx
  * Provide the .crt & .key files generated

* __Http headers__
  * Use Chrome inspector-Network panel to look at the request and response headers
  * Request payload in a post method is nothing but the form data
  * CORS - Cross Origin Resource Sharing
  * mime-type, content-type, file-extension
  * CORS - mechanism that allows resources to be shared from domains other than the origin
  * `Access-control-allow-origin` or `Access-control-allow-methods` etc
  * Necessary to prevent Cross-site-scripting attacks

* __Http Clients__
  * `curl example.com` - writes to the standard output
  * `curl -o file.html example.com`
  * `curl -d "name=geeta&location=nyc" example.com` - post data
  * [Curl Reference](http://curl.haxx.se/docs/manual.html/)

* __DNS__
  * Maps Ip addresses to human friendly domain names, so we dont have to remember a bunch of numbers to visit a website
  * TLD - top level domain - com net org gov
  * SLD - second level domain - google twitter
  * Zone File/Name Servers/Root Servers - contain the dns mapping
  * CNAME - alias
  * Name Server - Computers that run DNS are called Name servers
  * BIND - Ubuntu ships with BIND, the most common program for maintaining a name server on Linux

* __Email Servers__
  * SMTP - push protocol
  * Last step used Pop3/IMap which is pull protocol
  * Use polling to make it seem instantaneous

* __CDN__
  * Content Delivery Network
  * Takes static content and places them in locations closer to the users
  * Amazon, Akamai, Rackspace
  * They have node servers all over
  * Push & Pull 
  * Amazon Cloudfront
