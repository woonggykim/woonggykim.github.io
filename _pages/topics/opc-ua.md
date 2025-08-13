---
title: "OPC Unified Architecture"
permalink: /topics/opc-ua/
categories: [research, industrial-automation]
tags: [opc-ua, interoperability, plcs, iiot]
---

## Overview

**OPC Unified Architecture (OPC UA)** is an open, platform-independent standard for secure, reliable, and vendor-neutral industrial communication. Defined by the OPC Foundation and IEC 62541, it enables data exchange between diverse automation systems—such as PLCs, HMIs, SCADA, and MES—regardless of the manufacturer or operating system.

Compared to its predecessor, OPC Classic, OPC UA offers:

- Cross-platform compatibility without dependence on Windows/DCOM
- Rich information modeling for representing complex device data
- Built-in security with encryption, authentication, and auditing
- Firewall-friendly design for easier remote access

As a core technology for Industry 4.0 and Industrial IoT (IIoT), OPC UA serves as the backbone for connecting machines, systems, and enterprise applications in a unified, secure, and scalable way.

## My Research & Contributions

### Standalone OPC UA Wrapper for Legacy Integration

I designed and implemented a standalone OPC UA wrapper that allows modern OPC UA clients to access data from legacy OPC Classic servers without modifying existing systems.

**Technical innovations:**

- Platform independence via Java-based DCOM runtime, enabling low-cost, non-Windows embedded deployments.
- Event-driven update mechanism that significantly reduces data update delays compared to standard sampling methods.
- Robust namespace translation from Classic’s tree structure to UA’s hierarchical object model.
- Validated in real-world conditions using a motion control system for an industrial robot, achieving minimal latency overhead (18–39%) and high tracking accuracy.
- Systematic performance tuning covering JVM garbage collection, read batch sizing, and subscription intervals for optimal throughput and responsiveness under heavy load.

### PLCopen OPC UA Framework for Industrial IoT

I developed and evaluated a PLCopen OPC UA software component for PLC-based industrial control systems, extending open-source PLC platforms (Beremiz and OpenOpcUa) to fully support the PLCopen OPC UA specification.

**Technical innovations:**

- Implemented OPC UA server functions to expose IEC 61131-3 PLC variables and methods as a standardized information model.
- Developed OPC UA client function blocks (FBs) for PLCs to connect to external UA servers, perform synchronous/asynchronous reads/writes, and call remote methods.
- Designed a dual-thread execution model to separate real-time PLC tasks from non-real-time UA communication, preserving control loop performance.
- Performance validation using a 3-axis Cartesian robot system, achieving stable latency (9–14 ms) and up to 66 reads/sec throughput for synchronous read operations.

## Selected Work

- **Paper:** *OPC-UA Communication Framework for PLC-based Industrial IoT Applications*, **IEEE IoTDI**, 2017.  
- **Paper:** *Standalone OPC UA Wrapper for Industrial Monitoring and Control Systems*, **IEEE Access**, 2018.  

[← Back to Topics](/topics/)
