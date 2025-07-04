# 🎛️ Gesture Volume Control using OpenCV & MediaPipe

Control your system's volume using hand gestures in real time via your webcam. Built with OpenCV, MediaPipe, and Pycaw.

---

## 🚀 Features

- ✋ Real-time gesture detection using webcam
- 📏 Thumb & index finger distance maps to volume level
- 🔊 Smooth volume control with visual feedback (line between fingers)
- 🔐 Runs locally, no internet required

---

## 🛠️ Tech Stack

- Python 3.x
- OpenCV
- MediaPipe
- Pycaw (Windows audio control)
- ctypes, comtypes (for system-level API)

---

## ⚙️ Installation

```bash
# Clone the repo
git clone https://github.com/Sankalp-gupta1/gesture-volume-control.git
cd gesture-volume-control

# Create virtual environment (optional)
python -m venv venv
venv\Scripts\activate

# Install dependencies
pip install opencv-python mediapipe pycaw comtypes
