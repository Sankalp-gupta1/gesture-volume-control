# Gesture Volume Control

A computer-vision project for controlling volume with a hand gesture.

## Live browser demo

**https://gesture-volume-control-sankalp.vercel.app/**

## Two versions in this repository

### 1. Original Windows version

`volumecontrol.py` uses:

- OpenCV
- MediaPipe
- Pycaw
- Windows Core Audio

It can change the Windows system volume.

### 2. Deployed web version

The `web/` app uses:

- browser webcam access,
- MediaPipe Hands,
- Web Audio API,
- an in-page test tone.

Browsers do not allow a website to change the computer's master system volume. Because of that security restriction, the deployed version controls only the audio created inside the page.

The gesture logic is still real: thumb-to-index distance is measured from tracked hand landmarks and converted into a 0–100% audio level.

## Privacy

Webcam frames are processed in the browser and are not uploaded by this demo.

## Run locally

```bash
cd web
python -m http.server 8000
```

Open `http://localhost:8000`, click **Start camera**, and allow camera access.

## Original Windows setup

```bash
pip install opencv-python mediapipe pycaw comtypes
python volumecontrol.py
```

## Author

Sankalp Gupta  
GitHub: https://github.com/Sankalp-gupta1
