# Building Footprint Segmentation (Inria Aerial Imagery)

**Author:** Rafiqul Islam  
**Context:** PhD Technical Assessment Submission (UNLV - Dr. John Sohn)

## 📌 Project Overview
Semantic segmentation pipeline developed to extract building footprints from high-resolution aerial imagery using a U-Net architecture with a pre-trained `ResNet34` backbone. 

To eliminate spatial data leakage, evaluation was conducted using an **out-of-city holdout scheme** (testing strictly on unseen tiles from Vienna).

## 📊 Performance Metrics (Vienna Holdout)
- **Loss Function:** Hybrid BCE + Dice Loss ($\mathcal{L}_{\text{BCEWithLogits}} + \mathcal{L}_{\text{Dice}}$)
- **Mean IoU (Jaccard Index):** `0.6967`
- **Mean Dice Score ($F_1$):** `0.8203`

## 🗂️ Dataset & Execution
- **Dataset:** [Inria Aerial Image Labeling Dataset](https://project.inria.fr/aerialimagelabeling/)
- **Environment:** Executed on Kaggle GPU infrastructure (NVIDIA P100/T4).
- **Raw Data Note:** Due to GitHub file size limits, raw satellite tiles are not hosted in this repository. All data loading and preprocessing steps are fully reproducible inside the included `.ipynb` notebook.
