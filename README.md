<h1 align="center">📄 Document Scanner CV</h1>

<p align="center">
  <img src="https://img.shields.io/badge/OpenCV-4.11.0-blue?style=for-the-badge&logo=opencv"/>
  <img src="https://img.shields.io/badge/Python-3.10-yellow?style=for-the-badge&logo=python"/>
  <img src="https://img.shields.io/badge/NumPy-2.0.0-orange?style=for-the-badge&logo=numpy"/>
</p>

<p align="center">
  Transform any phone photo of a document into a clean, flat, scanned output — using pure classical Computer Vision. No deep learning. Just math.
</p>

---

## 🎯 Demo

| Input (Phone Photo) | Output (Scanned) |
|---|---|
| <img src="https://github.com/user-attachments/assets/b656b710-3892-41ea-8b82-58cbf93e011e" width="350"/> | <img src="https://github.com/user-attachments/assets/073f3c98-b568-45da-bc54-37879666edf3" width="350"/> |

---

## ⚙️ Pipeline
```
📷 Input → 🔲 Resize → ⚫ Grayscale → 🌫️ Blur → 🔍 Canny → 📐 Contours → 🔷 4-Point → 🪄 Warp → 📄 Threshold
```

---

## 🧠 Key Concepts

- **Contour Detection** — `findContours` + `approxPolyDP` to find the document boundary
- **Perspective Transform** — `getPerspectiveTransform` + `warpPerspective` to flatten the document
- **Adaptive Thresholding** — `adaptiveThreshold` to handle uneven lighting

---

## 🚀 Installation
```bash
git clone https://github.com/YOURUSERNAME/document-scanner-cv.git
cd document-scanner-cv
```

## ▶️ Usage
```bash
open in google colab documentScanner.ipynb 
```

---

## 📁 Project Structure
```
document-scanner-cv/
├── document_scanner.py
├── data/
│   └── Image1.jpg
│   └── Image3.jpg
│   └── Image4.jpg
├── demo/
│   └── scanned_output1.jpg
|    └── scanned_output3.jpg
|    └── scanned_output4.jpg
├── LEARNING.md
└── README.md
```

---

## 💡 What I Learned

- How `approxPolyDP` simplifies noisy contours to exactly 4 corner points
- Why corner ordering (top-left → top-right → bottom-right → bottom-left) is critical before warping
- How adaptive thresholding handles uneven lighting better than global threshold
- Why edge detection should be done on resized image but warp applied on original full-res image

---


<p align="center">Made with ❤️ by <a href="https://github.com/samy1406">Samy1406</a></p>
