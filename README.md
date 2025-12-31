# 🌊 MWCNN: Multi-level Wavelet Convolutional Neural Network

<p align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white" />
  <img src="https://img.shields.io/badge/Computer_Vision-Image_Denoising-blueviolet?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Research-CVPR_Workshops-green?style=for-the-badge" />
</p>

---

## 📖 Project Overview
Traditional CNNs often use **pooling layers** to reduce image resolution, which leads to significant information loss and blurry edges. This project implements the **MWCNN (Multi-level Wavelet-CNN)** architecture, which solves this by replacing standard pooling with **Discrete Wavelet Transforms (DWT)**.

By utilizing DWT, the network can reduce feature map resolution while perfectly preserving edge details and high-frequency textures, making it a state-of-the-art solution for **Image Denoising**, **Super-Resolution**, and **Artifact Removal**.

---

## 🧠 Technical Innovation

| Feature | Conventional CNN | MWCNN (This Project) |
| :--- | :--- | :--- |
| **Downsampling** | Max-Pooling / Strided Conv | **Discrete Wavelet Transform (DWT)** |
| **Information** | Loss of high-frequency data | ** lossless frequency decomposition** |
| **Upsampling** | Deconvolution / Bilinear | **Inverse Wavelet Transform (IWT)** |
| **Artifacts** | Checkerboard/Gridding patterns | **Clean, structural reconstruction** |

### Why Wavelets?
Standard pooling treats all pixels equally. **DWT** decomposes the image into four sub-bands:
1. **LL** (Low-frequency: core structural data)
2. **LH, HL, HH** (High-frequency: edges, noise, and fine details)
This allows the model to "clean" the noise in specific frequencies without ruining the overall structure of the image.

---

## 🛠️ Tech Stack & Requirements
* **Core:** Python 3.x, PyTorch
* **Image Processing:** OpenCV, Scikit-Image, ImageIO
* **Metrics:** PSNR (Peak Signal-to-Noise Ratio) & SSIM (Structural Similarity Index)

---

***Original architecture based on the MWCNN research paper by lpj-github-io.