# Search Skills

## Overview

This room introduced essential search techniques and online resources used in cyber security for both offensive and defensive purposes.

Cyber security professionals frequently rely on search engines, threat intelligence platforms, vulnerability databases, documentation, and open-source repositories to gather information during investigations, penetration testing, vulnerability research, and incident response.

The lesson demonstrated how effective searching is a critical skill in cyber security.

---

# Key Concepts Learned

## Importance of Search Skills in Cyber Security

Search skills help security professionals:

* Find vulnerabilities
* Research exploits
* Investigate threat actors
* Understand security tools
* Analyze suspicious files
* Gather intelligence
* Troubleshoot technical issues

---

# Topics Covered

* Shodan
* VirusTotal
* CVE Database
* CVSS Scoring
* Linux MAN Pages
* GitHub Security Research
* Open-Source Intelligence (OSINT)

---

# Shodan

## What is Shodan?

Shodan is a search engine used to discover internet-connected devices and services.

It scans the internet continuously and indexes:

* Web servers
* IoT devices
* Industrial control systems
* Security cameras
* Network infrastructure

---

# Practical Exercise — Shodan Simulation

## Objective

Use a Shodan-like interface to search for publicly exposed Apache servers.

## Search Performed

```text id="5f3qvt"
apache
```

---

# Shodan Filters Learned

| Filter     | Purpose                    | Example                 |
| ---------- | -------------------------- | ----------------------- |
| `country`  | Search by country          | `country:IE`            |
| `port`     | Search by port number      | `port:22`               |
| `org`      | Search by organization/ASN | `AS7224`                |
| `hostname` | Search by hostname/domain  | `hostname:fakebank.thm` |

---

# Skills Practiced

* Internet-wide reconnaissance
* Service identification
* Public asset discovery
* Understanding exposed services

---

# VirusTotal

## What is VirusTotal?

VirusTotal is a threat intelligence platform that analyzes:

* Files
* URLs
* Domains
* File hashes

using multiple antivirus engines and security scanners.

---

# Practical Exercise — VirusTotal Simulation

## Task

Analyze the suspicious file:

```text id="jlwmf3"
invoice_payment.exe
```

The platform displayed security vendors that flagged the file as malicious.

---

# Key Learning

* VirusTotal aggregates results from multiple antivirus engines.
* Security analysts use it to investigate suspicious files and malware.
* It helps identify known malicious indicators quickly.

---

# CVE and Vulnerability Databases

## What is a CVE?

CVE stands for:

```text id="vvpl3v"
Common Vulnerabilities and Exposures
```

Each vulnerability receives a unique identifier such as:

```text id="w99jjt"
CVE-2026-1337
```

---

# CVSS Scoring

CVSS (Common Vulnerability Scoring System) measures vulnerability severity based on:

* Impact
* Exploit complexity
* Availability
* Risk level

Organizations prioritize patching high-severity vulnerabilities first.

---

# Practical Exercise — Vulnerability Database

## Task

Investigated the vulnerability:

```text id="hdm7ht"
CVE-2026-1337
```

Reviewed:

* Vulnerability details
* Severity rating
* CVSS score
* Exploitation information

---

# Linux MAN Pages

## What are MAN Pages?

Linux MANual pages provide built-in command documentation directly in the terminal.

## Example Usage

```bash id="4a4gv4"
man nc
```

This displays the manual page for the `nc` (netcat) command.

---

# Practical Exercise — MAN Page Simulation

## Example Command Found

```bash id="mh0k1v"
nc host.example.com 42
```

This command opens a connection to:

* Host: `host.example.com`
* Port: `42`

---

# GitHub in Cyber Security

## Why GitHub is Important

GitHub is widely used in cyber security for:

* Proof-of-Concept (PoC) exploits
* Security research
* Vulnerability analysis
* Exploitation tools
* Detection scripts

Researchers often publish vulnerability research faster than official vendors.

---

# Practical Exercise — GitHub Repository Review

## Vulnerability Investigated

```text id="df57o8"
CVE-2026-1337
```

Reviewed the repository README and identified the exploit script.

## Script Name

```text id="a84kfk"
exploit.py
```

---

# Tools and Platforms Covered

| Tool/Platform   | Purpose                          |
| --------------- | -------------------------------- |
| Shodan          | Internet-connected device search |
| VirusTotal      | Malware and file analysis        |
| CVE Database    | Vulnerability tracking           |
| Linux MAN Pages | Command documentation            |
| GitHub          | Security research and PoCs       |

---

# Skills Practiced

* OSINT techniques
* Vulnerability research
* Threat intelligence gathering
* Malware investigation
* Documentation usage
* Security research
* Reconnaissance techniques

---

# Key Takeaways

* Search skills are essential in cyber security.
* Shodan helps discover exposed internet services.
* VirusTotal helps analyze suspicious files and domains.
* CVEs provide standardized vulnerability tracking.
* MAN pages are critical for learning Linux commands.
* GitHub is a valuable source for security research and PoC exploits.

---

# Platform

* TryHackMe

# Room

* Search Skills

# Status

✅ Completed
