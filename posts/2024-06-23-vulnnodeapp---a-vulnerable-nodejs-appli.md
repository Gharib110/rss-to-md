---
title: "VulnNodeApp - A Vulnerable NodeJs Application"
date: Sun, 23 Jun 2024 08:30:00 -0400
draft: false
type: posts
categories: 
- Scripting,vulnerabilities,Vulnerability,Vulnerable,VulnNodeApp
---
# VulnNodeApp - A Vulnerable NodeJs Application

<br/>

<br/>
[![](https://blogger.googleusercontent.com/img/a/AVvXsEjhkbtFHEZYZ2XWPDOmuQB510cU5uUDArQC0gsTgoippwjw8deFa6WZgTE4ubxRQ1ntloFXY__gPPWp9Ffeo7iqYqdKGeXzlNPd0VlvaX2S9wLXONtEvXzdPt2K68TYbV2m87R-CbCGQqgq6rc85_LeEeRMhCoxWPi7hImJVMsOk3YxRft3eO4kRFmtwpOw=w640-h320)](https://blogger.googleusercontent.com/img/a/AVvXsEjhkbtFHEZYZ2XWPDOmuQB510cU5uUDArQC0gsTgoippwjw8deFa6WZgTE4ubxRQ1ntloFXY__gPPWp9Ffeo7iqYqdKGeXzlNPd0VlvaX2S9wLXONtEvXzdPt2K68TYbV2m87R-CbCGQqgq6rc85_LeEeRMhCoxWPi7hImJVMsOk3YxRft3eO4kRFmtwpOw)

  

A [vulnerable](https://www.kitploit.com/search/label/Vulnerable "vulnerable") application made using node.js, express server and ejs template engine. This application is meant for educational purposes only.

  

Setup
=====

Clone this repository
---------------------

```
git clone https://github.com/4auvar/VulnNodeApp.git
```

Application setup:
------------------

-   Install the latest node.js version with npm.
-   Open terminal/command prompt and navigate to the location of downloaded/cloned repository.
-   Run command: `npm install`

DB setup
--------

-   Install and configure latest mysql version and start the mysql service/deamon
-   Login with root user in mysql and run below sql script:

```
CREATE USER 'vulnnodeapp'@'localhost' IDENTIFIED BY 'password';create database vuln_node_app_db;GRANT ALL PRIVILEGES ON vuln_node_app_db.* TO 'vulnnodeapp'@'localhost';USE vuln_node_app_db;create table users (id int AUTO_INCREMENT PRIMARY KEY, fullname varchar(255), username varchar(255),password varchar(255), email varchar(255), phone varchar(255), profilepic varchar(255));insert into users(fullname,username,password,email,phone) values("test1","test1","test1","test1@test.com","976543210");insert into users(fullname,username,password,email,phone) values("test2","test2","test2","test2@test.com","9887987541");insert into users(fullname,username,password,email,phone) values("test3","test3","test3","test3@test.com","9876987611");insert into users(fullname,username,password,email,phone) values("test4","test4","test4","test4@test.com","9123459876");insert into users(fullname,username,password,email,phone) values("test5","test5","test   5","test5@test.com","7893451230");
```

Set basic environment variable
------------------------------

-   User needs to set the below environment variable.
    -   DATABASE\_HOST (E.g: localhost, 127.0.0.1, etc...)
    -   DATABASE\_NAME (E.g: vuln\_node\_app\_db or DB name you change in above DB script)
    -   DATABASE\_USER (E.g: vulnnodeapp or user name you change in above DB script)
    -   DATABASE\_PASS (E.g: password or password you change in above DB script)

Start the server
================

-   Open the command prompt/terminal and navigate to the location of your repository
-   Run command: `npm start`
-   Access the application at http://localhost:3000

Vulnerability covered
=====================

-   SQL Injection
-   Cross Site Scripting (XSS)
-   Insecure Direct Object Reference (IDOR)
-   Command Injection
-   Arbitrary File Retrieval
-   Regular Expression Injection
-   External XML Entity Injection (XXE)
-   Node js Deserialization
-   Security Misconfiguration
-   Insecure Session Management

TODO
====

-   Will add new vulnerabilities such as CORS, Template Injection, etc...
-   Improve application documentation

Issues
======

-   In case of bugs in the application, feel free to create an [issues](https://github.com/4auvar/VulnNodeApp/issues "issues") on github.

Contribution
============

-   Feel free to create a pull request for any contribution.

You can reach me out at [@4auvar](https://twitter.com/4auvar "@4auvar")

  
  

**[Download VulnNodeApp](https://github.com/4auvar/VulnNodeApp "Download VulnNodeApp")**

[Source](http://www.kitploit.com/2024/06/vulnnodeapp-vulnerable-nodejs.html)
<br/>
---
