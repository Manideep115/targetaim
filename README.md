# 🎯 TargetAim
A Real-Time Smart Head Tracking and Aiming System
<br>
<p align="center">
  <a href="https://opensource.org/licenses/MIT"><img src="https://img.shields.io/badge/License-MIT-yellow.svg" alt="License: MIT"></a>
  <a href="https://www.python.org/"><img src="https://img.shields.io/badge/Python-3.7+-blue.svg" alt="Python"></a>
  <a href="https://ultralytics.com/yolo"><img src="https://img.shields.io/badge/YOLO-v8-blueviolet.svg" alt="YOLOv8"></a>
  <a href="https://www.arduino.cc/"><img src="https://img.shields.io/badge/Arduino-ESP32-00979D.svg" alt="Arduino/ESP32"></a>
</p>

---

TargetAim is an intelligent system that detects, recognizes, and physically tracks human heads in real-time. Using a webcam, it processes the video feed with **YOLOv8** for high-speed head detection and a **Face Recognition** library to identify specific individuals.

Based on the target's position relative to the center of the frame, the system calculates the error and sends corrective commands via serial communication to **servo motors** (controlled by an Arduino or ESP32). This allows a physical camera or aiming device to automatically pan and tilt to follow the recognized person.

## ✨ Features
* **🚀 Real-Time Detection:** Utilizes YOLOv8 for high-speed, accurate head detection.
* **👤 Face Recognition:** Identifies known individuals from a pre-registered database of faces.
* **🤖 Servo Aiming:** Automatically controls Pan (X-axis) and Tilt (Y-axis) servos to lock onto the target.
* **🔌 Hardware Integration:** Communicates serially with Arduino or ESP32 for precise hardware control.
* **🎯 Smart Tracking:** Calculates the positional error to send smooth and responsive movement commands.

---

## Diagram: System Architecture
Here is a high-level overview of the data flow:

```ascii
[ 📷 Webcam ] --> [ 💻 Python Script ] --> [ 🔌 Serial Port ] --> [ 🤖 Arduino/ESP32 ]
                     |                                                |
                     | 1. YOLOv8 (Detects Head)                       |
                     | 2. Face Recognition (Identifies Face)          V
                     | 3. Calculate (Δx, Δy)                 [ 🦾 Pan/Tilt Servos ]
                     V
                 [ 📺 Bounding Box on Screen ]
