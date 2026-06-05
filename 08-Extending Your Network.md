# Port Forwarding, Firewalls, VPNs, Routers and Switches

## Port Forwarding

Port forwarding allows a service running inside a private network to be accessed from the Internet.

### Example

Suppose a web server is running on:

```text
192.168.1.10:80
```

Normally, only devices on the same local network can access it.

By configuring port forwarding on the router, requests coming to the router's public IP on port 80 can be forwarded to:

```text
192.168.1.10:80
```

### Key Points

* Configured on a router.
* Makes internal services accessible externally.
* Commonly used for web servers, game servers, and remote access services.

## Firewall

A firewall is a security device that controls what traffic is allowed to enter or leave a network.

Think of it as a security guard for network traffic.

### Firewall Checks

A firewall can make decisions based on:

* Source IP address
* Destination IP address
* Port number
* Protocol (TCP/UDP)

### Types of Firewalls

#### Stateful Firewall

Tracks the entire connection.

Example:

* If a TCP connection is allowed, the firewall remembers it.
* Future packets are checked in the context of that connection.

**Advantages**

* More secure
* Understands connection state

**Disadvantages**

* Uses more resources

#### Stateless Firewall

Checks each packet independently.

Example:

* Every packet is compared against firewall rules.
* No memory of previous packets.

**Advantages**

* Faster
* Uses fewer resources

**Disadvantages**

* Less intelligent

### Key Points

* Firewalls commonly operate at OSI Layers 3 and 4.
* Stateful = connection aware.
* Stateless = packet aware.


## VPN (Virtual Private Network)

A VPN creates an encrypted tunnel between devices over the Internet.

This allows devices on different networks to communicate securely.

### Why Use a VPN?

#### Security

Traffic is encrypted and cannot easily be read by others.

#### Privacy

Helps protect activity from being monitored on public Wi-Fi.

#### Remote Access

Allows employees to access company resources from different locations.

### VPN Technologies

#### PPP (Point-to-Point Protocol)

Provides:

* Authentication
* Encryption

#### PPTP (Point-to-Point Tunneling Protocol)

Allows PPP traffic to travel across networks.

#### IPSec (Internet Protocol Security)

Uses the IP protocol framework to provide strong encryption and security.

### Key Points

* VPN = Secure private tunnel.
* PPP = Authentication and encryption.
* IPSec = Strong security using IP.


## Router

A router connects different networks together and forwards packets between them.

### Main Functions

* Connects networks
* Routes packets
* Performs port forwarding
* Often includes firewall functionality

### How Routing Works

The router chooses the best path based on:

* Shortest path
* Reliability
* Speed of connection

### Key Points

* Operates at OSI Layer 3.
* Uses IP addresses.
* Connects networks.


## Switch

A switch connects devices within the same network.

Examples:

* Computers
* Printers
* Servers

### Layer 2 Switch

Uses:

* MAC Addresses

Function:

* Forwards frames to the correct device.

### Layer 3 Switch

Uses:

* MAC Addresses
* IP Addresses

Function:

* Can perform routing in addition to switching.

### VLAN (Virtual LAN)

A VLAN logically separates devices on the same physical switch into different networks.

Example:

```text
Switch
├── Sales VLAN
└── Accounting VLAN
```

Even though both departments use the same switch, they can be isolated from each other.

### Key Points

* Layer 2 Switch → Uses MAC addresses.
* Layer 3 Switch → Uses MAC and IP addresses.
* VLANs improve security and organization.
