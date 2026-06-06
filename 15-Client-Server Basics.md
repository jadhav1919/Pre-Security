# Client-Server Model

## Overview

Modern computer systems communicate with each other using the Client-Server model.

A client requests a service or resource, and a server provides it.

```text
Client  ---> Request ---> Server
Client <--- Response --- Server
```

### Examples

| Client            | Server      |
| ----------------- | ----------- |
| Web Browser       | Web Server  |
| Email Application | Mail Server |
| Mobile App        | API Server  |


# Client

A client is a device or application that initiates communication and requests services.

## Examples

* Google Chrome
* Firefox
* Microsoft Outlook
* Mobile Applications

### Responsibilities

* Send requests
* Receive responses
* Display information to users

### Important Point

The client always starts the communication.


# Server

A server is a system that provides services, resources, or data to clients.

## Examples

* Web Servers
* Database Servers
* Mail Servers
* File Servers

### Responsibilities

* Receive requests
* Process requests
* Send responses

# Request and Response

Communication between a client and server follows a request-response model.

### Example

```text
Browser requests webpage
         ↓
Web Server processes request
         ↓
Web Server sends webpage
```

# Protocol

A protocol is a set of rules that defines how devices communicate.

Protocols specify:

* Message format
* Commands
* Response types
* Error handling

### Examples

| Protocol | Purpose                  |
| -------- | ------------------------ |
| HTTP     | Web Communication        |
| HTTPS    | Secure Web Communication |
| FTP      | File Transfer            |
| SMTP     | Email Transfer           |
| DNS      | Domain Name Resolution   |


# Port

A port identifies a specific service running on a server.

A single server can run multiple services simultaneously.

Each service uses a different port number.

### Examples

| Service | Port |
| ------- | ---- |
| HTTP    | 80   |
| HTTPS   | 443  |
| FTP     | 21   |
| SSH     | 22   |

### Example

```text
192.168.1.10:80
```

* IP Address → 192.168.1.10
* Port → 80


# DNS (Domain Name System)

DNS translates domain names into IP addresses.

### Example

```text
google.com
      ↓
142.250.x.x
```

Humans remember domain names.

Computers communicate using IP addresses.

### Purpose

* Domain Name → IP Address
* Makes websites easier to access


# IP Address

An IP address uniquely identifies a device on a network.

### Example

```text
192.168.1.100
```

### Purpose

* Device identification
* Communication between systems


# HTTP (HyperText Transfer Protocol)

HTTP is a protocol used for communication between web browsers and web servers.

### Characteristics

* Client-Server Protocol
* Stateless
* Request-Response Based


# Stateless Protocol

HTTP does not remember previous requests.

Each request is processed independently.

### Example

```text
Request 1
↓

Processed

Request 2
↓

Processed separately
```

The server does not automatically remember earlier requests.


# Maintaining State

Web applications use:

* Cookies
* Session IDs
* Tokens

to remember users between requests.

### Example

```text
User Logs In
      ↓
Server Creates Session
      ↓
Session ID Stored
      ↓
Future Requests Include Session ID
```

# HTTP Methods

HTTP methods define the action the client wants to perform.

## GET

Retrieves information from a server.

### Example

```http
GET /index.html
```

Purpose:

```text
Retrieve data
```

### Common Uses

* View webpages
* Read articles
* Fetch images


## Other Common Methods

| Method | Purpose               |
| ------ | --------------------- |
| GET    | Retrieve Data         |
| POST   | Create Data           |
| PUT    | Update Data           |
| DELETE | Remove Data           |
| PATCH  | Partially Update Data |

# URL Components

Example:

```text
https://www.iamlearning.thm/contact
```

### Scheme

```text
https
```

Defines the protocol.

---

### Host

```text
www.iamlearning.thm
```

Identifies the server.

### Path

```text
/contact
```

Identifies the requested resource.


# HTTP Request

A request is sent by the client to the server.

### Example

```http
GET / HTTP/1.1
Host: example.com
```

# HTTP Response

A response is sent by the server back to the client.

### Example

```http
HTTP/1.1 200 OK
```


# Important Response Information

## Status Code

Indicates the result of the request.

### Example

```text
200 OK
```

Request completed successfully.


## Response Header

Contains metadata about the response.

Examples:

* Content-Type
* Content-Length
* Server Information

## Response Body

Contains the requested content.

Examples:

* HTML
* Images
* JSON Data
* Files

# Complete Web Request Flow

```text
User enters URL
        ↓
DNS resolves domain name
        ↓
IP Address returned
        ↓
Browser connects to server
        ↓
HTTP Request sent
        ↓
Server processes request
        ↓
HTTP Response returned
        ↓
Browser displays content
```
