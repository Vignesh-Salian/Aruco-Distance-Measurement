# 📏 ArUco Spatial Tracker: Precision Distance Measurement

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![OpenCV](https://img.shields.io/badge/OpenCV-4.x-green.svg?logo=opencv)](https://opencv.org/)
[![Python](https://img.shields.io/badge/Python-3.x-blue.svg?logo=python)](https://www.python.org/)

> **A real-time computer vision pipeline for Euclidean distance estimation between anthropometric landmarks using ArUco fiducial markers.**

This system bridges the gap between 2D pixel space and 3D physical reality. By leveraging camera calibration and Perspective-n-Point (PnP) pose estimation, it performs non-invasive, sub-millimeter accurate distance calculations—specifically optimized for diagnostic use-cases like measuring inter-segmental shifts in the nose and jaw regions.

---

## ✨ System Highlights

- **Intrinsic Calibration Engine:** Mitigates radial and tangential lens distortion utilizing Zhang's Method via Chessboard grid analysis.
- **Robust Fiducial Tracking:** Real-time localization and decoding of specific ArUco markers (Target IDs: 23, 24, 25), optimized for stability under varying ambient lighting.
- **Dynamic 3D Visualization:** Real-time projection of coordinate axes ($R^3$ space) and physical distance vectors ($d = \sqrt{\Delta x^2 + \Delta y^2 + \Delta z^2}$).
- **Data Analytics:** Automated temporal distance logging, with results systematically stored as processed images and graphs.

---

## 🏗 Architecture & Workflow

The pipeline is modularized into three optimization phases to ensure maximum reproducibility:

1. **Geometric Calibration Phase:** Corrects optical aberrations and establishes the foundational focal length.
2. **Generative Synthesis:** Scripted generation of high-contrast, edge-defined markers.
3. **Inference Engine:** Low-latency frame processing, sub-pixel corner refinement, and spatial calculation.

<div align="center">
  <img width="802" alt="System Architecture Diagram" src="https://github.com/user-attachments/assets/2bd53e73-f529-45ad-9539-119d82802d46" />
</div>

---

## 🚀 Getting Started

### Prerequisites
Ensure a Python environment is configured with the necessary numerical and vision dependencies.

```bash
# Clone the repository
git clone https://github.com/salianvignesh05-droid/Aruco-Distance-Measurement.git
cd Aruco-Distance-Measurement

# Install dependencies
pip install -r requirements.txt
```

### Execution Pipeline

**Phase I: Camera Calibration**
> Derive the camera's intrinsic parameters through grid analysis.
```bash
python calibration.py
```

**Phase II: Fiducial Generation**
> Generate the specified ArUco markers for the physical anchor points.
```bash
python generate_aruco.py
```

**Phase III: Real-Time Inference**
> Execute the primary visual tracking and distance calculation loop.
```bash
python distance_calculation.py
```

---

## 📊 Evaluation & Results

<table>
  <tr>
    <td align="center"><b>Calibration Precision</b><br>Robust calibration with low re-projection error.</td>
    <td align="center"><b>Marker Localization</b><br>Stable corner subsets with high confidence scores.</td>
  </tr>
  <tr>
    <td><img src="results/chessboard_calibration.png" alt="Chessboard Calibration" width="400"/></td>
    <td><img src="results/aruco_markers.png" alt="ArUco Markers" width="400"/></td>
  </tr>
  <tr>
    <td align="center" colspan="2"><b>Real-time Vector Analysis</b><br>Translational distance plotted simultaneously on the video stream.</td>
  </tr>
  <tr>
    <td align="center" colspan="2"><img src="results/real_time_demo.png" alt="Real-time Demo" width="600"/></td>
  </tr>
</table>

---

## 🔍 Theoretical Methodology

The physical distance calculation relies on resolving perspective projection. For two markers $M_1$ and $M_2$:
1. **Corner Detection:** Isolate 2D image coordinates $\{c_{i,1}, c_{i,2}, c_{i,3}, c_{i,4}\}$ for both markers.
2. **Pose Estimation (PnP):** Compute the rotation vector ($rvec$) and translation vector ($tvec$) relative to the camera center.
3. **Transformation:** Map local marker coordinate systems into a unified world coordinate standard.
4. **Euclidean Metric:** Calculates the $L_2$ norm representing the absolute 3D physical distance across space between the centroids of $M_1$ and $M_2$.

---

## 📜 License
Distibuted under the **MIT License**. See `LICENSE` for more detailed specifications.

---

## 👨‍💻 Author

<div align="center">
  <h3>Vignesh N Salian</h3>
  <p>📍 Udupi, Karnataka, India</p>
  <a href="https://github.com/salianvignesh05-droid">
    <img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"/>
  </a>
  <a href="https://www.linkedin.com/in/vignesh-n-salian">
    <img src="https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white" alt="LinkedIn"/>
  </a>
</div>




