````md
# Edge-AI Audio-Based Emotion-Aware Human–Robot Interaction

This repository demonstrates a **real-time Edge-AI speech emotion recognition framework** for **emotion-aware human–robot interaction** using a **Raspberry Pi 4B** and a **RoArm-M2-S robotic manipulator**.

The framework performs **speech emotion recognition (SER)** using a lightweight CNN model optimized with **TensorFlow Lite** and converts the detected emotional state into corresponding robotic gestures.

---

# System Overview

The proposed framework consists of the following stages:

```text
Speech Signal
      │
      ▼
USB Microphone
      │
      ▼
Audio Acquisition
      │
      ▼
Audio Preprocessing
      │
      ▼
MFCC Feature Extraction
      │
      ▼
CNN Speech Emotion Recognition
      │
      ▼
TensorFlow Lite Inference
      │
      ▼
Emotion-to-Motion Mapping
      │
      ▼
ESP32 Controller
      │
      ▼
RoArm-M2-S Robotic Manipulator
```

---

# Speech Emotion Recognition Model

The CNN-based speech emotion recognition model is adapted from the following open-source implementation:

**Author:** sami002khan

GitHub Repository:

https://github.com/sami002khan/speech-emotion-recognition

Please clone or download the repository before proceeding.

---

# Dataset

The speech emotion recognition model is trained using the **RAVDESS** dataset.

Dataset:

https://www.kaggle.com/datasets/uwrfkaggler/ravdess-emotional-speech-audio

The dataset contains emotional speech recordings with the following emotion classes:

- Neutral
- Calm
- Happy
- Sad
- Angry
- Fearful
- Disgust
- Surprised

---

# Model Training

Train the CNN model on a desktop or laptop computer.

After successful training, save:

```text
emotion_recognition_model.h5
label_encoder.pkl
```

Training on a PC is recommended because it is significantly faster than training directly on Raspberry Pi hardware.

---

# TensorFlow Lite Conversion

Convert the trained Keras model into TensorFlow Lite format.

Input:

```text
emotion_recognition_model.h5
```

Output:

```text
emotion_model.tflite
```

The TensorFlow Lite model is used for real-time embedded inference on Raspberry Pi.

---

# Raspberry Pi Deployment

Copy the following files to the Raspberry Pi:

```text
emotion_model.tflite
label_encoder.pkl
```

The Raspberry Pi performs **real-time inference only**.

No model training is performed on the embedded device.

---

# Project Files

The following Python scripts are used for deployment and evaluation.

### 01.py

Real-time speech emotion recognition interface

Features:

- Live microphone capture
- MFCC feature extraction
- TensorFlow Lite inference
- Emotion prediction
- Confidence score
- Probability bars
- Latency measurement
- Inference time display

Output:

```text
audio_realtime_interface.png
```

---

### 02.py

Speech emotion probability visualization

Features:

- Load an audio file
- Predict emotion
- Display probability distribution
- Save publication-quality probability graph

Output:

```text
audio_probability_distribution.png
```

---

### 03.py

Emotion-to-motion robotic gesture simulation

Features:

- Generate predefined robotic poses
- Simulate robot responses
- Visualize emotional gestures

Generated figures:

```text
robot_neutral_response.png
robot_happy_response.png
robot_sad_response.png
robot_angry_response.png
robot_fear_response.png
robot_surprise_response.png
```

---

# Edge-AI Deployment Pipeline

The complete deployment workflow is illustrated below.

```text
RAVDESS Dataset
        │
        ▼
MFCC Feature Extraction
        │
        ▼
CNN Training
        │
        ▼
emotion_recognition_model.h5
        │
        ▼
TensorFlow Lite Conversion
        │
        ▼
emotion_model.tflite
        │
        ▼
Raspberry Pi 4B
        │
        ▼
USB Microphone
        │
        ▼
Real-Time Speech Emotion Recognition
        │
        ▼
Emotion-to-Motion Mapping
        │
        ▼
ESP32 Controller
        │
        ▼
RoArm-M2-S Robotic Manipulator
```

---

# Emotion-to-Motion Mapping

| Emotion | Robotic Response |
|----------|------------------|
| Neutral | Home Position |
| Happy | Elevated Gesture |
| Sad | Lowered Gesture |
| Angry | Forward Aggressive Pose |
| Fear | Retracted Defensive Pose |
| Surprise | Upward Reactive Pose |

---

# Experimental Results

The proposed framework provides:

- Real-time speech emotion recognition
- Embedded TensorFlow Lite inference
- Emotion probability visualization
- Confidence estimation
- Low-latency Edge-AI deployment
- Emotion-aware robotic behavior generation
- Real-time RoArm-M2-S control

---

# Hardware Requirements

- Raspberry Pi 4B
- Logitech USB Camera (built-in microphone) or USB Microphone
- ESP32 Controller
- RoArm-M2-S Robotic Manipulator

---

# Software Requirements

- Python 3
- TensorFlow
- TensorFlow Lite
- Librosa
- NumPy
- OpenCV
- Matplotlib
- Scikit-learn

---

# Citation

If you use the baseline speech emotion recognition implementation, please acknowledge the original repository:

https://github.com/sami002khan/speech-emotion-recognition

This repository extends the baseline model through TensorFlow Lite optimization, Raspberry Pi deployment, and real-time emotion-aware robotic interaction using the RoArm-M2-S platform.
````
