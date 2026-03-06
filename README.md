# Face Emotion Detection using CNN

## 📌 Project Overview

This project detects human emotions from facial images using **Deep Learning** and **Computer Vision**.
A **Convolutional Neural Network (CNN)** model is trained on facial emotion datasets to classify emotions such as:

* Angry
* Disgust
* Fear
* Happy
* Sad
* Surprise
* Neutral

The system first detects a face in an image using **OpenCV Haar Cascade**, then predicts the emotion using a trained CNN model.

---

## 🧠 Technologies Used

* Python
* TensorFlow / Keras
* OpenCV
* NumPy
* Matplotlib
* Google Colab

---

## 📂 Project Structure

```
Face-Emotion-Detection/
│
├── FaceDetection.ipynb        # Google Colab Notebook
├── emotion_model.h5           # Trained CNN Model
├── emotion_data/              # Dataset
│   ├── train/
│   └── test/
├── facedetection.py           # Python Script
└── README.md
```

---

## 📊 Model Architecture

The CNN model includes:

* Conv2D layers for feature extraction
* MaxPooling layers for downsampling
* Dropout layers for regularization
* Dense layers for classification

Input image size: **48 × 48 grayscale**

Example architecture:

```python
model = Sequential([
    Conv2D(32,(3,3),activation='relu',input_shape=(48,48,1)),
    MaxPooling2D(2,2),
    Dropout(0.25),

    Conv2D(64,(3,3),activation='relu'),
    MaxPooling2D(2,2),
    Dropout(0.25),

    Conv2D(128,(3,3),activation='relu'),
    MaxPooling2D(2,2),
    Dropout(0.25),

    Flatten(),
    Dense(128,activation='relu'),
    Dropout(0.5),
    Dense(7,activation='softmax')
])
```

---

## ⚙️ Installation

Clone the repository:

```
git clone https://github.com/yourusername/Face-Emotion-Detection.git
```

Install required libraries:

```
pip install tensorflow opencv-python numpy matplotlib
```

---

## ▶️ How to Run

### 1️⃣ Train the Model

Run the training script or notebook to train the CNN model:

```
python facedetection.py
```

The model will be saved as:

```
emotion_model.h5
```

---

### 2️⃣ Detect Emotion from Image

Upload an image containing a face.

The system will:

1. Detect the face using OpenCV
2. Resize it to **48×48**
3. Predict emotion using CNN

Example output:

```
Predicted Emotion: Angry
Confidence: 55.26%
```

---

## 📷 Example Output

The system draws a bounding box around the detected face and displays the predicted emotion.

Example:

```
Predicted Emotion: Angry
Confidence: 55.26%
```

---

## 🎯 Features

✔ Face detection using OpenCV
✔ Emotion classification using CNN
✔ Works with uploaded images
✔ Webcam capture supported in Google Colab
✔ Visual bounding box with predicted emotion

---

## 🚀 Future Improvements

* Real-time emotion detection using webcam
* Improve accuracy with larger datasets
* Deploy as a **Web App using Streamlit**
* Convert model to **TensorFlow Lite for mobile apps**

---

## 📚 Learning Outcomes

Through this project you will learn:

* Deep Learning with CNN
* Image preprocessing
* Face detection using OpenCV
* Emotion classification
* Model training and evaluation

---

## 👩‍💻 Author

**Ishwarya K**

Deep Learning & Computer Vision Project
