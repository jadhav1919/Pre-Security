# Offensive Security Intro

## Overview

This room introduced the fundamentals of **Offensive Security** and demonstrated how ethical hackers identify vulnerabilities in systems and web applications.

The room focused on understanding the attacker mindset and performing basic web enumeration using Gobuster.

---

# Key Concepts Learned

## What is Offensive Security?

Offensive Security involves:

* Simulating real-world cyber attacks
* Discovering vulnerabilities in systems
* Exploiting security weaknesses ethically
* Helping organizations improve their defenses

### Main Goal

Think like an attacker to secure systems before real hackers exploit them.

---

# Topics Covered

* Ethical Hacking Basics
* Offensive vs Defensive Security
* Website Enumeration
* Hidden Directory Discovery
* Basic Web Exploitation
* Using Gobuster

---

# Practical Exercise Performed

## Target Website

```bash
http://fakebank.thm
```

The objective was to discover hidden pages on the website and identify insecure functionality exposed to attackers.

---

# Tool Used

## Gobuster

Gobuster is a directory and file brute-forcing tool used to discover hidden content on websites.

### Command Used

```bash
gobuster -u http://fakebank.thm -w wordlist.txt dir
```

---

# Command Breakdown

| Option | Description                     |
| ------ | ------------------------------- |
| `-u`   | Target URL                      |
| `-w`   | Wordlist used for brute-forcing |
| `dir`  | Directory enumeration mode      |

---

# Enumeration Results

The scan discovered the following hidden paths:

```text
/images
/bank-transfer
```

The `/bank-transfer` page exposed sensitive banking functionality.

---

# Exploitation Scenario

An insecure bank transfer page allowed unauthorized money transfers between accounts.

### Task Performed

Transferred:

* `$2000`
* From Account: `2276`
* To Account: `8881`

This demonstrated how improper access controls can lead to serious security vulnerabilities.

---

# Security Lessons Learned

## Importance of Enumeration

Enumeration is one of the most critical phases in penetration testing because:

* Hidden pages may expose admin functionality
* Sensitive endpoints may lack authentication
* Misconfigurations can lead to unauthorized access

---

# Skills Practiced

* Basic Linux terminal usage
* Running security tools
* Web directory enumeration
* Understanding insecure web functionality
* Identifying exposed application features

---

# Cybersecurity Roles Mentioned

## Penetration Tester

Tests systems for exploitable vulnerabilities.

## Red Teamer

Simulates real-world attacks against organizations.

## Security Engineer

Builds and maintains defensive security systems.

---

# Key Takeaways

* Offensive Security focuses on attacking systems ethically.
* Enumeration is essential before exploitation.
* Hidden endpoints can expose sensitive functionality.
* Ethical hackers help organizations fix vulnerabilities before attackers exploit them.

---

# Platform

* TryHackMe

# Room

* Offensive Security Intro

# Status

✅ Completed
