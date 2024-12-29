---
title: 
tags: 
icon: 
aliases: 
---
> In computer science, an **instruction set architecture** (ISA) is an abstract model that generally defines how software controls the [[Central Processing Unit|CPU]] in a computer or a family of computers. A device or program that executes instructions described by that ISA, such as a central processing unit (CPU), is called an implementation of that ISA.
>
> In general, an ISA defines the supported instructions, data types, registers, the hardware support for managing main memory, fundamental features (such as the memory consistency, addressing modes, virtual memory), and the input/output model of implementations of the ISA.
>
> An ISA specifies the behavior of machine code running on implementations of that ISA in a fashion that does not depend on the characteristics of that implementation, providing binary compatibility between implementations. This enables multiple implementations of an ISA that differ in characteristics such as performance, physical size, and monetary cost (among other things), but that are capable of running the same machine code, so that a lower-performance, lower-cost machine can be replaced with a higher-cost, higher-performance machine without having to replace software.  It also enables the evolution of the microarchitectures of the implementations of that ISA, so that a newer, higher-performance implementation of an ISA can run software that runs on previous generations of implementations.
>
> If an operating system maintains a standard and compatible application binary interface (ABI) for a particular ISA, machine code will run on future implementations of that ISA and operating system.  However, if an ISA supports running multiple operating systems, it does not guarantee that machine code for one operating system will run on another operating system, unless the first operating system supports running machine code built for the other operating system.
>
> An ISA can be extended by adding instructions or other capabilities, or adding support for larger addresses and data values; an implementation of the extended ISA will still be able to execute machine code for versions of the ISA without those extensions.  Machine code using those extensions will only run on implementations that support those extensions.
>
> The binary compatibility that they provide makes ISAs one of the most fundamental abstractions in computing.
>
> [Wikipedia](https://en.wikipedia.org/wiki/Instruction%20set%20architecture)