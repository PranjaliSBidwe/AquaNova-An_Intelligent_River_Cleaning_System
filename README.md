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

# Working Flow

1. System Initialization – Raspberry Pi, Arduino, camera module, sensors, GPS, motors, and IoT communication modules are initialized and checked before operation.
2. Real-Time Image Capture – The Raspberry Pi camera continuously captures live images of the water surface for environmental monitoring and waste detection.
3. Image Preprocessing – The captured image frames are resized, enhanced, and processed using OpenCV before being provided to the AI model.
4. AI-Based Waste Detection – The trained AI model analyzes the camera frames and identifies objects present on the water surface.
5. Object Classification – The AI model classifies detected objects into categories such as Waste, Background, and Living Organism, helping the system distinguish waste from non-target objects.
6. Waste Position Detection – The camera frame is divided into left, center, and right zones to determine the direction and position of the detected waste.
7. Navigation Decision-Making – Based on the detected waste position, the Raspberry Pi generates the appropriate navigation command such as left, center, or right.
8. Raspberry Pi–Arduino Communication – The Raspberry Pi sends the navigation and collection commands to the Arduino controller through serial communication.
9. Autonomous Navigation – The Arduino controls the propellers and movement motors to automatically navigate AquaNova toward the detected waste.
10. Obstacle Detection & Avoidance – Ultrasonic sensors continuously monitor the surroundings for obstacles, allowing the system to adjust its movement and avoid collisions during navigation.
11. Waste Approach – When AquaNova reaches the detected waste, the navigation process transitions to the waste-collection operation.
12. Waste Collection Activation – The conveyor belt and suction pump mechanisms are activated to collect floating waste from the water surface and transfer it into the cleaning and storage system.
13. Multi-Layer Filtration – The collected material passes through a three-layer filtration system, where large debris, medium particles, and fine particles are separated before storage.
14. Waste Storage – After filtration, the collected waste is transferred into the onboard collection/storage bin.
15. Bin Monitoring – The load cell sensor with HX711 continuously monitors the waste-bin weight/level and calculates the collected waste percentage.
16. Bin Threshold Alert – When the storage bin reaches a predefined threshold, the system activates the buzzer alert and generates a corresponding dashboard notification; when the bin becomes full, further collection operations are stopped for maintenance and safety.
17. GPS Tracking – The GPS module continuously provides AquaNova's geographical location for real-time tracking.
18. IoT Data Transmission – Operational information such as GPS location, bin level, waste collection status, system status, and alerts is transmitted through the IoT communication system.
19. Real-Time Dashboard Monitoring – The web-based IoT dashboard displays the robot's location, bin level, operational status, and alerts for remote monitoring.
20. Continuous Autonomous Operation – The system continuously repeats the cycle of camera monitoring → AI detection → classification → directional navigation → obstacle avoidance → waste collection → filtration → bin monitoring → IoT updates until the system is stopped or the storage bin reaches its capacity.
21. Safe System Stop – When the system is stopped or the bin reaches full capacity, the collection operation is safely stopped and the system enters the required maintenance/safe state.

# Applications 

1. River Cleaning — Automating the detection and collection of floating waste from rivers to reduce water pollution
2. 1. Lake & Reservoir Cleaning — Supporting automated removal of floating debris from lakes, reservoirs, and other water bodies.
3. Water Pollution Management — Using AI-based waste detection and automated collection to help manage floating plastic and other debris.
4. Smart Environmental Monitoring — Providing real-time GPS location, bin level, system status, and alerts through an IoT-based dashboard.
5. Municipal Cleaning Operations — Supporting regular water-body cleaning activities while reducing manual effort and intervention.
6. Environmental & Robotics Research — Providing a practical platform for research in AI, Computer Vision, IoT, autonomous navigation, robotics, and smart environmental systems.
