# 💧 Water Flow and Volume Monitor using Arduino

A smart Arduino-based system to **measure real-time water flow rate (L/min)** and **total volume (Liters)** using a water flow sensor. Ideal for smart irrigation, water management, and industrial flow monitoring.

---

## 🎥 Demo Video
![Watch the demo](waterflowmeter.mp4)

---

## 🖼️ Circuit Diagram

![waterflow](https://github.com/user-attachments/assets/0ff7ba32-23df-4351-b016-d754c7c14186)

---

## ⚙️ Components Used

- Arduino Uno
- YF-S201 Water Flow Sensor
- 16x2 LCD (with I2C module recommended)
- Breadboard + Jumper wires

---

## 🔌 Connections

| Component        | Arduino Pin      |
|------------------|------------------|
| Flow Sensor VCC  | 5V               |
| Flow Sensor GND  | GND              |
| Flow Sensor Data | D2 (interrupt)   |
| LCD (if used)    | D4–D9 (Standard) |

> **Note:** The flow sensor sends a pulse for every fixed amount of liquid that flows through it.

---

## 🧠 How It Works

- The sensor emits **pulses** as water flows.
- An **interrupt service routine (ISR)** counts pulses on pin D2.
- Flow rate (L/min) is calculated based on **calibration factor**.
- Volume is continuously accumulated.
- Data is displayed on the **Serial Monitor** or optionally on an **LCD**.

---
