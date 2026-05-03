# 🧠 Custom 32-bit Processor Design (Logisim)

## 📌 Overview
This project presents the design and implementation of a **custom 32-bit processor** using **Logisim**.  
It demonstrates a complete datapath architecture including instruction execution, control logic, and memory interaction.



---

## 🧩 System Architecture

![Main Datapath](images/Main.png)

**Description:**  
This image represents the full processor datapath. It shows how instructions flow from the Program Counter (PC) through instruction memory, register file, ALU, and memory, then back through the write-back stage.

---

## ⚙️ Core Components

### 🟣 Control Unit

![Control Unit](images/ControlUnit.png)

**Description:**  
The Control Unit generates all necessary control signals based on the opcode.  
It manages:
- Register destination selection
- Memory read/write operations
- ALU operation selection
- Write-back control

---

### 🔁 PC Control Unit (Branching Logic)

![PC Control](images/Pc CU.png)

**Description:**  
Handles branching decisions using comparison results:
- Equal (E)
- Greater than (G)
- Less or equal (LE)

This unit determines whether to update the PC sequentially or jump to another address.

---

### 🗂️ Register File

![Register File](images/Reg.png)

**Description:**  
Stores processor data using multiple registers.  
Supports:
- Two read ports (BusX, BusY)
- One write port  
- Controlled via decoder and clock

---

### 🧮 ALU (Arithmetic Logic Unit)

![ALU](images/Alu.png)

**Description:**  
Performs all arithmetic and logical operations including:
- Addition / Subtraction
- AND / OR
- Shifting (logical & arithmetic)
- Rotate operations
- Comparisons

---

## 🔄 Instruction Execution Flow

1. **Fetch** → Instruction is loaded from memory using PC  
2. **Decode** → Control Unit interprets opcode  
3. **Execute** → ALU performs operation  
4. **Memory** → Read/write if needed  
5. **Write Back** → Result stored in registers  

---

## 🛠️ Technologies Used

- 🧩 Logisim (Circuit Design)
- ⚙️ Digital Logic Design
- 🔌 Multiplexers (MUX)
- 🔢 Decoders
- 🧠 Control Unit Design
- 🧮 ALU Implementation
- 🗂️ Register File Design

---

## 📄 Documentation

- `report.pdf` → Full project report  
- `control.txt` → Control signals logic  

---

## ▶️ How to Run

1. Open **Logisim**
2. Load `main.circ`
3. Enable clock simulation
4. Run step-by-step
5. Observe outputs in:
   - Registers
   - ALU
   - Memory

---

## 💡 Key Features

- ✔️ Complete datapath implementation  
- ✔️ Modular design (ALU, REG, CU separated)  
- ✔️ Branching logic supported  
- ✔️ Multiple instruction formats  
- ✔️ Clean and scalable architecture  

---

## 🤝 Collaboration

This project was developed as a team effort, combining design, implementation, and testing across all processor components.

---

## 👩‍💻 Authors

- Lana Sayes  
- Tasneem Shella  

---

## ⭐ Final Note

This project reflects a strong understanding of:
- Computer Architecture  
- Datapath Design  
- Control Logic Integration  

---
