# Computer Vision Image Enhancement

Implementation of image enhancement techniques using Python, NumPy,
Matplotlib, and frequency-domain processing.

## 📌 Project Overview

This project implements two image enhancement techniques:

1. **High-Boost Filtering**
2. **Adaptive Local Gamma Enhancement**

The project demonstrates how images can be processed in both the
**spatial domain** and **frequency domain**.

---

## 🔹 1. High-Boost Filtering

High-boost filtering enhances high-frequency components such as edges
and fine details while retaining information from the original image.

### Process

Original Image  
↓  
2D Fourier Transform (FFT)  
↓  
FFT Shift  
↓  
High-Pass Mask  
↓  
Frequency-Domain Filtering  
↓  
Inverse FFT  
↓  
High-Frequency Component  
↓  
Sharpened Image  
↓  
High-Boost Image

### Formula

\[
f_{hb} = (A-1)f_{orig} + f_{sharpened}
\]

### Concepts Used

- Spatial Domain
- Frequency Domain
- 2D FFT
- FFT Shift
- Frequency Masking
- High-Pass Filtering
- Inverse FFT
- Image Sharpening
- High-Boost Filtering

---

## 🔹 2. Adaptive Local Gamma Enhancement

Adaptive local enhancement improves image brightness by applying
different gamma values to different regions of an image.

The image is divided into local regions and the mean intensity of
each region is calculated.

- Dark regions → γ < 1 → Brightening
- Bright regions → γ > 1 → Darkening

### Gamma Transformation

\[
s = r^\gamma
\]

where pixel values are normalized to the range [0, 1].

### Process

Original Image  
↓  
Divide into Local Regions  
↓  
Calculate Mean Intensity  
↓  
Determine Dark/Bright Region  
↓  
Select Gamma Value  
↓  
Apply Gamma Correction  
↓  
Reconstruct Enhanced Image

---

## 🛠️ Technologies Used

- Python
- NumPy
- Matplotlib
- Scikit-image
- Jupyter Notebook

## 📂 Project Structure

```text
computer-vision-image-enhancement/
│
├── Image_Enhancement.ipynb
├── README.md
└── requirements.txt
