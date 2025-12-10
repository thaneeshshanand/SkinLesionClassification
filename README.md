# Skin Lesion Classification – README

This repository contains the notebook used for training a skin lesion classification model using the HAM10000 dataset. Follow the steps below to run the notebook successfully.

---

## 1. Requirements

Ensure you have the following installed:

- Python 3.8+
- PyTorch
- torchvision
- scikit-learn
- scikit-image
- OpenCV (optional depending on preprocessing)
- pandas
- numpy
- matplotlib
- jupyter or jupyterlab

Install dependencies:

```bash
pip install torch torchvision scikit-learn scikit-image opencv-python pandas numpy matplotlib
```

---

## 2. Dataset Setup

1. Download the **HAM10000 dataset** from the ISIC Archive - https://api.isic-archive.com/collections/212/
2. Place all images inside a directory such as:
```
ISIC-images/
```
3. Place the metadata CSV file ham10000_metadata_2025-11-04.csv in the base folder.

---

## 3. Notebook Structure

The notebook contains:

- Data loading and preprocessing  
- Optional segmentation using classical morphology  
- Training using ResNet-34  
- Imbalance handling using weighted BCE  
- Evaluation metrics and threshold tuning  
- Visualization plots

---

## 4. Running the Notebook

1. Open the notebook:
```bash
jupyter notebook
```
2. Run each cell in order.
3. Update file paths inside the notebook if necessary.
4. Training runs on:
   - **MPS** (MacBook Apple Silicon)
   - **GPU (CUDA)** if available  
   - Otherwise CPU (slower)

---

## 5. Notes

- If using segmentation, ensure scikit-image is installed.
- Training for 50 epochs may take time depending on your hardware.
- Threshold tuning is included to achieve >90% malignant recall.

---

## 6. Output

The notebook generates:

- Confusion matrix  
- ROC-AUC  
- Precision, recall, F1-score  
- Threshold-optimized metrics  
- Visualizations of predictions and performance curves  

---
