# 💤 SleepCompanion — Sleep Tracking Module

This module handles **real-time sleep phase tracking** using motion and heart rate data collected from a wearable device.

---

## 📈 Features

Collects accelerometer and heart rate data  
Classifies sleep stages: Awake, Light, REM, Deep  
Applies smoothing/filtering algorithms  
Stores results for long-term trends

---

## ⚙️ How It Works

1. Collects data from the wearable device (e.g., Bangle.js or any BLE sensor).
2. Applies dynamic thresholds or AI models to classify sleep phases.
3. Saves and syncs data to local storage or Firebase.

---

## 🗂️ Files

sleeptracker/
├── appinfo.json
├── sleeptracker.app.js


---

## 🚀 Setup

1. Make sure your wearable device is paired and running.
2. Deploy the `sleeptracker` module to the device.
3. Use BLE services to stream data to the Companion App.

---

## 📝 Requirements

- Compatible BLE-enabled wearable
- Bangle.js SDK (if using Bangle)
- Node.js (for companion integration)

---

## 📄 License

MIT License
