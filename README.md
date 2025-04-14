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

##  Project Structure

```
├── dataset/                         # Image datasets (real & fake notes)
├── rois/                            # Region of Interest for feature extraction
├── KNN/
│   ├── extracted_features_200.xlsx # Feature matrix for training
│   ├── extracted_features_500.xlsx # Extended feature matrix
│   ├── knn_currency_model.pkl      # Trained KNN model
│   ├── KNN.ipynb                   # Notebook to train and test KNN
│   ├── tempCodeRunnerFile.py       # Local test script
├── DATSET_PREP.ipynb               # Notebook for image preprocessing
├── app.py                          # Flask app to integrate frontend and backend
├── denomination.py                 # Extract denomination & reference image setup
├── project.py                      # Main image processing pipeline
├── .venv/                          # Virtual environment (ignored in `.gitignore`)
├── README.md                       # This file
```

---

## 🧠 Methodologies Used

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
