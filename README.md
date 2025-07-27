# Air Quality Monitoring System in Smart Parking

implemented with Hussein Mohammad

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

- **MQTT Protocol**
  - `door/status`
  - `co/level`
  - `smoke/level`
  - `fan/status`
  - `control/fan`
  - `control/fan/manual`

## Files Included

- `Arduino_Code/air_quality_code.ino`: Source code written for Arduino IDE.
- `presentation/IOT_Project.pptx`: Project presentation slides.
- `.gitignore`: Files to be excluded from version control.
- `README.md`: You’re reading it!

## Future Work

- Improve UI of mobile application
- Add historical logging of air quality data
- Extend integration into a smart city framework

## License

This project is licensed under the MIT License.
