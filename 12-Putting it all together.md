# How Websites Work - Complete Overview

## What Happens When We Visit a Website?

When we enter a website address in a browser:

```text id="3y8rqh"
https://tryhackme.com
```

many things happen behind the scenes.

### Step 1: DNS Lookup

The browser needs to find the IP address of the website.

```text id="syjlwm"
tryhackme.com
      ↓
104.26.xx.xxx
```

DNS converts the domain name into an IP address.


### Step 2: Establish Connection

The browser connects to the server using:

```text id="ovpkh9"
HTTP
or
HTTPS
```

HTTPS is the secure version because it encrypts data.


### Step 3: Send Request

The browser sends an HTTP request.

Example:

```http id="pgjlwm"
GET / HTTP/1.1
```

This means:

```text id="mxa6xh"
Please send me the homepage.
```


### Step 4: Server Response

The web server returns:

* HTML
* CSS
* JavaScript
* Images
* Videos


### Step 5: Browser Renders Website

The browser combines everything and displays the webpage.

```text id="m0wiyh"
Browser
   ↓
HTML
CSS
JavaScript
Images
   ↓
Website Displayed
```

# Load Balancers

## What Problem Do They Solve?

Imagine a website receives millions of visitors.

A single server may become overloaded.


## What is a Load Balancer?

A load balancer sits in front of multiple servers and distributes traffic among them.

### Without Load Balancer

```text id="lm7fuz"
Users
  ↓
Server
```

One server handles everything.


### With Load Balancer

```text id="kg4zvg"
Users
   ↓
Load Balancer
  ↙ ↓ ↘
Server1
Server2
Server3
```

Traffic is shared among multiple servers.


## Benefits

### Better Performance

No single server becomes overloaded.

### High Availability

If one server fails:

```text id="tzl6q4"
Server1 

Traffic automatically goes to:

Server2 
Server3 
```

Users may not even notice the failure.


## Health Checks

Load balancers continuously check whether servers are working.

This process is called:

```text id="67tyl6"
Health Check
```

If a server fails the health check, traffic is no longer sent to it.


# CDN (Content Delivery Network)

## What is a CDN?

A CDN stores copies of static website files across many servers worldwide.


## Why Use a CDN?

Imagine:

```text id="hj9hkm"
Website Server
Location: USA
```

A user in India requests an image.

Without CDN:

```text id="v3bqzs"
India
  ↓
USA
```

Slow.

With CDN:

```text id="vq1rhv"
India
  ↓
Nearest CDN Server
```

Much faster.


## CDN Stores

Usually static content:

* Images
* CSS
* JavaScript
* Videos
* Downloads


## Benefits

### Faster Website Loading

Files are served from the nearest location.

### Reduced Server Load

The main server handles fewer requests.


# Databases

## Why Are Databases Needed?

Websites often need to store information.

Examples:

* User accounts
* Passwords
* Blog posts
* Orders
* Messages


## Example

When a user logs in:

```text id="8e2nnm"
Username + Password
         ↓
Database Check
         ↓
Login Success/Failure
```

## Popular Databases

### MySQL

Very common relational database.

### PostgreSQL

Advanced relational database.

### MSSQL

Microsoft SQL Server.

### MongoDB

NoSQL database.


# WAF (Web Application Firewall)

## What is a WAF?

A WAF sits between the user and the web server.

### Normal Flow

```text id="bjlwmx"
User
  ↓
Web Server
```

### With WAF

```text id="h7q7fc"
User
  ↓
WAF
  ↓
Web Server
```

## Purpose

Protect web applications from attacks.

## What Does a WAF Check?

### Malicious Requests

Example:

```text id="hytu7u"
SQL Injection
XSS
Command Injection
```


### Bots

Detects automated traffic.


### Rate Limiting

Prevents excessive requests.

Example:

```text id="o1aqvx"
Maximum:
100 requests per minute
```

Requests above the limit may be blocked.


# Web Servers

## What is a Web Server?

A web server is software that:

* Receives HTTP requests
* Processes them
* Sends responses

## Popular Web Servers

### Apache

Most widely used web server.

### Nginx

Known for speed and performance.

### IIS

Microsoft web server.

### NodeJS

JavaScript runtime often used for web applications.


# Root Directory

Web servers serve files from a specific directory.

### Linux

```text id="kl5v6w"
/var/www/html
```

### Windows IIS

```text id="z6bhvh"
C:\inetpub\wwwroot
```


## Example

Request:

```text id="nd9b9l"
http://example.com/image.jpg
```

Server returns:

```text id="bbn0z0"
/var/www/html/image.jpg
```

# Virtual Hosts

## Problem

One server may host multiple websites.

Example:

```text id="3n2ppr"
google.com
example.com
blog.com
```

## Solution

Virtual Hosts

The web server checks:

```http id="y0ljv7"
Host: example.com
```

and loads the correct website.


## Example

```text id="q0j99t"
example.com
     ↓
/var/www/site1

blog.com
     ↓
/var/www/site2
```

One server, multiple websites.


# Static Content

## What is Static Content?

Content that does not change.

Examples:

* Images
* CSS
* JavaScript Files
* PDFs

## Example

```text id="zkpr5m"
logo.png
```

Everyone receives the same file.


# Dynamic Content

## What is Dynamic Content?

Content that changes depending on the request.


## Example

### Search Engine

Search:

```text id="nzm9j0"
cats
```

Result:

```text id="6mtx5m"
Cat Articles
```

Search:

```text id="4yy0u4"
dogs
```

Result:

```text id="m50v2n"
Dog Articles
```

Different output based on user input.


# Backend Languages

## What is Backend Code?

Backend code runs on the server.

Users never see it.

## Common Backend Languages

* PHP
* Python
* JavaScript (NodeJS)
* Ruby
* Perl


# Example

URL:

```text id="a0wkpw"
example.com/index.php?name=adam
```

PHP Code:

```php id="4r4mns"
Hello <?php echo $_GET["name"]; ?>
```

Output:

```html id="1oh9vd"
Hello adam
```

## Important Point

The user only sees:

```html id="4ckf9q"
Hello adam
```

The PHP code remains hidden on the server.

# Frontend vs Backend

| Frontend        | Backend            |
| --------------- | ------------------ |
| Runs in Browser | Runs on Server     |
| User Can See It | User Cannot See It |
| HTML            | PHP                |
| CSS             | Python             |
| JavaScript      | NodeJS             |
| Images          | Database Logic     |

---
