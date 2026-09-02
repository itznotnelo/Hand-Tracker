# Hand-Tracker

A browser-based hand-tracking UI built with [MediaPipe Hands](https://developers.google.com/mediapipe). Move your index finger to control a virtual cursor, pinch (thumb + index) to "click" on cards.

## Usage

Open `index.html` in a browser and grant camera access. No build step or install required — dependencies load from CDN.

## How it works

- MediaPipe Hands tracks 21 hand landmarks per frame from the webcam feed.
- The index fingertip (landmark 8) position drives the on-screen cursor.
- Distance between index fingertip and thumb tip (landmark 4) below a threshold registers as a pinch/click.
- Cursor position is checked against card bounding boxes for hover/active state.
