1.1 Introduction to C

C Language

* C is one of the oldest programming languages in the world.
* According to the TIOBE Index, C is one of the most popular programming languages.
* The book provides extensive hands-on experience in writing C instructions that tell computers what tasks to perform.
* C instructions are also called code.

Software and Hardware

* Software: The instructions/code written by programmers that control computer hardware.
* Hardware: The physical components of a computer and its associated devices.
* Programmers write software instructions that tell hardware what to do.
* Without software, hardware cannot perform useful programmed tasks.

Uses of C

C is widely used in industry.

Major systems and applications that are written partly in C include:

* Operating systems:
    * Windows
    * macOS
    * Linux
* Web browsers:
    * Google Chrome
    * Firefox
* Database management systems:
    * Microsoft SQL Server
    * Oracle

Why C Is Important

* C was developed in the 1970s.
* It has strongly influenced many later programming languages.
* Languages influenced by C include:
    * C++
    * C#
    * Java
* Learning C helps programmers understand concepts that appear in many other programming languages.

Low-Level Memory Access

* C provides relatively low-level access to computer memory.
* Unlike some higher-level languages that hide many memory-management details, C gives programmers significant control over memory.
* This control can allow programs to be efficient, fast, and lightweight.

C and Operating Systems

* C is heavily used in operating-system development.
* The kernel is the core part of an operating system.
* Operating-system code manages communication between components such as:
    * CPU
    * RAM
    * Input/output devices

Compilers

* Computers ultimately execute machine code.
* Machine code is represented using binary instructions.
* A compiler translates source code written in C into machine code that the computer can execute.
* Common compilers include:
    * Clang
    * GCC
    * Microsoft’s compiler

⸻

1.2 Hardware and Software

Computer Performance

* Computers can perform enormous numbers of calculations per second.
* Personal computers can perform billions of operations per second.
* Supercomputers can perform vastly more operations.
* Fugaku is an example of a powerful supercomputer.
* Supercomputers can perform operations on the scale of quadrillions of calculations per second.

Silicon Chips

* Modern computers depend heavily on silicon chips.
* Silicon is abundant because it is a major component of materials such as sand.
* Advances in silicon-chip technology have dramatically reduced the cost and size of computing hardware.
* Modern chips can contain enormous numbers of electronic components while being physically very small.

⸻

1.2.1 Moore’s Law

Definition

Moore’s Law is an observation associated with Gordon Moore, co-founder of Intel.

It describes the historical trend that:

* The number of components/transistors on integrated circuits increased rapidly.
* Computing performance increased over time.
* Computing costs generally decreased.

A commonly stated version is that computing capability approximately doubles every two years.

Moore’s Law and Computing Resources

The trend affected things such as:

* Memory capacity
* Secondary storage capacity
* Processor speeds

Secondary Storage

Examples include:

* Hard disk drives (HDDs)
* Solid-state drives (SSDs)

Embedded Systems

Processors are not used only in traditional computers.

They are also used in embedded systems.

An embedded system is a computer system built into a larger device to perform specific functions.

Examples:

* Smart household devices
* Security systems
* Robots
* Intelligent traffic-light systems

The End of Traditional Moore’s Law Scaling

Modern semiconductor technology has encountered physical and engineering limitations.

Companies and technology leaders have increasingly emphasized alternative approaches, including:

* Better processor architectures
* Multicore processors
* More efficient chip designs

⸻

Bandwidth and the Information Revolution

Computing is not the only area that experienced rapid technological progress.

Bandwidth

Bandwidth refers to the amount of data that can be transmitted over a communication channel during a given period of time.

Over time:

* Communication costs decreased.
* Available bandwidth increased.
* Demand for data transmission increased dramatically.

This contributed to what is commonly called the Information Revolution.

⸻

1.2.2 Computer Organization

A computer can be viewed as a collection of logical units that work together.

The major units are:

1. Input Unit
2. Output Unit
3. Memory Unit
4. Arithmetic and Logic Unit (ALU)
5. Central Processing Unit (CPU)
6. Secondary Storage Unit

⸻

Input Unit

Definition

The Input Unit receives data and instructions from outside the computer and makes them available to the computer’s other components.

Traditional Input Devices

* Keyboard
* Mouse
* Touch screens

Other Sources of Input

Input can also come from:

* Voice commands
* Barcode readers
* Cameras
* Internet data
* Motion sensors
* GPS
* Secondary-storage devices
* USB flash drives
* Blu-ray discs

Streaming and Downloads

When your computer receives data from the Internet, that data is considered input.

Examples:

* Streaming a YouTube video
* Downloading an e-book
* Receiving data from an online service

GPS

A computer/device can receive geographical-location information through GPS.

Accelerometer

An accelerometer detects movement and changes in orientation.

It can detect movement along different directions, such as:

* Up/down
* Left/right
* Forward/backward

⸻

Multicore Processors

Core

A core is an individual processing unit within a processor.

It can execute instructions and perform computational operations.

Multicore Processor

A multicore processor is a single processor chip containing multiple processing cores.

Examples:

* Dual-core → 2 cores
* Quad-core → 4 cores
* Octa-core → 8 cores

Multiple cores can allow different tasks to execute concurrently.

Parallelism

When multiple processing units work on different tasks at the same time, this is called parallelism.

⸻

Why Multicore Processors Became Important

Historically, one approach to improving performance was to increase the clock speed of a processor.

Clock speed is commonly measured in:

* Hertz (Hz)
* Megahertz (MHz)
* Gigahertz (GHz)

However, increasing clock speed creates problems.

Thermal Problem

Higher clock speeds can result in:

* Higher power consumption
* More heat generation
* Greater cooling requirements

Eventually, simply making one core faster became increasingly difficult.

Multicore Solution

Instead of continually making one core faster:

* Multiple cores can be placed on one chip.
* The workload can be distributed between the cores.
* Overall processing capability can increase without relying entirely on increasing the speed of one core.

⸻

Cache Memory

Processors use very fast memory called cache memory.

Common cache levels include:

L1 Cache

* Very small
* Extremely fast
* Closely associated with an individual core

L2 Cache

* Larger than L1
* Very fast
* Often associated with individual cores

L3 Cache

* Larger than L1/L2
* Can be shared among multiple cores

Cache memory helps processors access frequently needed data and instructions faster than accessing main RAM.

⸻

Operating Systems and Multicore Processors

The operating system helps manage processor resources.

It can:

* Manage running programs.
* Schedule tasks.
* Distribute work among available processor cores.
* Prevent one core from being unnecessarily overloaded while others remain idle.

⸻

Multithreading

Thread

A thread is an execution path within a program.

A program can be divided into multiple threads.

For example, a game could potentially have separate threads for:

* Character movement
* Audio
* Artificial intelligence

Multiple threads can potentially execute on different processor cores.

Important Point

Having multiple CPU cores does not automatically mean that every program will use all of them efficiently.

The software and operating system must be designed to take advantage of parallel execution.

⸻

Moore’s Law → Transistors → Multicore

The technological development can be understood as a chain:

Moore’s Law

↓

More transistors can be placed on a chip.

↓

Transistors become smaller.

↓

Physical limitations become increasingly important.

↓

Increasing the speed of a single core becomes difficult.

↓

Engineers increasingly use multicore architectures and other architectural improvements.

⸻

Transistors

A transistor is a fundamental electronic component used to build digital circuits.

Modern processors contain billions of transistors.

Transistors can be used to implement:

* Logic gates
* Digital circuits
* Processing units
* Memory-related circuitry

⸻

Quantum Tunneling and Electron Leakage

As transistor dimensions become extremely small, physical effects become increasingly significant.

One such phenomenon is quantum tunneling.

Quantum Tunneling

At extremely small scales, electrons can pass through barriers that would normally prevent them from crossing.

This can contribute to:

* Electron leakage
* Increased power consumption
* Heat generation
* Difficulties in further shrinking transistors

This is one of the physical challenges associated with continued transistor scaling.

⸻

Output Unit

Definition

The Output Unit takes processed information and communicates it to the outside world.

Examples of Output

Output can be:

* Displayed on screens
* Printed on paper
* Played as audio
* Displayed as video
* Sent through the Internet
* Used as signals to control other devices

Modern Output Examples

Output can also include:

* Game-controller vibrations
* Virtual Reality (VR) devices
* Augmented/Mixed Reality (AR/MR) devices
* Control signals for autonomous vehicles

⸻

Memory Unit

Definition

The Memory Unit stores data and instructions that the computer is currently using or is likely to need soon.

The primary memory discussed here is RAM.

RAM

RAM = Random Access Memory

Characteristics:

* Fast
* Used while programs are running
* Stores currently needed data and instructions
* Volatile

Volatile Memory

Volatile memory loses its contents when electrical power is removed.

Therefore:

Power OFF → RAM contents are lost

Common RAM Capacity

Typical computer systems may have capacities such as:

* 8 GB
* 16 GB

⸻

Bits and Bytes

Bit

A bit is the smallest basic unit of binary information.

It can have one of two values:

* 0
* 1

Byte

A byte = 8 bits

Gigabyte

A gigabyte is approximately one billion bytes in the simplified terminology commonly used in introductory computing.

⸻

Arithmetic and Logic Unit (ALU)

Definition

The Arithmetic and Logic Unit (ALU) performs:

Arithmetic Operations

* Addition
* Subtraction
* Multiplication
* Division

Logical Operations

It can also perform operations involved in:

* Comparisons
* Decision-making
* Logical processing

For example:

* Is A greater than B?
* Is A equal to B?

ALU and CPU

In modern processors, the ALU is integrated into the CPU.

⸻

Central Processing Unit (CPU)

Definition

The CPU (Central Processing Unit) is the main processing component of a computer.

It coordinates and performs processing operations.

The CPU can coordinate interactions between:

* Input
* Memory
* ALU
* Output
* Other system components

Simplified Processing Flow

A typical process can be thought of as:

Input → Memory → Processing/ALU → Memory → Output

The CPU coordinates these activities.

Multicore CPUs

Modern CPUs commonly contain multiple cores.

Some processors can contain many cores, depending on their design and intended use.

⸻

Secondary Storage

Definition

Secondary storage provides long-term storage for programs and data.

Unlike RAM, secondary storage is persistent.

Persistent Storage

Data remains stored even after the computer is turned off.

Examples

* Hard Disk Drives (HDDs)
* Solid-State Drives (SSDs)
* USB flash drives

Characteristics

Compared with RAM, secondary storage is generally:

* Slower
* Less expensive per unit of capacity
* Available in much larger capacities
* Persistent

Capacities can reach the terabyte (TB) range.

Terabyte

A terabyte is approximately:

1 trillion bytes

⸻

RAM vs Secondary Storage

Feature	RAM	Secondary Storage
Purpose	Current/active data and instructions	Long-term data and programs
Speed	Faster	Generally slower
Volatility	Volatile	Non-volatile / persistent
Power off	Data is lost	Data remains
Capacity	Usually smaller	Usually much larger
Examples	RAM modules	SSD, HDD, USB drive

⸻

Computer Organization — Complete Picture

1. Input Unit

Receives:

* Data
* Instructions
* User input
* Sensor information
* Internet data

↓

2. Memory Unit

Temporarily stores:

* Data
* Instructions
* Intermediate results

↓

3. CPU

Coordinates processing.

Inside/associated with the CPU:

* Processing cores
* ALUs
* Cache memory

↓

4. ALU

Performs:

* Arithmetic
* Logic
* Comparisons

↓

5. Memory

Stores intermediate/final results.

↓

6. Output Unit

Communicates results to the outside world.

7. Secondary Storage

Keeps programs and data for long-term use.

⸻

Important Terms to Memorize

Term	Meaning
Hardware	Physical computer components
Software	Instructions/programs that control hardware
C	A widely used programming language
Compiler	Translates source code into machine code
Machine Code	Low-level instructions executed by the processor
Moore’s Law	Historical trend of rapid growth in transistor density/computing capability
Bandwidth	Amount of data that can be transmitted over a connection per unit time
Input Unit	Receives data/instructions
Output Unit	Communicates processed information
RAM	Fast, volatile main memory
ALU	Performs arithmetic and logical operations
CPU	Main processing and coordination component
Core	Individual processing unit inside a CPU
Multicore Processor	Processor containing multiple cores
Cache	Very fast memory close to/inside the processor
Thread	An execution path within a program
Transistor	Fundamental electronic switching component
Quantum Tunneling	Quantum phenomenon allowing particles to cross energy barriers
Secondary Storage	Persistent long-term storage
HDD	Hard Disk Drive
SSD	Solid-State Drive
Volatile	Loses stored data when power is removed
Persistent	Retains data after power is removed
Bit	Binary digit: 0 or 1
Byte	8 bits
GB	Gigabyte
TB	Terabyte
Parallelism	Multiple computations/tasks occurring simultaneously
