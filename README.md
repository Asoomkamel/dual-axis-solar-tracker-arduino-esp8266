# Dual-Axis Solar Tracker with Remote Control

An intelligent, dual-axis solar tracking system designed to maximize energy efficiency by dynamically aligning solar panels with the sun's position. This project integrates **Arduino UNO** for local control, **ESP8266** for Wi-Fi-based remote management, and a custom **Voltage Regulator Circuit** for optimized battery charging.

---

## 📺 Demo Video

Check out the system in action! The video demonstrates both the automatic tracking capability and the manual remote control via the smartphone interface.

https://github.com/Asoomkamel/dual-axis-solar-tracker-arduino-esp8266/raw/main/demo_video.mp4

---

## 🌟 Key Features

*   **Dual-Axis Tracking**: Actively tracks the sun's movement along both horizontal (X-axis) and vertical (Y-axis) directions using 4 LDR sensors.
*   **30% Efficiency Boost**: Generates approximately 30% more energy daily compared to fixed solar panels.
*   **Dual Operation Modes**:
    *   **Automatic Mode**: Uses an LDR-based algorithm for autonomous sun tracking.
    *   **Manual Mode**: Allows remote control via a Wi-Fi-enabled GUI (RemoteXY) using an ESP8266 module.
*   **Integrated Power Management**: Includes a custom voltage regulator circuit (MOSFET/Zener based) to stabilize output for safe battery charging.
*   **IoT Ready**: Features an ESP8266 interface for real-time monitoring and control through a mobile application.

---

## 🛠️ Hardware Components

| Component | Description |
| :--- | :--- |
| **Microcontroller** | Arduino UNO |
| **Connectivity** | ESP8266 Wi-Fi Module |
| **Actuators** | 2x Servo Motors (Horizontal & Vertical) |
| **Sensors** | 4x Light Dependent Resistors (LDRs) |
| **Power System** | 2x Solar Panels (Series for 10V), Custom Regulator (BC547, 2N7000, Zener), Rechargeable Battery |

---

## 📸 Project Gallery

### Physical System Design
The mechanical structure is designed for stability and precision, featuring a dual-axis pivot for full range of motion.

![Solar Tracking System](Solar%20Tracking.png)

### Electronic Design & Simulation
The system includes a precise voltage regulator circuit and an Arduino-based sensor interface.

| Voltage Regulator Circuit | Arduino & ESP8266 Interface |
| :---: | :---: |
| ![Voltage Regulator](Voltage%20Regulator%20Circuit%20.png) | ![Arduino Interface](Screenshot%202026-04-18%20202021.png) |

### Remote Control GUI
The manual control interface developed using RemoteXY, allowing for precise adjustment of both axes via a smartphone.

![RemoteXY GUI](Gui%20Manual%20Solar%20Tracking%20.png)

---

## 💻 Software & Logic

The project includes two primary code segments:
1.  **Automatic Tracking**: Calculates the difference between LDR pairs (Top/Bottom, Left/Right) and adjusts servos to minimize the light intensity difference.
2.  **Manual Remote Control**: Interfaces with the RemoteXY library to receive slider positions over Wi-Fi for manual orientation.

### Key Algorithm Parameters
*   **Tolerance**: 50 (Adjustable sensitivity to light changes)
*   **Delay Time**: 10ms (System responsiveness)
*   **Servo Limits**: Defined to prevent mechanical strain on the structure.

---

## 📂 Repository Structure

*   `demo_video.mp4`: Full demonstration of the system's functionality.
*   `Automatic & Manual Solar-1.pdf`: Comprehensive project report with methodology and results.
*   `Solar Tracking Code.txt`: Source code for both Automatic and Manual modes.
*   `*.png`: High-resolution simulation and system images.

---

## 🚀 Setup & Installation

1.  **Hardware Assembly**: Build the mechanical structure using the provided laser-cutting template (see PDF).
2.  **Circuit Integration**: Connect the LDRs, Servos, and ESP8266 as shown in the interface diagram.
3.  **Firmware**:
    *   Install the `Servo.h` and `RemoteXY.h` libraries in the Arduino IDE.
    *   Upload the desired code (Manual or Automatic) from `Solar Tracking Code.txt`.
4.  **Remote Control**: Configure the RemoteXY mobile app with the credentials specified in the code (`SSID: RemoteXY`, `Pass: 12345678`).

---
*Developed by Osamaa Maaudhah & Mutasim Makin Al-Kamil - Sana'a University (2024)*
