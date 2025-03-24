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
<img width="640" alt="image" src="https://github.com/user-attachments/assets/e792b145-966f-45c0-9b43-acd508eab3d2" />

DinoController/
│
├── arduino/
│   ├── DinoController.ino
│   ├── model.h
│   └── README.md   
│
├── flutter_app/dino_ble
│   ├── lib/
│   │    ├── main.dart
│   │    ├── trex_widget.dart
│   │    ├── player.dart
│   │    ├── game_over.dart
│   │    ├── trex_game.dart
│   │    └── trex_widget.dart
│   │    
|   ├── pubspec.yaml
│   │  
│   └── README.md       
│
├── data/
│   ├── idle.csv
│   ├── jump.csv
│   └── model_training.ipynb  
│     
└── README.md               


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
- Also download <a href=https://github.com/tensorflow/tflite-micro-arduino-examples>https://github.com/tensorflow/tflite-micro-arduino-examples</a>

### Flutter App
- Pair with Arduino over BLE
- Jump signal triggers Dino jump 🦖

## 🙌 Contributors
- <a href=https://github.com/YASHMITHA-3>Yashmitha Ramesh</a>
- <a href=https://github.com/nishmanair>Nishma Nair</a> 
- <a href=https://github.com/riteesh-ram>Riteesh Ram Chander Bollavaram Golla </a>
 
## Downloads
- 👉 [Download APK](https://github.com/YASHMITHA-3/DinoBLE-Game/releases/tag/v1.0#:~:text=3-,app%2Drelease.apk,-16.6%20MB)
