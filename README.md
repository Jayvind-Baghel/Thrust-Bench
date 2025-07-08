# 🚀 Thrust Measurement Bench
<ins> *by Jayvind, Maitreya, Om, Sahil* </ins>

This project showcases a **wireless thrust measurement system** for BLDC motors using an **ESP32 microcontroller**, **load cell with HX711**, and **web-based interface**. It allows remote control of motor throttle and real-time monitoring of generated thrust through any Wi-Fi-enabled device.

<img src="https://github.com/user-attachments/assets/6a0ae2a2-2bdb-4fc4-81e3-3f4bd0df844d" alt="Circuit Diagram" width="300"/>

## 📽️ Demo Videos
- [Web Control Interface](https://drive.google.com/file/d/13VkjJ6KgbWr46ZEnIpFhb0-TNKEIvEUk/view?usp=sharing)
- [Thrust Bench Demonstration](https://drive.google.com/file/d/1V0klxTG0ecIqba6FCgYzNDWVHw7kRkY_/view?usp=sharing)

---

## 📝 Features
- **Motor Throttle Control:** Adjust motor speed remotely via web.
- **Thrust Measurement:** Real-time thrust display using load cell.
- **ESC Calibration:** Initial calibration ensures accurate motor control.
- **Load Cell Calibration:** Ensures precise thrust readings.
- **Persistent Storage:** Calibration values saved in EEPROM.
- **Responsive Web Interface:** Mobile and PC friendly.

---

## 🛠 Hardware Used
- ESP32 WROOM Module
- HX711 Load Cell Amplifier Module
- Load Cell Sensor
- BLDC Motor + ESC (Electronic Speed Controller)
- Power Supply (as per motor specs)
- Basic electronic components (resistors, jumpers, etc.)

---

## 💻 Software and Libraries
- **Arduino IDE**
- Libraries:
  - `WiFi.h` (for web server)
  - `ESP32Servo.h` (for ESC control)
  - `HX711_ADC.h` (for load cell interfacing)
  - `EEPROM.h` (for storing calibration values)

---

## 🚦 How It Works

1. **Load Cell Calibration:**
   - Calibrates HX711 + Load Cell.
   - Allows dynamic tare and calibration through serial commands.

2. **Final Integrated Code:**
   - Combines motor control and thrust measurement.
   - Creates a Wi-Fi hotspot.
   - Hosts a webpage to control motor speed and view thrust.
   - Calibration values stored in EEPROM for persistence.

---

## 🌐 Web Interface
- Adjustable slider to control motor throttle (0% - 100%).
- Real-time thrust display in grams.
- Simple and responsive HTML/JavaScript frontend served by ESP32.

---

## 📋 Installation & Setup

1. Install **Arduino IDE** and required libraries:
   ```bash
   ESP32Servo
   HX711_ADC
   WiFi
   EEPROM

2. Upload the codes in sequence for

   First upload Load Cell Calibration code and calibrate the load cell with known weight. Default Load Cell Calibration Factor: 108.0 (adjustable in code) for our load cell.
   Then upload Final Integrated Control code. 

3. Connect to ESP32 Wi-Fi network with your own credentials.

4. Access the web interface via the displayed IP address (Serial Monitor).
