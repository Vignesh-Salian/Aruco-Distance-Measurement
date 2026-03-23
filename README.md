# 📏 ArUco Distance Measurement

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![OpenCV](https://img.shields.io/badge/OpenCV-4.x-green.svg?logo=opencv)](https://opencv.org/)
[![Python](https://img.shields.io/badge/Python-3.x-blue.svg?logo=python)](https://www.python.org/)

> **A real-time computer vision system for measuring the distance between ArUco markers placed on the nose and jaw regions.**

This project provides an accurate, non-invasive method for distance estimation. By leveraging **OpenCV**, **camera calibration**, and **ArUco marker detection**, it securely bridges the gap between 2D camera pixels and real-world 3D measurements. It is specifically designed to support **dental and orthodontic diagnostics**.

---

## ✨ Key Features

- **Automated Camera Calibration:** Uses chessboard images to correct camera lens distortion for highly accurate measurements.
- **Custom Marker Generation:** Easily generate specific ArUco markers (IDs 23, 24, 25) for physical placement.
- **Real-Time Detection:** Live tracking of ArUco markers directly from a standard camera feed.
- **Precision Distance Calculation:** Automatically computes the real-world distance (in millimeters) between the nose and jaw markers.
- **Dynamic Visualization:** Displays a live, annotated overlay of the distance directly on the video stream.
- **Data Export:** Automatically saves the results as processed images and graphs for easy review.

---

## 📂 Repository Structure

<div align="center">
  <img width="802" height="446" alt="Repository Structure" src="https://github.com/user-attachments/assets/2bd53e73-f529-45ad-9539-119d82802d46" />
</div>

---

## 🚀 Installation & Setup

### 1. Clone the Repository
Ensure you have Python installed, then setup the project:
```bash
git clone https://github.com/salianvignesh05-droid/Aruco-Distance-Measurement.git
cd Aruco-Distance-Measurement
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Run the System

The project is broken down into three simple steps:

- **Step 1: Calibrate the Camera** (Required for accuracy)
  ```bash
  python calibration.py
  ```
- **Step 2: Generate ArUco Markers** (To print and use)
  ```bash
  python generate_aruco.py
  ```
- **Step 3: Run Distance Measurement** (Live detection)
  ```bash
  python distance_calculation.py
  ```

---

## 📊 Results & Outputs

### 1. System Architecture
Our pipeline processes the live feed, detects the markers, applies camera calibration math, and outputs the final distance.
![System Architecture](results/system_architecture.png)

### 2. Camera Calibration
![Chessboard Calibration](results/chessboard_calibration.png)

### 3. ArUco Markers
![ArUco Markers](results/aruco_markers.png)

### 4. Real-time Measurement
![Real-time Demo](results/real_time_demo.png)

---

## 📜 License
This project is licensed under the **MIT License** – see the [LICENSE](LICENSE) file for details.

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







