# 🤖 Robotics Projects

A curated library of embedded firmware and sensor codebases for Arduino and ESP32-based robotics systems — covering autonomous navigation, motor control, sensor interfacing, and teleoperation.

---

## 📁 Project Overview

| Project | Platform | Description |
|---|---|---|
| [Line Follower Robot (2 IR Sensors)](#line-follower-robot) | Arduino | Basic line-following using 2 IR sensors |
| [Line Follower Robot (3 IR Sensors)](#line-follower-robot) | Arduino | Enhanced line-following with centre sensor for better accuracy |
| [Holonomic Drive with PS4 Remote](#holonomic-drive-with-ps4-remote) | ESP32 | 4-wheel holonomic drive controlled via Bluetooth PS4 controller |
| [Robot Odometry (3 Rotary Encoders)](#robot-odometry) | Arduino/ESP32 | Position and heading estimation using three rotary encoders |
| [QMC Compass Sensor](#qmc-compass-sensor) | Arduino/ESP32 | Heading calculation using the QMC5883L magnetometer |
| [TF-Mini LiDAR Sensor (UART)](#tf-mini-lidar-sensor) | Arduino/ESP32 | Distance sensing via TF-Mini LiDAR over UART |
| [Ultrasonic Sensor Distance Measurement](#ultrasonic-sensor) | Arduino | Distance measurement with HC-SR04 ultrasonic sensor |
| [General Autonomous Robot Debugging Functions](#debugging-functions) | Arduino/ESP32 | Reusable diagnostic and debugging utility functions |

---

## 🔧 Projects

### Line Follower Robot
Two variants — using 2 and 3 IR sensors respectively. Implements basic differential drive logic to follow a line on a surface. The 3-sensor variant adds a centre sensor for improved straight-line tracking and sharper turn response.

**Key concepts:** Digital IR sensing, differential drive, motor PWM control

---

### Holonomic Drive with PS4 Remote
ESP32-based holonomic (omnidirectional) drive system paired with a PS4 DualShock controller over Bluetooth. Supports forward/reverse, lateral strafing, and rotation via left/right analog sticks and D-pad. Includes solenoid/piston actuator control via shoulder buttons.

**Key concepts:** PS4BT library, holonomic kinematics, analog PWM motor control, Bluetooth pairing

**Hardware:** ESP32, 4× DC motors, motor driver, PS4 controller, solenoid actuator

---

### Robot Odometry
Estimates robot position (x, y) and heading (θ) using three rotary encoders. Useful as a dead-reckoning module for autonomous navigation tasks where GPS or external localisation is unavailable.

**Key concepts:** Encoder interrupt handling, odometry kinematics, pose estimation

---

### QMC Compass Sensor
Reads heading data from the QMC5883L (or HMC5883L-compatible) magnetometer over I²C. Provides calibrated compass bearing for orientation-aware navigation.

**Key concepts:** I²C communication, magnetic declination compensation, heading calculation

---

### TF-Mini LiDAR Sensor
Interfaces with the Benewake TF-Mini LiDAR module over UART to obtain distance measurements. Includes frame parsing and error handling for the 9-byte serial protocol.

**Key concepts:** UART/Serial parsing, LiDAR distance sensing, byte-level protocol handling

---

### Ultrasonic Sensor
Classic HC-SR04 ultrasonic distance measurement using `pulseIn()`. Good reference for obstacle detection and proximity sensing in low-cost setups.

**Key concepts:** Pulse timing, speed-of-sound distance formula, digital I/O

---

### Debugging Functions
A collection of reusable diagnostic helper functions for autonomous robot development — including serial print wrappers, motor test routines, and sensor validation utilities.

**Key concepts:** Modular firmware design, diagnostic logging, test harnesses

---

## 🛠️ Prerequisites

- **Hardware:** Arduino Uno/Mega or ESP32 development board
- **IDE:** [Arduino IDE](https://www.arduino.cc/en/software) (v1.8+) or [PlatformIO](https://platformio.org/)
- **Libraries (install via Library Manager):**
  - `PS4Controller` — for Holonomic Drive project
  - `QMC5883LCompass` — for Compass Sensor project
  - Standard `Wire`, `SoftwareSerial` as needed

---

## 🚀 Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/AdityaTerdalkar/Robotics-Projects.git
   ```
2. Open the desired project file in Arduino IDE.
3. Install any required libraries via **Sketch → Include Library → Manage Libraries**.
4. Select the correct board and port under **Tools**.
5. Upload to your microcontroller.

---

## 👤 Author

**Aditya Terdalkar**
Electronics & Telecommunication Engineering, PVPIT Pune

---

## 📄 License

This repository is open for educational and personal use. Attribution appreciated.
