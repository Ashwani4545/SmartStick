# SmartStick
Introduction
A Smart Blind Stick using a Raspberry Pi is an assistive device designed for visually impaired individuals. It enhances mobility by detecting obstacles, providing real-time feedback via voice alerts, vibration, and GPS navigation. The system utilizes ultrasonic sensors, a camera, GPS, and AI-based object detection to assist users in navigating safely.

Objectives
✔️ Obstacle Detection – Detect obstacles and alert the user via buzzer/vibration.
✔️ GPS Navigation – Helps in tracking location and guiding the user.
✔️ AI-Based Object Recognition – Uses a camera to identify objects in front.
✔️ Voice Feedback – Provides real-time voice guidance.
✔️ Cloud Connectivity – Sends alerts to family members in case of emergencies.

Components Required
Component	Purpose
Raspberry Pi 4/3B+	Main processing unit
Ultrasonic Sensor (HC-SR04)	Obstacle detection
Pi Camera/USB Camera	Object recognition
Buzzer	Audio alert for obstacles
Vibration Motor	Haptic feedback for obstacles
GPS Module (NEO-6M)	Location tracking
Speaker (3.5mm/USB)	Voice assistant output
Microphone	Voice input for assistance
Power Bank (5V, 2.5A)	Portable power supply
Jumper Wires & PCB Board	Circuit connections
Working Principle
Obstacle Detection:

The HC-SR04 ultrasonic sensor measures the distance of objects.
If an obstacle is detected within 1.5 meters, the buzzer and vibration motor are triggered.
AI-Based Object Recognition:

The Pi Camera captures images and OpenCV with TensorFlow detects objects.
If a recognized object is ahead, a voice alert is generated using Google Text-to-Speech (gTTS).
GPS Tracking & Navigation:

The GPS module (NEO-6M) determines the user's real-time location.
Can provide directions to a destination using Google Maps API.
In case of an emergency (e.g., button press), the current location is sent to a caregiver via SMS/WhatsApp.
Voice Assistance:

The microphone captures user commands, and speech recognition helps in giving responses.
Example: "Where am I?" → The system replies with current location coordinates.
Circuit Connections
Sensor/Module	Raspberry Pi Pin
HC-SR04 (Ultrasonic Sensor)	GPIO 23 (Trig), GPIO 24 (Echo)
Buzzer	GPIO 18
Vibration Motor	GPIO 27
Pi Camera	CSI Port
GPS Module (NEO-6M)	UART (Tx → GPIO 14, Rx → GPIO 15)
Speaker	USB/3.5mm Jack
Microphone	USB/3.5mm Jack
