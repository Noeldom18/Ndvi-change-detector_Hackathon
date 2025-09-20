# 🌱 Crop Field Analysis using Deep Learning

## 📌 Project Overview
This project applies **Computer Vision and Machine Learning** to analyze crop fields using **RGB and Multispectral images**.  
The objective is to detect crop health variations and support **precision farming** by enabling data-driven decision-making.  

By leveraging **YOLOv8**, the model learns features from crop images (color, texture, spectral signatures) and maps them into numerical values for training and prediction.  
The system also integrates with a **Streamlit web app** for easy NDVI estimation and visualization.

---

## 🎯 Objectives
- Detect crop regions and classify health conditions using drone imagery.  
- Compare the effectiveness of **RGB vs Multispectral** data for crop monitoring.  
- Provide an end-to-end tool for **NDVI estimation and precision agriculture**.  

---

## 🚀 Methodology

1. **Data Collection & Preprocessing**
   - Drone-based **RGB and Multispectral images** captured from crop fields.  
   - Used **PIX4Dfields** trial version to generate NDVI ground-truth maps.  
   - Preprocessing steps included resizing, normalization, and data augmentation.  

2. **Model Training**
   - Adapted **YOLOv8** as a feature extractor.  
   - Mapped image features to NDVI values using supervised regression.  
   - Training executed in **Google Colab** with GPU acceleration.  

3. **Evaluation**
   - Metrics: **Precision, Recall, F1-score, RMSE (for NDVI regression)**.  
   - Compared NDVI predicted by the model with NDVI obtained via PIX4Dfields.  

4. **Deployment**
   - Developed a **Streamlit web app** where users upload drone images.  
   - The trained AI model processes images and outputs **NDVI index values**.  

---

## 📊 Results
- The model successfully learned to predict NDVI from both RGB and Multispectral images.  
- **Multispectral input improved prediction accuracy** compared to RGB-only.  
- The Streamlit app enabled **real-time NDVI estimation** for crop health monitoring.  

---

## 🛠 Tech Stack
- **Programming Language**: Python  
- **Frameworks/Libraries**:  
  - PyTorch  
  - Ultralytics YOLOv8  
  - OpenCV  
  - NumPy, Pandas, Matplotlib  
  - Streamlit (for deployment)  
- **Tools**:  
  - Google Colab (training)  
  - PIX4Dfields (NDVI ground truth)  
  - GitHub for version control  

---

## 📂 Repository Structure
├── Deep Learning Model Code
├── report/ Project report
├── app/ Streamlit app files
└── README.md Project documentation


---

## ⚡ Installation & Usage

### 1️⃣ Clone the repository
```bash
git clone https://github.com/yourusername/crop-field-analysis.git
cd crop-field-analysis

pip install -r requirements.txt
yolo task=detect mode=train data=config.yaml model=yolov8n.pt epochs=50 imgsz=640
yolo task=detect mode=predict model=path/to/best.pt source=data/test_images
streamlit run app/app.py
```
## 📌 Future Work

Extend to multi-temporal crop monitoring across growth stages.

Explore Vision Transformers (ViTs) for improved feature learning.

Integrate GIS mapping and live drone feeds.

## 🙌 Acknowledgements

Dataset providers and open-source contributors.

Ultralytics team for YOLOv8.

PIX4Dfields for NDVI baseline generation.
