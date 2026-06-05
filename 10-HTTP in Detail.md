# HTTP Fundamentals

## What is HTTP?

**HTTP (HyperText Transfer Protocol)** is the protocol used for communication between a web browser and a web server.

When you open a website:

```text
Browser  ←→  Web Server
```

HTTP defines the rules for how requests and responses are exchanged.

### Example

When you visit:

```text
https://tryhackme.com
```

Your browser sends an HTTP request to the server, and the server sends back:

* HTML
* Images
* CSS
* JavaScript
* Videos

# What is HTTPS?

**HTTPS (HyperText Transfer Protocol Secure)** is the secure version of HTTP.

HTTPS encrypts data before it is sent across the internet.

### Benefits

* Prevents attackers from reading data.
* Protects usernames and passwords.
* Confirms you are talking to the real website.

### Example

```text
HTTP  → Data visible
HTTPS → Data encrypted
```

### Common Ports

| Protocol | Port |
| -------- | ---- |
| HTTP     | 80   |
| HTTPS    | 443  |

# What is a URL?

A URL (Uniform Resource Locator) is the address used to access a resource on the internet.

### Example

```text
http://user:password@tryhackme.com:80/view-room?id=1#task3
```


# Parts of a URL

## 1. Scheme

Specifies the protocol.

Example:

```text
http
https
ftp
```

## 2. User Information

Used for authentication.

Example:

```text
user:password
```


## 3. Host

The domain name or IP address.

Example:

```text
tryhackme.com
```

## 4. Port

Specifies which service to connect to.

Example:

```text
80   → HTTP
443  → HTTPS
```


## 5. Path

The location of the resource.

Example:

```text
/view-room
```


## 6. Query String

Extra information sent to the server.

Example:

```text
?id=1
```

Meaning:

```text
Give me item with ID 1
```


## 7. Fragment

Points to a specific section on a page.

Example:

```text
#task3
```


# HTTP Request

A request is sent from the client (browser) to the server.

### Example

```http
GET / HTTP/1.1
Host: tryhackme.com
User-Agent: Firefox
```

### What Happens?

```text
Browser
   ↓ Request
Web Server
```

The browser asks for a resource.

# HTTP Response

A response is sent from the server back to the client.

### Example

```http
HTTP/1.1 200 OK
Content-Type: text/html
```

### What Happens?

```text
Browser
   ↑ Response
Web Server
```

The server returns the requested data.


# Important Response Headers

## Content-Length

Tells the browser how much data to expect.

### Example

```http
Content-Length: 1000
```

Meaning:

```text
The response contains 1000 bytes.
```


## Content-Type

Tells the browser what type of data is being returned.

### Examples

```text
text/html
image/png
application/pdf
```


# HTTP Methods

HTTP methods tell the server what action the client wants to perform.


## GET

Used to retrieve information.

### Example

```text
View a blog post
View a profile
Open a webpage
```


## POST

Used to create new data.

### Example

```text
Create account
Submit form
Create blog post
```


## PUT

Used to update existing data.

### Example

```text
Change email address
Edit profile
```

## DELETE

Used to remove data.

### Example

```text
Delete account
Delete uploaded image
```


# HTTP Status Codes

Status codes tell us whether a request succeeded or failed.


## 1xx - Informational

Request received.

```text
100 Continue
```


## 2xx - Success

Request completed successfully.

### Examples

```text
200 OK
201 Created
```

## 3xx - Redirection

Redirects the user somewhere else.

### Examples

```text
301 Moved Permanently
302 Found
```


## 4xx - Client Errors

Problem caused by the client.

### Examples

```text
400 Bad Request
401 Unauthorized
403 Forbidden
404 Not Found
405 Method Not Allowed
```

## 5xx - Server Errors

Problem caused by the server.

### Examples

```text
500 Internal Server Error
503 Service Unavailable
```

# Most Important Status Codes

| Code | Meaning                 |
| ---- | ----------------------- |
| 200  | Success                 |
| 201  | Resource Created        |
| 301  | Permanent Redirect      |
| 302  | Temporary Redirect      |
| 401  | Authentication Required |
| 403  | Access Denied           |
| 404  | Page Not Found          |
| 500  | Server Error            |
| 503  | Service Unavailable     |


# HTTP Headers

Headers contain additional information about requests and responses.


## Common Request Headers

### Host

Specifies which website is being requested.

```http
Host: tryhackme.com
```

### User-Agent

Specifies the browser.

```http
User-Agent: Firefox
```


### Content-Length

Specifies how much data is being sent.


### Cookie

Sends stored cookie data to the server.


# Common Response Headers

### Set-Cookie

Stores cookie data on the user's browser.


### Content-Type

Specifies the type of returned data.


### Cache-Control

Controls browser caching.


### Content-Encoding

Specifies compression type.


# Cookies

HTTP is stateless, meaning the server does not automatically remember previous requests.

Cookies help websites remember users.

## How Cookies Work

### Step 1

Server sends:

```http
Set-Cookie: session=abc123
```

### Step 2

Browser stores the cookie.

### Step 3

Future requests automatically include:

```http
Cookie: session=abc123
```

### Result

The server can recognize the user.

# Common Uses of Cookies

* User login sessions
* Shopping carts
* Website preferences
* User tracking

# Example Login Process

```text
1. User logs in
        ↓
2. Server creates session
        ↓
3. Server sends Set-Cookie
        ↓
4. Browser stores cookie
        ↓
5. Browser sends cookie with future requests
        ↓
6. User stays logged in
```

---
