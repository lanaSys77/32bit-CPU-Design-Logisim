# 🧠 Custom 32-bit Processor (Logisim)

> A complete 32-bit processor designed from scratch using digital logic in Logisim, demonstrating full datapath execution, control logic integration, and modular CPU architecture.

---

## 👩‍💻 Authors
- **Lana Sayes**
- **Tasneem Shella**

---

## 📌 Overview

This project implements a **custom-designed 32-bit processor** using Logisim.  
It simulates how real processors execute instructions through a structured datapath and control logic.

The system integrates:
- Instruction Fetch & Decode
- Register-based execution
- ALU operations
- Memory access
- Branching decisions

The design follows a **modular architecture**, separating datapath components from control logic, similar to real-world CPU design principles.

---

## 🏗️ High-Level Architecture

```mermaid
flowchart LR
    PC --> IM[Instruction Memory]
    IM --> CU[Control Unit]
    IM --> REG[Register File]
    REG --> ALU
    ALU --> DM[Data Memory]
    DM --> WB[Write Back]
    WB --> REG

    CU --> ALU
    CU --> REG
    CU --> DM
    CU --> PCU[PC Control Unit]

    PCU --> PC
