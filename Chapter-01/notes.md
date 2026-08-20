## 1.1 Introduction to C

### C Language
- C is one of the oldest widely used programming languages.
- It is widely used in industry and systems programming.
- Major operating systems such as Windows, macOS, and Linux contain significant amounts of C code.
- Many widely used applications and database systems also contain C code.

### Software vs Hardware
- **Hardware**: The physical components of a computer and its connected devices.
- **Software**: The instructions/programs that tell the hardware what to do.
- Programmers write software by creating ordered instructions that the computer executes.

---

## 1.2 Hardware and Software

- Modern computers can perform billions of operations per second.
- Supercomputers can perform vastly more operations per second.
- Silicon chips made modern computing devices much smaller and less expensive.
- Silicon is abundant in nature and is a major component of sand.

### Moore's Law
- Moore's Law describes the historical trend that processor capability approximately doubled about every two years while the cost per capability decreased.
- The trend has influenced improvements in:
  - Memory capacity
  - Secondary storage capacity
  - Processor speeds
- The traditional scaling described by Moore's Law has become increasingly difficult to maintain.
- Modern performance improvements increasingly rely on architectural techniques such as **multicore processors**.

### Embedded Systems
- An **embedded system** is a computer system built into a larger device to perform specific functions.
- Examples include:
  - Smart home devices
  - Security systems
  - Robots
  - Smart traffic systems

### Bandwidth
- **Bandwidth** is the amount of data that can be transmitted over a communication channel in a given amount of time.
- Improvements in communication technology and reduced communication costs contributed to the **Information Revolution**.

---

## 1.2.2 Computer Organization

A computer can be viewed as a collection of major functional units:

### 1. Input Unit
Receives data and instructions from outside the computer.

Examples:
- Keyboard
- Mouse
- Touchscreen
- Microphone / voice input
- Camera
- Barcode reader
- Internet data
- GPS data
- Accelerometer data
- Data read from secondary storage
  - USB flash drives
  - Blu-ray discs

**Important:** Receiving data from the Internet or reading data from storage is also considered input.

---

### 2. Output Unit
Presents processed information to the outside world.

Examples:
- Displays/screens
- Printed documents
- Audio
- Video
- Data transmitted over the Internet
- Signals controlling other devices
- Game-controller vibrations
- VR/AR devices

---

### 3. Memory Unit
- Stores data and instructions that are currently being used.
- Main memory is typically **RAM (Random Access Memory)**.
- RAM is **volatile memory**: its contents are lost when power is removed.
- A byte consists of **8 bits**.
- A bit represents a binary value: **0 or 1**.

---

### 4. Arithmetic and Logic Unit (ALU)
Performs:
- Arithmetic operations:
  - Addition
  - Subtraction
  - Multiplication
  - Division
- Logical operations and comparisons.

The ALU is integrated into modern CPUs.

---

### 5. Central Processing Unit (CPU)
- The CPU coordinates and controls the activities of the computer.
- It directs data movement between the input unit, memory, ALU and output unit.
- Modern CPUs commonly contain multiple processing cores.

---

### 6. Secondary Storage
- Provides long-term, persistent storage for programs and data.
- Unlike RAM, its contents remain after power is removed.
- It is generally slower than RAM but provides much larger storage capacity at lower cost.

Examples:
- Hard Disk Drives (HDDs)
- Solid-State Drives (SSDs)
- USB flash drives

---

## Multicore Processors

### Core
- A **core** is an individual processing unit within a processor.

### Multicore Processor
- A multicore processor contains multiple processing cores on a single chip.
- Multiple cores can execute tasks concurrently, allowing greater overall processing capability.

Examples:
- Dual-core → 2 cores
- Quad-core → 4 cores
- Octa-core → 8 cores

### Why Multicore?
Increasing the clock speed of a single core produces problems such as:
- Higher power consumption
- Increased heat generation
- Physical limitations of transistor scaling

Using multiple cores provides another way to increase overall processing performance without relying entirely on increasing the speed of one core.

### Multithreading
- **Multithreading** allows a program to divide work into multiple threads.
- Threads can potentially execute concurrently on different CPU cores.
- The operating system schedules and distributes tasks among available cores.

---

## Important Engineering Connections

### Electron Leakage and Transistor Scaling
- As transistors become extremely small, physical effects become increasingly important.
- **Quantum tunneling** can allow electrons to pass through barriers that would normally prevent them from crossing.
- Leakage increases unwanted power consumption and heat.
- These physical limitations are among the challenges that make continued traditional transistor scaling difficult.

### CPU Cache
- Modern processors use very fast **cache memory** to reduce the time needed to access frequently used data and instructions.
- Common cache levels include **L1, L2 and L3**.
- L1/L2 are generally closer to individual cores, while L3 is typically shared across multiple cores.

### RAM vs Secondary Storage
| RAM | Secondary Storage |
|---|---|
| Volatile | Persistent |
| Faster | Generally slower |
| Smaller capacity | Much larger capacity |
| Used for active data/programs | Used for long-term storage |
| Data lost when power is removed | Data remains after power is removed |


