# Stage 1 – Object-Based Anomaly Detection (Fire, Smoke, Gun)

This repository contains the **Stage 1 pipeline** of our Video Anomaly Detection project.  
Stage 1 uses a **custom-trained YOLOv8 model** to detect **object-based anomalies** that can be recognized without temporal context, namely:

- 🔥 Fire  
- 💨 Smoke  
- 🔫 Guns  

Videos that do not trigger Stage 1 detections are passed to **Stage 2** (contextual anomaly detection, ongoing).

---

✅ Quick Checklist

- Run the notebook if you want to understand training + pipeline.

- Use best.pt directly if you only want inference.

- Check results/ for sample outputs.


## 📝 What’s Inside the Notebook?

The notebook (`stage_1_new_workspace.ipynb`) walks through the **entire Stage 1 workflow** step by step:

### 1. Imports & Setup
- Installs and imports required libraries (**Ultralytics YOLOv8, OpenCV, Roboflow**, etc.).

### 2. Dataset Preparation
- Loads custom dataset (**MSAD + Fire-SM + additional sources**).  
- Preprocessing: resizing, frame extraction, augmentations.  
- Defines class labels: `['fire', 'smoke', 'gun']`.

### 3. Training the Model
- Trains **YOLOv8** on curated dataset.  
- Logs metrics (**mAP, precision, recall**).  
- Saves trained weights as `best.pt`.

### 4. Testing & Evaluation
- Runs inference on test images/videos.  
- Generates bounding boxes with class labels and confidence scores.  
- Saves annotated outputs in the **`results/`** folder.

### 5. Analysis
- Compares detections across multiple test videos.  
- Fine-tunes thresholds for optimal anomaly flagging.
