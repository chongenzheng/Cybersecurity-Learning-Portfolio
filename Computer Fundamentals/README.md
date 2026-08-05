## Overview
This module covers the fundamental concepts of modern computer systems and provides the foundation for future cybersecurity learning. Understanding how computers are built, how operating systems boot, and how computing environments are organized is essential before moving into networking, operating systems, and security.

## Learning Objectives
- Understand the major hardware components inside a computer.
- Learn the role of the CPU, RAM, storage devices, motherboard, PSU, and GPU.
- Differentiate common computer types and their use cases.
- Understand the client-server architecture.
- Learn the fundamentals of virtualization.
- Understand the basic concepts of cloud computing.
- Understand the operating system boot process from power-on to OS initialization.

## Knowledge Sources
- TryHackMe – Computer Fundamentals
- Intel Processor Documentation
- Microsoft Windows Documentation
- UEFI Specification
- General Computer Architecture References

## Topics Covered

### Inside a Computer System

Studied the purpose and interaction of major hardware components:

- CPU
- RAM
- Motherboard
- Power Supply Unit (PSU)
- Storage Devices (HDD / SSD)
- GPU
- Cooling System
- Firmware (BIOS / UEFI)

Learned the computer boot process:

1. Power Button
2. Firmware (UEFI)
3. POST (Power-On Self-Test)
4. Boot Device Selection
5. Bootloader
6. Operating System Kernel Initialization

### Computer Types

Compared different computer systems:
- Desktop
- Laptop
- Workstation
- Server
- Mobile Devices
- Embedded Systems
Understood the advantages, limitations, and common applications of each.

### Client-Server Basics
Learned how client-server communication works.
Key concepts:
- Client
- Server
- Request
- Response
- Services
- Network Communication
Examples:
- Web browsing
- File sharing
- Email
- Database services

### Virtualization Basics
Studied the purpose of virtualization.
Learned:

- Virtual Machine (VM)
- Hypervisor
- Host Operating System
- Guest Operating System
- Resource Allocation
- Isolation

Compared virtualization with running multiple physical computers.

### Cloud Computing Fundamentals

Learned the basic cloud service models:

- IaaS
- PaaS
- SaaS

Deployment models:

- Public Cloud
- Private Cloud
- Hybrid Cloud

Advantages:

- Scalability
- High Availability
- Cost Efficiency
- Elastic Resources

## Hands-on Practice


## Challenges & Troubleshooting

### Understanding the Boot Process

Initially confused about the difference between:

- Boot Device
- Bootloader
- Operating System Kernel

After further research, I understood that:

- UEFI selects **where** to boot from.
- Bootloader loads the operating system kernel into RAM.
- The kernel then initializes drivers, system services, and user processes.

---

### BIOS vs UEFI

Initially, it was assumed that BIOS and UEFI were different operating systems.

Learned that:

- Both are firmware.
- UEFI is the modern replacement for BIOS.
- UEFI provides additional security features and supports larger storage devices.

### GPU vs Graphics Card

Initially thought the GPU referred to the entire graphics card.

Learned the distinction:

- GPU is the graphics processor.
- A graphics card includes:
  - GPU
  - VRAM
  - PCB
  - VRM
  - Cooling System
  - Fans

## Key Takeaways

- A computer is a collection of coordinated hardware components rather than a single processing unit.
- UEFI initializes hardware before the operating system starts.
- The bootloader is responsible for loading the operating system kernel into memory.
- RAM contains only the components currently required by the operating system and running applications—not the entire operating system installation.
- Virtualization allows multiple isolated operating systems to share the same physical hardware.
- Cloud computing builds upon virtualization to provide scalable computing resources over the Internet.
- Understanding these fundamentals is critical before learning networking, operating systems, and cybersecurity.

## Future Improvements

Next learning goals:
- Memory Management
- Process Management
- File Systems
- Virtual Machines (VirtualBox / VMware)
- AWS Cloud Fundamentals
