# 🏥 Smart Healthcare Monitoring System (ESP32 + MQTT)

A real-time **IoT-based healthcare monitoring system** using **ESP32 and MQTT** to track vital parameters like heart rate, SpO₂, body temperature, height, and blood pressure.

---

## 🚀 Features

* ❤️ Heart Rate Monitoring (MAX30102)
* 🩸 SpO₂ Measurement
* 🌡 Body Temperature (MLX90614)
* 📏 Height Measurement (Ultrasonic Sensor)
* 🩺 Blood Pressure (UART-based module)
* 📺 OLED Display for real-time data
* 🌐 WiFi connectivity using ESP32
* 📡 MQTT data transmission to server/dashboard

---

## 🏗️ System Architecture

<p align="center">
  <img src="https://github.com/user-attachments/assets/42536d82-94a4-4c2c-876e-4f29203aee86" width="400"/>
</p>

<p align="center">
  <img src="https://github.com/user-attachments/assets/da9a331c-de9e-427d-b1cc-d249a347df50" width="400"/>
</p>

---

## 📊 Parameters Measured

| Parameter        | Sensor Used       |
| ---------------- | ----------------- |
| Heart Rate (HR)  | MAX30102          |
| SpO₂             | MAX30102          |
| Body Temperature | MLX90614          |
| Height           | Ultrasonic Sensor |
| Blood Pressure   | UART BP Sensor    |

---

## 📡 MQTT Topics

```text
health/spo2
health/hr
health/temp
health/height
health/sys
health/dia
health/pulse
```

---

## ⚙️ Hardware Requirements

* ESP32 / ESP32-S3
* MAX30102 Pulse Oximeter Sensor
* MLX90614 IR Temperature Sensor
* Ultrasonic Sensor (HC-SR04 or similar)
* Blood Pressure Sensor (UART-based)
* OLED Display (SH1106)
* Connecting wires & power supply

---

## 🛠️ Software Requirements

* Arduino IDE / PlatformIO
* Required Libraries:

  * WiFi.h
  * PubSubClient.h
  * Wire.h
  * Adafruit_GFX
  * Adafruit_SH110X
  * DFRobot_BloodOxygen_S
  * DFRobot_MLX90614

---

## 🔌 Setup Instructions

1. Clone the repository:

   ```bash
   git clone git@github.com:MOHAMMADIKRAM03/-Smart-Healthcare-Monitoring-System-.git
   ```

2. Open the project in Arduino IDE

3. Update WiFi credentials:

   ```cpp
   const char* ssid = "YOUR_WIFI";
   const char* password = "YOUR_PASSWORD";
   ```

4. Set MQTT broker:

   ```cpp
   const char* mqtt_server = "YOUR_BROKER_IP";
   ```

5. Connect all sensors properly

6. Upload code to ESP32

7. Open Serial Monitor to verify data

---

## 📺 OLED Display Output

Displays:

* HR & SpO₂
* Temperature
* Height
* Blood Pressure

---

## 📤 MQTT Data Example

```text
health/spo2 → 98
health/hr → 75
health/temp → 36.5
health/height → 170
health/sys → 120
health/dia → 80
health/pulse → 72
```

---

## 🔍 Debugging

Check Serial Monitor:

```text
Connecting WiFi...
MQTT connecting...
------DATA------
SpO2: 98
HR: 75
Temp: 36.5
```

---

## 📈 Future Enhancements

* 📊 Node-RED Dashboard
* ☁ Cloud storage (Firebase / AWS)
* 📱 Mobile App integration
* 🚨 Health alerts & notifications
* 🧠 AI-based health analysis

---

## 👨‍💻 Author

**Mohammad Ikram**
IoT Developer | Embedded Systems Enthusiast

---

## ⭐ Notes

* Uses MQTT for lightweight real-time communication
* Designed for scalability and remote monitoring
* Suitable for hospitals, clinics, and home healthcare

---
