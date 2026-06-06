# How Websites Work

## Overview

When you visit a website, your browser sends a request to a web server.

The web server processes the request and sends back a response that the browser displays.

```text id="zv14fh"
Browser
   ↓ Request
Web Server
   ↑ Response
Browser displays webpage
```

# Components of a Website

A website has two main parts:

## Front End (Client-Side)

The part users interact with in their browser.

Examples:

* Buttons
* Images
* Forms
* Menus
* Text

### Technologies Used

* HTML
* CSS
* JavaScript

## Back End (Server-Side)

The part running on the server.

Responsibilities:

* Processing requests
* Handling logins
* Accessing databases
* Returning responses

### Examples

```text id="qv5d3m"
User Login
     ↓
Backend checks database
     ↓
Success / Failure response
```


# HTML (HyperText Markup Language)

## What is HTML?

HTML is the language used to create the structure of a webpage.

Think of HTML as the skeleton of a website.

Without HTML, there would be no:

* Headings
* Paragraphs
* Images
* Buttons
* Forms


# Basic HTML Structure

```html id="jzwdhu"
<!DOCTYPE html>
<html>
<head>
    <title>My Website</title>
</head>

<body>
    <h1>Hello World</h1>
    <p>This is a paragraph.</p>
</body>
</html>
```

# Important HTML Tags

## html

Root element of the webpage.

```html id="h1z70e"
<html>
```

## head

Contains page information.

```html id="x7h42w"
<head>
```

Examples:

* Title
* Metadata


## body

Contains visible content.

```html id="l7r3b6"
<body>
```

Everything displayed in the browser is usually inside the body tag.


## h1

Creates a heading.

```html id="wjlwmz"
<h1>Welcome</h1>
```

## p

Creates a paragraph.

```html id="1frqcs"
<p>Hello World</p>
```

## img

Displays an image.

```html id="79zm0r"
<img src="cat.jpg">
```

## button

Creates a button.

```html id="4ht4h7"
<button>Click Me</button>
```


# HTML Attributes

Attributes provide extra information about elements.

Example:

```html id="m2f5lv"
<img src="cat.jpg">
```

Here:

```text id="u4e4gr"
src
```

is an attribute.


## Common Attributes

### class

Used for styling multiple elements.

```html id="6k2ovz"
<p class="red-text">
```

### id

Used to uniquely identify an element.

```html id="vk7o5f"
<p id="example">
```

Important:

* IDs must be unique.
* JavaScript often uses IDs.


### src

Specifies a file location.

```html id="8vx19q"
<img src="dog.png">
```

# CSS (Cascading Style Sheets)

## What is CSS?

CSS controls how a webpage looks.

Think of CSS as the appearance of a website.

Without CSS:

```text id="rrs35k"
Website works
But looks plain
```


## CSS Controls

* Colors
* Fonts
* Layout
* Spacing
* Animations

### Example

```css id="uzk6nt"
h1 {
    color: red;
}
```

This changes the heading color to red.


# JavaScript (JS)

## What is JavaScript?

JavaScript adds functionality and interactivity to a webpage.

Think of JavaScript as the brain of the webpage.


# What Can JavaScript Do?

### Change Text

```javascript id="5r4h7z"
document.getElementById("demo").innerHTML = "Hello";
```

### Respond to Clicks

```javascript id="c1g4s6"
button clicked
```

### Update Content Dynamically

```text id="ek2d0o"
Without reloading page
```

### Create Animations

```text id="j6gqpd"
Moving menus
Popups
Sliders
```


# HTML + CSS + JavaScript

Together they create modern websites.

```text id="zzmk9e"
HTML → Structure

CSS → Appearance

JavaScript → Functionality
```

### Example

```text id="bb5g4t"
Car Example

HTML = Car Frame
CSS = Car Paint
JavaScript = Engine
```


# Sensitive Data Exposure

## What is Sensitive Data Exposure?

Occurs when sensitive information is accidentally exposed to users.

Examples:

* Passwords
* API Keys
* Hidden URLs
* Secret Tokens
* Internal Information


# Example

A developer leaves:

```html id="ykwbgo"
<!-- Password: admin123 -->
```

inside the page source.

Anyone viewing the source code can see it.


# Why is it Dangerous?

Attackers may use exposed information to:

* Access accounts
* Access admin panels
* Discover hidden pages
* Escalate attacks


# Prevention

Never expose:

* Passwords
* Tokens
* Secrets
* Credentials

in:

* HTML
* JavaScript
* Public source code


# HTML Injection

## What is HTML Injection?

HTML Injection occurs when user input is displayed on a webpage without proper filtering.


## Example

Suppose a website asks:

```text id="0jctcw"
What is your name?
```

User enters:

```html id="78m9k8"
<h1>Hacked</h1>
```

If the website does not sanitize input:

```text id="qhmx5x"
The browser renders it as HTML
```

instead of displaying it as text.

# Why is HTML Injection Dangerous?

Attackers can:

* Modify page appearance
* Add fake content
* Insert malicious links
* Trick users

Example:

```html id="n0x4xe"
<a href="http://evil-site.com">
Click Here
</a>
```

# Input Sanitization

## What is Sanitization?

Sanitization means cleaning user input before displaying or processing it.


## Goal

Prevent:

* HTML Injection
* JavaScript Injection
* Other Injection Attacks

# Security Rule

```text id="j53n6y"
Never trust user input.
```

Always validate and sanitize data before using it.

---
