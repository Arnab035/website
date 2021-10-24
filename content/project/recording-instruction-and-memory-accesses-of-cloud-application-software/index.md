---
title: Recording Instruction and Memory Accesses of Cloud Application Software
subtitle: A full-system simulation technique to record all instructions and
  memory access addresses of applications running in off-the-shelf server
  systems.
date: 2021-10-24T06:56:19.818Z
summary: ""
draft: false
featured: false
image:
  filename: featured
  focal_point: Smart
  preview_only: false
---
Abstract: 

Micro-architecture research often relies on processing instruction and memory traces. However, the traditional approach of using micro-architectural simulation to collect traces presents many challenges and practical limitations. Simulators and emulators are slow (limiting the length of trace collected), have incomplete ISA or system support (precluding tracing of the operating system), work on a single host (incapable of tracing networked systems such as servers), perturb the timing of IO events (compromising the fidelity of the traces), and typically suffer from multiple of these characteristics.

In this work, we explore leveraging a combination of virtualization (Intel VT) and software debugging support (Intel PT) to collect instruction and memory traces from off-the-shelf server systems. We develop a system to record a light-weight trace of the CPU control-flow, timer, network, and disk events on a live server system and then replay this light-weight trace in an emulator whose execution is forced to follow the previously recorded trace.  The emulator is then able to collect detailed instruction and memory traces that exactly match the timing and full-system behavior of the original live networked server. We validate the traces we collect against performance counters of a live unperturbed server system and demonstrate the benefits of our approach compared to traditional simulators, including Gem5, Flexus, and ZSim.