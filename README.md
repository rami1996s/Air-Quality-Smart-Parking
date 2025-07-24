# Air-Quality-Smart-Parking
Smart parking system with CO/smoke detection, automated gate control, and MQTT-based remote monitoring using ESP32.
implemented with Hussein Mohammad.

# Air Quality Monitoring System in Smart Parking

This project integrates **smart parking control** with **air quality monitoring**, aimed at improving parking management efficiency and environmental conditions in indoor/outdoor facilities.

##  Project Objectives

- Detect vehicle entry and exit using PIR sensors.
- Automate gate control using a servo motor.
- Monitor CO and smoke levels using an MQ-2 gas sensor.
- Activate ventilation (fan) based on air quality thresholds.
- Enable real-time monitoring and manual control via:
  - **Node-RED Dashboard**
  - **Android Mobile App**

## Components Used

- **ESP32** – main microcontroller
- **PIR Sensors** – motion detection at entry/exit
- **Servo Motor** – gate control
- **12V Fan** – air ventilation
- **MQ-2 Sensor** – smoke and CO detection
- **LED** – status indicator
- **Android App** – remote control
- **Node-RED** – for MQTT integration and dashboard

##  System Architecture

- ESP32 communicates with Node-RED using **MQTT**.
- Topics:
  - Subscriptions: `door/status`, `co/level`, `smoke/level`, `fan/status`
  - Publications: `control/fan`, `control/fan/manual`

##  Operation Logic

- **PIR Sensors** detect cars → Gate opens → LED on.
- **MQ-2 Sensor** checks air:
  - If CO ≥ 35 or Smoke ≥ 12 → Fan turns ON.
- **Manual override** via dashboard or app.
- Live data on Node-RED dashboard.

##  Results

- Serial Monitor for debugging and sensor readings.
- Functional Node-RED Dashboard.
- Android app with fan control features.

##  Files Included

- `Arduino_Code/` – source code for ESP32 (Arduino IDE)
- `presentation/` – project presentation slides
- `images/` – optional: add circuit diagrams or photos
- `README.md` – this file

##  Future Improvements

- Improve Android app UI/UX
- Add air quality data logging
- Integrate with city-wide smart systems

##  License

This project is open source under the MIT License.

