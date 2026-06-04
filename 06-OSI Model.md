# OSI Model (Open Systems Interconnection)

## Overview

The **OSI Model (Open Systems Interconnection Model)** is a framework that explains how devices communicate over a network.

### Key Benefits

* Standardizes network communication.
* Allows different devices and software to communicate.
* Helps troubleshoot network issues.
* Divides networking into 7 layers.

### Encapsulation

As data moves through the OSI layers, information is added at each layer.

**This process is called: Encapsulation**

# OSI Layers

```text
7. Application
6. Presentation
5. Session
4. Transport
3. Network
2. Data Link
1. Physical
```

# Layer 1 - Physical Layer

## Purpose

Responsible for the physical transmission of data using electrical signals.

### Examples

* Ethernet Cables
* Fiber Optic Cables
* Network Connectors

### Key Facts

* Transfers data as 1s and 0s.
* Lowest layer of the OSI Model.

### Exam Answers

| Question         | Answer          |
| ---------------- | --------------- |
| Layer Name       | Physical        |
| Numbering System | Binary          |
| Cables Used      | Ethernet Cables |


# Layer 2 - Data Link Layer

## Purpose

Responsible for physical addressing using MAC addresses.

### Functions

* Adds MAC addresses.
* Controls access to the physical medium.
* Formats data for transmission.

### Important Term

**NIC (Network Interface Card)**

Every networked device contains a NIC with a unique MAC address.

### Exam Answers

| Question                          | Answer                       |
| --------------------------------- | ---------------------------- |
| Layer Name                        | Data Link                    |
| Hardware Found in Network Devices | Network Interface Card (NIC) |


# Layer 3 - Network Layer

## Purpose

Responsible for:

* Routing
* Path Selection
* Packet Delivery

### Uses

* IP Addresses
* Routers

### Routing Factors

1. Shortest path
2. Most reliable path
3. Fastest connection

### Important Protocols

| Protocol | Full Form                    |
| -------- | ---------------------------- |
| OSPF     | Open Shortest Path First     |
| RIP      | Routing Information Protocol |

### Key Facts

* Routers operate at Layer 3.
* Uses IP addresses.

### Exam Answers

| Question            | Answer                       |
| ------------------- | ---------------------------- |
| Layer Name          | Network                      |
| Optimal Route Used? | Y                            |
| OSPF                | Open Shortest Path First     |
| RIP                 | Routing Information Protocol |
| Address Type        | IP Addresses                 |


# Layer 4 - Transport Layer

## Purpose

Responsible for transporting data between devices.

### Protocols

#### TCP (Transmission Control Protocol)

Reliable protocol.

##### Advantages

* Guarantees delivery.
* Error checking.
* Maintains connection.

##### Disadvantages

* Slower.
* Requires more resources.

##### Used For

* Email
* File Downloads
* Web Browsing

#### UDP (User Datagram Protocol)

Fast but unreliable protocol.

##### Advantages

* Faster than TCP.
* Low overhead.

##### Disadvantages

* No delivery guarantee.
* No error checking.

##### Used For

* Video Streaming
* Online Gaming
* VoIP
* DHCP
* ARP


## TCP vs UDP

| TCP                 | UDP               |
| ------------------- | ----------------- |
| Reliable            | Unreliable        |
| Slower              | Faster            |
| Connection-Oriented | Connectionless    |
| Error Checking      | No Error Checking |
| Email               | Video Streaming   |
| File Downloads      | Gaming            |

### Exam Answers

| Question                    | Answer                        |
| --------------------------- | ----------------------------- |
| Layer Name                  | Transport                     |
| TCP Full Form               | Transmission Control Protocol |
| UDP Full Form               | User Datagram Protocol        |
| Accurate Data Protocol      | TCP                           |
| Doesn't Care About Delivery | UDP                           |
| Email Client Uses           | TCP                           |
| File Download Uses          | TCP                           |
| Video Streaming Uses        | UDP                           |


# Layer 5 - Session Layer

## Purpose

Responsible for creating, maintaining, and terminating sessions between devices.

### Functions

* Establishes connections.
* Maintains active sessions.
* Closes inactive sessions.
* Uses checkpoints for recovery.

### Important Term

When a connection is successfully established:

**Session Established**

### Exam Answers

| Question                   | Answer  |
| -------------------------- | ------- |
| Layer Name                 | Session |
| Successful Connection Term | Session |


# Layer 6 - Presentation Layer

## Purpose

Acts as a translator between applications.

### Functions

* Data Translation
* Data Formatting
* Data Encryption
* Data Decryption

### Example

Two users can use different email software, but both can still read the same email.

### Security

Encryption such as HTTPS occurs here.

### Exam Answers

| Question     | Answer       |
| ------------ | ------------ |
| Layer Name   | Presentation |
| Main Purpose | Translator   |


# Layer 7 - Application Layer

## Purpose

Provides services directly to the user.

### Examples

* Web Browsers
* Email Clients
* FileZilla
* DNS

### Common Protocols

| Protocol | Purpose                |
| -------- | ---------------------- |
| HTTP     | Web Browsing           |
| HTTPS    | Secure Browsing        |
| DNS      | Domain Name Resolution |
| FTP      | File Transfer          |

### GUI

Users interact with software through a:

**Graphical User Interface (GUI)**

### Exam Answers

| Question                     | Answer                         |
| ---------------------------- | ------------------------------ |
| Layer Name                   | Application                    |
| Software User Interface Term | Graphical User Interface (GUI) |

# OSI Layer Summary

| Layer | Name         | Main Function                 |
| ----- | ------------ | ----------------------------- |
| 7     | Application  | User Interaction              |
| 6     | Presentation | Translation & Encryption      |
| 5     | Session      | Establish & Maintain Sessions |
| 4     | Transport    | TCP / UDP Data Transfer       |
| 3     | Network      | Routing & IP Addresses        |
| 2     | Data Link    | MAC Addresses                 |
| 1     | Physical     | Cables & Signals              |


