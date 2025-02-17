🚗 Real-Time Vehicle Detection and Adaptive Headlight System 💡

An ESP32-based IoT solution that dynamically adjusts vehicle headlights using real-time sensor data to improve road safety.

Project Banner (Replace with an actual image of your project)
🌟 Overview

This project enhances vehicle safety by detecting oncoming traffic, fog, and road conditions to automatically adjust the headlight brightness and beam mode. The ESP32 microcontroller processes sensor data and integrates with ThingSpeak for cloud monitoring and Twilio for emergency SMS alerts.
🎯 Features

✅ Vehicle Detection: Ultrasonic sensor detects oncoming vehicles and adjusts headlights.
✅ Adaptive Headlights: LDR & fog sensors control brightness based on ambient light and weather.
✅ Emergency Alerts: Flame sensor detects fire hazards and sends SMS alerts via Twilio.
✅ Cloud Monitoring: Sensor data is uploaded to ThingSpeak for real-time tracking.
✅ Web-Based Control: A remote control interface allows manual and automatic mode switching.
🛠️ Hardware Components
Component	Function
ESP32	Central controller for processing and connectivity
Ultrasonic Sensor (HC-SR04)	Detects distance to vehicles/obstacles
LDR	Measures ambient light levels
DHT11	Monitors temperature and humidity for fog detection
LM393 Sensor	Adjusts LED brightness dynamically
Flame Sensor	Detects fire hazards
Buzzer	Provides audible alerts in case of emergency
L298N Motor Driver	Controls servo motor for beam adjustment
OLED Display	Displays system status and sensor data
🖥️ Software & Communication

    ESP32 Programming: C++ (Arduino Framework)
    Web Interface: HTML, JavaScript (for remote control)
    Cloud Services: ThingSpeak (sensor data monitoring)
    Communication Protocols: I2C (OLED), PWM (LEDs & motors), HTTP (ThingSpeak & Twilio)
    Alert System: Twilio API for SMS notifications

📷 System Block Diagram

(Include a diagram of your hardware connections here!)
🔧 Installation & Setup
1️⃣ Hardware Connections

Connect the ESP32 and components as per the circuit diagram.
2️⃣ Install Required Libraries

In Arduino IDE, install the following:

WiFi.h
WebServer.h
Adafruit_Sensor.h
DHT.h
Adafruit_SSD1306.h
Wire.h
ArduinoJson.h
Base64.h

3️⃣ Update Configuration

Modify config.h with your WiFi and Twilio credentials:

const char* ssid = "YOUR_WIFI_SSID";
const char* password = "YOUR_WIFI_PASSWORD";
const char* twilioSID = "YOUR_TWILIO_ACCOUNT_SID";
const char* twilioToken = "YOUR_TWILIO_AUTH_TOKEN";
const char* twilioFrom = "YOUR_TWILIO_PHONE_NUMBER";
const char* twilioTo = "RECIPIENT_PHONE_NUMBER";

4️⃣ Upload the Code

    Open ESP32_Adaptive_Headlight.ino in Arduino IDE.
    Select the correct Board (ESP32 Dev Module) and Port.
    Upload the code.

5️⃣ Monitor & Control

    Open the Serial Monitor (115200 baud rate) to debug.
    Access the Web Interface via ESP32’s IP (shown in Serial Monitor).
    Check ThingSpeak Dashboard for real-time sensor data.

🚀 Working Principle

    Vehicle & Obstacle Detection: Ultrasonic sensor detects distance, adjusts headlight beam.
    Brightness Adjustment: LDR and fog sensor modify LED intensity based on conditions.
    Fire Detection: Flame sensor triggers buzzer & sends SMS alerts via Twilio.
    Remote Control: Web-based interface allows switching between manual & automatic mode.
    Cloud Monitoring: ThingSpeak logs sensor data for real-time tracking.

📸 Project Demonstration

(Add images/videos of your working project!)
📌 Future Improvements

🔹 Implement AI/ML for predictive traffic analysis.
🔹 Add GPS for location-based lighting adjustments.
🔹 Extend to automated traffic signaling for smart cities.
🤝 Contributors

👨‍💻 Priyanshu Singh - GitHub
📝 License

This project is licensed under the MIT License 
