# Sleep Detector

A real-time Sleep Detection System built with Python that uses a webcam to monitor eye closure and detect signs of drowsiness. When the user's eyes remain closed for a predefined duration, the system activates an alarm to alert the user.

## 📌 Features

- Real-time webcam-based monitoring
- Face and eye landmark detection using MediaPipe
- Eye Aspect Ratio (EAR) calculation for detecting closed eyes
- Automatic drowsiness detection
- Audio alarm using Pygame
- Real-time visual status overlay
- Displays EAR value and eye-closure duration
- Face detection box with status indication
- Alarm automatically stops when the eyes are opened

## 🛠️ Technologies Used

- **Python**
- **OpenCV**
- **MediaPipe**
- **NumPy**
- **Pygame**
- **Threading**

## ⚙️ How It Works

The system captures live video from the webcam using OpenCV.

MediaPipe Face Mesh detects facial landmarks around the eyes. These landmarks are used to calculate the **Eye Aspect Ratio (EAR)**.

If the EAR falls below a predefined threshold, the system considers the eyes to be closed.

```text
Webcam
   ↓
OpenCV
   ↓
MediaPipe Face Mesh
   ↓
Eye Landmarks
   ↓
Eye Aspect Ratio (EAR)
   ↓
Eyes Closed?
   ↓
2.5 Seconds
   ↓
🚨 Alarm
