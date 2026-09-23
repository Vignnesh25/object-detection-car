
# 🚗 Object Detection Car Using Arduino

An autonomous robotic car that detects obstacles and avoids collisions using an HC-SR04 ultrasonic sensor, Arduino Uno, and L298N motor driver.

## 📌 Project Overview

The Object Detection Car is an Arduino-based autonomous vehicle designed to detect obstacles in its path and automatically avoid collisions.

The HC-SR04 ultrasonic sensor measures the distance between the car and nearby objects. The Arduino Uno processes the sensor data and controls two DC motors through the L298N motor driver.

When an obstacle is detected within a predefined distance, the car stops, reverses, turns, and continues moving forward.

## 🎯 Objectives

- Build a low-cost autonomous robotic car.
- Detect obstacles using an ultrasonic sensor.
- Avoid collisions automatically.
- Learn Arduino programming and motor control.
- Understand embedded systems and robotics.

## 🛠️ Components Required

| Component | Quantity |
|---|---|
| Arduino Uno | 1 |
| HC-SR04 Ultrasonic Sensor | 1 |
| L298N Motor Driver | 1 |
| DC Geared Motors | 2 |
| Robot Car Chassis | 1 |
| Wheels | 2 |
| Castor Wheel | 1 |
| Battery Pack | 1 |
| Jumper Wires | As required |
| Power Switch | 1 |

## 🔌 Circuit Connections

### HC-SR04 to Arduino Uno

| HC-SR04 Pin | Arduino Pin |
|---|---|
| VCC | 5V |
| GND | GND |
| TRIG | D9 |
| ECHO | D10 |

### L298N to Arduino Uno

| L298N Pin | Arduino Pin |
|---|---|
| IN1 | D6 |
| IN2 | D7 |
| IN3 | D4 |
| IN4 | D5 |

### Motor Connections

| Motor | L298N Terminal |
|---|---|
| Left Motor | OUT1 and OUT2 |
| Right Motor | OUT3 and OUT4 |

> ⚠️ Ensure that the Arduino and motor driver share a common GND. Use a suitable motor power supply and verify the wiring before powering the circuit.

## ⚙️ Working Principle

1. The ultrasonic sensor transmits ultrasonic waves.
2. The waves reflect from nearby obstacles.
3. The Arduino calculates the distance using the echo time.
4. The measured distance is compared with a safety threshold.
5. If the path is clear, the car moves forward.
6. If an obstacle is detected, the car stops, reverses, and turns right.
7. The process repeats continuously.

## 💻 Software Requirements

- Arduino IDE
- Embedded C / Arduino programming
- USB cable for uploading code

## 📂 Project Structure

```text
Object-Detection-Car/
│
├── Object_Detection_Car.ino
├── README.md
├── circuit_diagram.png
├── project_report.docx
└── images/
    └── robot_car.jpg
```

## 🚀 How to Run the Project

1. Assemble the robot car chassis.
2. Connect the motors, ultrasonic sensor, and motor driver.
3. Connect the Arduino Uno to your computer.
4. Open the `.ino` file in Arduino IDE.
5. Select the correct board and COM port.
6. Upload the program to the Arduino.
7. Power the motor driver and Arduino safely.
8. Place the car on a clear surface and test obstacle avoidance.

## 📏 Obstacle Detection Threshold

The default obstacle detection threshold is **20 cm**.

You can change the threshold in the Arduino code:

```cpp
if (distance > 20)
{
    moveForward();
}
else
{
    stopCar();
    moveBackward();
    turnRight();
}
```

## ✨ Features

- Automatic obstacle detection
- Autonomous movement
- Collision avoidance
- Real-time distance measurement
- Simple and affordable design
- Beginner-friendly Arduino implementation

## 🔮 Future Enhancements

- Bluetooth or Wi-Fi remote control
- Mobile application integration
- Camera-based object detection
- Machine learning-based navigation
- IoT monitoring
- Automatic path planning
- Servo-controlled ultrasonic scanning

#

## 👨‍💻 Team Members

JS Vignnesh,
Harshit Kumar BV,
Akash,
Akshay kumar,

## 🎓 Academic Project

This project was developed as an educational project to understand Arduino programming, embedded systems, robotics, sensors, and motor control.

## 📄 License

This project is intended for educational and learning purposes.
