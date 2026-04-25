# Traffic Light Controller at Crossroad 🚦

## 📖 Introduction
In the context of increasingly complex urban traffic, the management and control of traffic flow at intersections have become a significant challenge. This project focuses on the design and implementation of a digital traffic light controller for an intersection, utilizing LEDs without the need for countdown timers. The system aims to ensure traffic safety, optimize vehicle waiting times, and provide a transparent method for traffic regulation.

**Institution:** VNU-HCM University of Science  
**Course:** Digital Electronics (Class: 23DTV_CLC1)  
**Instructor:** Dr. Bùi Trọng Tú  

## 👥 Team Members
* Đàm Nguyễn Như Ngọc – 23207087
* Trần Đông Dương – 23207049
* Hồ Trọng Hải – 23207050

## 🎯 Project Objectives
* **Optimal Timing:** Reasonable allocation of signal times based on traffic volume and time of day.
* **Safety First:** Ensure safety and transparency in traffic regulation without relying on countdown timers.
* **Practicality:** Focus on ease of operation, maintenance, and high reliability for simple intersections.

## ⚙️ System Architecture & Circuit Design

The control system is built using fundamental digital electronic components:
* **D Flip-Flops:** The circuit utilizes 10 D flip-flops operating synchronously to perform counting cycles and control the light states.
* **Logic Gates:** Used primarily for setting or clearing data, having a direct impact on the accurate state transitions of the entire circuit.

### 🚥 State Sequence & Timing
The traffic lights operate based on a 4-state sequence controlling two main directions:

| State | Direction 1 (Light 1) | Direction 2 (Light 2) | Duration |
| :---: | :--- | :--- | :---: |
| **1** | 🔴 Red | 🟢 Green | 4s |
| **2** | 🔴 Red | 🟡 Yellow | 1s |
| **3** | 🟢 Green | 🔴 Red | 1s |
| **4** | 🟡 Yellow | 🔴 Red | 1s |

### 🧮 Logic Optimization (K-Maps)
Based on the state transition table, the Boolean expressions were optimized using Karnaugh Maps to minimize the required logic gates. 

**Direction 1:**
* `R1 = Q0 + Q4`
* `Y1 = Q9`
* `G1 = Q5`

**Direction 2:**
* `R2 = Q5 + Q9`
* `Y2 = Q4`
* `G2 = Q0`

## 🎥 Demo Video

<video src="https://github.com/user-attachments/assets/532fe692-629f-4bc1-a734-e8da0112d734" controls="controls" style="max-width: 100%;"></video>

*(Note: The system accurately controls the timing of transitions between traffic lights, ensuring signals change exactly as simulated.)*

## 🚀 Evaluation & Future Directions

### Current Performance
The system successfully manages traffic flow at intersections with moderate traffic, strictly adhering to the preset cycles. 

### Future Development
To enhance the system for more complex urban environments, the following developments are proposed:
* **Algorithm Optimization:** Integrating adaptive control algorithms to handle dynamically changing traffic situations in real-time.
* **Complex Intersections:** Expanding the logic to manage intersections with multiple lanes and directions.
* **Artificial Intelligence:** Incorporating AI to automatically adjust light timings based on real traffic conditions and respond flexibly to emergency situations.
* **Software Tools:** Building a user-friendly interface to support the installation and configuration of the system in practice.
