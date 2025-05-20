# 💤 Driver Drowsiness Detection System 🚗🔔

A real-time **Driver Drowsiness Detection System** that uses **Computer Vision** and **Deep Learning** to monitor the driver’s eye state. When drowsiness is detected (eyes closed for a threshold duration), the system triggers a **buzzer alert** and **stops the vehicle motor** using an **Arduino** connected through serial communication.

---

## 🎯 Objective

To enhance road safety by preventing accidents caused due to driver fatigue or drowsiness by:

- Monitoring eye activity via webcam
- Classifying eye state using a trained CNN model
- Alerting the driver via buzzer
- Automatically stopping the vehicle motor via Arduino when drowsiness is detected

---

## 🚀 Features

- Real-time webcam-based eye tracking
- CNN model to classify open vs closed eyes
- Integration with Arduino to activate buzzer and motor
- Audio and motor alert system for enhanced safety
- Lightweight and suitable for embedded applications

---

## 🛠️ Technologies Used

- Python
- OpenCV
- TensorFlow / Keras
- NumPy
- Arduino (with C/C++ for microcontroller)
- PySerial (for serial communication)

---

## 📁 Project Structure

```
Driver-Drowsiness-Detection/
│
├── dataset/               # Eye state image dataset (open/closed)
├── model/                 # Trained CNN model and weights
├── src/                   # Core Python scripts
│   ├── detect_drowsiness.py     # Real-time eye state detection using webcam
│   ├── utils.py                # Helper functions
│   └── arduino_interface.py    # Code to trigger buzzer/motor via serial port
├── arduino/              # Arduino sketch (.ino) for buzzer and motor control
├── media/                # Screenshots, sample output images/videos
├── app/                  # Optional GUI or Flask app for visualization
├── requirements.txt      # Python dependencies
├── README.md             # Project documentation
└── report/               # Project report, presentation slides, etc.
```

---

## ⚙️ How It Works

1. **Image Dataset**: A dataset of eye images (2,000 open, 2,000 closed) is used to train a CNN model.
2. **Model**: The CNN learns to classify whether eyes are open or closed.
3. **Real-Time Detection**: OpenCV captures webcam frames and detects eye region.
4. **Prediction**: The model predicts the state of the eyes.
5. **Alert System**: If eyes are closed for a set duration:
   - A buzzer is triggered via Arduino
   - A motor is stopped to simulate braking

---

## 🔌 Hardware Requirements

- Arduino Uno/Nano
- IR Sensor or Camera Module
- Buzzer
- Motor (for simulation)
- USB Cable for Serial Communication

---

## 🧪 Installation & Usage

### Clone the Repository

```bash
git clone https://github.com/yourusername/Driver-Drowsiness-Detection.git
cd Driver-Drowsiness-Detection
