# Linux CLI Basics

## What is Linux?

Linux is an open-source operating system widely used in:

* Servers
* Cloud Computing
* Cyber Security
* Networking Devices
* Embedded Systems

Linux is very popular in cybersecurity because most security tools run on Linux.


# What is CLI?

CLI = Command Line Interface

A text-based interface where users interact with the operating system by typing commands.

Example:

```bash
ls
pwd
cd
```


# Why Use CLI?

Advantages:

* Faster than GUI
* More control over the system
* Uses fewer resources
* Essential for cybersecurity work
* Many security tools only work in CLI


# Linux Filesystem Basics

Linux stores everything inside a hierarchical directory structure.

Root Directory:

```text
/
```

Example Structure:

```text
/
├── home
├── etc
├── var
├── usr
├── root
```



# Important Directories

| Directory | Purpose                     |
| --------- | --------------------------- |
| /         | Root directory              |
| /home     | User home directories       |
| /etc      | Configuration files         |
| /var      | Logs and variable data      |
| /usr      | Applications and programs   |
| /root     | Home directory of root user |
| /tmp      | Temporary files             |



# Home Directory

Each user has a home directory.

Example:

```text
/home/ubuntu
```

Shortcut:

```bash
~
```

Example:

```bash
cd ~
```

Moves directly to home directory.


# pwd Command

## Purpose

Displays current working directory.

### Syntax

```bash
pwd
```

### Example

```bash
$ pwd
/home/ubuntu
```


# ls Command

## Purpose

Lists files and directories.

### Syntax

```bash
ls
```

### Example

```bash
$ ls
Desktop Documents Downloads
```


# ls -l Command

## Purpose

Displays detailed information.

### Syntax

```bash
ls -l
```

### Information Shown

* Permissions
* Owner
* Group
* File Size
* Date Modified
* File Name

Example:

```bash
drwxr-xr-x Documents
```


# ls -a Command

## Purpose

Shows hidden files.

### Syntax

```bash
ls -a
```


# ls -al Command

## Purpose

Shows hidden files with detailed information.

### Syntax

```bash
ls -al
```


# Hidden Files

Hidden files begin with a dot (.).

Examples:

```text
.bashrc
.profile
.gitconfig
```

They are normally hidden from standard directory listings.


# cd Command

## Purpose

Change directory.

### Syntax

```bash
cd directory_name
```

### Example

```bash
cd Documents
```


# Move Back One Directory

### Syntax

```bash
cd ..
```

### Example

```bash
/home/ubuntu/Documents
```

↓

```bash
cd ..
```

↓

```bash
/home/ubuntu
```


# find Command

## Purpose

Search for files and directories.

### Syntax

```bash
find starting_location -name filename
```

### Example

```bash
find ~ -name mission_brief.txt
```

Output:

```text
/home/ubuntu/Documents/mission_brief.txt
```


# cat Command

## Purpose

Display file contents.

### Syntax

```bash
cat filename
```

### Example

```bash
cat mission_brief.txt
```


# whoami Command

## Purpose

Displays current logged-in user.

### Syntax

```bash
whoami
```

### Example

```bash
ubuntu
```


# uname Command

## Purpose

Displays operating system information.

### Syntax

```bash
uname
```

### Example

```bash
Linux
```


# uname -a Command

## Purpose

Displays complete system information.

### Syntax

```bash
uname -a
```

### Example Output

```bash
Linux tryhackme 6.14.0-1018-aws x86_64 GNU/Linux
```

### Information Shown

| Field          | Meaning             |
| -------------- | ------------------- |
| Linux          | Kernel name         |
| Hostname       | Computer name       |
| Kernel Version | Linux version       |
| x86_64         | System architecture |
| GNU/Linux      | OS type             |


# df Command

## Purpose

Displays disk usage.

### Syntax

```bash
df
```


# df -h Command

## Purpose

Displays disk usage in human-readable format.

### Syntax

```bash
df -h
```

### Example

```bash
Filesystem Size Used Avail Use%
/dev/root 70G 12G 58G 17%
```

### Information Shown

| Column | Meaning               |
| ------ | --------------------- |
| Size   | Total disk size       |
| Used   | Used space            |
| Avail  | Free space            |
| Use%   | Disk usage percentage |


# Reading System Information

Linux stores system information inside configuration files.

Important location:

```text
/etc
```


# Navigate to /etc

```bash
cd /etc
```


# View Files in /etc

```bash
ls
```


# os-release File

Contains Linux distribution information.

### Read File

```bash
cat /etc/os-release
```

Example:

```text
NAME="Ubuntu"
VERSION="24.04.1 LTS"
```


# Important Linux Commands Summary

| Command  | Purpose                   |
| -------- | ------------------------- |
| pwd      | Show current directory    |
| ls       | List files                |
| ls -l    | Detailed file list        |
| ls -a    | Show hidden files         |
| ls -al   | Detailed hidden files     |
| cd       | Change directory          |
| cd ..    | Move back one directory   |
| find     | Search files              |
| cat      | Display file contents     |
| whoami   | Current username          |
| uname    | OS information            |
| uname -a | Full system information   |
| df       | Disk usage                |
| df -h    | Human-readable disk usage |


# Common Symbols

| Symbol | Meaning           |
| ------ | ----------------- |
| /      | Root directory    |
| ~      | Home directory    |
| .      | Current directory |
| ..     | Parent directory  |



# Linux Permissions Preview

Example:

```bash
drwxr-xr-x
```

Meaning:

| Character | Meaning   |
| --------- | --------- |
| d         | Directory |
| r         | Read      |
| w         | Write     |
| x         | Execute   |

Permission groups:

1. Owner
2. Group
3. Others


# System Information Checklist

To gather system information:

### Current User

```bash
whoami
```

### OS Information

```bash
uname -a
```

### Disk Usage

```bash
df -h
```

### Linux Distribution

```bash
cat /etc/os-release
```


---
