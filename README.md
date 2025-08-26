## Ultrasonic Sensor with Servo Motor – Arduino Uno

This project uses an HC-SR04 Ultrasonic Sensor to detect objects and a Servo Motor to move when an object comes within a set distance.

## 🔧 Components Required

Arduino Uno

HC-SR04 Ultrasonic Sensor

SG90 / MG90 Servo Motor (or similar)

Jumper Wires

Breadboard

(Optional) External 5V power supply for servo

## 🔌 Circuit Connections
## Ultrasonic Sensor (HC-SR04)

VCC → 5V

GND → GND

TRIG → Pin 5

ECHO → Pin 6

## Servo Motor

Red (VCC) → 5V

Brown/Black (GND) → GND

Orange/Yellow (Signal) → Pin 9

⚠️ If the servo is not moving properly, use an external 5V power supply (connect its GND to Arduino GND).


## ⚙️ How It Works

The HC-SR04 sensor measures the distance to the nearest object.

If the object is within 20 cm, the servo motor turns to 90°.

If no object or object farther than 20 cm, the servo resets to 0°.

The distance values can be monitored using Serial Monitor at 9600 baud.

## 📌 Notes

You can change the detection distance by modifying this line in the code:

if (distance > 0 && distance < 20) {  


Replace 30 with your preferred distance in cm.


For larger servos, always use an external power supply.
