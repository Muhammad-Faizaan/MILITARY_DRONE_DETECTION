### MILITARY_DRONE_DETECTION   
RealTime Military UAV Threat Identification with YOLO11  

Author: **Muhammad Faizaan – Initiator of FΛVEN INTELLIGENCE (FΛVI)**  

---

## 🔎 Overview
**MILITARY_DRONE_DETECTION** is a specialized AI-powered system for detecting and classifying **military drones** in real time.  
Unlike consumer drone detection, this project focuses on **combat UAVs, reconnaissance platforms, and loitering munitions** — addressing a critical defense technology challenge.  

Built on **YOLO11n**, fine-tuned with a **synthetic dataset of 14 UAV types**, the system achieves high precision and recall while maintaining ultra-fast inference speeds suitable for operational deployment.

---

## ✨ Features
- **Specialized Military UAV Detection** – Shahed, Lancet, Orlan, ZALA, Forpost, Mohajer, Granat, SuperCam, Techyon, DJI Mavic 3.  
- **Synthetic Dataset Training** – Blender-generated imagery with perfect annotations.  
- **Real-Time Performance** – GPU-accelerated inference (~370 FPS on RTX 4060).  
- **Multi-Modal Interface** – Image upload, video processing, and live webcam surveillance.  
- **Streamlit Web App** – Intuitive control panel with confidence threshold adjustment.  
- **Robust Against False Positives** – Configurable thresholds to ignore birds and non-UAV aerial objects.  

---

## 📊 Performance Metrics
| Metric        | Score   |
|---------------|---------|
| mAP50         | 94.8%   |
| mAP50-95      | 76.1%   |
| Precision     | 95.6%   |
| Recall        | 90.7%   |
| Inference Speed | 2.7ms (GPU) |

> Recommended confidence threshold: **0.40** to eliminate false positives.

---

## ⚙️ Tech Stack
- **YOLO11n** – Nano variant optimized for speed/accuracy balance  
- **PyTorch** – Deep learning backend  
- **OpenCV** – Video I/O and visualization  
- **Streamlit** – Web interface for deployment  
- **Blender Synthetic Dataset** – Perfectly annotated training data  

---

## 🚀 Getting Started
### 1. Clone the Repository
```bash
git clone https://github.com/Muhammad-Faizaan/MILITARY_DRONE_DETECTION.git
cd MILITARY_DRONE_DETECTION
```

### 2. Setup Environment
```bash
pip install uv
uv venv
source .venv/bin/activate   # Mac/Linux
.\.venv\Scripts\activate    # Windows
uv pip install ultralytics opencv-python streamlit pillow kaggle
```

### 3. Download Dataset
```bash
kaggle datasets download -d banderastepan/drone-detection
unzip drone-detection.zip -d drone-detection
```

### 4. Train the Model
```bash
python main.py
```

### 5. Launch the Application
```bash
streamlit run app.py
```
Access at: **http://localhost:8501**

---

## 📂 Project Structure
```
MILITARY_DRONE_DETECTION/
├── app.py                  # Streamlit web application
├── main.py                 # Training pipeline
├── inspect_dataset.py      # Dataset analyzer
├── drone-detection/        # Kaggle dataset
├── military-drones-dataset # Prepared training dataset
├── results/                # Training outputs
│   └── military_drone_model/
│       ├── weights/best.pt
│       ├── results.png
│       ├── confusion_matrix.png
│       └── F1_curve.png
```

---

## 🖼️ Demo Media
### 📸 Image Detection Example

<img width="1920" height="921" alt="app_interface" src="https://github.com/user-attachments/assets/f0b07620-a646-4eeb-854c-333dcb8bf8cf" />
<img width="1920" height="920" alt="drone_detection" src="https://github.com/user-attachments/assets/a53a9d09-e8bf-4ef6-aaaf-d5eacb4f3fc2" />
<img width="1917" height="920" alt="no_detection" src="https://github.com/user-attachments/assets/3519329e-ab76-4a53-bee4-041a329f4e19" />


### 🎥 Video Processing Example
https://github.com/user-attachments/assets/834f4e58-fdd0-411c-a684-3ae49639ed17
---

## 🔮 Future Enhancements
- Multi-object tracking for continuous UAV monitoring  
- Radar/acoustic sensor integration  
- Real-time alert system with configurable triggers  
- Thermal/IR camera support for night ops  
- Edge deployment (Jetson, Coral TPU)  
- Multi-class detection (specific UAV type classification)  
- Geospatial tracking and distributed detection networks  

---

## ⚠️ Operational Considerations
This project is for **educational and research purposes**.  
Deployment in defense systems requires:  
- Validation on real-world imagery  
- Integration with command & control systems  
- Extensive field testing  
- Compliance with regulations and protocols  
- Regular updates for new UAV types  

---

## 📜 License
MIT License – Free to use, modify, and distribute with attribution.  

---

## 🙏 Acknowledgments
- **Ultralytics** – YOLO11 implementation  
- **banderastepan** – Synthetic military drone dataset  
- **Streamlit** – Rapid ML deployment framework  
- **OpenCV & PyTorch communities** – Advancing computer vision  

---

### 🛡️ Founder’s Note
This repository reflects my vision as **Initiator of FΛVEN INTELLIGENCE (FΛVI)**:  
to push boundaries in **AI-driven defense technology**, blending **technical mastery** with **futuristic branding**. Every detail is engineered for precision, speed, and impact.  

---
```
