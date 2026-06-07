# Operating Systems (OS) Fundamentals

## What is an Operating System?

An Operating System (OS) is the core software that manages computer hardware, software applications, and system resources.

It acts as an intermediary between:

```text
User
  ↓
Applications
  ↓
Operating System
  ↓
Hardware
```

Without an OS, applications would need to directly control hardware, causing conflicts and instability.


# Why Do We Need an Operating System?

The OS provides:

* Resource management
* Hardware control
* Application execution
* Security
* User interaction

It ensures all components work together efficiently.

# System Privilege Layers

Modern operating systems separate responsibilities into different privilege levels.

## Kernel Space

Kernel Space is the most privileged part of the operating system.

### Characteristics

* Direct access to hardware
* Controls CPU, RAM, storage, and devices
* Executes critical system functions

### Examples

* Memory allocation
* Device communication
* Process scheduling

### Key Point

```text
Kernel Space = Full Hardware Access
```


## User Space

User Space is where normal applications execute.

### Characteristics

* Limited permissions
* Cannot directly access hardware
* Must request services from the kernel

### Examples

* Web Browsers
* Music Players
* Text Editors
* Games

### Key Point

```text
User Space = Restricted Access
```


# System Calls

Applications communicate with the kernel through system calls.

### Examples

* Open File
* Save File
* Print Document
* Connect to Network

```text
Application
     ↓
System Call
     ↓
Kernel
     ↓
Hardware
```

# Core Responsibilities of an Operating System


# 1. Process Management

Process Management controls running programs.

### Responsibilities

* Create processes
* Schedule processes
* Prioritize processes
* Terminate processes

### Example

Running:

* Browser
* Music Player
* Chat Application

at the same time.


# 2. Memory Management

Memory Management controls RAM allocation.

### Responsibilities

* Allocate memory
* Protect memory
* Reclaim unused memory
* Manage virtual memory

### Example

Multiple applications can run without interfering with each other.


# 3. File System Management

Organizes and manages files and folders.

### Responsibilities

* File storage
* Folder organization
* Permissions
* Metadata management

### Metadata Examples

* File Name
* File Size
* File Type
* Creation Date

### Example

```text
Documents/
   ├── notes.txt
   ├── report.pdf
```


# 4. User Management

Controls user accounts and permissions.

### Responsibilities

* Authentication
* Authorization
* Account Management

### Example

```text
User A → Own Files
User B → Cannot Access User A Files
```


# 5. Device Management

Manages communication with hardware devices.

### Responsibilities

* Load drivers
* Detect devices
* Provide hardware abstraction

### Examples

* Mouse
* Keyboard
* Printer
* USB Drive


# Operating System Security

The OS provides the first layer of security.


## Authentication

Verifies user identity.

### Methods

* Passwords
* PINs
* Biometrics


## Permissions

Defines what users and applications can access.

### Examples

* Read
* Write
* Execute

## Isolation

Keeps applications separated.

### Benefits

* Prevents interference
* Improves stability
* Increases security



## System Protection

Protects critical system files and settings.


# Operating System Interfaces

Users interact with operating systems through interfaces.


# Graphical User Interface (GUI)

A visual interface using:

* Windows
* Icons
* Menus
* Buttons

### Examples

* Windows Desktop
* Ubuntu Desktop
* macOS Desktop

### Advantages

* Easy to learn
* User friendly


# Command-Line Interface (CLI)

A text-based interface.

### Examples

```bash
ls
pwd
cd
```

### Advantages

* Faster for advanced users
* Greater control
* Automation support

### Disadvantages

* Requires command knowledge


# GUI vs CLI

| Feature        | GUI      | CLI       |
| -------------- | -------- | --------- |
| Interaction    | Visual   | Text      |
| Learning Curve | Easy     | Moderate  |
| Speed          | Slower   | Faster    |
| Automation     | Limited  | Excellent |
| Precision      | Moderate | High      |



# Types of Operating Systems


## Desktop Operating Systems

Designed for personal computers.

### Characteristics

* Rich graphical interface
* Multitasking
* User-focused

### Examples

* Windows 11
* macOS
* Ubuntu Desktop

## Server Operating Systems

Designed for hosting services.

### Characteristics

* High uptime
* Stability
* Multi-user support

### Examples

* Windows Server
* Ubuntu Server
* Red Hat Linux


## Mobile Operating Systems

Designed for smartphones and tablets.

### Characteristics

* Touchscreen support
* Battery optimization
* Mobile applications

### Examples

* Android
* iOS


## Embedded Operating Systems

Designed for dedicated devices.

### Characteristics

* Lightweight
* Specialized functions
* Limited hardware resources

### Examples

* Smart TVs
* Routers
* IoT Devices


## Virtual / Cloud Operating Systems

Used in virtual machines and cloud environments.

### Characteristics

* Lightweight
* Scalable
* Optimized for virtualization

### Examples

* Ubuntu Server
* Amazon Linux
* Rocky Linux


# Major Operating System Families


# Microsoft Windows

Most widely used desktop operating system.

### Examples

* Windows 10
* Windows 11

### Strengths

* Ease of use
* Software compatibility


# Linux

Open-source operating system family.

### Examples

* Ubuntu
* Debian
* Fedora
* Red Hat

### Strengths

* Stability
* Security
* Flexibility


# macOS

Apple's operating system.

### Strengths

* User experience
* Apple ecosystem integration

### Examples

* Sonoma
* Sequoia


# Android

Most widely used mobile operating system.

### Characteristics

* Open-source foundation
* Large application ecosystem


# iOS

Apple's mobile operating system.

### Characteristics

* Security
* Performance
* Apple ecosystem integration


# File Systems

A file system determines how data is stored and organized.

### Examples

| File System | Operating System |
| ----------- | ---------------- |
| NTFS        | Windows          |
| ext4        | Linux            |
| APFS        | macOS            |


# Why Different Operating Systems Exist

Different environments require different capabilities.

| Environment | Requirement          |
| ----------- | -------------------- |
| Desktop     | User Friendliness    |
| Server      | Stability & Security |
| Mobile      | Battery Efficiency   |
| Embedded    | Small Size           |
| Cloud       | Scalability          |

No single OS is ideal for every situation.

