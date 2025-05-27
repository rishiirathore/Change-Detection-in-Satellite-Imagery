# 🌍 Change Detection in Satellite Imagery

This project implements a simple yet effective methodology for detecting land cover changes between two satellite images captured at different times. It focuses on identifying environmental changes such as deforestation and urban expansion using classical image processing and unsupervised learning techniques.

## 📌 Objectives

- Detect meaningful changes in satellite imagery over time.
- Highlight areas impacted by deforestation and other land-use changes.
- Create an interpretable and efficient change detection pipeline.

## 🧪 Methodology

### 1. Data Preprocessing
- Satellite images were loaded using the **Rasterio** library.
- Images were **resampled** to ensure consistent spatial resolution.
- **Normalization** was applied to standardize pixel values across image bands.

### 2. Change Detection Pipeline
- **Otsu’s Thresholding**: Used to separate changed and unchanged regions based on pixel intensity variations.
- **K-Means Clustering**: Applied for unsupervised segmentation to identify land cover types before and after change.
- **Morphological Operations**: Binary opening and closing were used to reduce noise in the final change map.

### 3. Visualization
- The final change map was overlaid on the original image to aid interpretation.

## 📊 Results

- **Total area analyzed**: 47.79 km²  
- **Total changed area**: 6.14 km² (12.85%)  
  - **Deforestation**: 4.32 km² (9.03%)  
  - **Other changes**: 1.82 km² (3.82%)  

The algorithm effectively detected deforestation and urban expansion zones. The combined use of thresholding and clustering reduced false positives and enhanced overall accuracy.

## ✅ Conclusion

This project demonstrates a computationally efficient and interpretable change detection workflow using classical image analysis techniques. Future improvements could include the integration of **deep learning models** for more precise and automated change detection.

## 🛠 Tech Stack

- Python
- Rasterio
- NumPy
- Scikit-learn (K-Means)
- OpenCV (Morphological operations)
- Matplotlib

## 📁 Repository Structure

├── notebook.ipynb # Jupyter notebook with code and visualizations
├── summary.pdf # 1-page project summary
├── images/ # Sample inputs and outputs (optional)
├── data/ # Input satellite images (not included here)
└── README.md # This file
