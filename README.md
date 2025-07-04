🎛️ Gesture Volume Control using OpenCV & MediaPipe
Control your system volume using just your hand gestures via your webcam in real time. This project uses OpenCV, MediaPipe, and Pycaw to detect finger movements and dynamically adjust system volume — all running completely offline on your machine.

🚀 Features
✋ Real-time Hand Tracking using webcam

📏 Finger Distance Mapping: Thumb & index finger distance controls the volume

🔊 Visual Feedback: Green line between fingers shows detection

🧠 No Internet Required: Fully offline & local

💻 Windows OS Compatible (uses Pycaw API for volume control)

🛠️ Tech Stack
Component	Description
Python 3.x	Programming Language
OpenCV	For real-time video frame capture
MediaPipe	Google's ML framework for hand tracking
Pycaw	Controls Windows volume programmatically
ctypes, comtypes	For low-level Windows API access

⚙️ Installation Guide
🔧 Step-by-step setup:
bash
Copy
Edit
# 1. Clone the repository
git clone https://github.com/Sankalp-gupta1/gesture-volume-control.git
cd gesture-volume-control

# 2. (Optional) Create and activate virtual environment
python -m venv venv
venv\Scripts\activate      # On Windows

# 3. Install all required libraries
pip install opencv-python mediapipe pycaw comtypes
