# Smart Energy Monitoring System

A **low-cost, intelligent energy monitoring device** built using the **Duo-EM3**.  
The system provides real-time insights into power usage, enabling users to **monitor, analyze, and optimize** their energy consumption through **local display** and **remote access**.

---

## 📌 Features

- **Real-Time Energy Monitoring**  
  Measure voltage, current, power, and energy usage using PZEM-004T modules.

- **Dual-Channel Support**  
  Monitor two independent devices simultaneously through a single **Dou-EM3**

- **Data Logging & Analytics**  
  Store readings locally and process them for trend analysis and predictions.

- **Alerts & Notifications**  
  Visual indicators and audible alerts for abnormal/normal power conditions.

- **Cloud & GSM Integration**  
  Send live data to IoT platforms for remote access and control.

- **Energy Efficiency Optimization**  
  Identify energy wastage patterns and suggest actions to reduce costs.

---

## 🛠️ Hardware Components

| Component                            | Description                                  |
|---------------------------------------|----------------------------------------------|
| **ESP32 **                      | Main microcontroller with Wi-Fi & Bluetooth |
| **PZEM-004T Energy Monitor**          | Measures voltage, current, power, and energy |
| **Gsm module**                        | Enables sms alert system for Users           |
| **LCD Display (I2C)**                  | Displays live readings locally              |
| **Buzzer**                            | Audible alerts                               |
| **LED Indicators**                    | Status and alert signals                     |
| **Power Supply Module**               | Powers the ESP32 and peripherals             |

---

## 📂 Project Structure

project/
├── main.py              # Orchestration only
├── config.py            # Central configuration
└── modules/
   ├── pzem_handler.py    # Reads PZEM-004T sensors
   ├── display_handler.py # Manages LCD output
   ├── gsm_handler.py     # GSM communication
   ├── rtc_handler.py     # DS3231 timekeeping
   └── alert_handler.py   # Alerts and indicators



