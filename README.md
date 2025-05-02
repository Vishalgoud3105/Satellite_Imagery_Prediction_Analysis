
# 🛰️ Satellite Imagery Prediction & Analysis using Deep Learning

## 🧩 Problem Statement
> Accurate segmentation of satellite imagery is crucial for a wide range of applications, from urban planning and agriculture to disaster management.  
> The goal of this project is to perform pixel-wise classification of satellite images using a deep learning model, enabling effective detection of features such as buildings, vegetation, water bodies, and more.

---

## 💡 Project Description
> This project uses the **UNet Convolutional Neural Network architecture** for semantic segmentation of satellite imagery.  
> The model is trained to classify each pixel in a satellite image into one of several predefined classes using supervised learning.  
>
> The dataset consists of **high-resolution RGB images and corresponding ground-truth masks**. We preprocess the images, build a robust CNN model, train it on labeled satellite data, evaluate the segmentation results, and visualize the predictions effectively.

---

## 📦 Dataset Details
- **Source**: Custom Satellite Dataset (from Kaggle / local repo)
- **Data Format**: RGB images (.jpg/.png) + masks (.png)
- **Image Dimensions**: 128x128 (resized)
- **Classes**: Multiple segmented regions (e.g., urban, vegetation, water)

```
Dataset Directory Structure:
satellite_image/
├── images/
└── masks/
```

---

## 🛠️ Technical Stack
- **Language**: Python
- **Frameworks**: TensorFlow, Keras
- **Libraries**: NumPy, OpenCV, Matplotlib, scikit-learn

---

## ⚙️ Steps Followed

### 1. 📥 Data Preparation
- Loaded RGB satellite images and binary masks
- Resized to 128x128 and normalized

### 2. 🏗️ Model Architecture
- Used **UNet** for semantic segmentation
- Encoder-Decoder architecture with skip connections
- Activation: ReLU for hidden layers, Sigmoid for final mask output

### 3. 🧠 Model Training
- **Loss Function**: Binary Crossentropy
- **Optimizer**: Adam
- **Evaluation Metrics**: Accuracy and IoU (Intersection over Union)

### 4. 💾 Save & Load Model
- Save model:
```python
model.save("satellite_unet.h5")
```
- Load model:
```python
from tensorflow.keras.models import load_model
model = load_model("satellite_unet.h5")
```

### 5. 📊 Evaluation
- Visualized predicted masks vs. ground truth
- Evaluated performance on test data

---

## 📈 Results
- ✅ High segmentation accuracy achieved
- 🎯 Accurate boundary detection for roads and buildings
- ⚠️ Minor inconsistencies in blurred/overlapping regions

---

## 🚀 How to Run

1. Clone this repository
2. Install required libraries:
   ```bash
   pip install tensorflow keras numpy matplotlib opencv-python
   ```
3. Ensure dataset is structured like this:
   ```
   /satellite_image/
     ├── images/
     └── masks/
   ```
4. Run the notebook:
   ```
   Satellite_Imagery_DeepLearning_SaveLoadModel.ipynb
   ```

---

## 🎯 Project Goals
- To segment satellite imagery using deep learning
- To demonstrate the use of UNet in real-world semantic segmentation
- To deliver a complete pipeline: preprocessing → training → prediction

---

## 🔗 Credits
- **Developer**: C. Vishal Goud  
- **Project Type**: Minor Project - Artificial Intelligence (Nov Batch)  
- **Dataset**: Custom Satellite Imagery (Kaggle/local)  
- **Model Reference**: UNet - Convolutional Networks for Biomedical Image Segmentation  
