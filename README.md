## 🚀 Installation & Setup

### 1. Python (Host PC)
            
1.  **Clone this repository:**
    ```sh
    git clone [https://github.com/Manideep115/TargetAim.git](https://github.com/Manideep115/TargetAim.git)
    cd TargetAim
    ```
2.  **Create a virtual environment (Recommended):**
    ```sh
    python -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    ```
3.  **Install required Python packages:**
    ```sh
    pip install ultralytics opencv-python face_recognition numpy pyserial
    ```
4.  **Add known faces:**
    * Place images of people you want to recognize in the `known_faces/` directory.
    * Name the image files as the person's name (e.g., `manideep.jpg`, `alex.png`). The script will use the filename as the person's name.

### 2. Arduino / ESP32 (Microcontroller)
            
1.  Open the `arduino_servo_control/arduino_servo_control.ino` sketch in the Arduino IDE.
2.  Select your board (Arduino Uno / ESP32) and the correct COM port.
3.  Install the `Servo.h` library (or `ESP32Servo.h` for ESP32) if not already present.
4.  Upload the sketch to your microcontroller.

---

## 🔌 Wiring
Connect your components to the Arduino/ESP32 as follows.

| Component | Arduino Pin | ESP32 Pin | Connection |
| :--- | :--- | :--- | :--- |
| **Pan Servo** | D9 | GPIO 13 | Signal Pin |
| **Tilt Servo** | D10 | GPIO 12 | Signal Pin |
| **Servo V+** | 5V | 5V / VIN | 5V Power |
| **Servo GND** | GND | GND | Ground |



**Serial Communication:** The Python script communicates with the Arduino/ESP32 via USB serial. Ensure you update the COM port in the Python script (`main.py`) to match the one your device is connected to.

---

## 🎬 Demo

*(A video or GIF of the project in action will be added here.)*



---

## 🔗 Project Ecosystem
This repository is part of a larger project. The related components are:
* **[face_recognition_project](https://github.com/Manideep115/face_recognition_project):** The core library and scripts for managing and performing face recognition.
* **[headaim](https://github.com/Manideep115/headaim):** Contains earlier versions and related experiments for the head aiming logic.

---

## 👨‍💻 Author
* **ALUR MANIDEEP**

## 📄 License
This project is licensed under the MIT License. See the `LICENSE` file for details.
