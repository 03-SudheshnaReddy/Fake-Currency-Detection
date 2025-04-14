#  Fake Currency Detection using Image Processing + KNN Model

A robust machine learning and image processing pipeline to detect **counterfeit currency** through visual feature analysis and **K-Nearest Neighbors (KNN)** classification. Deployed as a full-stack Flask web app with support for real-time image uploads and instant feedback.

---

##  Overview

This project analyzes and classifies currency notes as **real or fake** by combining:

-  Traditional image processing (OpenCV + NumPy)
-  Region-based feature extraction
-  KNN classification using extracted features
-  Full-stack web deployment (HTML/CSS/JS + Flask backend)

>  We assess security features like transparent strips, Gandhiji watermark, serial numbers, and security lines, and then classify using pixel-level intensity metrics or a trained machine learning model.

---

## Methodologies Used

### 1.  Image Processing (Baseline)
- **Thresholding & Morphological Filtering** to isolate specific regions.
- **ROI Analysis**: Transparent strip, Gandhiji watermark, serial number zone.
- **Pixel intensity comparison** between user-uploaded and known real note samples.

### 2. KNN Classifier (Advanced)
- Features like **mean intensity**, **edge density**, and **contour count** extracted from each region.
- KNN model trained on labeled feature sets (real vs fake) for multiple denominations.
- Outputs binary classification: `Real` or `Fake`.

---

##  Web Deployment

The project is deployed using Flask and supports real-time user uploads.

### How to Run:

1. Clone the repo and install dependencies:
   ```bash
   git clone https://github.com/your-username/fake-currency-detector.git
   cd fake-currency-detector
   pip install -r requirements.txt
   ```

2. Run the Flask app:
   ```bash
   python app.py
   ```

3. Open `http://localhost:5000` in your browser.

4. Upload any note image via the Detector page — the result will be displayed instantly.

---

## Website demo
![image](https://github.com/user-attachments/assets/e3181104-c7e7-4ba7-b736-97299e1ac50d)
![image](https://github.com/user-attachments/assets/401f358f-de8f-44a1-af63-ca6e9c5a262e)
![image](https://github.com/user-attachments/assets/d174a06c-b8e9-4bec-a547-dcb3405d66af)

----

##  Output Metrics

- **Prediction (Real/Fake)**
- **Denomination Detection**
- **Audio saying fake/real**
- **Region-wise Comparison**
- **KNN Confidence Score** (if applicable)

---

##  Tech Stack

- **Frontend**: HTML, CSS, JavaScript
- **Backend**: Flask (Python)
- **Libraries**: OpenCV, NumPy, Pandas, Scikit-learn, Matplotlib
- **OCR**: Tesseract (for serial numbers and printed text)

---

##  Use Cases

- Retail currency verification systems
- Banknote counterfeiting detection in ATMs
- Visual quality control in printing presses

---

##  Future Work

-  Mobile app integration for instant camera-based verification
-  Add user authentication and history dashboard
-  Use real-world datasets with more variation in lighting, rotation, etc.

---

## 🤝 Contribution

Contributions are welcome! Fork the repo, improve it, and create a PR.

---
