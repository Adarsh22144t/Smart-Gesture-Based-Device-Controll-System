# Smart Gesture-Based Device Control System

> 🧭 **Motto:** Designed to empower **physically challenged individuals** by enabling **touch-free, intuitive control** of digital devices using simple hand gestures.  
> This project promotes **accessibility**, **inclusivity**, and **independence** through technology.

---

A real-time gesture-controlled interface to replace traditional mouse and keyboard inputs. The system leverages MediaPipe, U-Net, and Pynput in a unified pipeline for robust and contactless human-computer interaction (HCI).

<img width="536" height="445" alt="image" src="https://github.com/user-attachments/assets/f954c312-e9bf-4fd5-bf35-787255a19d59" />


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
<img width="745" height="522" alt="image" src="https://github.com/user-attachments/assets/0190eba8-566d-4f53-8e5a-1b8c22e72e35" />


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
<img width="733" height="459" alt="image" src="https://github.com/user-attachments/assets/909afbf1-1317-4294-842e-c999f9f8c5d8" />


### Methodology 2 – Image Denoising (U-Net)
- Adds Gaussian noise → Encodes → Decodes using U-Net  
- Enhances image clarity before gesture detection  
<img width="748" height="457" alt="image" src="https://github.com/user-attachments/assets/d3a8df12-2fe5-41e6-8a62-9644e0e444f1" />


### Methodology 3 – Gesture Mapping (MediaPipe + Pynput)
- Tracks hand landmarks  
- Identifies gesture states (e.g., fingers up/down)  
- Triggers cursor/keyboard actions via Pynput  
<img width="746" height="461" alt="image" src="https://github.com/user-attachments/assets/bdd8e725-9121-417a-9619-3875838721c4" />


---

## 📊 Results

### Inference Speed
<img width="735" height="474" alt="image" src="https://github.com/user-attachments/assets/d2f5a2d3-cf5f-4060-9290-8650fd33a14d" />


### Model Performance
- **MediaPipe** consistently outperformed YOLO/DETR in latency and stability  
- **U-Net** denoising improves gesture localization accuracy  
<img width="727" height="342" alt="image" src="https://github.com/user-attachments/assets/5027ee3b-74a1-4d28-8f1f-46744c69304b" />

<img width="721" height="368" alt="image" src="https://github.com/user-attachments/assets/f17244d2-0555-461a-ba36-13305bd5a6be" />


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


