---
title: 
tags: 
icon: 
aliases: 
---
> In computer programming, **machine code** is computer code consisting of machine language instructions, which are used to control a computer's central processing unit (CPU). Although decimal computers were once common, the contemporary marketplace is dominated by binary computers; for those computers, machine code is "the binary representation of a computer program which is actually read and interpreted by the computer. A program in machine code consists of a sequence of machine instructions (possibly interspersed with data)."
>
> Each instruction causes the [[Central Processing Unit|CPU]] to perform a very specific task, such as a load, a store, a jump, or an arithmetic logic unit (ALU) operation on one or more units of data in the CPU's registers or memory.
>
> Early CPUs had specific machine code that might break backward compatibility with each new CPU released. The notion of an [[instruction set architecture]] (ISA) defines and specifies the behavior and encoding in memory of the instruction set of the system, without specifying its exact implementation. This acts as an abstraction layer, enabling compatibility within the same family of CPUs, so that machine code written or generated according to the ISA for the family will run on all CPUs in the family, including future CPUs.
>
> In general, each architecture family (e.g. x86, ARM) has its own ISA, and hence its own specific machine code language. There are exceptions, such as the VAX architecture, which included optional support of the PDP-11 instruction set and IA-64, which included optional support of the IA-32 instruction set. Another example is the PowerPC 615, a processor designed to natively process both PowerPC and x86 instructions. 
>
> Machine code is a strictly numerical language, and is the lowest-level interface to the CPU intended for a programmer. Assembly language provides a direct mapping between the numerical machine code and a human-readable version where numerical opcodes and operands are replaced by readable strings (e.g. 0x90 as the NOP instruction on x86, with 0xB8 being the MOV instruction, 0xE8 meaning CALL or 0x0F05 standing for the SYSCALL instruction). While it is possible to write programs directly in machine code, managing individual bits and calculating numerical addresses and constants manually is tedious and error-prone. For this reason, programs are very rarely written directly in machine code in modern contexts, but may be done for low-level debugging, program patching (especially when assembler source is not available) and assembly language disassembly.
>
> The majority of practical programs today are written in higher-level languages. Those programs are either translated into machine code by a compiler, or are interpreted by an interpreter, usually after being translated into an intermediate code, such as a bytecode, that is then interpreted.
>
> Machine code is by definition the lowest level of programming detail visible to the programmer, but internally many processors use microcode or optimize and transform machine code instructions into sequences of micro-ops. Microcode and micro-ops are not generally considered to be machine code; except on some machines, the user cannot write microcode or micro-ops, and the operation of microcode and the transformation of machine-code instructions into micro-ops happens transparently to the programmer except for performance related side effects.
>
> [Wikipedia](https://en.wikipedia.org/wiki/Machine%20code)