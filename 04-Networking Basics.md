# Networking Basics

## What is a Network?

A network is a group of connected devices that can communicate with each other.

### Real-Life Examples

* Public transportation systems
* Power grids
* Postal services
* Social circles (friends connected together)

### Computing Examples

* Computers
* Laptops
* Smartphones
* Security Cameras
* Traffic Lights
* Smart Devices (IoT)

# Why is Networking Important in Cyber Security?

Modern systems depend on networks to:

* Share information
* Access websites
* Transfer files
* Communicate between devices

Understanding networks is essential for identifying and defending against cyber attacks.

# The Internet

The Internet is a massive network made up of many smaller networks connected together.

## History of the Internet

| Year  | Event                                             |
| ----- | ------------------------------------------------- |
| 1960s | ARPANET created by the US Department of Defense   |
| 1989  | Tim Berners-Lee invented the World Wide Web (WWW) |

### Key Fact

**Tim Berners-Lee** invented the **World Wide Web (WWW)**.

# Types of Networks

## Private Network

A network used internally between devices.

### Examples

* Home Wi-Fi
* Office Network
* School Network

## Public Network

Networks that connect private networks together.

### Example

* The Internet

# Device Identification

Devices need unique identifiers to communicate on a network.

Humans use:

* Names
* Fingerprints

Devices use:

* IP Address
* MAC Address

# IP Address (Internet Protocol Address)

An IP address identifies a device on a network.

## Example IPv4 Address

```text
192.168.1.10
```

### Structure

An IPv4 address consists of:

```text
192 . 168 . 1 . 10
 ↑     ↑    ↑    ↑
Octet Octet Octet Octet
```

Each section is called an **Octet**.

### Important Facts

* IPv4 contains **4 octets**
* IP addresses can change
* No two devices can use the same IP address on the same network at the same time

# Public vs Private IP Addresses

| Type       | Purpose                                   |
| ---------- | ----------------------------------------- |
| Private IP | Identifies devices inside a local network |
| Public IP  | Identifies devices on the Internet        |

### Example

| Device | Private IP   | Public IP    |
| ------ | ------------ | ------------ |
| PC 1   | 192.168.1.77 | 86.157.52.21 |
| PC 2   | 192.168.1.74 | 86.157.52.21 |

Notice both devices share the same public IP when accessing the Internet.

# IPv4 vs IPv6

## IPv4

Example:

```text
192.168.1.1
```

### Features

* Uses 32 bits
* Supports approximately 4.29 billion addresses

## IPv6

Example:

```text
2001:0db8:85a3:0000:0000:8a2e:0370:7334
```

### Features

* Uses 128 bits
* Supports approximately 340 undecillion addresses
* More efficient than IPv4

# MAC Address (Media Access Control Address)

A MAC address is a unique hardware identifier assigned to a network interface card (NIC).

## Example

```text
a4:c3:f0:85:ac:2d
```

### Structure

```text
a4:c3:f0 : 85:ac:2d
└──────┘   └──────┘
Company      Unique Device ID
```

### Important Facts

* Assigned by manufacturer
* Usually unique worldwide
* Stored in hardware
* Used within local networks

# MAC Spoofing

MAC Spoofing is the process of changing or faking a MAC address.

## Why Attackers Use It

* Bypass MAC-based restrictions
* Impersonate trusted devices
* Gain unauthorized network access

### Example

A hotel Wi-Fi allows only paid devices.

An attacker changes their MAC address to match an authorized device and gains access.

# Ping

Ping is a basic network troubleshooting tool.

It uses the **Internet Control Message Protocol (ICMP)** to test connectivity between devices.

## How Ping Works

```text
Your Device
      │
      │ ICMP Echo Request
      ▼
Target Device
      │
      │ ICMP Echo Reply
      ▼
Your Device
```

## Ping Command Syntax

```bash
ping <IP_Address>
```

### Example

```bash
ping 10.10.10.10
```

### Example

```bash
ping 8.8.8.8
```

# ICMP (Internet Control Message Protocol)

ICMP is used to:

* Check connectivity
* Measure response times
* Diagnose network problems

Ping uses ICMP Echo Request and Echo Reply packets.

---
