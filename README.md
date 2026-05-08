# Sign Language to Speech Converter

## 📌 Overview

The **Sign Language to Speech Converter** is an AI-powered assistive system designed to bridge the communication gap between deaf/mute individuals and non-sign language users.
The project uses **Computer Vision**, **Machine Learning**, and **Text-to-Speech (TTS)** technologies to recognize hand gestures in real time and convert them into spoken words.

---

## 🚀 Features

* Real-time hand gesture recognition
* Sign language to text conversion
* Text-to-speech audio output
* User-friendly interface
* Live webcam integration
* Fast and accurate gesture detection

---

## 🛠️ Technologies Used

* **Python**
* **OpenCV**
* **MediaPipe**
* **NumPy**
* **gTTS (Google Text-to-Speech)**
* **Machine Learning**

---

## 📂 Project Structure

```bash
Sign-Language-To-Speech-Converter/
│── dataset/                 # Training images/data
│── models/                  # Trained ML models
│── main.py                  # Main application file
│── gesture_recognition.py   # Gesture detection logic
│── text_to_speech.py        # Speech conversion module
│── requirements.txt         # Required dependencies
│── README.md                # Project documentation
```

---

## ⚙️ Installation

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/your-username/sign-language-to-speech-converter.git
cd sign-language-to-speech-converter
```

### 2️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

---

## ▶️ Usage

Run the application using:

```bash
python main.py
```

* Show hand gestures in front of the webcam.
* The system detects the sign language gesture.
* Recognized text is converted into speech automatically.

---

## 🧠 Working Principle

1. Webcam captures hand gestures.
2. MediaPipe detects hand landmarks.
3. Machine Learning model classifies gestures.
4. Recognized gesture is converted into text.
5. gTTS converts text into speech output.

---

## 💻 Sample Code

```python
import cv2
import mediapipe as mp
from gtts import gTTS

# Initialize webcam
cap = cv2.VideoCapture(0)

# Initialize MediaPipe Hands
mp_hands = mp.solutions.hands
hands = mp_hands.Hands()

while True:
    success, frame = cap.read()

    # Convert image to RGB
    rgb = cv2.cvtColor(frame, cv2.COLOR_BGR2RGB)

    # Process hand detection
    result = hands.process(rgb)

    # Display output
    cv2.imshow("Sign Language Detection", frame)

    if cv2.waitKey(1) & 0xFF == ord('q'):
        break

cap.release()
cv2.destroyAllWindows()
```

---

## 📊 Applications

* Communication assistance for deaf and mute individuals
* Smart assistive devices
* Educational platforms
* Healthcare communication systems
* Accessibility technology

---

## 🔮 Future Enhancements

* Support for multiple sign languages
* Mobile application integration
* Sentence-level recognition
* AI chatbot integration
* Cloud-based speech processing

---

## 🎯 Outcome

This project improves accessibility and inclusivity by enabling seamless communication through real-time sign language interpretation and speech generation.

---

## 👨‍💻 Author

**Ghoushenisha Begam J**
B.Tech Information Technology Student
Passionate about AI, Accessibility, and Full Stack Development.
