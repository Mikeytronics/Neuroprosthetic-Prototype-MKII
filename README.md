# Neuroprosthetic-Prototype-MKII
A prosthetic prototype utilizing EMG from a 3D printed frame

## Overview
The **Neuroprosthetic Prototype MkII** is a functional proof-of-concept for a compact, 3D-printed myoelectric prosthetic hand controlled via surface EMG (Electromyography) signals. The device is built using low-cost, accessible components and is designed to explore control strategies, signal processing, and user interaction through bio-signals.

## Features
- 🦾 **2-Servo Finger Control** – Drives a pair of fingers using myoelectric inputs.
- 🧠 **EMG Signal Processing** – Incorporates the AD8232 heart rate monitor module to capture EMG signals from muscle activity.
- 🔧 **Custom Arduino EMG Filter Shield** – Designed to reduce noise and enhance signal clarity.
- 🖐️ **3D-Printed Frame** – Lightweight and fully customizable mechanical structure.
- 🕹️ **Potentiometer + Button Interface** – For calibration, manual override, or testing.
- 📟 **OLED Display** – Displays live system status and force or signal indicators.

## Hardware Components
- **Microcontroller**: Arduino (Uno/Nano/etc.)
- **EMG Module**: SparkFun AD8232
- **Display**: 128x64 OLED
- **Servos**: 2x 20–25kg rated servo motors
- **User Inputs**: 10k potentiometer, tactile button
- **Signal Processing**: Custom filtering shield (NE5532 op-amp based)
- **Frame**: Custom 3D-printed parts

## Software & Firmware
The firmware reads analog EMG data, processes it through a software filter, and maps signal thresholds to servo positions for finger motion. It also displays relevant status messages or data on the OLED for debugging or monitoring purposes.

### Features:
- 📈 Real-time signal filtering
- 🎛️ Threshold-based actuation
- 📟 OLED UI display of signal magnitude or function
- 📶 Potentiometer-based sensitivity tuning

## How It Works
1. EMG signal is captured via electrodes and amplified by the AD8232.
2. The signal is cleaned by a custom Arduino shield with analog filtering.
3. The Arduino processes the signal and determines whether it exceeds the activation threshold.
4. If triggered, it drives the servo motors to flex or release the fingers.
5. OLED shows data (signal value, motor state, etc.) for user feedback.

## Use Cases
- Research into myoelectric prosthetic control
- Educational demos for biomedical signal processing
- Proof of concept for future full-hand neuroprosthetics

## Future Work
- Add more servos for full hand articulation
- Integrate Bluetooth for wireless control or logging
- Improve signal quality via differential EMG
- Replace potentiometer/button with gesture or AI classifier
- Add haptic feedback and force sensors

## Getting Started
1. Clone this repo
2. Open the `.ino` file in Arduino IDE
3. Connect your hardware according to the schematic
4. Upload the code to your Arduino
5. Adjust thresholds and calibration as needed using the potentiometer

## License
This project is open-source under the MIT License. You are free to use, modify, and distribute the code and design with proper attribution.
