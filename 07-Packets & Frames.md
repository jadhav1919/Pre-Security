## Packets and Frames

### What is a Packet?

A **Packet** is a piece of data at **Layer 3 (Network Layer)** of the OSI Model.

A packet contains:

* IP Address Information
* Header Information
* Payload (Actual Data)

### What is a Frame?

A **Frame** is a piece of data at **Layer 2 (Data Link Layer)** of the OSI Model.

A frame contains:

* MAC Addresses
* Packet Information
* Error Checking Information

---

## Packet vs Frame

| Packet                 | Frame                     |
| ---------------------- | ------------------------- |
| Layer 3 (Network)      | Layer 2 (Data Link)       |
| Uses IP Addresses      | Uses MAC Addresses        |
| Routed across networks | Delivered within networks |
| Contains IP Header     | Encapsulates Packet       |

---

## Encapsulation

Encapsulation is the process of adding information to data as it moves through OSI layers.

### Example

```text id="eg7u2a"
Data
 ↓
Packet (IP Address Added)
 ↓
Frame (MAC Address Added)
 ↓
Transmission
```

## Important Packet Headers

| Header              | Purpose                                |
| ------------------- | -------------------------------------- |
| Time To Live (TTL)  | Prevents packets from existing forever |
| Checksum            | Verifies data integrity                |
| Source Address      | Sender's IP Address                    |
| Destination Address | Receiver's IP Address                  |


## Exam Answers

| Question                               | Answer |
| -------------------------------------- | ------ |
| Data with IP addressing information    | Packet |
| Data without IP addressing information | Frame  |

# TCP (Transmission Control Protocol)

## What is TCP?

TCP is a reliable, connection-oriented protocol used for accurate data transmission.

Before data is sent, TCP establishes a connection between devices.

## Advantages of TCP

* Reliable
* Error Checking
* Guarantees Delivery
* Correct Packet Ordering
* Prevents Data Loss

## Disadvantages of TCP

* Slower than UDP
* Requires more resources
* Needs an active connection


## Common TCP Uses

| Service       | Uses TCP? |
| ------------- | --------- |
| Email         | Yes       |
| File Download | Yes       |
| Web Browsing  | Yes       |
| File Transfer | Yes       |


# TCP Headers

| Header                 | Description            |
| ---------------------- | ---------------------- |
| Source Port            | Sender's Port          |
| Destination Port       | Receiver's Port        |
| Source IP              | Sender's Address       |
| Destination IP         | Receiver's Address     |
| Sequence Number        | Packet Order Tracking  |
| Acknowledgement Number | Confirms Received Data |
| Checksum               | Data Integrity         |
| Data                   | Actual Content         |
| Flag                   | Packet Purpose         |

---

# TCP Three-Way Handshake

TCP establishes connections using the Three-Way Handshake.

## Step 1 - SYN

Client requests a connection.

```text id="4g3lmx"
Client → Server : SYN
```

---

## Step 2 - SYN/ACK

Server acknowledges the request.

```text id="iqij1l"
Server → Client : SYN/ACK
```

---

## Step 3 - ACK

Client confirms the connection.

```text id="s61kaf"
Client → Server : ACK
```

---

## Handshake Flow

```text id="fq5m4j"
Client                    Server

SYN      ------------>

          <------------ SYN/ACK

ACK      ------------>

Connection Established
```

## TCP Closing Connection

TCP uses the **FIN** flag to close a connection properly.

### Closing Process

```text id="5x3g06"
Client → FIN
Server → ACK
Server → FIN
Client → ACK
```

Connection Closed.


## TCP Flags

| Flag    | Meaning                     |
| ------- | --------------------------- |
| SYN     | Start Connection            |
| SYN/ACK | Synchronize and Acknowledge |
| ACK     | Acknowledge                 |
| DATA    | Transfer Data               |
| FIN     | Close Connection            |
| RST     | Forcefully Reset Connection |


## Sequence Numbers

Used to ensure packets arrive in the correct order.

Example:

```text id="p2nlhf"
Packet 1 → Sequence 0
Packet 2 → Sequence 1
Packet 3 → Sequence 2
```

## Exam Answers

| Question                  | Answer          |
| ------------------------- | --------------- |
| Header ensuring integrity | Checksum        |
| Three-Way Handshake Order | SYN,SYN/ACK,ACK |


# UDP (User Datagram Protocol)

## What is UDP?

UDP is a fast, connectionless (stateless) protocol.

It does not:

* Create a connection
* Verify delivery
* Perform error checking


## Advantages of UDP

* Very Fast
* Low Resource Usage
* Suitable for Real-Time Applications


## Disadvantages of UDP

* No Delivery Guarantee
* No Error Recovery
* Packets May Be Lost


## Common UDP Uses

| Service         | Uses UDP? |
| --------------- | --------- |
| Video Streaming | Yes       |
| Voice Calls     | Yes       |
| Online Gaming   | Yes       |
| DHCP            | Yes       |
| ARP             | Yes       |


# UDP Headers

| Header              | Purpose            |
| ------------------- | ------------------ |
| TTL                 | Packet Lifetime    |
| Source Address      | Sender IP          |
| Destination Address | Receiver IP        |
| Source Port         | Sender Port        |
| Destination Port    | Receiver Port      |
| Data                | Actual Information |


## TCP vs UDP

| TCP                 | UDP               |
| ------------------- | ----------------- |
| Reliable            | Unreliable        |
| Connection-Oriented | Connectionless    |
| Slower              | Faster            |
| Error Checking      | No Error Checking |
| File Downloads      | Streaming         |
| Email               | Video Calls       |


## Exam Answers

| Question                      | Answer                 |
| ----------------------------- | ---------------------- |
| UDP Full Form                 | User Datagram Protocol |
| Connection Type               | Stateless              |
| File Transfer Protocol Choice | TCP                    |
| Video Call Protocol Choice    | UDP                    |


# Ports

## What is a Port?

A port is a communication endpoint used by applications and services.

### Port Range

```text id="fxt4eh"
0 - 65535
```

# Common Ports

| Protocol | Port | Description            |
| -------- | ---- | ---------------------- |
| FTP      | 21   | File Transfer          |
| SSH      | 22   | Secure Remote Login    |
| HTTP     | 80   | Web Browsing           |
| HTTPS    | 443  | Secure Web Browsing    |
| SMB      | 445  | File & Printer Sharing |
| RDP      | 3389 | Remote Desktop         |


## Common Ports Range

```text id="ndydz0"
0 - 1024
```

Known as **Well-Known Ports**.


# Port Example

### HTTP

```text id="i5i7kj"
http://example.com
```

Uses:

```text id="m4d56x"
Port 80
```


### HTTPS

```text id="e7gh6q"
https://example.com
```

Uses:

```text id="gcnw4f"
Port 443
```

### Custom Port

If a service uses a non-standard port:

```text id="2r0pdx"
http://example.com:8080
```
