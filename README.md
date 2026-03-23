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

## 💻 Technologies Used

- **Language:** [![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org/)
- **Core Library:** [![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)](https://opencv.org/)
- **Numerical Computation:** [![NumPy](https://img.shields.io/badge/Numpy-777BB4?style=flat-square&logo=numpy&logoColor=white)](https://numpy.org/)

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

<table>
  <tr>
    <td align="center"><b>1. System Architecture</b><br>Pipeline for live feed processing and distance calculation.</td>
    <td align="center"><b>2. Camera Calibration</b><br>Using chessboard pattern for intrinsic parameters.</td>
  </tr>
  <tr>
    <td><img src="results/system_architecture.png" alt="System Architecture" width="400"/></td>
    <td><img src="results/chessboard_calibration.png" alt="Chessboard Calibration" width="400"/></td>
  </tr>
  <tr>
    <td align="center"><b>3. ArUco Markers</b><br>Custom detection for IDs 23, 24, 25.</td>
    <td align="center"><b>4. Real-time Measurement</b><br>Live overlay of physical distance vector.</td>
  </tr>
  <tr>
    <td><img src="results/aruco_markers.png" alt="ArUco Markers" width="400"/></td>
    <td><img src="results/real_time_demo.png" alt="Real-time Demo" width="400"/></td>
  </tr>
</table>

---

## 📜 License
This project is licensed under the **MIT License** – see the [LICENSE](LICENSE) file for details.

---

## 🧑‍💻 Author

<a href="https://github.com/salianvignesh05-droid">
  <img src="https://img.shields.io/badge/VIGNESH%20SALIAN-DEVELOPER-0084c8?style=for-the-badge&logo=github&labelColor=555555" alt="Vignesh Salian GitHub">
</a>
<br>
<a href="https://github.com/salianvignesh05-droid">
  <img src="https://img.shields.io/github/followers/Vignesh-Salian?label=Follow&style=social" alt="GitHub Followers"/>
</a>







