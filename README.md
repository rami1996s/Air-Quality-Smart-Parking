# Air Quality Monitoring System in Smart Parking

implemented with Hussein Mohammad in 2024

This project combines **vehicle detection** and **air quality monitoring** in a smart parking environment. It uses an ESP32 microcontroller to control a gate, fan, and sensors while communicating with a mobile app and Node-RED dashboard via MQTT.

## System Features

- Detects car movement using PIR sensors
- Automatically opens/closes gate using servo motor
- Monitors CO and smoke levels using MQ-2 sensor
- Controls fan automatically or manually
- Displays status in Node-RED dashboard and Android app

## Hardware Components

- ESP32
- PIR Sensors
- MQ-2 Gas Sensor
- Servo Motor
- 12V Fan
- LED
- Push Button

## Communication
Technologies Used

Frontend: Flutter

Backend: ESP32 Microcontroller, Arduino IDE (C++)

Communication: MQTT (HiveMQ Broker used in example)

Sensors: MQ-135 Gas Sensor, PIR Sensor(s)

System Architecture
The Flutter app subscribes to MQTT topics published by the ESP32 to receive sensor data and status updates. It also publishes messages to control the fan and door.

Arduino Code (ESP32)
The Arduino code manages the sensors, actuators, and MQTT communication. Key features include:

Sensor Reading: Reads data from the MQ-135 and PIR sensors.

MQTT Publishing: Publishes sensor readings and status updates to MQTT topics.

MQTT Subscribing: Subscribes to control topics for manual fan control.

Actuator Control: Controls the relay (fan) and servo motor (door) based on sensor readings and user commands.

Automatic/Manual Fan Control: Allows switching between automatic (sensor-based) and manual fan control.

For Arduino Code (look for attached file: arduino_code.cpp)

Flutter Code (Highlights)
The Flutter code provides the user interface and handles MQTT communication. Key features include:

MQTT Client: Uses the mqtt_client package to connect to the MQTT broker. Real-time Data Display: Displays sensor readings and status information. User Interaction: Allows users to manually control the fan and door. Air Quality Visualization: Provides visual cues indicating good or poor air quality.

Setup and Installation
Install Arduino IDE: Download and install the Arduino IDE from https://www.arduino.cc/.

Install Libraries: Install the necessary Arduino libraries (PubSubClient, ESP32Servo, MQUnifiedsensor).

Configure WiFi and MQTT: Update the Arduino code with your WiFi credentials and MQTT broker details.

Install Flutter: Download and install Flutter from https://flutter.dev/.

Install Dependencies: Run flutter pub get to install the Flutter dependencies.

Run the Application: Run the Flutter app on your device or emulator.
Contributing

## Files Included

- `Arduino_Code/air_quality_code.ino`: Source code written for Arduino IDE.
- `presentation/IOT_Project.pptx`: Project presentation slides.
- `.gitignore`: Files to be excluded from version control.
- `README.md`: You’re reading it!

## Future Work

- Improve UI of mobile application
- Add historical logging of air quality data
- Extend integration into a smart city framework

