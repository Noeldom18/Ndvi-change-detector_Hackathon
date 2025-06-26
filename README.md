# 🌿 NDVI Change Detection Web App

This project provides a **Streamlit-based web app** to analyze NDVI (Normalized Difference Vegetation Index) screenshots taken from agricultural fields on two different days. It helps detect areas of **plant growth**, **stress**, and **no change** over time using image comparison.

---

## 📌 Project Purpose

To assist **farmers**, **agronomists**, and **researchers** in:

- Tracking plant health using drone NDVI screenshots
- Visually analyzing temporal changes in vegetation
- Detecting early signs of plant stress

---

## 💻 How to Run (Using Google Colab + ngrok)

This web app is designed to be run on **Google Colab**, and hosted using **ngrok** for public access.

### 🚀 Steps to Run the App:

1. **Open Google Colab**

   👉 Go to: [https://colab.research.google.com](https://colab.research.google.com)

2. **Upload Files**

   - Upload `ndvi_app.py` (main Streamlit app)
   - Paste and run the Colab setup code (provided below)

3. **Install Required Packages**

   ```bash
   !pip install streamlit opencv-python-headless matplotlib pillow pyngrok
