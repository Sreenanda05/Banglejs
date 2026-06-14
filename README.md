# DreamPulse — Bangle.js Watch Firmware

Real-time sleep stage classification running on the Bangle.js 2 
smartwatch. Part of the DreamPulse sleep tracking system built 
at the Ubiquitous Systems Lab, University of Siegen (2025).

## What it does
- Reads heart rate (HRM) and motion (accelerometer) from watch sensors
- Applies low-pass filtering and sliding window smoothing for noise reduction
- Classifies sleep into 4 stages every second: Awake / Light / REM / Deep
- Dynamically adjusts detection thresholds every 60 seconds
- Transmits live data to companion app via BLE (Nordic UART Service)
- Saves sleep history locally to watch storage

## Files
| File | Description |
|------|-------------|
| `sleeptracker_watch.js` | Main watch firmware (Espruino JavaScript) |
| `appinfo.json` | Bangle.js app metadata |

## How to install on Bangle.js 2
1. Open [Espruino Web IDE](https://espruino.com/ide)
2. Connect your Bangle.js 2 via Web Bluetooth
3. Upload `sleeptracker_watch.js`

## System Architecture

[Bangle.js 2 Watch]
├── HRM Sensor → Heart Rate
└── Accelerometer → Motion
↓
Signal Processing
(Low-pass filter + Sliding window)
↓
Sleep Classification
(Awake / Light / REM / Deep)
↓
BLE Nordic UART
↓
[React Native Companion App]

## Tech Stack
- **Language:** JavaScript (Espruino runtime)
- **Hardware:** Bangle.js 2 smartwatch
- **Communication:** BLE — Nordic UART Service (NUS)
- **Signal processing:** Low-pass filter, sliding window average
- **Classification:** Rule-based scoring algorithm

## Companion App
👉 [DreamPulse React Native App](https://github.com/Sreenanda05/Sleeptrack)

## Author
Sreenanda Manikandan
M.Sc. Applied Computer Science (Embedded Systems)
University of Siegen, Germany
