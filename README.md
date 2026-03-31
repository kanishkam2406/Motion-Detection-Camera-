# 🔍 Smart Detection System

![Python](https://img.shields.io/badge/Python-3.x-blue)
![OpenCV](https://img.shields.io/badge/OpenCV-ComputerVision-green)
![Pygame](https://img.shields.io/badge/Pygame-Audio-orange)
![License](https://img.shields.io/badge/License-OpenSource-yellow)

A **real-time computer vision project** built using **Python, OpenCV, NumPy, and Pygame** that detects:

- 👤 Faces  
- 👀 Eyes  
- 🏃 Motion  
- 🔵 Blue Objects  
- 🚨 Alarm Alerts  

The system uses a **webcam feed** to monitor activity and automatically triggers an **alarm when motion or blue objects are detected**.

---
## 🎥 Demo Video

Click the thumbnail below to watch the demo.

<p align="center">
<a href="Demo.mp4">
<img src="https://github.com/user-attachments/assets/34416924-52e2-4a0b-8f7b-e1cbf1c39dbb" width="800"/>
</a>
</p>

---

# 📑 Table of Contents

- Features
- Tech Stack
- Installation
- Usage
- Project Structure
- How It Works
- Code Highlights
- Example Detection
- Limitations
- Future Improvements
- Author
- License

---

# ✨ Features

✔ Real-time webcam monitoring  
✔ Face detection using **Haar Cascade**  
✔ Eye detection inside detected faces  
✔ Motion detection using **Background Subtraction (MOG2)**  
✔ Blue object detection using **HSV color filtering**  
✔ Alarm alert when suspicious activity is detected  
✔ Multi-threaded alarm system for smooth performance  
✔ Bounding boxes around detected objects  

---

# 🛠 Tech Stack

| Technology | Purpose |
|------------|--------|
| Python | Main programming language |
| OpenCV | Computer vision processing |
| NumPy | Image processing |
| Pygame | Alarm sound playback |
| Threading | Background alarm execution |

---

# ⚙ Installation

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/yourusername/smart-detection-system.git
cd smart-detection-system
```

---

### 2️⃣ Install Dependencies

```bash
pip install opencv-python numpy pygame
```

---

# ▶ Usage

Run the project:

```bash
python "Motion Detection Camera.py"
```

A webcam window will open showing the **live detection feed**.

### Controls

Press **Q** to exit the program.

---

# 📁 Project Structure

```
smart-detection-system
│
├── Motion Detection Camera.py
├── alarm.mp3.wav
├── demo.mp4
└── README.md
```

---

# 🧠 How the System Works

```
Webcam Input
      ↓
Frame Processing (OpenCV)
      ↓
Face Detection
Eye Detection
Motion Detection
Blue Object Detection
      ↓
Alarm Trigger System
      ↓
Live Output Display
```

---

# 💻 Code Highlights

### Face Detection

```python
face_cascade = cv2.CascadeClassifier(
    cv2.data.haarcascades + 'haarcascade_frontalface_default.xml'
)
```

---

### Eye Detection

```python
eyes = eye_cascade.detectMultiScale(roi_gray)
```

---

### Motion Detection

```python
fgbg = cv2.createBackgroundSubtractorMOG2()
```

---

### Blue Object Detection

```python
lower_blue = np.array([100,150,0])
upper_blue = np.array([140,255,255])
```

---

### Alarm System

```python
alarm_thread = threading.Thread(target=play_alarm)
alarm_thread.daemon = True
alarm_thread.start()
```

---

# 📊 Example Detection

This system can detect:

👤 Human faces  
👀 Eyes within faces  
🏃 Motion in the environment  
🔵 Blue objects such as:

- Blue bottle
- Blue cloth
- Blue marker
- Blue box

When motion or blue objects appear, the **alarm automatically activates**.

---

# ⚠ Limitations

- Haar cascade detection may struggle in **low lighting**
- Motion detection can produce **false positives**
- Blue color detection depends on lighting conditions
- Alarm may trigger frequently in dynamic environments

---

# 🚀 Future Improvements

Possible upgrades for this project:

✔ YOLO object detection  
✔ Face recognition system  
✔ Drowsiness detection  
✔ Automatic video recording  
✔ Email or SMS alerts  
✔ Screenshot capture when motion occurs  
✔ Multi-color object detection  
✔ GUI interface for settings  

---

# 👨‍💻 Author

**Gagandeep Singh**

Computer Science Student  
Interested in **Artificial Intelligence, Computer Vision, and Automation**

---

# 📜 License

This project is **open-source and available for educational purposes.**

---

# ⭐ GitHub Repository Description

Real-time Smart Detection System using Python and OpenCV for face, eye, motion, and blue object detection with alarm alerts.

---

# 🏷 GitHub Topics

```
python
opencv
computer-vision
motion-detection
face-detection
eye-detection
color-detection
pygame
surveillance
```
