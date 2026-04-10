# ESP-IDF IoT Labs

Welcome! This is the repository for laboratory work from the "Internet of Things" (IoT) course, based on ESP32 microcontrollers.

## Repository Structure

This repository is organized by the principle **"one branch per lab"**.

* The **`main`** branch (this branch) is "clean". It contains only this `README.md` file and a global `.gitignore`.
* Each laboratory assignment (`lab01`, `lab02`, etc.) is located in its **own separate branch** with the corresponding name.
* Within each branch (e.g., `lab01`), you will find a complete ESP-IDF project structure ready to be opened in VS Code.

## Tools Used

* **IDE:** Visual Studio Code with the ESP-IDF Extension
* **Framework:** ESP-IDF (Espressif IoT Development Framework)
* **Hardware:** ESP32 / ESP32-S3 Development Boards
* **Version Control:** Git

---

## General Build and Flash Instructions

### Step 1: Get the Lab Code

1.  Clone this repository (if you haven't already):
    ```bash
    git clone https://github.com/1GinRan1/ESP_Labs.git
    cd ESP_Labs
    ```
    *(Note: update the repository URL if you changed the repository name)*

2.  Check out the branch for the lab you want to run. For example, for Lab 1:
    ```bash
    git checkout lab01
    ```

### Step 2: Open the Project in VS Code

1.  Open **Visual Studio Code**.
2.  Open the folder of the specific lab project (the folder containing the `CMakeLists.txt` file and the `main` directory).
3.  Ensure your **ESP-IDF extension** is properly configured and the correct framework version is selected.

### Step 3: Configure, Build, and Flash

1.  **Set the Target (Microcontroller):**
    * Press `Ctrl+Shift+P` to open the Command Palette.
    * Type and select `ESP-IDF: Set Espressif device target`.
    * Choose your specific board (e.g., `esp32s3`).

2.  **Select the Serial Port:**
    * Press `Ctrl+Shift+P` -> `ESP-IDF: Select port to use (COM, tty, usbserial)`.
    * Select the COM port your ESP32 is connected to.

3.  **Build the Project:**
    * Click the **Build** icon (Hammer) on the ESP-IDF bottom toolbar, or run the command `ESP-IDF: Build your project`.
    * Wait for the "Project build complete" message.

4.  **Flash and Monitor:**
    * Click the **Flash** icon (Lightning bolt) to upload the firmware to the board.
    * Click the **Monitor** icon (Screen) to open the Serial Monitor and view the application's output in real-time.
