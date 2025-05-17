# Hand Gesture Volume Control

This project allows you to control your system's volume using hand gestures captured via webcam. It uses real-time hand tracking to detect the distance between the thumb and index finger. If the fingers are far apart, the volume is increased; if they are close together, the volume is decreased. The idea is to make media control touchless and intuitive using computer vision.

## How It Works

- The webcam feed is captured using OpenCV.
- MediaPipe detects hand landmarks in real-time.
- The coordinates of the thumb tip (landmark 4) and index finger tip (landmark 8) are extracted.
- The Euclidean distance between these two points is calculated.
- Based on this distance:
  - If the fingers are apart: `volumeup` key is triggered.
  - If the fingers are close: `volumedown` key is triggered.
- PyAutoGUI simulates the volume keypress actions.

## Technologies Used

- Python
- OpenCV
- MediaPipe
- PyAutoGUI
- Math (for distance calculation)

## Learning Outcomes

- Understanding real-time gesture control
- Using MediaPipe for hand landmark tracking
- Applying OpenCV to process live video streams
- Interfacing computer vision with system-level automation using PyAutoGUI

