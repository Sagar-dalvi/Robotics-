# 🚨 Gas Detector System using Arduino Uno

A simple Arduino-based Gas Detector System that detects harmful gases using an MQ-series gas sensor. When the gas concentration exceeds a predefined threshold, the system activates a buzzer and an LED to alert users.

## 📌 Features

- Detects LPG, Smoke, and other combustible gases
- Real-time gas monitoring
- LED warning indicator
- Buzzer alarm for gas leakage
- Easy to build and beginner-friendly
- Low-cost safety project

## 🛠️ Components Required

- Arduino Uno
- MQ-2 Gas Sensor (or MQ-135)
- LED
- 220Ω Resistor
- Active Buzzer
- Breadboard
- Jumper Wires
- USB Cable

## 🔌 Circuit Connections

### MQ-2 Sensor
- VCC → 5V
- GND → GND
- AO → A0

### LED
- Positive → Digital Pin 7 (through 220Ω resistor)
- Negative → GND

### Buzzer
- Positive → Digital Pin 8
- Negative → GND

## 💻 Arduino Code

```cpp
const int gasSensor = A0;
const int led = 7;
const int buzzer = 8;

int threshold = 350;

void setup() {
  pinMode(led, OUTPUT);
  pinMode(buzzer, OUTPUT);
  Serial.begin(9600);
}

void loop() {
  int gasValue = analogRead(gasSensor);

  Serial.print("Gas Value: ");
  Serial.println(gasValue);

  if (gasValue > threshold) {
    digitalWrite(led, HIGH);
    digitalWrite(buzzer, HIGH);
  } else {
    digitalWrite(led, LOW);
    digitalWrite(buzzer, LOW);
  }

  delay(500);
}
```

## ▶️ How It Works

1. The MQ-2 sensor continuously measures the gas concentration.
2. Arduino reads the analog value from the sensor.
3. If the reading exceeds the threshold value:
   - The LED turns ON.
   - The buzzer sounds an alarm.
4. When the gas level returns to normal, the LED and buzzer turn OFF.

## 📷 Project Preview

Add your project images here.

Example:

```
images/gas_detector.jpg
```

## 📂 Project Structure

```
Gas-Detector-System/
│
├── GasDetector.ino
├── README.md
├── circuit_diagram.png
├── images/
│   └── gas_detector.jpg
└── LICENSE
```

## 🚀 Future Improvements

- LCD/OLED Display
- IoT Monitoring using ESP8266/ESP32
- SMS Alert using GSM Module
- Mobile App Notification
- Automatic Exhaust Fan Control
- Firebase Dashboard

## 🎯 Applications

- Home Gas Leakage Detection
- Kitchen Safety
- Industrial Safety
- Laboratory Monitoring
- LPG Storage Areas

## 👨‍💻 Author

**Sagar Dalvi**

AI & STEM Engineer

GitHub: https://github.com/Sagar-dalvi

LinkedIn: https://www.linkedin.com/in/sagardalvi01/

## 📄 License

This project is licensed under the MIT License.

⭐ If you found this project useful, don't forget to Star the repository!# Robotics-
Make gas detector system using Arduino Uno and sensor 
