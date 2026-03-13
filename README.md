# Fashion Analysis AI App

AI-powered fashion analysis application combining computer vision and machine learning.

This application analyzes fashion characteristics from an uploaded image and provides interpretable results using visualization.

---

# Overview

This project is a fashion analysis system built with Python and Streamlit.

The application integrates two independent analysis pipelines:

1. **Color Analysis Pipeline**
2. **Shape Analysis Pipeline**

Each pipeline extracts different visual features from an image and produces interpretable outputs.

---

# Features

## Color Analysis

* Average color extraction from images
* Feature generation using color spaces (L*a*b and HSV)
* Personal color classification into **four seasonal types**
* Machine learning model using **RandomForest**

### Output

* Predicted personal color season
* Visualization of color features

---

## Shape Analysis

* Image preprocessing
* Contour extraction using **OpenCV**
* Clothing silhouette classification using **YOLOv8**
* Rule-based body type scoring

### Output

* Predicted silhouette category
* Body type scoring results

---

## Explainable AI

To improve interpretability, prediction results are visualized using charts.

* Visualization using **Altair**
* Interpretable prediction outputs

---

# Tech Stack

* Python
* Streamlit
* OpenCV
* scikit-learn (RandomForest)
* YOLOv8
* Altair
* NumPy
* Pandas

---

# Architecture

The system processes images through two independent pipelines.

## Color Analysis Pipeline

1. Image upload via Streamlit
2. Average color extraction
3. Feature generation (L*a*b, HSV)
4. Personal color classification using RandomForest
5. Visualization of prediction results

## Shape Analysis Pipeline

1. Image preprocessing
2. Contour extraction using OpenCV
3. Clothing silhouette classification using YOLOv8
4. Rule-based body type scoring
5. Visualization of results

---

# Project Structure

```
fashion_app
│
├ fashion_app.py                 # Streamlit application
├ season_inference.py            # Personal color inference
├ silhouette_inference_local.py  # Silhouette classification
├ extract_colors_v2.py           # Color feature extraction
├ extract_shape_features_from_image.py
│
├ season_model_rf_proba.pkl      # Trained RandomForest model
├ best.pt                        # YOLOv8 classification model
│
├ train_season_rf_proba.py       # Model training script
├ score_body_type.py             # Body type scoring logic
│
└ requirements.txt
```

---

# How to Run Locally

Install dependencies

```
pip install -r requirements.txt
```

Run the Streamlit application

```
streamlit run fashion_app.py
```

---

# Future Improvements

* Improve silhouette classification accuracy
* Expand training dataset
* Deploy the application as a web service
* Improve explainability features

---

# Author

This project was developed as part of an AI / Data Science portfolio.
