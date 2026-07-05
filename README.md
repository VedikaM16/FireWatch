# 🔥 FireWatch
Automated Wildfire Detection and Spread Prediction System

 #About
FireWatch is an end-to-end satellite-based wildfire monitoring system that detects active fires, maps burned areas, and predicts future fire spread — all visualized on a live interactive dashboard.

# Three Model Pipeline

1. YOLOv8 — Fire & Smoke Detection
- Detects active wildfire smoke from satellite imagery
- Dataset: Wildfire Smoke dataset (Roboflow Universe) — 147 validation images
- Result: mAP50 improved from 0.419 to 0.917 (119% improvement)

2. U-Net — Burned Area Segmentation
- Segments exactly which pixels are burned in a satellite image
- Dataset: Custom CEMS pipeline — 9 global wildfire events, 193 image-mask pairs
- Result: IoU 0.4011, Dice 0.5726, Recall 79.93%

3. LSTM — Fire Spread Prediction
- Predicts fire risk across all of India — daily, weekly, and monthly
- Dataset: 991,083 FSI Van Agni fire hotspot records, 3,575 India grid cells, 164 weeks
- Result: Monthly Fire F1 0.72, Weekly Fire Recall 73%, Daily Accuracy 81%

# Data Sources
- [FSI Van Agni Portal](https://fsiforestfire.gov.in) — India official fire hotspot data
- [Copernicus EMS](https://mapping.emergency.copernicus.eu) — Global burned area vector data
- [Roboflow Universe](https://universe.roboflow.com) — Wildfire smoke detection dataset
- [NASA FIRMS](https://firms.modaps.eosdis.nasa.gov) — Satellite fire hotspot data

# Tech Stack
- **Backend**: Flask (Python)
- **Frontend**: HTML5, CSS3, JavaScript
- **Maps**: Folium + Leaflet.js
- **ML**: TensorFlow, PyTorch, Ultralytics YOLOv8, segmentation-models-pytorch
- **Auth**: Flask-Login + SQLite
- **Deployment**: Render



