# Windows CLI Basics (Command Prompt)

## What is Windows CLI?

Windows CLI (Command Line Interface) is a text-based interface used to interact with the Windows operating system.

Instead of clicking through folders and menus, users type commands to perform tasks.

The most common Windows CLI is:

```text
Command Prompt (CMD)
```

# Why Use Windows CLI?

Advantages:

* Faster than GUI for many tasks
* Better system control
* Useful for troubleshooting
* Commonly used in IT support
* Important in cybersecurity investigations
* Useful for system administration


# Opening Command Prompt

Methods:

### Method 1

```text
Windows Key + R
```

Type:

```text
cmd
```

### Method 2

Search:

```text
Command Prompt
```

from Start Menu.


# Windows File System Basics

Windows stores files using drives.

Example:

```text
C:\
```

Typical structure:

```text
C:\
├── Users
├── Program Files
├── Windows
├── ProgramData
```


# Important Windows Directories

| Directory        | Purpose                |
| ---------------- | ---------------------- |
| C:\              | Root of drive          |
| C:\Users         | User profiles          |
| C:\Windows       | Operating system files |
| C:\Program Files | Installed applications |
| C:\ProgramData   | Application data       |
| Desktop          | User desktop files     |
| Documents        | User documents         |


# cd Command

## Purpose

Display current directory or change directory.

### Show Current Directory

```cmd
cd
```

Example:

```cmd
C:\Users\Administrator
```


## Change Directory

Syntax:

```cmd
cd folder_name
```

Example:

```cmd
cd Documents
```


## Move Back One Directory

Syntax:

```cmd
cd ..
```

Example:

```text
C:\Users\Administrator\Documents
```

↓

```cmd
cd ..
```

↓

```text
C:\Users\Administrator
```


# dir Command

## Purpose

List files and folders.

### Syntax

```cmd
dir
```

Example:

```cmd
Volume in drive C
Directory of C:\Users\Administrator

Documents
Downloads
Desktop
```


# dir /a Command

## Purpose

Show all files including hidden files.

### Syntax

```cmd
dir /a
```


# Hidden Files

Hidden files do not appear in a normal directory listing.

Use:

```cmd
dir /a
```

to display them.

Examples:

```text
AppData
NTUSER.DAT
```


# Searching for Files

Windows allows searching using dir.

### Syntax

```cmd
dir /s filename
```

## Example

```cmd
dir /s task_brief.txt
```

Output:

```text
C:\Users\Administrator\Documents\Notes\task_brief.txt
```

The /s option searches all subfolders.


# type Command

## Purpose

Display file contents.

### Syntax

```cmd
type filename
```


## Example

```cmd
type task_brief.txt
```

Output:

```text
TASK-BRIEF-FOUND
```

# whoami Command

## Purpose

Display current logged-in user.

### Syntax

```cmd
whoami
```

### Example

```cmd
administrator
```


# hostname Command

## Purpose

Display computer name.

### Syntax

```cmd
hostname
```

### Example

```cmd
THMLAB
```


# systeminfo Command

## Purpose

Display detailed system information.

### Syntax

```cmd
systeminfo
```


# Important Information From systeminfo

### OS Name

Example:

```text
Microsoft Windows Server 2019 Datacenter
```


### OS Version

Example:

```text
10.0.17763 Build 17763
```


### System Type

Example:

```text
x64-based PC
```

Meaning:

64-bit operating system.


### Host Name

Example:

```text
THMLAB
```


### Total Physical Memory

Displays installed RAM.


# ipconfig Command

## Purpose

Display network configuration.

### Syntax

```cmd
ipconfig
```



# Important Network Information

### IPv4 Address

Example:

```text
192.168.1.10
```

Unique address of the computer.



### Default Gateway

Example:

```text
192.168.1.1
```

Usually the router address.

Used to access external networks.


# Common Windows CLI Commands

| Command    | Purpose                     |
| ---------- | --------------------------- |
| cd         | Show/change directory       |
| cd ..      | Move back one directory     |
| dir        | List files and folders      |
| dir /a     | Show hidden files           |
| dir /s     | Search files recursively    |
| type       | Read file contents          |
| whoami     | Current user                |
| hostname   | Computer name               |
| systeminfo | Detailed system information |
| ipconfig   | Network information         |


# Common Cybersecurity Uses

## User Enumeration

Identify current user:

```cmd
whoami
```


## System Enumeration

Gather OS information:

```cmd
systeminfo
```


## Network Enumeration

Gather network details:

```cmd
ipconfig
```


## File Discovery

Search files:

```cmd
dir /s filename
```


## File Analysis

Read text files:

```cmd
type filename
```


# Windows vs Linux Command Comparison

| Task              | Linux         | Windows    |
| ----------------- | ------------- | ---------- |
| Current User      | whoami        | whoami     |
| Current Directory | pwd           | cd         |
| List Files        | ls            | dir        |
| Change Directory  | cd            | cd         |
| Read File         | cat           | type       |
| Hostname          | hostname      | hostname   |
| System Info       | uname -a      | systeminfo |
| Network Info      | ifconfig/ip a | ipconfig   |


# Common Paths

### User Profile

```text
C:\Users\Administrator
```


### Desktop

```text
C:\Users\Administrator\Desktop
```


### Documents

```text
C:\Users\Administrator\Documents
```


### Windows Folder

```text
C:\Windows
```


# Cybersecurity Workflow

When accessing a Windows machine:

### Step 1: Identify User

```cmd
whoami
```

### Step 2: Identify Machine

```cmd
hostname
```

### Step 3: Gather OS Details

```cmd
systeminfo
```

### Step 4: Check Network

```cmd
ipconfig
```

### Step 5: Search Files

```cmd
dir /s filename
```

### Step 6: Read Files

```cmd
type filename
```

---


