# 🧠 CogniSign: Real-Time Sign Language Detection using Deep Learning & MediaPipe

CogniSign is an end-to-end deep learning system that enables real-time recognition of American Sign Language (ASL) gestures using a webcam. Built with TensorFlow, MediaPipe, and OpenCV, it identifies and classifies 7 common gestures with high accuracy using LSTM neural networks.

---

## 🔍 Project Highlights

- 🧩 **Custom Dataset Creation**: Captures and stores landmark coordinates for face, pose, and hands using MediaPipe Holistic.
- 🧠 **LSTM Model**: Classifies gestures based on sequences of 3D keypoints (30 frames per gesture).
- 🖥️ **Real-Time Webcam Inference**: Uses OpenCV to predict and overlay gesture labels live.
- 🎯 **100% Accuracy** on test data (7-class classification).
- 🎨 **Probability Visualization Bar**: Displays class probabilities dynamically on-screen.

---

## 📊 Tech Stack

| Tech | Purpose |
|------|---------|
| `Python` | Core language |
| `MediaPipe` | Pose, hand, and face landmark detection |
| `OpenCV` | Real-time webcam integration & drawing |
| `TensorFlow/Keras` | LSTM model architecture |
| `NumPy, Matplotlib` | Data processing & visualization |
| `Scikit-learn` | Train/test split, metrics |

---

## 📈 Model Architecture

```text
Input Shape: (30 frames, 1662 features)
→ LSTM (64 units)
→ LSTM (128 units)
→ LSTM (64 units)
→ Dense (64) → Dense (32) → Dense (7 classes, softmax)
```

---

## 📹 How It Works
	1.	User performs a gesture in front of the webcam.
	2.	MediaPipe detects pose, hand, and face landmarks.
	3.	30 frames of keypoints are collected to form a sequence.
	4.	Trained LSTM model predicts the gesture class.
	5.	Class label and probability bar are shown live on screen.

---

## 🧪 Results
	•	✅ Trained on 210 gesture sequences across 7 classes
	•	✅ 100% test accuracy with zero misclassifications
	•	✅ Real-time performance ~30 FPS on Mac M1

---

## 🛠️ Future Work
	•	Add more gestures (extend from 7 to 20+)
	•	Add support for multilingual signs
	•	Deploy as a browser-based app using TensorFlow.js or Streamlit

---

## ⭐️ If you like it…

Give this repo a ⭐️ and share your feedback or improvement ideas!
