# Computer Fundamentals

## Introduction

Before we can secure a computer, we need to understand how it works.

Think of a computer like a castle:

```text
Before protecting a castle,
we must know:

- What is inside?
- Who can enter?
- How does everything work?
```

Similarly, before learning cybersecurity, we need to understand the basic components of a computer system.

---

# Main Components of a Computer

A computer consists of several hardware components that work together.

---

# Motherboard

## What is a Motherboard?

The motherboard is the main circuit board of a computer.

It connects all components together and allows them to communicate.

### Human Body Analogy

```text
Motherboard = Skeleton + Nervous System
```

Just as the skeleton holds body parts together, the motherboard holds all computer components together.

---

## Connected Components

* CPU
* RAM
* Storage Devices
* Graphics Card
* Network Adapter
* Power Supply
* Input/Output Devices

---

# CPU (Central Processing Unit)

## What is a CPU?

The CPU is the brain of the computer.

It executes instructions and performs calculations.

### Human Body Analogy

```text
CPU = Brain
```

---

## Responsibilities

* Process instructions
* Perform calculations
* Control computer operations
* Execute programs

---

## Important Fact

Modern CPUs contain multiple cores.

```text
1 Core  = One task at a time

Multiple Cores
= Multiple tasks simultaneously
```

---

# RAM (Random Access Memory)

## What is RAM?

RAM is temporary memory used by the CPU.

It stores data that the CPU needs immediately.

### Human Body Analogy

```text
RAM = Short-Term Memory
```

---

## Characteristics

### Fast

Provides quick access to data.

### Temporary

Data is lost when power is turned off.

```text
Power Off
    ↓
RAM Cleared
```

---

## Example

When opening:

```text
Google Chrome
```

The application is loaded into RAM for quick access.

---

# Storage Devices

## What is Storage?

Storage permanently saves data.

### Human Body Analogy

```text
Storage = Long-Term Memory
```

---

# HDD (Hard Disk Drive)

Uses spinning disks and moving parts.

### Advantages

* Cheap
* Large storage capacity

### Disadvantages

* Slower
* Mechanical parts can fail

---

# SSD (Solid State Drive)

Uses memory chips instead of moving parts.

### Advantages

* Much faster
* More reliable
* Lower power consumption

### Disadvantages

* More expensive

---

## Comparison

| HDD             | SSD                |
| --------------- | ------------------ |
| Slower          | Faster             |
| Moving Parts    | No Moving Parts    |
| Cheaper         | More Expensive     |
| Larger Capacity | Better Performance |

---

# Network Adapter

## What is a Network Adapter?

A network adapter allows a computer to communicate with other devices and networks.

### Human Body Analogy

```text
Network Adapter = Voice/Vocal Cords
```

---

## Types

### Wired

Uses Ethernet cables.

### Wireless

Uses Wi-Fi.

---

## Purpose

* Internet access
* Communication with other computers
* Network connectivity

---

# Power Supply Unit (PSU)

## What is a PSU?

The Power Supply Unit provides electricity to all components.

### Human Body Analogy

```text
PSU = Heart
```

---

## Responsibilities

* Converts wall power into usable power
* Distributes power to components

Without a PSU:

```text
No Power
   ↓
No Computer
```

---

# Graphics Card (GPU)

## What is a Graphics Card?

The Graphics Processing Unit processes and displays visual information.

### Human Body Analogy

```text
GPU = Visual Cortex
```

---

## Responsibilities

* Render graphics
* Display images
* Display videos
* Gaming performance
* Graphic design workloads

---

# Input and Output Devices

## Input Devices

Devices used to provide information to a computer.

### Examples

* Keyboard
* Mouse
* Microphone
* Scanner

---

## Output Devices

Devices used to receive information from a computer.

### Examples

* Monitor
* Printer
* Speakers

---

## Simple Flow

```text
Input Device
      ↓
Computer Processes Data
      ↓
Output Device
```

---

# Computer Boot Process

## What is Booting?

Booting is the process of starting a computer.

---

# Step 1: Power Button Pressed

The power button sends a signal to the PSU.

```text
Power Button
      ↓
PSU Activated
```

---

# Step 2: UEFI / BIOS Starts

The firmware begins running.

### Firmware

Special software stored on the motherboard.

---

## UEFI

```text
Unified Extensible Firmware Interface
```

Modern replacement for BIOS.

---

## BIOS

```text
Basic Input Output System
```

Older firmware system.

---

# Step 3: POST

## Power-On Self Test

The system checks whether hardware is working correctly.

### Checks

* CPU
* RAM
* Storage
* Other hardware

---

## Purpose

Detect hardware problems before booting.

---

# Step 4: Select Boot Device

The firmware looks for a device containing an operating system.

### Examples

* SSD
* HDD
* USB Drive

---

# Step 5: Bootloader Starts

The bootloader loads the operating system into RAM.

```text
Storage
   ↓
Bootloader
   ↓
RAM
   ↓
Operating System
```

---

# Operating System Takes Control

Once loaded:

```text
Windows
Linux
macOS
```

takes control of all hardware components.

The computer is now ready to use.

---

# Complete Boot Sequence

```text
1. Press Power Button
        ↓
2. UEFI/BIOS Starts
        ↓
3. POST Runs
        ↓
4. Select Boot Device
        ↓
5. Bootloader Loads OS
        ↓
6. Operating System Starts
```

---

# Human Body Analogy Summary

| Computer Component | Human Equivalent          |
| ------------------ | ------------------------- |
| Motherboard        | Skeleton + Nervous System |
| CPU                | Brain                     |
| RAM                | Short-Term Memory         |
| Storage            | Long-Term Memory          |
| Network Adapter    | Vocal Cords               |
| PSU                | Heart                     |
| GPU                | Visual Cortex             |
| Input Devices      | Senses                    |
| Output Devices     | Actions/Speech            |
