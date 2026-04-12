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
![tableopen](https://github.com/user-attachments/assets/20bb7c28-d9a5-439c-acc4-0ec342681049)
<img width="1091" height="700" alt="tableclode" src="https://github.com/user-attachments/assets/4877eb44-01be-4054-83da-f8ccb4ab23b2" />
![last](https://github.com/user-attachments/assets/34708ba0-b20e-402b-907a-70089b97281d)
![1](https://github.com/user-attachments/assets/86699231-e373-46c9-b9b7-da4e093c03c0)
![2](https://github.com/user-attachments/assets/c7d667cd-b7f6-4f46-936b-def0ea22bb39)
![3](https://github.com/user-attachments/assets/64674867-4509-4722-943c-e29b9bb435dc)
![4](https://github.com/user-attachments/assets/9c3db8e6-6cae-43ac-a56b-0ad9b604fd33)
![5](https://github.com/user-attachments/assets/365c0601-4a97-4665-9774-15362eb727ae)
![full](https://github.com/user-attachments/assets/9442b2e9-410e-4d08-b6eb-e36fbf8d964b)

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
