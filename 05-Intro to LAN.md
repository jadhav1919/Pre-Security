# Networking Fundamentals

## 1. LAN (Local Area Network)

A **LAN (Local Area Network)** is a network that connects devices within a limited area such as:

* Home
* School
* Office
* Building

# LAN Topologies

A **topology** is the physical or logical design of a network.

## 1. Star Topology

### Diagram

```text
       PC1
        |
PC2 -- Switch -- PC3
        |
       PC4
```

### How It Works

* All devices connect to a central device (Switch/Hub).
* Data passes through the central device.

### Advantages

* Easy to add new devices.
* Reliable.
* Easy to manage.
* Scalable.

### Disadvantages

* Expensive due to more cables and hardware.
* If the switch fails, the entire network fails.
* More maintenance required.

### Key Point

**Most commonly used topology today.**


## 2. Bus Topology

### Diagram

```text
PC1 ---- PC2 ---- PC3 ---- PC4
        (Backbone Cable)
```

### How It Works

* All devices share one main cable called the backbone cable.

### Advantages

* Cheap to implement.
* Less cabling required.
* Easy setup.

### Disadvantages

* Slow when many devices communicate.
* Difficult troubleshooting.
* Single point of failure.

### Key Point

**Most cost-efficient topology.**


## 3. Ring Topology

### Diagram

```text
PC1 ---- PC2
 |         |
PC4 ---- PC3
```

### How It Works

* Devices form a circular loop.
* Data travels around the ring until it reaches the destination.

### Advantages

* Easy fault identification.
* Less network congestion.

### Disadvantages

* Data may travel through many devices.
* A single cable break can stop the entire network.

### Key Point

**Data travels in one direction around the ring.**

# Switch

## What is a Switch?

A switch is a networking device that connects multiple devices within a LAN.

### Functions

* Connects computers, printers, servers, etc.
* Sends data only to the intended device.
* Reduces unnecessary network traffic.

### Common Port Sizes

* 4 Ports
* 8 Ports
* 16 Ports
* 24 Ports
* 32 Ports
* 64 Ports

### Advantages

* Faster than hubs
* Intelligent packet forwarding
* Efficient communication

### Exam Point

**Switch = Connects devices inside a network.**

# Router

## What is a Router?

A router connects different networks together and transfers data between them.

### Functions

* Connects LAN to the Internet.
* Finds the best path for data.
* Performs routing.

### Routing

Routing is the process of moving data between networks.

### Exam Point

**Router = Connects networks.**


# Subnetting

## Definition

Subnetting is the process of dividing a network into smaller networks.

### Example

A company may create separate networks for:

* Accounting Department
* Finance Department
* Human Resources Department

## Benefits of Subnetting

### 1. Efficiency

Reduces unnecessary traffic.

### 2. Security

Departments can be isolated.

### 3. Control

Better network management.

# Subnet Mask

A subnet mask determines how many devices can exist within a network.

### Characteristics

* Consists of 32 bits.
* Made of 4 octets.
* Each octet ranges from 0–255.

### Example

```text
255.255.255.0
```

# Important Network Addresses

## 1. Network Address

Identifies the network itself.

### Example

```text
192.168.1.0
```


## 2. Host Address

Identifies a specific device on the network.

### Example

```text
192.168.1.100
```


## 3. Default Gateway

Device responsible for sending traffic to other networks.

### Example

```text
192.168.1.254
```

### Key Point

Usually the first or last usable address:

```text
192.168.1.1
or
192.168.1.254
```


# ARP (Address Resolution Protocol)

## What is ARP?

ARP maps an IP address to a MAC address.

### Purpose

Allows devices to find the physical address of another device.


## ARP Cache

Each device stores mappings of:

```text
IP Address ↔ MAC Address
```

in an ARP Cache.


## ARP Process

### Step 1: ARP Request

Device asks:

```text
Who has IP 192.168.1.10?
```

Broadcasted to all devices.


### Step 2: ARP Reply

The owner replies:

```text
I have 192.168.1.10
My MAC is AA:BB:CC:DD:EE:FF
```

## Key Terms

| Address Type | Purpose             |
| ------------ | ------------------- |
| MAC Address  | Physical Identifier |
| IP Address   | Logical Identifier  |

# DHCP (Dynamic Host Configuration Protocol)

## What is DHCP?

DHCP automatically assigns IP addresses to devices.

Without DHCP, IP addresses must be configured manually.


# DHCP Process (DORA)

Remember:

```text
DORA
```

## 1. DHCP Discover

Device searches for a DHCP server.

```text
"Is there a DHCP server?"
```

## 2. DHCP Offer

Server offers an available IP address.

```text
"You can use 192.168.1.100"
```

## 3. DHCP Request

Device accepts the offered address.

```text
"I want 192.168.1.100"
```

## 4. DHCP ACK

Server confirms the assignment.

```text
"Approved. Start using it."
```

# DHCP Flow

```text
Client
   |
   | DHCP Discover
   v
Server
   |
   | DHCP Offer
   v
Client
   |
   | DHCP Request
   v
Server
   |
   | DHCP ACK
   v
Client receives IP Address
```

---

