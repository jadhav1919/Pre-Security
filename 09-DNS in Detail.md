# DNS (Domain Name System)

## What is DNS?

DNS (Domain Name System) is the internet's phonebook.

Humans prefer remembering names such as:

```text
tryhackme.com
google.com
github.com
```

Computers communicate using IP addresses such as:

```text
104.26.10.229
```

DNS translates a domain name into its corresponding IP address.

### Example

```text
tryhackme.com
      ↓
104.26.10.229
```

Without DNS, we would have to remember IP addresses for every website we visit.

# Domain Structure

Example:

```text
admin.tryhackme.com
```

## TLD (Top-Level Domain)

The right-most part of a domain.

```text
tryhackme.com
           ↑
          TLD
```

### Types of TLDs

#### gTLD (Generic Top-Level Domain)

Examples:

```text
.com
.org
.edu
.gov
```

#### ccTLD (Country Code Top-Level Domain)

Examples:

```text
.co.uk
.ca
.in
.jp
```

Used to represent countries.


## Second-Level Domain

The main domain name.

Example:

```text
tryhackme.com
↑
Second-Level Domain
```

### Rules

* Maximum 63 characters
* Can contain:

  * a-z
  * 0-9
  * hyphens (-)

Cannot:

* Start with a hyphen
* End with a hyphen
* Contain consecutive hyphens


## Subdomain

A subdomain appears before the main domain.

Example:

```text
admin.tryhackme.com
```

Here:

```text
admin
```

is the subdomain.

### More Examples

```text
blog.google.com
mail.google.com
api.github.com
```

### Important Facts

* Maximum length: 63 characters
* Cannot use underscore (_)
* Multiple subdomains can exist

Example:

```text
jupiter.servers.tryhackme.com
```


# Domain Limits

| Item        | Maximum Length |
| ----------- | -------------- |
| Subdomain   | 63 Characters  |
| Domain Name | 253 Characters |

---

# DNS Record Types

DNS stores different types of records.

## A Record

Maps a domain name to an IPv4 address.

### Example

```text
tryhackme.com
      ↓
104.26.10.229
```

## AAAA Record

Maps a domain name to an IPv6 address.

### Example

```text
2606:4700:20::681a:be5
```


## CNAME Record

Points one domain to another domain.

### Example

```text
store.tryhackme.com
        ↓
shops.shopify.com
```

DNS then looks up the IP address of the destination domain.


## MX Record

Mail Exchange Record.

Specifies which server handles email for a domain.

### Example

```text
tryhackme.com
      ↓
mail.google.com
```

### Purpose

* Email delivery
* Backup mail servers
* Mail priority configuration


## TXT Record

Stores text information.

Common uses:

### Email Security

SPF

```text
Which servers can send email for a domain?
```

### Domain Verification

```text
Prove domain ownership
```

### DMARC

```text
Email protection policies
```


# DNS Resolution Process

When you type:

```text
www.tryhackme.com
```

DNS follows several steps.

## Step 1 - Local Cache

Your computer checks:

```text
Have I looked this up recently?
```

If yes:

```text
Return saved IP address
```

Done.


## Step 2 - Recursive DNS Server

If not found locally:

```text
Computer
    ↓
Recursive DNS Server
```

Usually provided by your ISP.

Examples:

```text
Google DNS
8.8.8.8

Cloudflare DNS
1.1.1.1
```

The recursive server checks its cache.

If found:

```text
Return result
```

Done.


## Step 3 - Root DNS Server

If not cached:

```text
Recursive DNS
      ↓
Root DNS Server
```

The root server identifies the TLD.

Example:

```text
www.tryhackme.com
                ↑
              .com
```

## Step 4 - TLD Server

The root server sends the request to the .com TLD server.

The TLD server knows where the domain's nameserver is located.


## Step 5 - Authoritative DNS Server

The authoritative server contains the actual DNS records.

Example:

```text
A Record
MX Record
TXT Record
CNAME Record
```

This server returns the correct answer.


## Step 6 - Response Returned

The answer travels back:

```text
Authoritative Server
          ↓
Recursive DNS
          ↓
Your Computer
```

Now the website can be visited.


# DNS Resolution Flow

```text
User
 ↓
Local Cache
 ↓
Recursive DNS Server
 ↓
Root DNS Server
 ↓
TLD Server
 ↓
Authoritative DNS Server
 ↓
IP Address Returned
```


# TTL (Time To Live)

TTL determines how long a DNS record should be cached.

Example:

```text
TTL = 3600
```

Means:

```text
Cache for 3600 seconds
(1 hour)
```

After that, DNS must be queried again.


# Key DNS Servers

## Recursive DNS Server

* Usually provided by ISP
* Performs DNS lookups on behalf of users
* Uses caching


## Authoritative DNS Server

* Stores actual DNS records
* Source of truth for a domain

---
