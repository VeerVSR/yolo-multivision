# YOLO Multi-Vision System 🎯

![Python](https://img.shields.io/badge/Python-3.10-blue?style=flat&logo=python)
![YOLOv8](https://img.shields.io/badge/YOLO-v8-purple?style=flat)
![OpenCV](https://img.shields.io/badge/OpenCV-Computer%20Vision-green?style=flat&logo=opencv)

A real-time computer vision system using **YOLOv8** and **OpenCV** that supports multiple visual modes from a **single webcam and a single model**.

This project combines multiple vision simulations (such as Thermal and Night Vision) into **one clean, scalable Python program**.

---

## ✨ Features

- ✅ **Real-time Detection:** Powered by Ultralytics YOLOv8  
- 🎥 **Resource Efficient:** Uses a single webcam stream and a single loaded model instance  
- 🔁 **Instant Switching:** Toggle between vision modes instantly using keyboard shortcuts  
- 🧠 **Clean Architecture:** Modular code structure for easy expansion  
- 💾 **Recording:** Optional capability to save the output to video  
- 🪟 **Cross-Platform:** Windows, macOS, and Linux ready  

---

## 👁️ Vision Modes & Controls

The application captures the video feed and applies different color maps and processing logic based on the selected mode.

| Key | Mode | Description |
|---|---|---|
| `1` | **Normal Vision** | Standard RGB video feed with YOLO detections |
| `2` | **Grayscale Vision** | High-contrast black and white mode |
| `3` | **Thermal Vision** | Simulated thermal heat map (JET colormap) |
| `4` | **Night Vision** | Simulated green-tinted low-light amplification |
| `Q` | **Quit** | Close the application |

---

## 🛠️ Tech Stack

- **Python 3.10+**
- **Ultralytics YOLOv8** (Object Detection)
- **OpenCV** (Image Processing)
- **NumPy** (Matrix operations)

---

## 📂 Project Structure
```
yolo-multivision/
├── yolo_multivision.py # Main application logic
├── requirements.txt # Dependencies
├── .gitignore # Ignored files (envs, weights, videos)
└── README.md # Project documentation
```

---

## 🚀 Installation & Setup

### 1️⃣ Clone the repository
```bash
git clone https://github.com/YOUR_USERNAME/yolo-multivision.git
cd yolo-multivision
```
### 2️⃣ Install dependencies
It is recommended to use a virtual environment.
pip install -r requirements.txt

### 3️⃣ Run the project
python yolo_multivision.py
Note: On first run, YOLOv8 will automatically download the required weight file (yolov8n.pt).

## ⚙️ Configuration
You can tweak the settings directly inside yolo_multivision.py.

### 💾 Video Recording
To save your session to a file (output_multivision.avi), change the flag at the top of the script:
```bash
save_video = True  # Set to False to disable recording 
```

### 📷 Camera Source
By default, the script uses the primary webcam (index 0).
For an external USB camera, change to:
```bash
cap = cv2.VideoCapture(1)
```

## 🧠 Learning Goals
This project demonstrates:
```
Resource Sharing: Handling a single AI model and camera stream across different logical modes
Computer Vision Pipelines: Building real-time pipelines with OpenCV
State Management: Implementing a mode-based system design
Workflow: Establishing a clean Git & GitHub workflow
```

### 🔮 Future Improvements
```
⬜ Object tracking with unique IDs
⬜ FPS optimization and on-screen display
⬜ Voice control for switching modes
⬜ Autonomous detection triggers
⬜ Modular plugin-based effects system
```
