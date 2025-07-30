# 🚦 Traffic Light Controller using Verilog HDL

This project implements a basic **Traffic Light Controller** using **Verilog HDL**. It simulates the operation of a traffic signal system at a four-way junction using timing and state transitions.

---

## 📌 Project Overview

- 🕒 Time-based state machine controlling Red, Yellow, and Green lights.
- 🚗 Controls North-South and East-West traffic.
- 🔄 Implements smooth transitions with delays between each state.
- 🧪 Simulated using **Xilinx Vivado**.

---

## 🧾 Features

- FSM (Finite State Machine) based control
- Four major states: `Red`, `Green`, `Yellow`, and `All Red`
- Each signal remains active for a predefined duration
- Optionally handles pedestrian crossing or emergency override (advanced)

---

## 🗂️ Folder Structure

traffic-light-controller-verilog/
├── src/
│ └── traffic_light_controller.v # Verilog source code
├── testbench/
│ └── traffic_tb.v # Testbench file
├── simulation/
│ └── traffic_output.vcd (optional)
├── video/
│ └── output_demo.mp4 # Output video of simulation
└── README.md # Project documentation


## 🛠️ Tools Used

- **Vivado Design Suite 2025.1**
- Platform: Windows / Linux
- Simulation: Vivado Behavioral Simulation

- ## 🧪 How to Simulate

1. Open Vivado and create a new project.
2. Add:
   - `traffic_light_controller.v` to **Design Sources**
   - `traffic_tb.v` to **Simulation Sources**
3. Run **Behavioral Simulation**.
4. Observe the timing and transitions in the simulation output or waveform.

---

## 💡 Working Logic

| State       | NS Signal | EW Signal | Duration |
|-------------|-----------|-----------|----------|
| State 0     | Green     | Red       | 10 sec   |
| State 1     | Yellow    | Red       | 2 sec    |
| State 2     | Red       | Green     | 10 sec   |
| State 3     | Red       | Yellow    | 2 sec    |

Clock divider is used to simulate delay in seconds using simulation time.

