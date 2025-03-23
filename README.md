# DinoBLE-Game
# 🦖 Dino Controller - Arduino + BLE + TinyML + Flutter

Control a Flutter-based Dino Game using jump gestures detected by an Arduino Nano 33 BLE Sense with TinyML and Bluetooth Low Energy.

## 🔧 Tech Stack
- **Arduino Nano 33 BLE Sense**
- **TensorFlow Lite for Microcontrollers**
- **Flutter** (for mobile game)
- **BLE (Bluetooth Low Energy)** communication
- **Python** for model training

## 📁 Project Structure
DinoController/
│
├── arduino/
│   ├── DinoController.ino
│   ├── model.h
│   └── README.md      
│
├── flutter_app/
│   ├── lib/
│   │   └── main.dart   ← Your Flutter code
│   └── README.md       ← Optional (explain Flutter side)
│
├── data/
│   ├── idle.csv
│   ├── jump.csv
│   └── model_training.ipynb  ← Python script or notebook to train & export model
│
└── README.md           ← Main project readme


## 🚀 How It Works
1. IMU reads acceleration data.
2. A trained TinyML model detects "jump" gestures.
3. On detection, Arduino sends "1" via BLE.
4. Flutter app receives signal and makes the Dino jump.

## 🧠 Model Training
See `data/model_training.ipynb` to:
- Load `idle.csv` and `jump.csv`
- Train a lightweight model
- Export to `model.tflite` and convert to `model.h`

## 🔌 Setup
### Arduino
- Upload `arduino/DinoController.ino` with `model.h`
- Monitor BLE output for gesture detection

### Flutter App
- Pair with Arduino over BLE
- Jump signal triggers Dino jump 🦖

## 🙌 Contributors
- Yashmitha Ramesh <a href=https://github.com/YASHMITHA-3>
- Nishma Nair
- Riteesh Ram Chander Bollavaram Golla 
