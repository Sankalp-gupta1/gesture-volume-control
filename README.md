# Gesture Volume Control

A computer-vision project for controlling volume with a hand gesture.

## Live demo

**https://gesture-volume-control-sankalp.vercel.app/**

The browser demo tracks your hand with MediaPipe and converts the distance between the thumb tip and index fingertip into a 0–100% volume value.

## What the live demo does

- asks for webcam permission,
- detects one hand,
- tracks thumb and index fingertips,
- measures the distance between them,
- maps the distance to a volume percentage,
- controls a browser-generated test tone,
- draws the hand landmarks on screen.

Webcam frames are processed in the browser and are not intentionally uploaded by this demo.

## Important browser limitation

A normal website cannot change the computer's master system volume.

Because of that security restriction, the live version controls only audio generated inside the page.

The original Python version is still included and can control Windows system volume.

## Original Windows version

File:

```text
volumecontrol.py
```

Main technologies:

- Python
- OpenCV
- MediaPipe
- Pycaw
- Windows Core Audio

Install:

```bash
pip install opencv-python mediapipe pycaw comtypes
```

Run:

```bash
python volumecontrol.py
```

This version requires Windows and a webcam.

## Run the web demo locally

```bash
cd web
python -m http.server 8000
```

Open:

```text
http://localhost:8000
```

Then click **Start camera** and allow camera access.

## Tech stack

### Desktop
- Python
- OpenCV
- MediaPipe
- Pycaw

### Web
- HTML
- CSS
- JavaScript
- MediaPipe Hands
- Web Audio API
- Vercel

## Author

**Sankalp Gupta**

- GitHub: https://github.com/Sankalp-gupta1
- LinkedIn: https://www.linkedin.com/in/sankalp-gupta-rishi-8617302b0/
