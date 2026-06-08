# Operating System Security

## What is an Operating System (OS)?

An Operating System (OS) is software that acts as an intermediary between hardware and applications.

### Role of an OS

* Manages hardware resources
* Runs applications
* Controls access to hardware
* Provides security mechanisms
* Manages files and users

### OS Layer Structure

```text
User
│
Applications
│
Operating System
│
Hardware
```

# Hardware vs Software

## Hardware

Physical components that can be touched.

Examples:

* CPU
* RAM
* Keyboard
* Mouse
* Monitor
* Printer
* HDD
* SSD

## Software

Programs and applications that run on hardware.

Examples:

* Operating Systems
* Browsers
* Messaging Apps
* Games

# Common Operating Systems

## Desktop Operating Systems

| OS      | Usage               |
| ------- | ------------------- |
| Windows | Personal computers  |
| macOS   | Apple computers     |
| Linux   | Desktop and servers |


## Mobile Operating Systems

| OS      | Usage             |
| ------- | ----------------- |
| Android | Smartphones       |
| iOS     | iPhones and iPads |



## Server Operating Systems

| OS             | Usage              |
| -------------- | ------------------ |
| Windows Server | Enterprise servers |
| Linux          | Web servers        |
| AIX            | Enterprise systems |
| Solaris        | Enterprise systems |


# CIA Triad

The foundation of information security.

## 1. Confidentiality

Ensures information is accessible only to authorized users.

### Goal

Prevent unauthorized access.

### Examples

* Password protection
* File permissions
* Encryption



## 2. Integrity

Ensures data cannot be modified without authorization.

### Goal

Protect data accuracy and trustworthiness.

### Examples

* File hashing
* Digital signatures
* Access controls


## 3. Availability

Ensures systems and data remain accessible when needed.

### Goal

Prevent service interruptions.

### Examples

* Backups
* Redundancy
* Disaster recovery


# Operating System Security Threats

Three common security weaknesses:

1. Weak Authentication
2. Weak File Permissions
3. Malicious Programs


# Authentication

Authentication is the process of verifying identity.

## Authentication Factors

### Something You Know

Examples:

* Password
* PIN


### Something You Are

Examples:

* Fingerprint
* Face recognition


### Something You Have

Examples:

* Mobile phone
* Security token
* Smart card


# Weak Passwords

Weak passwords are easy to guess or crack.

Examples:

```text
123456
password
qwerty
abc123
iloveyou
```


## Characteristics of Weak Passwords

* Common words
* Dictionary words
* Personal information
* Keyboard patterns
* Short length

Examples:

```text
qwerty
123456
dragon
monkey
```

## Characteristics of Strong Passwords

* Long length
* Uppercase letters
* Lowercase letters
* Numbers
* Special characters
* Unique for each account

Example:

```text
LearnM00r
```

# Password Security Best Practices

## Use Unique Passwords

Never reuse passwords across websites.

Bad:

```text
Facebook = Password123
Gmail = Password123
Instagram = Password123
```

Good:

```text
Facebook = Unique Password
Gmail = Different Password
Instagram = Different Password
```


## Use Password Managers

Benefits:

* Generate strong passwords
* Store passwords securely
* Prevent password reuse


## Enable Multi-Factor Authentication (MFA)

Combines:

```text
Password
+
Phone Verification
```

This greatly increases security.


# Principle of Least Privilege (PoLP)

Users should only receive permissions necessary to perform their tasks.

## Rule

```text
Minimum Access Required
```


## Benefits

* Reduces attack surface
* Limits damage from compromised accounts
* Protects sensitive data


# File Permissions

File permissions determine:

```text
Who can access a file
Who can modify a file
Who can execute a file
```


# Risks of Weak File Permissions

## Confidentiality Impact

Unauthorized users can read files.

Example:

```text
Private Documents
Passwords
Financial Records
```


## Integrity Impact

Unauthorized users can modify files.

Example:

```text
Edit reports
Delete data
Modify configurations
```


# Malicious Programs (Malware)

Software designed to harm systems or steal information.


## Common Malware Types

### Trojan Horse

Pretends to be legitimate software.

Capabilities:

* Remote access
* Data theft
* System control

Impacts:

```text
Confidentiality
Integrity
```

### Ransomware

Encrypts files and demands payment.

Effects:

```text
Files become inaccessible
Victim pays ransom
```

Impacts:

```text
Availability
```

# Linux Accounts

Linux uses user accounts to control access.

Examples:

```text
sammie
johnny
linda
```


# Root Account

Most privileged account in Linux.

Equivalent to:

```text
Administrator (Windows)
Root (Linux)
```

Root can:

* Read any file
* Modify any file
* Install software
* Create users
* Delete system files


# Linux Commands Used

## whoami

Displays current user.

```bash
whoami
```

Example:

```bash
sammie
```


## ssh

Securely connect to a remote Linux system.

Syntax:

```bash
ssh username@IP
```

Example:

```bash
ssh sammie@192.168.1.10
```


## ls

Lists files and directories.

```bash
ls
```

Example:

```text
notes.txt
image.jpg
password.txt
```

## cat

Displays file contents.

Syntax:

```bash
cat filename
```

Example:

```bash
cat notes.txt
```


## history

Displays previously executed commands.

Syntax:

```bash
history
```

Example Output:

```text
1 ls
2 cat notes.txt
3 sudo su
```

# Privilege Escalation

Privilege escalation occurs when a user gains higher privileges than intended.

Example:

```text
User Account
↓
Root Account
```


## Why It Is Dangerous

Attackers can:

* Access sensitive files
* Install malware
* Modify system settings
* Create backdoors

# Common Attack Path

## Step 1

Obtain username.

Example:

```text
johnny
```

## Step 2

Guess weak password.

Example:

```text
abc123
```

## Step 3

Login to account.

```bash
ssh johnny@IP
```

## Step 4

Check command history.

```bash
history
```

## Step 5

Discover sensitive information.

Example:

```text
Root Password
```

## Step 6

Switch to root.

```bash
su - root
```

## Step 7

Gain full system access.


# Security Lessons

## Never Use Weak Passwords

Bad:

```text
123456
abc123
dragon
password
```

Good:

```text
LearnM00r
```


## Never Reuse Passwords

One breached website can expose all accounts.

 

## Protect Command History

Sensitive information should never be typed directly into commands.

 
## Apply Least Privilege

Give users only required permissions.


## Monitor Privileged Accounts

Root and administrator accounts require additional protection.

---

