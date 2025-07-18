# 🤖 Edge Avoidance Bot

An Arduino-based autonomous robot that uses **ultrasonic sensors** to detect edges (like table ends or stairs) and avoid falling using real-time obstacle logic.

![Bot Image](https://github.com/Gaganh2403/Edge-Avoidence-Bot/blob/main/Image/image1%20(1).jpg?raw=true)

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

The **Edge Avoidance Bot** is a basic embedded systems project that prevents a robot from falling off edges using **ultrasonic sensors**. It makes intelligent movement decisions—forward, backward, or turning—based on sensor feedback, making it ideal for table-top or elevated environments.

---

## 🔧 Components Used

| Component                  | Quantity |
|----------------------------|----------|
| Arduino Uno                | 1        |
| Ultrasonic Sensor (HC-SR04)| 2        |
| Motor Driver (L298N)       | 1        |
| DC Motors                  | 2        |
| Wheels & Chassis           | 1 Set    |
| Power Source (Battery)     | 1        |
| Jumper Wires               | As needed |
| Breadboard (optional)      | 1        |

---

## ⚙️ Working Principle

- Two **ultrasonic sensors** are mounted at the front edge of the bot.
- If **both sensors** detect a short distance (<10 cm), the bot moves **backward**.
- If only **one sensor** detects the edge, it turns in the opposite direction.
- If **no edge** is detected, it moves **forward**.

---

## 🔌 Circuit Diagram

![Circuit Diagram](https://github.com/Gaganh2403/Edge-Avoidence-Bot/blob/main/Circuit%20daigram/circuit_image.png?raw=true)

---

## 📜 Code Explanation

- Uses the **NewPing** library for ultrasonic distance measurement.
- `ping_cm()` is used to get the current distance from each sensor.
- Motor control pins are toggled via digital output from the Arduino based on logic decisions.

> Refer to [`Code.txt`](https://github.com/Gaganh2403/Edge-Avoidence-Bot/blob/main/Code.txt) for the complete Arduino sketch.

---

## 🎥 Demo

Here’s a quick demo of the bot avoiding edges:

▶️ [Watch video](https://github.com/Gaganh2403/Edge-Avoidence-Bot/blob/main/Image/video.mp4)

> GitHub plays `.mp4` videos inline when viewed in a browser.

---

## 🚀 How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/Gaganh2403/Edge-Avoidence-Bot.git
