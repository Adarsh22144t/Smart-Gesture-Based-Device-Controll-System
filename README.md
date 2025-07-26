# Smart Gesture-Based Device Control System

A real-time gesture-controlled interface to replace traditional mouse and keyboard inputs. The system leverages MediaPipe, U-Net, and Pynput in a unified pipeline for robust and contactless human-computer interaction (HCI).

![Uploading image.png…]

## 👨‍💻 Authors
- Shaik Sadik (22341A05G2)  
- S. Adarsh (22341A05F4)  
- V. Varshini (22341A05J4)  
- Shaik Sumsuddin (22341A05G3)

**Guide:** Mr. G. Dharma Raju (Asst. Professor, GMR Institute of Technology)

---

## 📖 Abstract

Touchless systems have become a necessity for hygienic and intuitive interaction. This project implements a lightweight yet versatile hand gesture control system that supports:
- Mouse movements
- Virtual keyboard typing
- System actions like clicks and scrolls

Unlike traditional models relying on heavy deep learning architectures, our approach uses efficient methods suitable for low-power devices.

---

## 🎯 Features

- Real-time hand tracking and gesture recognition  
- Mouse and keyboard emulation  
- Works in varying light conditions and hand orientations  
- Modular pipeline for future enhancements (like facial recognition)  

---

## 🧠 Technologies Used

- Python
- OpenCV
- MediaPipe
- PyAutoGUI / Pynput
- U-Net (for image denoising)
- BlazePose (for localization)
- Vision Transformer (for noise addition)

---

## ⚙️ System Workflow

### General Workflow Diagram
![General Workflow](general_workflow.png)

1. **Live Feed** is captured via camera  
2. **Vision Transformer** adds noise to simulate challenging environments  
3. **U-Net** denoises the image for better localization  
4. **MediaPipe** detects hand keypoints  
5. **Pynput** maps gestures to mouse/keyboard events  

---

## 🧪 Methodology

### Methodology 1 – Localization (BlazePose)
- Uses BlazePose + CNN to predict bounding boxes  
- Optimizes Region of Interest (ROI) for gesture detection  
![Localization Diagram](methodology_1.png)

### Methodology 2 – Image Denoising (U-Net)
- Adds Gaussian noise → Encodes → Decodes using U-Net  
- Enhances image clarity before gesture detection  
![Denoising Diagram](methodology_2.png)

### Methodology 3 – Gesture Mapping (MediaPipe + Pynput)
- Tracks hand landmarks  
- Identifies gesture states (e.g., fingers up/down)  
- Triggers cursor/keyboard actions via Pynput  
![Gesture Mapping Diagram](methodology_3.png)

---

## 📊 Results

### Inference Speed
![Inference Speed Graph](inference_times.png)

### Model Performance
- **MediaPipe** consistently outperformed YOLO/DETR in latency and stability  
- **U-Net** denoising improves gesture localization accuracy  

![Performance Metrics](performance_metrics.png)  
![Denoising Model Results](denoising_results.png)

---

## 💡 Conclusion

Our system integrates localization, denoising, and gesture detection into a seamless pipeline for robust gesture-based interaction. Key highlights:

- Real-time operation with low latency  
- Works even on laptops without GPU  
- Applications: Smart home, assistive tech, VR/AR, education  

### 🔮 Future Enhancements
- Multi-user tracking  
- Gesture personalization (adaptive learning)  
- Integration with drawing/game/presentation tools  

---

## 📷 Screenshots / Demo (Add your images here)

- `live_feed_sample.png` – Sample input from webcam  
- `detected_gesture.png` – Gesture with bounding box  
- `keyboard_typing.png` – Virtual keyboard control  
- `cursor_control.png` – Mouse control using hand gestures  

---

## 📦 How to Run

```bash
git clone https://github.com/Adarsh22144t/Smart-Gesture-Based-Device-Controll-System.git
cd Smart-Gesture-Based-Device-Controll-System
pip install -r requirements.txt
python gesture.py
