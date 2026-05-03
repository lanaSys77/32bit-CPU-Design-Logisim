# 🧠 Custom 32-bit Processor (Logisim)

> A fully functional 32-bit processor designed and implemented using Logisim, featuring a complete datapath, control logic, ALU operations, register management, and branching mechanisms.

---

## 👩‍💻 Authors
- **Lana Sayes**
- **Tasneem Shella**

---

## 📌 Overview
This project presents the design and implementation of a **custom 32-bit processor** using digital logic principles in **Logisim**.

It demonstrates:
- Full datapath execution
- Control signal generation
- Register-based operations
- Memory interaction
- Branching logic

---

## 🏗️ Architecture Overview

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
