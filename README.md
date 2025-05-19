# Fire and Smoke Detection using OpenCV

This project performs real-time fire and smoke detection using your webcam. It utilizes color thresholding for fire and background subtraction for smoke, making it lightweight and fast — suitable for basic fire/smoke monitoring applications.

## How it Works

- Fire Detection: Uses HSV color segmentation to detect reddish/yellow regions that typically represent flames.
- Smoke Detection: Uses motion-based background subtraction followed by thresholding and morphological filtering to isolate smoke-like regions.

---


## Features

- Real-time detection using webcam
- Separate labeling for  Fire and  Smoke
- Adjustable color and motion parameters
- Uses only OpenCV and NumPy — no deep learning required

---

## Requirements

Make sure you are using Python 3.6+

Install dependencies:

bash
pip install opencv-python numpy


# How to Run
Clone the repo and run the script:

bash

git clone https://github.com/yourusername/fire-smoke-detection.git
cd fire-smoke-detection
python detect_fire_smoke.py

- Press q to exit the video stream.

# Algorithm Details
# Fire Detection
 > Convert each frame to HSV color space.

 > Apply a color mask for fire-like hues:
 > lower_fire = [0, 50, 50]
 > upper_fire = [40, 255, 255]

- Filter small noise using morphological operations.

- Draw red bounding boxes for fire regions.

# Smoke Detection
 > Use background subtraction (MOG2) to detect motion.

 > Apply Gaussian blur and thresholding.

 > Use morphological closing to reduce noise.

 > Draw blue bounding boxes for smoke regions.
