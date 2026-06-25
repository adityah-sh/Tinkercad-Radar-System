# Ultrasonic Radar System Simulation with Audio-Visual Alert Framework

A functional prototype radar system simulated using **Tinkercad**, designed for real-time object detection, continuous $180^\circ$ environmental scanning, and proximity safety tracking.

## 🛠️ Tech Stack & Components
* **Language:** Embedded C++ / Arduino Language
* **Platform:** Tinkercad Simulation Environment
* **Hardware Elements:** Microcontroller (Arduino Uno R3), Ultrasonic Distance Sensor (HC-SR04), Micro Servo Motor, Piezo Buzzer, LED Indicator, Resistors, and Breadboard.

## 🚀 Key Features & Implementation
* **Dynamic 180-Degree Sweep:** Utilizes a servo motor to continuously sweep the ultrasonic sensor from 15° to 165° and back, capturing directional spatial data.
* **Real-Time Distance Extraction:** Processes raw acoustic reflection flight time from the echo pin using optimized mathematical conversions to yield precise obstacle distance metrics in centimeters.
* **Conditional Safety Alert System (`handleAlerts`):** Programmed with threshold safety barriers. Instantly triggers a hardware interrupt loop to light up an LED and sound a 500 Hz tone on a piezo buzzer if any target enters a critical 100cm zone.
* **Latency Optimization:** Written with compact memory overhead and clear structural divisions to keep tracking processing times minimal between the servo adjustments and the sonic ping.

## 📄 Core Algorithm Overview
1. The microcontroller signals the Servo Motor to change its angle position step-by-step.
2. The Ultrasonic Sensor shoots a high-frequency sound wave at each dynamic point.
3. The script captures the duration of the returning echo and runs the distance formula calculation.
4. Proximity status is checked against hardcoded limits, executing synchronous component state changes (LED/Buzzer).
5. Positional coordinates and raw telemetry are parsed and streamed down to the Serial Monitor interface.
