---
layout: default
title: Java Systems Concurrency & Memory Management
excerpt: Java-based systems projects exploring multiprocessing, synchronization, and virtual memory management.
tech:
  - Java
  - Multithreading
  - Operating Systems
  - Synchronization
  - Memory Management
github: https://github.com/Susse001/Javacoursework
---
## Java Systems Coursework: Concurrency & Memory Management

This project consists of two systems-focused subprojects implemented in Java, emphasizing core operating system concepts including multiprocessing, synchronization, and memory management.

---

## Producer–Consumer Multiprocessing System

Implemented a classic **Producer–Consumer** problem using Java threads and synchronization primitives to analyze concurrency behavior and throughput.

### Key Details
- Producers and consumers implemented as independent threads
- Shared buffer used for synchronization between threads
- Evaluated system behavior across 18 experimental runs

### Metrics & Experiments
- Producer threads: 2, 5, 10
- Consumer threads: 2, 5, 10
- Shared buffer sizes: 3, 10
- Total configurations tested: 18

### Concepts Demonstrated
- Thread synchronization
- Shared resource coordination
- Concurrency performance tradeoffs

---

## Virtual Memory Management Comparison

Designed and evaluated simulations comparing multiple page replacement algorithms under varying memory constraints.

### Algorithms Compared
- FIFO (First-In, First-Out)
- LRU (Least Recently Used)
- MRU (Most Recently Used)
- Optimal

### Metrics & Experiments
- Page sizes: 512, 1024, 2048 bytes
- Frame counts: 4, 8, 12
- Evaluated memory utilization and replacement behavior

### Concepts Demonstrated
- Paging and memory abstraction
- Performance tradeoffs in memory management
- Algorithmic comparison and analysis

---

## 🔗 Repository
[View on GitHub](https://github.com/Susse001/Javacoursework)
