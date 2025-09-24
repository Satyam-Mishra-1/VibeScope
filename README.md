# 🎥 Video-Based Motion Amplification and Vibration Analysis

This repository contains the codebase that under the problem statement **PS1415**.  

It enables motion magnification and vibration analysis from videos, allowing engineers, researchers, and data scientists to detect subtle movements, extract vibration signals, and perform quantitative analysis.  

---

## 🚀 Features

- ✅ **Self-supervised motion magnification** (no manual labeling required)  
- ✅ **Targeted magnification** using bounding boxes  
- ✅ **Optical flow-based amplification**  
- ✅ **Vibration analysis** via FFT and time-series graphs  
- ✅ **3D graph plotting** and **heatmap visualization**  
- ✅ **Region of Interest (ROI)-based graph generation**  
- ✅ Support for **multiple amplification settings**  

---

## 🛠 Tech Stack

**Languages & Frameworks**
- Python (main implementation)  
- PyTorch (deep learning & optical flow models)  
- OpenCV (image/video processing)  
- NumPy / SciPy (signal processing, FFT)  

**Visualization & Reporting**
- Matplotlib, Seaborn (static plots)  
- Plotly (interactive 3D heatmaps, dynamic graphs)  

**Data Science Tooling**
- Pandas (ROI metadata storage & experiment tracking)  
- Scikit-learn (optional preprocessing, filtering, baseline comparisons)  
- Jupyter Notebooks (exploratory analysis & prototyping)  

---

## 🧠 Implementation Details (Data Science Perspective)

### 1. **Data Acquisition & Preprocessing**
- Input: Raw videos (MP4, AVI, etc.).  
- Extract frames with OpenCV.  
- Apply preprocessing:
  - Resizing frames to fixed resolution  
  - Normalization of pixel values  
  - ROI extraction for focused analysis  

### 2. **Feature Extraction (Motion Estimation)**
- Use **optical flow** (deep learning–based and classical) to capture subtle pixel displacements.  
- Represent motion as **flow vectors** over time → forms the feature space for vibration analysis.  

### 3. **Motion Magnification**
- Apply **self-supervised motion magnification**:
  - Backpropagation through optical flow  
  - Amplification factors (tunable hyperparameters)  
- Supports **localized bounding boxes** to magnify only target areas.  

### 4. **Signal Processing Pipeline**
- Convert extracted motion signals into **time-series data**.  
- Apply:
  - **Fast Fourier Transform (FFT):** frequency spectrum of vibrations  
  - **Band-pass filters:** remove noise, focus on structural vibration ranges  
  - **Spectral analysis:** detect resonance peaks & anomalies  

### 5. **Vibration Analysis & Graphs**
- Generate:
  - **Time-domain vibration plots** (displacement over time)  
  - **Frequency-domain FFT plots** (dominant frequencies)  
  - **3D vibration maps & heatmaps** (spatial vibration patterns across the structure)  
- ROI-specific plots for **localized defect detection**.  

### 6. **Data Considerations**
- **Data Validation:** Outlier removal & noise filtering on signals.  
- **Experiment Tracking:** Metadata stored for different runs (ROI, amplification factor, FFT params).  
- **Scalability:** Supports batch video processing for larger datasets.  
- **Interpretability:** Visualizations directly map signals to real-world physical vibrations → helps in predictive maintenance.  

