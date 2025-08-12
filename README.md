# Dual-Tenant Energy Monitoring System

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Platform](https://img.shields.io/badge/platform-PlatformIO)](#)
[![Language](https://img.shields.io/badge/language-C/C++-green.svg)](#)

## 📌 Overview
The **Duo Energy Monitoring System** is an **ESP32-based open-source project** designed to measure, monitor, and analyze the energy consumption of connected electrical devices in **real-time**.  
It integrates **PZEM-004T energy meters**, **alert indicators**, **SMS Alert**, and **cloud connectivity** for intelligent data visualization and alerts.

This project aims to provide a **low-cost,transparent, modular, and IoT-ready solution** for households, laboratories, and small-scale industries to track power usage, optimize consumption, and enhance energy efficiency.

---

## 🎯 Features
- **Real-time Energy Monitoring** via PZEM-004T modules (voltage, current, power, energy).
- **ESP32-DevKit Control** running **MicroPython** firmware.
- **LED & Buzzer Alerts** for configurable threshold violations.
- **Modular Code Structure** for easy customization.
- **Cloud Integration** (Wi-Fi, GSM-ready) for remote monitoring.
- **Multi-device Support** via Modbus RTU over RS485.
- **Low Power Consumption** design with sleep mode support.

---

## 📦 Hardware Components
| Component | Description | Qty |
|-----------|-------------|-----|
| ESP32 | Main MCU with Wi-Fi & Bluetooth | 1 |
| PZEM-004T v3.0 | Energy monitoring sensor | 1–2 |
| TTL ↔ UART Converter | Enables multi-drop Modbus RTU | 1 |
| Active Buzzer | Audio alert system | 1 |
| LEDs (Green, Red, Blue) | Status indicators | 3 |
| OLED/LCD Display | Local data visualization | 1 |
| Power Supply | 5V regulated | 1 |

---

## 📂 Project Structure

DUO-EM3/
│
├── main.py # Main script
├── config.py # Configuration & system constants
├── utilities/
│ ├── alert_handler.py # Manages buzzer & LED indicators
│ ├── display_handler.py # LCD/OLED update logic
│ ├── pzem_handler.py # Reads data from PZEM modules
│ └── comms_handler.py # Handles Wi-Fi / GSM communication
├── README.md # Project documentation
└── LICENSE # Open-source license file



---

## ⚙️ Installation & Setup

### 1️⃣ Prerequisites
- Install **[MicroPython](https://micropython.org/)** firmware on ESP32-DevKit.
- Use **Thonny** or **ampy** to upload `.py` scripts.
- Have a configured **PZEM-004T** module connected via **MAX485 RS485 converter**.

### 2️⃣ Hardware Wiring
#### ESP32 ↔ MAX485 ↔ PZEM-004T
| ESP32 Pin | MAX485 Pin | PZEM-004T Pin |
|-----------|------------|--------------|
| GPIO17 (TX) | DI | RX |
| GPIO16 (RX) | RO | TX |
| 5V | VCC | VCC |
| GND | GND | GND |
| DE/RE | GPIO4 | — |

### 3️⃣ Software Setup
```bash
# Clone this repository
git clone https://github.com/username/Duo-EM3.git

# Upload files to ESP32
ampy --port COM3 put main.py
ampy --port COM3 put config.py
ampy --port COM3 put utilities/

🚦 Usage
Power up the ESP32-DevKit and connected sensors.
The system will initialize and start reading data.
Alerts will trigger based on thresholds set in config.py.
Data can be logged locally or sent to the cloud (optional).

🔄 Future Enhancements
Web dashboard for remote monitoring.
AI-based anomaly detection in power usage.
Multi-device MQTT integration.
Battery backup support.

📜 License
This project is licensed under the MIT License – see the LICENSE file for details.

🤝 Contribution
We welcome contributions! Please:
Fork the repository.
Create a new branch: git checkout -b feature/YourFeature.
Commit your changes: git commit -m 'Add new feature'.
Push and open a Pull Request.

📧 Contact
Maintainer: Saviour – Embedded Hardware Designer
📍 Accra, Ghana
✉️ Email: senamdagadusaviour@gmail.com
🔗 GitHub: -------------------------


