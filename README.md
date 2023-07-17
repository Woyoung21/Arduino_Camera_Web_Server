# Arduino_Camera_Web_Server

This repository contains an example application for an ESP32-based camera server. The program configures the ESP32 to capture images using a camera module, and then serves those images over WiFi.

This application uses the ESP32's integrated WiFi capabilities and PSRAM. When a user connects to the ESP32's IP address, they will be able to see the images captured by the camera.

Please note that this application requires an ESP32 board with PSRAM (such as the ESP32 Wrover Kit), as the UXGA resolution and high JPEG quality settings require a lot of memory.

# Requirements
Freenove ESP32 WROVER Board
Camera module compatible with the ESP32 board
Arduino IDE version 1.8.16

# Dependencies
esp_camera.h: This library is used to interact with the camera module.
WiFi.h: This library is used to establish a WiFi connection.
camera_pins.h: This file should define the pins used by the camera module.
Setup
Camera Model
The camera model used must be defined at the start of the script. Please uncomment the line that corresponds to your camera model.

# MAC Address Spoofing (Optional)
This script includes commented out code that can be used to spoof the ESP32's MAC address. If you wish to use this functionality, uncomment the relevant code and replace CustomMACaddress with the desired MAC address.

# WiFi Credentials
Replace the ssid and password variables with your WiFi credentials.

# Usage
Upload the sketch to your ESP32 board using the Arduino IDE. Once the board is powered on, it will start the camera server and connect to the WiFi network. You can then connect to the ESP32's IP address to view the images captured by the camera.

The loop function in this sketch does not contain any functionality as everything is handled in separate tasks by the web server.

# Troubleshooting
If the camera fails to initialize, the error code will be printed to the Serial Monitor. Please refer to the ESP32 Camera library documentation for more information on what these codes mean.

# Contributing
If you'd like to contribute, please fork the repository and make changes as you'd like. Pull requests are warmly welcome.

# License
MIT license applies.

