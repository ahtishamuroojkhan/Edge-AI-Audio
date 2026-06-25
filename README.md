# Edge-AI-Audio 
Download the speech emotion recognition model from the following link of sami002khan:
<br>
[Link](https://github.com/sami002khan/speech-emotion-recognition)
<br>
Download the audio speech dataset from the following Kaggle link:
<br>
[Link](https://www.kaggle.com/datasets/uwrfkaggler/ravdess-emotional-speech-audio)
Train the CNN on your PC.
Save:
  emotion_recognition_model.h5
  label_encoder.pkl
Convert the .h5 model to:
  emotion_model.tflite
Copy those files to Raspberry Pi.
Run only inference on the Pi. The following files:



Raspberry Pi deployment

Live microphone capture
MFCC extraction
Real-time TFLite inference
Probability bars, latency, and confidence display
RoArm-M2-S control
