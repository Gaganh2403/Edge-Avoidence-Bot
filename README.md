# 🤖 Edge Avoidance Bot

An Arduino-based autonomous robot that uses **ultrasonic sensors** to detect edges (such as table ends or stairs) and avoid falling off by making real-time motor decisions.

![Bot Image](https://github.com/Gaganh2403/Edge-Avoidence-Bot/blob/main/Images/image(1).jpg?raw=true)

---

## 📌 Table of Contents

- [About the Project](#about-the-project)
- [Components Used](#components-used)
- [Working Principle](#working-principle)
- [Circuit Diagram](#circuit-diagram)
- [Code Explanation](#code-explanation)
- [Demo](#demo)
- [How to Run](#how-to-run)
- [Future Improvements](#future-improvements)
- [Contributors](#contributors)

---

## 📖 About the Project

The **Edge Avoidance Bot** is a simple embedded systems project designed to prevent a robot from falling off edges using **two ultrasonic sensors**. The robot makes intelligent movement decisions based on sensor feedback — moving forward, turning, or backing away — to ensure safety on elevated surfaces.

---

## 🔧 Components Used

| Component              | Quantity |
|------------------------|----------|
| Arduino Uno            | 1        |
| Ultrasonic Sensor (HC-SR04) | 2        |
| Motor Driver Module (L298N) | 1        |
| DC Motors              | 2        |
| Chassis & Wheels       | 1 Set    |
| Power Supply (Battery) | 1        |
| Jumper Wires           | As needed |
| Breadboard (optional)  | 1        |

---

## ⚙️ Working Principle

- **Two Ultrasonic Sensors** are placed at the left and right front edges of the robot.
- If **both sensors detect close proximity** (e.g., less than 10 cm), the bot moves **backward**.
- If only **one sensor detects an edge**, the bot turns in the opposite direction.
- If **no edge is detected**, it moves **forward**.

---

## 🔌 Circuit Diagram

![Circuit](https://github.com/Gaganh2403/Edge-Avoidence-Bot/blob/main/Images/circuit%20connection.png?raw=true)

---

## 📜 Code Explanation

- The code uses the **NewPing library** to handle ultrasonic sensors.
- Distance is measured using `ping_cm()` method.
- Motor movement is controlled using digital pins connected to the **L298N motor driver**.

> Refer to [`code.ino`](https://github.com/Gaganh2403/Edge-Avoidence-Bot/blob/main/code.ino) for full implementation.

---

## 🎥 Demo

Watch a working demo of the bot in action:

[![Demo Video](https://img.youtube.com/vi/YOUR_VIDEO_ID_HERE/0.jpg)](https://www.youtube.com/watch?v=YOUR_VIDEO_ID_HERE)

> Replace with actual video link if available.

---

## 🚀 How to Run

1. Clone the repo:
   ```bash
   git clone https://github.com/Gaganh2403/Edge-Avoidence-Bot.git
