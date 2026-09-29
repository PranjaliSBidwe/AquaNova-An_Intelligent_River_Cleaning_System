#  AquaNova — An Intelligent River Cleaning System

AquaNova is an AI and IoT-enabled autonomous river cleaning system designed to detect and collect floating waste while monitoring the condition and location of the cleaning boat in real time.

The system combines Computer Vision, TensorFlow Lite, Raspberry Pi, Arduino, sensors, GPS, automated waste collection mechanisms, and a web-based monitoring dashboard to create an integrated approach to water-body cleaning.

The Raspberry Pi processes camera input using a TensorFlow Lite waste-detection model to identify floating waste and distinguish it from living organisms. Based on the detected object's position, the system sends movement commands to the Arduino through serial communication.

The Arduino controls the robot's propulsion motors, conveyor belt, water pump, and servo-based collection mechanism, enabling the detected waste to be approached and collected automatically.

The system also integrates an HX711 load cell to monitor the collected waste weight and provides buzzer alerts when the bin reaches configured capacity levels. A GPS module provides the boat's geographical location for monitoring.

A web-based dashboard provides authorized users with real-time information about AquaNova's GPS location, bin weight, sensor readings, and system status. The dashboard uses Firebase Google Authentication, Node.js, Express.js, MongoDB, Chart.js, and Leaflet for authentication, backend communication, data storage, visualization, and location tracking.

#  Main Components

#  Artificial Intelligence
TensorFlow Lite

Computer Vision

OpenCV

Waste detection

Living-organism detection

Region-based detection

Confidence-based decision making

#  Autonomous Hardware

Raspberry Pi

Arduino

DC motors

Motor drivers

Conveyor mechanism

Water pump

Servo mechanism

Buzzer

#  Sensors & Monitoring

RaspberryPi Camera

GPS

HX711 Load Cell

Bin weight monitoring

GPS location tracking

#  Web Dashboard

HTML

CSS

JavaScript

Firebase Authentication

Node.js

Express.js

MongoDB

Mongoose

Chart.js

Leaflet

OpenStreetMap
