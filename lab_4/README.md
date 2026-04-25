# ESP32 Wi-Fi SoftAP Example

This example demonstrates how to configure an ESP32 device as a **Soft Access Point (SoftAP)**, allowing other devices (smartphones, laptops) to connect directly to it.

## Features
* **Access Point Mode**: Serves as a Wi-Fi hotspot.
* **DHCP Server**: Automatically assigns IP addresses to connected stations (default gateway: `192.168.4.1`).
* **Security**: Supports WPA2-PSK and Protected Management Frames (PMF).

## Project Configuration
1.  Open the configuration menu: `idf.py menuconfig`.
2.  Navigate to **Example Configuration**.
3.  Set your desired **WiFi SSID** and **WiFi Password** (minimum 8 characters).
4.  Optional: Adjust the **WiFi Channel** and **Max Connections**.

## Build and Flash
To build, flash, and monitor the project in one command:
```bash
idf.py -p PORT flash monitor