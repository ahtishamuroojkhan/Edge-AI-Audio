# Edge-AI Audio-Based Emotion-Aware Human–Robot Interaction

This repository demonstrates a real-time Edge-AI speech emotion recognition framework** for emotion-aware human–robot interaction** using a Raspberry Pi 4B and a RoArm-M2-S robotic manipulator.

The framework performs speech emotion recognition (SER) using a lightweight CNN model optimized with TensorFlow Lite and converts the detected emotional state into corresponding robotic gestures.

# Speech Emotion Recognition Model

The CNN-based speech emotion recognition model is adapted from the following open-source implementation:

GitHub Repository:

[sami002khan](https://github.com/sami002khan/speech-emotion-recognition)

Please clone or download the repository before proceeding.


# Dataset

The speech emotion recognition model is trained using the RAVDESS dataset.

Dataset:

[Link](https://www.kaggle.com/datasets/uwrfkaggler/ravdess-emotional-speech-audio)

# Model Training

-Train the CNN on your PC. 
-Save: emotion_recognition_model.h5 
-label_encoder.pkl 
-Convert the .h5 model to: emotion_model.tflite 
-Copy those files to Raspberry Pi. 
-Run only inference on the Pi. The following files: 
-01.py 
-02.py 
-03.py 
-Raspberry Pi deployment Live microphone capture MFCC extraction Real-time TFLite inference 
-Probability bars
-latency
-confidence display RoArm-M2-S control

# Software Requirements

- Python 3
- TensorFlow
- TensorFlow Lite
- Librosa
- NumPy
- OpenCV
- Matplotlib
- Scikit-learn

