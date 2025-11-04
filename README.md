# voting-machine

# 🗳️ FPGA-Based Digital Voting Machine

A fully functional **digital voting system** implemented in **Verilog HDL**, designed and simulated using **Xilinx Vivado**.  
This project provides a modular, reliable, and secure design for small-scale electronic voting systems, complete with mode control, vote logging, and candidate selection interfaces.

---

## 📁 Project Structure


---

## ⚙️ Key Features

- **Mode Selection:**  
  Controlled via hardware switches or buttons to toggle between:
  - **Voting Mode** – allows voters to cast their votes.
  - **Result Mode** – displays vote count for each candidate.
  - **Reset Mode** – clears all stored votes.

- **Button Debounce Logic:**  
  Clean input handling to ensure valid and single vote registration per button press.

- **Modular Design:**  
  Each function (button control, mode management, and vote logging) is isolated for scalability and readability.

- **FPGA Implementation Ready:**  
  Synthesizable on most Xilinx FPGAs (tested on Artix-7 / Spartan-6 families).

---

## 🧠 Module Overview

| Module Name       | Description |
|--------------------|-------------|
| `buttonControl.v`  | Debounces mechanical button inputs and generates clean voting signals. |
| `modeControl.v`    | Controls operational states (Voting / Result / Reset) using input switches. |
| `voteLogger.v`     | Records votes, counts per candidate, and provides outputs to the display module. |
| `votingMachine.v`  | Integrates all modules into a cohesive system. Top-level design used for synthesis. |

---

## 🧩 How It Works

1. **Voting Mode:**  
   - Each candidate is assigned a button.  
   - When a button is pressed, the vote count for that candidate is incremented.

2. **Result Mode:**  
   - The system outputs the total votes per candidate on display/LEDs.

3. **Reset Mode:**  
   - Clears all vote data for a new election cycle.

---

## 🛠️ Tools & Technologies

| Tool / Technology | Purpose |
|--------------------|----------|
| **Vivado (Xilinx)** | Simulation and synthesis environment |
| **Verilog HDL** | Hardware description and implementation |
| **FPGA Board (Optional)** | For hardware deployment and testing |

---

## 🚀 Simulation & Testing

1. **Open Project in Vivado:**  
   - Launch Vivado and open `votingMachine.xpr`.

2. **Add Source Files:**  
   - Ensure all `.v` files are included in the project.

3. **Run Simulation:**  
   - Use Vivado’s behavioral simulator.  
   - Observe signal transitions and vote counts in waveform view.

4. **Synthesize and Implement:**  
   - Map design to FPGA (optional).  
   - Verify output using LEDs or 7-segment display (if available).

---

## 🧾 Example Testbench (optional)

If you create a testbench (e.g., `votingMachine_tb.v`), include:
- Button press simulation
- Mode transitions
- Vote count verification

---

## 📊 Possible Enhancements

- Add a **display interface** (7-segment or LCD) for results.  
- Implement **security features** (voter ID lockout).  
- Use **non-volatile memory** for vote retention after power loss.  
- Introduce **parameterized number of candidates**.

---

## 🧑‍💻 Authors

- **Om Prakash** – Hardware Design & Verification  

---

## 📜 License

This project is released under the **AICTE License** – free to use, modify, and distribute with attribution.

---

**Keywords:** `Verilog`, `FPGA`, `Vivado`, `Voting Machine`, `Digital Systems`, `Mode Control`, `Debouncing`, `Vote Counter`

---

