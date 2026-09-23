# Digital Systems & Computer Organization Core (VHDL)

A modular hardware design repository implementing fundamental digital computing blocks, arithmetic logic units, finite state machines (FSM), and sequential logic elements using **VHDL** and synthesized via **Intel Quartus Prime**.

---

## Overview of Implemented Modules

This repository contains synthesized RTL designs and testbenches for core computer organization sub-systems:

* **Arithmetic Logic Unit (ALU):** Multi-bit arithmetic and logic execution block supporting fundamental operations (Addition, Subtraction, Bitwise AND, OR, XOR, Shifts).
* **Control Unit & Finite State Machine (FSM):** Synchronous Moore/Mealy state machines executing sequential micro-operations and instruction decoding states.
* **Encoders & Decoders:** Priority encoders and binary-to-line decoders for control-line management.
* **Latches & Registers:** D-type and register files managing synchronous data storage and pipeline staging.
* **Seven-Segment Display Controller (sseg):** Combinational display decoder translating binary/hex register outputs into 7-segment drive lines.

---

## Architecture & Structural Hierarchy

   +-------------------------------------------------------+
   |                  Control Unit (FSM)                   |
   +-------------------------------------------------------+
                              | (Control Signals)
                              v

+---------------+       +-------------------+       +-----------------+
| Register File | ----> | Arithmetic Logic  | ----> | Seven-Segment   |
| (Latches/Reg) |       |    Unit (ALU)     |       | Display Decoder |
+---------------+       +-------------------+       +-----------------+
|
v
(Status / Flags)


---

## Technical Specifications

| Subsystem | Description | HDL / Design Tool |
| :--- | :--- | :--- |
| **Logic Description** | RTL behavioral & structural VHDL | VHDL-93 / VHDL-2008 |
| **Synthesis Tool** | Intel Quartus Prime | Max 10 / Cyclone IV target families |
| **Verification** | Functional & Timing Simulation | ModelSim / Quartus Waveform Editor |
| **Key Blocks** | ALU, FSM, Encoders, Decoders, Registers, SSeg | Modular entity architecture |

---

## Verification & Simulation Workflow

1. **Compilation & Synthesis:** Projects are synthesized targeting standard Intel FPGA architectures, checking for zero critical warnings and setup/hold timing margins.
2. **Functional Simulation:** Vector Waveform Files (`.vwf`) and testbenches validate combinational truth tables, arithmetic overflow/carry flags, and sequential state transitions.
3. **Hardware Deployment:** Pin assignments mapped for rapid deployment onto FPGA development kits.

---

## Tools Used

* **Design Suite:** Intel Quartus Prime (Lite Edition)
* **Simulation:** ModelSim / Quartus Simulation Toolset
* **Language:** VHDL
