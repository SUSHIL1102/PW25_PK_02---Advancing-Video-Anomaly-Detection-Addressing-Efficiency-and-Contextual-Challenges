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
