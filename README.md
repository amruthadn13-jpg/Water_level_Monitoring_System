# Water_level_Monitoring_System
**💧 Water Level Monitoring System using ESP32 (Wokwi Simulation)**

This project implements a Water Level Monitoring System using an ESP32 and an HC-SR04 Ultrasonic Sensor.

The system measures the distance between the sensor and the water surface and indicates the water level using:

🔴 Red LED – High Water Level

🟡 Yellow LED – Medium Water Level

🟢 Green LED – Low Water Level

🔊 Buzzer – Alert when water level is high

The project is fully simulated using the Wokwi Online Simulator.

**🚀 Features**

Real-time distance measurement using Ultrasonic Sensor

Automatic water level classification (Low / Medium / High)

LED visual indication

Buzzer alert for high water level

Serial Monitor output for debugging

**🛠️ Components Used**

ESP32 Dev Module

HC-SR04 Ultrasonic Sensor

3 LEDs (Red, Yellow, Green)

Buzzer

Jumper Wires

Wokwi Simulation Platform

**🔌 Pin Configuration**
Component	ESP32 Pin
Trig	22
Echo	23
High Level LED	12
Medium Level LED	14
Low Level LED	27
Buzzer	4

**📊 Working Principle**

The ESP32 sends a 10µs trigger pulse to the ultrasonic sensor.

The sensor sends an ultrasonic wave.

The wave reflects back from the water surface.

The echo time is measured.

Distance is calculated using:

Distance = (Duration × 0.034) / 2

Where:

0.034 cm/µs is the speed of sound

Divided by 2 because the wave travels to the object and back

**💡 Water Level Conditions**
Distance (cm)	Water Level	Indication
> 20 cm	Low	Green LED ON
< 10 cm	Medium	Yellow LED ON
10–20 cm	High	Red LED ON + Buzzer ON
🖥️ Serial Monitor Output Example
Distance:
15.23
Cm
Water Level: High
🌐 Simulation Platform

This project was simulated using:

**🔗 Wokwi Online Simulator**
https://wokwi.com/

📂 How to Run

Open Wokwi

Select ESP32 Dev Module

Connect components as per pin configuration

Paste the Arduino code

Start Simulation

Open Serial Monitor (115200 baud)

**🎯 Applications**

Water tank monitoring

Industrial liquid level monitoring

Smart irrigation systems

Smart home automation

**👩‍💻 Author**

Amrutha D N
