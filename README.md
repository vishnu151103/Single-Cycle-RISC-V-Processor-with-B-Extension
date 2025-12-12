# Single-Cycle-RISC-V-Processor-with-B-Extension

A clean, modular, and fully functional 32-bit single-cycle RISC-V processor designed in Verilog and implemented using Xilinx Vivado.
This processor supports RV32I (36 instructions) and includes 17 Bit-Manipulation instructions from Zbb and Zbkb, making it suitable for both standard RISC-V learning and cryptographic applications.

## Overview

This processor implements:

-> 36 out of 40 RV32I instructions
(All except AUIPC and system instructions)

-> 17 Bit-Manipulation instructions from:

-> Zbb (Basic Bit Manipulation)

-> Zbkb (Bitwise Cryptography Primitives)

## B-Extension Integration

The 17 bit-manipulation instructions are implemented directly inside the ALU, without any extra modules.
This approach makes the design:

-> Easy to remove B Extension from ALU (if a pure RV32I processor is preferred)

-> Efficient for cryptographic algorithms such as ARX ciphers (ChaCha20, Speck, etc.)

-> You can use the processor happily as a standard RV32I design, or enable the extended ALU for crypto applications.

## Hardware Architecture Design

![image](https://github.com/EkthaReddy/RISC-V-Single-Cycle-Processor/assets/152515939/a96949c0-6e89-426c-97c5-8d158f3afae8)

## Encoding of the Bit-manipulation Instructions

![image](https://github.com/EkthaReddy/RISC-V-Single-Cycle-Processor/assets/152515939/e5042813-b772-4bf1-a8a8-44d33539c6b8)

## Implemented Instructions

✔️ RV32I (36 Instructions)

Supports all RV32I instructions except:

-> AUIPC

-> System instructions (ECALL, EBREAK, CSR)

✔️ 17 Bit-Manipulation Instructions

From Zbb and Zbkb subsets:

-> min, minu, max, maxu

-> andn, orn, xnor

-> rol, ror, rori

-> pack, packh

-> rev8, brev8

 -> cpop, clz, ctz

Tools Used

-> HDL: Verilog

-> Simulation & Implementation: Xilinx Vivado

## Attached Resources

This repo includes:

-> Simulation waveforms of all 17 bit-manipulation instructions

-> The machine code encodings of Bit instructions (For base instructions, we can use several websites)

-> Verification screenshots

 ## How to Run

Simulation

-> Open Vivado → Create RTL project

-> Add all files inside rtl/

-> Add testbenches from tb/

-> Run simulation → view waveforms

## Contact

If you have:

Questions

Doubts

Suggestions

Corrections

Feel free to reach out!
Contributions and issues are always welcome.
