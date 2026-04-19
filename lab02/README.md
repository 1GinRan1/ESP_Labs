# Laboratory Work №2: MQTT Communication with ESP32-S3

This project demonstrates the implementation of the MQTT protocol on an ESP32-S3 microcontroller to exchange JSON data with a local broker.

## Prerequisites

* **Hardware:** ESP32-S3 (with built-in RGB LED on GPIO 48 and BOOT button on GPIO 0).
* **Tools:** VS Code + ESP-IDF Extension, MQTT.fx, and Mosquitto Broker.

## Project Setup

1. **Configure MQTT Broker:**
   - Install **Mosquitto** on your PC.
   - Create a `mosquitto_my_cfg.conf` file with:
     ```conf
     listener 1883
     allow_anonymous true
     ```
   - Start the broker: `mosquitto.exe -v -c mosquitto_my_cfg.conf`.

2. **Configure ESP32 Project:**
   - Open the project in VS Code.
   - Open **Menuconfig** (`Ctrl+Shift+P` -> `SDK Configuration Editor`):
     - **Example Connection Configuration:** Set your WiFi SSID and Password.
     - **Example Configuration:** Set **Broker URL** to `mqtt://your_pc_ip_address`.
   - Add dependencies (if needed): `idf.py add-dependency "espressif/led_strip^3.0.0"`.

3. **Build and Flash:**
   - Build the project (`Build`).
   - Flash to the device (`Flash`).
   - Open the serial monitor (`Monitor`).

## How to Test

### 1. Button Event (Publish)
* In **MQTT.fx**, subscribe to the topic: `/Meshko/button_event`.
* Press the **BOOT** button on the ESP32.
* You will receive a JSON message: `{"event": "button_pressed", "user": "Meshko", "uptime": ...}`.

### 2. LED Control (Subscribe)
* In **MQTT.fx**, publish a JSON message to the topic: `/Meshko/led_control`.
* **Example Payload:** ```json
  {"r": 255, "g": 0, "b": 0}