# ESP RainMaker: LED Light Example

This project demonstrates a smart lightbulb built with **ESP RainMaker**, featuring physical control, mobile app integration, and a command-response framework.

## Core Features
* **Smart Control**: Manage Hue, Saturation, and Brightness via the cloud.
* **Physical Interaction**: Use the **BOOT button** to toggle power locally; state changes sync with the app in real-time.
* **Factory Reset**: Press and hold the BOOT button for **>3 seconds** to reset Wi-Fi and provisioning settings.

## Command-Response Framework
This example includes a demonstration of the command-response system:
* **Custom Commands**: Supports direct JSON commands (e.g., `{"brightness": 50}`).
* **Independent Logic**: Handles cloud requests separately from standard parameter updates for consistent device state.
* **CLI Support**: Advanced debugging and control using the **RainMaker CLI**.

## Get Started
1.  **Build & Flash**: Follow the [ESP RainMaker Documentation](https://rainmaker.espressif.com/docs/get-started.html).
2.  **Provisioning**: Scan the **QR code** generated in the serial monitor using the RainMaker app.
3.  **App Download**:
    * [Android Play Store](https://play.google.com/store/apps/details?id=com.espressif.rainmaker)
    * [iOS App Store](https://apps.apple.com/us/app/esp-rainmaker/id1497491540?l=)

