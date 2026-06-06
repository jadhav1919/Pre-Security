# Virtualization Fundamentals

## Overview

Virtualization is a technology that allows multiple virtual computers to run on a single physical computer.

Instead of dedicating one physical server to one application, virtualization enables multiple systems and applications to share the same hardware efficiently.


# Why Virtualization Was Needed

## Traditional Approach

Previously:

```text
1 Physical Server
        ↓
1 Application
```

### Example

| Physical Server | Purpose              |
| --------------- | -------------------- |
| Server 1        | Website              |
| Server 2        | Database             |
| Server 3        | Email Service        |
| Server 4        | Internal Application |


## Problems

### High Cost

Organizations needed to purchase:

* More hardware
* More storage
* More power
* More cooling systems


### Low Hardware Utilization

Most servers used only:

```text
5% - 20%
```

of their available resources.

The remaining hardware capacity was wasted.


### Slow Deployment

Provisioning new physical servers could take:

```text
Days or Weeks
```


### Difficult Scaling

When an application required more resources:

```text
More Users
      ↓
Need New Server
      ↓
Higher Cost
```


# What is Virtualization?

Virtualization allows multiple virtual systems to run on a single physical server.

```text
Physical Server
       ↓
Hypervisor
    ↙  ↓  ↘
 VM1 VM2 VM3
```

Each VM behaves like an independent computer.


# Benefits of Virtualization

## Better Hardware Utilization

Multiple systems share the same hardware.


## Cost Reduction

Fewer physical servers are required.


## Faster Deployment

New virtual machines can be created quickly.


## Easier Scalability

Resources can be increased without purchasing additional hardware.


## Isolation

Problems in one VM usually do not affect other VMs.


# Hypervisor

## What is a Hypervisor?

A hypervisor is software responsible for creating and managing virtual machines.

### Responsibilities

* Create VMs
* Start VMs
* Stop VMs
* Clone VMs
* Delete VMs
* Allocate resources


# Hypervisor Functions

The hypervisor manages:

* CPU
* RAM
* Storage
* Networking

for each virtual machine.


# Types of Hypervisors

## Type 1 Hypervisor

Runs directly on physical hardware.

```text
Hardware
    ↓
Hypervisor
    ↓
Virtual Machines
```

### Characteristics

* High performance
* Efficient
* Used in production environments

### Common Use Cases

* Data Centers
* Production Servers
* Enterprise Infrastructure


## Type 2 Hypervisor

Runs on top of an operating system.

```text
Hardware
    ↓
Operating System
    ↓
Hypervisor
    ↓
Virtual Machines
```

### Characteristics

* Easier to install
* Suitable for personal use
* Ideal for learning and testing

### Common Use Cases

* Kali Linux Labs
* Software Testing
* Cybersecurity Practice
* Home Labs


# Virtual Machine (VM)

## What is a VM?

A Virtual Machine is a software-based computer created by a hypervisor.

It behaves like a real computer.

# VM Components

A VM has its own:

* Virtual CPU
* Virtual RAM
* Virtual Disk
* Virtual Network Adapter


# VM Characteristics

### Independent

Each VM has its own operating system.

### Isolated

One VM crashing does not affect others.

### Flexible

Different operating systems can run on the same host.


# VM Examples

### Learning Linux

```text
Windows Host
      ↓
Linux VM
```

### Cybersecurity Labs

```text
Host System
      ↓
Kali Linux VM
```

### Malware Analysis

```text
Host Computer
      ↓
Isolated Test VM
```


# Popular Hypervisors

## Type 2 Examples

### Oracle VirtualBox

Free virtualization software.

### VMware Workstation

Popular professional virtualization software.

# Containers

## What is a Container?

A container is a lightweight isolated environment used to run applications.

Unlike VMs, containers do not contain a complete operating system.


# How Containers Work

Containers share the host operating system kernel.

```text
Host Operating System
         ↓
Container 1
Container 2
Container 3
```


# Advantages of Containers

### Lightweight

Require fewer resources.

### Fast Startup

Start almost instantly.

### Efficient

Multiple containers can run on the same system.

### Portable

Run consistently across environments.


# Limitations of Containers

Containers must use the same operating system family as the host.

### Example

```text
Linux Host
      ↓
Linux Containers 

Windows Containers 
```


# VM vs Container

| Feature                   | VM       | Container |
| ------------------------- | -------- | --------- |
| Includes Operating System | Yes      | No        |
| Resource Usage            | Higher   | Lower     |
| Startup Speed             | Slower   | Faster    |
| Isolation                 | Stronger | Moderate  |
| Flexibility               | Higher   | Lower     |


# Docker

## What is Docker?

Docker is an open-source platform used to create and manage containers.

### Benefits

* Easy deployment
* Application packaging
* Scalability
* Consistent environments


# Relationship Between Components

```text
Physical Server
        ↓
Hypervisor
        ↓
Virtual Machines
        ↓
Containers
```

# Virtualization Management

Virtualization platforms allow administrators to:

### Monitor VMs

* CPU Usage
* Memory Usage
* Disk Usage

### Manage VMs

* Create
* Start
* Stop
* Restart
* Delete

### Monitor Hosts

* Resource Utilization
* Performance
* Availability
