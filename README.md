# Edge Avoidance Robot using Ultrasonic Sensors and Arduino

This project is a smart 4-wheel edge-avoidance robot that uses **dual ultrasonic sensors** and **motor driver logic** to detect edges, obstacles, and prevent falls. The bot intelligently decides whether to move forward, reverse, or turn based on the sensor data.

---

## 📷 Project Images

| Front View | Sensor Mount |
|------------|---------------|
| ![Front](./images/front.jpg) | ![Sensor](./images/sensor_mount.jpg) |

*(Replace the above with actual image paths from your repo)*

---

## Features

- Dual **HC-SR04** ultrasonic sensors (left & right)
- Smart edge detection using **NewPing** library
- Controlled via **Arduino UNO**
- Motor control via **L293D Motor Driver Shield**
- Autonomous movement: Forward, Reverse, Left Turn, Right Turn
- Custom logic for perfect turning (one side forward, other backward)

---

##  How It Works

- If both sensors detect a distance > 15 cm → Move **forward**
- If both detect a gap (≤15 cm) → **Stop**, **reverse**, and **right turn**
- If only right detects a gap → **Left turn** and move forward
- If only left detects a gap → **Right turn** and move forward

---

##  Components Used

| Component            | Quantity |
|----------------------|----------|
| Arduino UNO          | 1        |
| L293D Motor Driver Shield | 1  |
| HC-SR04 Ultrasonic Sensor | 2  |
| DC Gear Motors       | 4        |
| Robot Chassis        | 1        |
| Wheels               | 4        |
| 9V or 12V Battery Pack | 1      |
| Jumper Wires         | -        |

---

##  Arduino Libraries Used

- [NewPing](https://github.com/ErickSimoes/NewPing) – for accurate ultrasonic sensing
- AFMotor (for L293D Motor Driver Shield)

>  Install via Library Manager in Arduino IDE

---

##  Pin Configuration

###  Ultrasonic Sensors:
| Sensor      | TRIG Pin | ECHO Pin |
|-------------|----------|----------|
| Left        | A0       | A1       |
| Right       | A2       | A3       |

### ⚙ Motors (via AFMotor):
| Motor Position   | Channel |
|------------------|---------|
| Left Front       | M1      |
| Left Rear        | M2      |
| Right Front      | M3      |
| Right Rear       | M4      |

---

##  Arduino Code Overview

Main logic includes:
- Reading distances via `sonarLeft.ping_cm()` and `sonarRight.ping_cm()`
- Deciding motion type
- Setting motor directions using `AF_DCMotor` methods

**Default speed is set to `60`** for stable motion.

---

##  Acknowledgments

Special thanks to my mentor **[Insert Mentor's Name]** for guiding me through this project.  
And sincere appreciation to **[Insert Company Name]** for providing the kit and learning platform.

---

##  License

This project is open-source under the [MIT License](LICENSE).

---

##  Author  
[LinkedIn](https://www.linkedin.com/in/gagan-h-ba69a9328/) | [GitHub](https://github.com/Gaganh2403)

