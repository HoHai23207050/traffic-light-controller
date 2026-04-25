# Traffic Light Controller at Crossroad 🚦

## 📖 Introduction
[cite_start]In the context of increasingly complex urban traffic, the management and control of traffic flow at intersections have become a significant challenge[cite: 33]. [cite_start]This project focuses on the design and implementation of a digital traffic light controller for an intersection, utilizing LEDs without the need for countdown timers[cite: 39, 42]. [cite_start]The system aims to ensure traffic safety, optimize vehicle waiting times, and provide a transparent method for traffic regulation[cite: 40, 45, 430].

[cite_start]**Institution:** VNU-HCM University of Science 
[cite_start]**Course:** Digital Electronics (Class: 23DTV_CLC1) 
[cite_start]**Instructor:** Dr. Bùi Trọng Tú 

## 👥 Team Members
* [cite_start]Đàm Nguyễn Như Ngọc – 23207087 
* [cite_start]Trần Đông Dương – 23207049 
* [cite_start]Hồ Trọng Hải – 23207050 

## 🎯 Project Objectives
* [cite_start]**Optimal Timing:** Reasonable allocation of signal times based on traffic volume and time of day.
* [cite_start]**Safety First:** Ensure safety and transparency in traffic regulation without relying on countdown timers.
* [cite_start]**Practicality:** Focus on ease of operation, maintenance, and high reliability for simple intersections.

## ⚙️ System Architecture & Circuit Design

The control system is built using fundamental digital electronic components:
* [cite_start]**D Flip-Flops:** The circuit utilizes 10 D flip-flops operating synchronously to perform counting cycles and control the light states.
* [cite_start]**Logic Gates:** Used primarily for setting or clearing data, having a direct impact on the accurate state transitions of the entire circuit.

### 🚥 State Sequence & Timing
[cite_start]The traffic lights operate based on a 4-state sequence controlling two main directions:

| State | Direction 1 (Light 1) | Direction 2 (Light 2) | Duration |
| :---: | :--- | :--- | :---: |
| **1** | 🔴 Red | 🟢 Green | 4s |
| **2** | 🔴 Red | 🟡 Yellow | 1s |
| **3** | 🟢 Green | 🔴 Red | 1s |
| **4** | 🟡 Yellow | 🔴 Red | 1s |

### 🧮 Logic Optimization (K-Maps)
[cite_start]Based on the state transition table, the Boolean expressions were optimized using Karnaugh Maps to minimize the required logic gates. 

**Direction 1:**
* [cite_start]`R1 = Q0 + Q4`
* [cite_start]`Y1 = Q9` 
* [cite_start]`G1 = Q5` 

**Direction 2:**
* [cite_start]`R2 = Q5 + Q9` 
* [cite_start]`Y2 = Q4` 
* [cite_start]`G2 = Q0` 

## 🎥 Demo Video

[![Traffic Light Demo]
https://github.com/user-attachments/assets/532fe692-629f-4bc1-a734-e8da0112d734
[cite_start]*(Note: The system accurately controls the timing of transitions between traffic lights, ensuring signals change exactly as simulated.)*

## 🚀 Evaluation & Future Directions

### Current Performance
[cite_start]The system successfully manages traffic flow at intersections with moderate traffic, strictly adhering to the preset cycles. 

### Future Development
To enhance the system for more complex urban environments, the following developments are proposed:
* [cite_start]**Algorithm Optimization:** Integrating adaptive control algorithms to handle dynamically changing traffic situations in real-time.
* [cite_start]**Complex Intersections:** Expanding the logic to manage intersections with multiple lanes and directions.
* [cite_start]**Artificial Intelligence:** Incorporating AI to automatically adjust light timings based on real traffic conditions and respond flexibly to emergency situations.
* [cite_start]**Software Tools:** Building a user-friendly interface to support the installation and configuration of the system in practice.
