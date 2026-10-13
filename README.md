# Gesture Volume Control

## Live browser demo

**https://gesture-volume-control.vercel.app/**

The original Python project controls Windows master volume. A normal website cannot change the operating system's master volume, so the hosted version safely applies the same **thumb-to-index pinch distance** idea to a generated demo tone inside the page.

The browser demo:

- requests webcam permission
- runs MediaPipe hand tracking locally in the browser
- tracks thumb and index fingertips
- converts pinch distance into a 0–100% volume value
- visualizes the tracked fingertips
- controls the demo audio level

No video frames are uploaded by the app.

---

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


## Run the hosted-style demo locally

```bash
cd web
python -m http.server 8000
```

Open `http://localhost:8000` in a modern browser and allow camera access.
