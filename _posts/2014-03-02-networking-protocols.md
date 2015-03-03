---
layout: post
title:  "Networking Protocols"
date:   2015-03-02 18:41:32
categories: Cheatsheets
---

* Frequently Used Networking Protocols
  * HTTP, HTTPS, SSH, DNS, SMTP, POP3/IMAP

* IP Address
  * public ip or dns - external - reachable over the internet
  * private ip or dns - internal - reachable in the private network

* Ports
  * An IP address has multiple ports for various servers
  * Each server binds to a port and listens for incoming connections
  * `http 22`
  * `https 443`
  * `dns 53`
  * `ssh 22`
  * `smtp 25`
  * Port ~ Apartment Number. Socket ~ Door of Apartment. IP address ~ street address
  * Port Forwarding

* https
  * When you use https protocol to make a connection from a browser, you see a green lock icon to the left
  * All data transfer between the client and server is encrypted
  * The server should know how to handle this connection
  * The server needs a certificate - .crt and a private key - .key 

* Generating an SSL certificate
  * Popular Implementation - openssl
  * Use openssl to generate a certificate signing request .csr
  * You can use these files to generate a self-sign certificate for local environment
  * You can submit these to a dns provider and request for a .crt and .key
  * Normally expires in 365 days
  * `openssl x509 -enddate -noout -in certif.crt` To check the expiration of a .crt

* Using an ssl Certificate
  * Turn on the ssl config option in nginx
  * Provide the .crt & .key files generated

* SSH
  * Secure Shell
  * Succesor to telnet, but encrypted
  * Popular Implementations - openssh
  * `ssh host`
  * `ssh user@host` - if username is different on the host
  * `ssh host cmd` - To run a single command on the host

* SSH configuration
  * `/etc/ssh/sshd_config` - Configures the ssh server
  * `sudo service ssh restart` - if you changed any configuration

* SSH Key based Authentication
  * `ssh-keygen -t rsa` Generates id_rsa id_rsa.pub in ~/.ssh folder
  * Provide the public key aka host key to the machines you want to access
  * Private Key ~ real life key.   Public Key ~ Real life lock
  * `.ssh/known_hosts` - Lists the servers your machine can connect with
  * `.ssh/authorized_keys` - Lists the key that were authorized to connect

* Http Protocol - Verbs
  * get - fetch an existing resource
  * post - creates a new resource
  * put - update an existing resource
  * delete - delete an existing resource
  * head - retrives the headers
  * options - retrieves the server capabilities
  * Safe Method - has no effect on the server - get
  * Idempotent Method - Effect of 1 method is the same as the effect of multiple methods - put, delete


* Http Status Codes
  * 1xx - informational messages
  * 2xx - success messages
  * 3xx - redirection messages
  * 4xx - client error 
  * 5xx - server error

* Http headers
  * Use Chrome inspector-Network panel to look at the request and response headers
  * Request payload in a post method is nothing but the form data
  * Options Method is also commonly known as preflight request
  * CORS - Cross Origin Resource Sharing
  * mime-type, content-type, file-extension
  * CORS - mechanism that allows resources to be shared from domains other than the origin
  * `Access-control-allow-origin` or `Access-control-allow-methods` etc
  * Necessary to prevent Cross-site-scripting attacks


