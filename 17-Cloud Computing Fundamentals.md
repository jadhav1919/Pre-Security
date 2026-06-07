# Cloud Computing Fundamentals

## What is Cloud Computing?

Cloud computing is the delivery of computing resources over the internet.

Instead of buying and managing physical hardware, users can access servers, storage, databases, networking, and applications whenever needed.

```text
User
  ↓
Internet
  ↓
Cloud Provider
  ↓
Servers, Storage, Applications
```

# Why Cloud Computing?

Traditional systems relied on physical servers.

## Problems with Physical Servers

### High Cost

Organizations must purchase:

* Hardware
* Storage
* Power
* Cooling systems
* Maintenance services


### Limited Capacity

Resources are restricted by available hardware.


### Difficult Scaling

When demand increases:

```text
More Users
     ↓
Need More Hardware
     ↓
Higher Cost
```

### Downtime Risk

If the server fails, services may become unavailable.


# Evolution of Computing

```text
Physical Servers
        ↓
Virtualization
        ↓
Containers
        ↓
Cloud Computing
```

Cloud computing builds on virtualization and container technology.


# Key Characteristics of Cloud Computing

## 1. Scalability

The ability to increase or decrease resources based on demand.

### Example

```text
100 Users
    ↓
1000 Users
    ↓
Cloud Automatically Adds Resources
```

### Benefit

Applications can handle unexpected traffic increases.


## 2. On-Demand Self-Service

Resources can be created or removed whenever needed.

### Examples

* Virtual Machines
* Storage
* Databases

No need to purchase physical hardware.


## 3. Pay-As-You-Go

Users pay only for resources they consume.

### Benefit

Reduces upfront investment costs.


## 4. Security

Cloud providers secure infrastructure through:

* Physical security
* Network security
* Encryption
* Monitoring


## 5. High Availability

Services remain accessible even when part of the infrastructure fails.

### Benefit

Reduced downtime.


## 6. Global Access

Applications can be accessed worldwide.

### Benefit

Improved user experience regardless of location.


# Cloud Deployment Models

Cloud environments can be deployed in different ways.


## Public Cloud

Infrastructure is owned and managed by a cloud provider.

### Characteristics

* Most common model
* Cost-effective
* Easy to scale
* No infrastructure management required

### Examples

* AWS
* Microsoft Azure
* Google Cloud

### Best For

* Startups
* Websites
* Mobile Applications


## Private Cloud

Infrastructure is dedicated to a single organization.

### Characteristics

* Greater control
* Higher security
* Customizable

### Best For

* Banks
* Healthcare Organizations
* Government Agencies


## Hybrid Cloud

Combination of Public Cloud and Private Cloud.

### Characteristics

* Sensitive data remains private
* Public cloud used for scaling

### Best For

* Large Enterprises
* E-commerce Platforms


# Cloud Service Models

Cloud services are divided into three major models.


# IaaS (Infrastructure as a Service)

## Definition

Provides virtualized computing resources.

### User Manages

* Operating System
* Applications
* Configurations

### Provider Manages

* Physical Hardware
* Networking
* Storage Infrastructure

### Examples

* AWS EC2
* Azure Virtual Machines

### Use Cases

* Cybersecurity Labs
* Custom Servers
* Testing Environments


# PaaS (Platform as a Service)

## Definition

Provides a platform for developing and deploying applications.

### User Manages

* Application Code
* Application Data

### Provider Manages

* Infrastructure
* Operating System
* Runtime Environment

### Benefits

* Faster Development
* No Server Management

### Examples

* Heroku
* Google App Engine


# SaaS (Software as a Service)

## Definition

Complete software delivered through the internet.

### User Responsibility

Simply use the application.

### Provider Responsibility

Manages everything.

### Examples

* Gmail
* Zoom
* Microsoft 365

### Benefits

* No installation
* Easy access
* Automatic updates

# Major Cloud Providers

## Amazon Web Services (AWS)

* Market leader
* Largest cloud platform


## Microsoft Azure

* Popular in enterprise environments
* Strong hybrid cloud support


## Google Cloud Platform (GCP)

* Strong in AI and Data Analytics


## Alibaba Cloud

* Major cloud provider in Asia


## IBM Cloud

* Focus on hybrid cloud and AI


## Oracle Cloud

* Strong database and enterprise solutions


# AWS Concepts

## Region

A geographical area where cloud resources are deployed.

### Examples

* North America
* Europe
* Asia

### Purpose

Deploy applications closer to users.


## EC2 (Elastic Compute Cloud)

A virtual server in AWS.

### Characteristics

* CPU
* RAM
* Storage
* Networking

### Purpose

Run applications in the cloud.


# Instance Types

Instance types define how powerful an EC2 server is.

### Larger Instance

```text
More CPU
More RAM
Higher Cost
```


### Smaller Instance

```text
Less CPU
Less RAM
Lower Cost
```


# Benefits of Cloud Computing

## Cost Savings

Pay only for resources used.


## Flexibility

Resources can be added or removed instantly.


## Scalability

Applications grow without purchasing hardware.


## Reliability

Cloud providers maintain highly available infrastructure.


## Global Reach

Users can access applications worldwide.


# Real-World Uses of Cloud Computing

## Netflix

Uses cloud infrastructure to stream content globally.


## Spotify

Uses cloud services to manage music streaming.


## Instagram

Uses cloud storage and computing for photos and videos.


## E-Commerce Websites

Use cloud scaling during high-traffic events.

### Example

```text
Black Friday
      ↓
Traffic Spike
      ↓
Cloud Adds Resources
```

---
