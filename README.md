# Gesture Volume Control

A computer-vision prototype that maps **the distance between the thumb and index finger** to the system's master volume level in real time.

The application uses a webcam to detect hand landmarks and updates Windows audio volume through Pycaw.

## Features

- Real-time webcam capture
- MediaPipe hand landmark detection
- Thumb and index-finger tracking
- Finger-distance measurement
- Distance-to-volume mapping
- Windows master-volume control
- Visual line between tracked fingertips
- Fully local processing

## Tech Stack

- Python
- OpenCV
- MediaPipe
- Pycaw
- comtypes
- Windows Core Audio API

## How It Works

```text
Webcam frame
    │
    ▼
MediaPipe hand detection
    │
    ▼
Thumb tip + index tip coordinates
    │
    ▼
Euclidean distance
    │
    ▼
Normalize distance to 0.0–1.0
    │
    ▼
Windows master volume
```

## Requirements

This project is designed for **Windows**, because Pycaw controls the Windows Core Audio API.

Install dependencies:

```bash
pip install opencv-python mediapipe pycaw comtypes
```

The current script also imports the Twilio client library, so if you run the file exactly as stored you may also need:

```bash
pip install twilio
```

The volume-control workflow itself does not require a real Twilio account.

## Run

Clone the repository:

```bash
git clone https://github.com/Sankalp-gupta1/gesture-volume-control.git
cd gesture-volume-control
```

Run:

```bash
python volumecontrol.py
```

Press `q` in the OpenCV window to exit.

## Important Note

The script is a learning/prototype implementation. Review the placeholder Twilio configuration and Python indentation before using it as a production-ready application.

## Author

**Sankalp Gupta**

GitHub: https://github.com/Sankalp-gupta1
