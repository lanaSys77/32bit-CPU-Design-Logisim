# 🧠 Custom 32-bit Processor Design (Logisim)

## 📌 Overview
This project presents the design and implementation of a **custom 32-bit processor** using **Logisim**.  
The processor follows a simplified architecture that integrates core components such as:

- Program Counter (PC)
- Instruction Memory
- Control Unit (CU)
- Register File (REG)
- Arithmetic Logic Unit (ALU)
- Data Memory
- PC Control Unit (Branching Logic)

The system supports multiple instruction types (R-type, I-type, J-type) and demonstrates full data flow from instruction fetch to write-back.

---

## 🧩 System Architecture

### 🔹 Main Datapath
![Main](images/main.png)

The main datapath shows how instructions flow through the processor:
1. Fetch instruction from memory using PC  
2. Decode instruction fields  
3. Execute using ALU  
4. Access memory (if needed)  
5. Write back results to registers  

---

## ⚙️ Core Components

### 🟣 Control Unit (CU)
- Generates all control signals:
  - `RegDst`
  - `RegWrite`
  - `ExtOp`
  - `BSel`
  - `MemWrite`
  - `MemRead`
  - `WriteBack`
  - `ALUOp`

- Controls overall behavior based on opcode

---

### 🧮 ALU (Arithmetic Logic Unit)
![ALU](images/alu.png)

Supports:
- Arithmetic operations (Add, Sub)
- Logical operations (AND, OR)
- Shift operations (Logical & Arithmetic)
- Rotate operations
- Comparison operations

Controlled using `selectorALU`.

---

### 🗂️ Register File (REG)
![REG](images/reg.png)

- Contains multiple registers (R1 → R7)
- Supports:
  - Dual read (BusX, BusY)
  - Single write
- Controlled using:
  - Decoder
  - Clock
  - RegWrite signal

---

### 🔁 Program Counter & PC Control Unit
![PC CU](images/pc_cu.png)

Handles:
- Sequential execution (PC + 2)
- Branching decisions based on:
  - Equal (E)
  - Greater (G)
  - Less or Equal (LE)

Uses logic gates to determine next PC value.

---

### 💾 Data Memory
- Supports read/write operations
- Controlled via:
  - `MemRead`
  - `MemWrite`
- Connected to ALU output

---

## 🔄 Instruction Flow

1. **Fetch** → Instruction from memory using PC  
2. **Decode** → Extract opcode & registers  
3. **Execute** → ALU performs operation  
4. **Memory** → Access data if needed  
5. **Write Back** → Store result in registers  

---

## 🛠️ Technologies Used

- 🧩 **Logisim** – Digital circuit design
- ⚙️ Combinational & Sequential Logic
- 🔌 Multiplexers (MUX)
- 🔢 Decoders
- 🧠 Control Logic Design
- 🧮 ALU Design
- 🗂️ Register File Implementation

---

## 📄 Documentation

- 📘 Full Report: `report.pdf`
- ⚙️ Control Signals: `control.txt`

---

## ▶️ How to Run

1. Open **Logisim**
2. Load file: `main.circ`
3. Enable clock simulation
4. Run step-by-step or auto simulation
5. Observe:
   - Registers
   - ALU output
   - Memory operations

---

## 💡 Key Features

- ✔️ Modular design (ALU, REG, CU separated)
- ✔️ Supports multiple instruction formats
- ✔️ Branching logic implemented
- ✔️ Clean datapath visualization
- ✔️ Scalable architecture

---

## 👩‍💻 Authors

- Lana Sayes  
- Tasneem Shella

---

## ⭐ Notes

This project demonstrates a full understanding of:
- Computer Architecture
- Datapath Design
- Control Logic Integration

---
