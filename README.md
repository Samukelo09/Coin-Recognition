#  South African Bank Coins Recognition

A computer vision project for automatic classification of South African bank coins using image processing, feature extraction, and deep learning.

##  Team Members
- Linda Sekhoasha (222004139)  
- Wandile Ngobese (222056013)  
- **Samukelo Mkhize (220009930)**  
- Khonzinkosi Mkhize (219005273)  

---

##  Project Overview

This project aims to identify and classify South African bank coins using an automated pipeline that is invariant to coin side, scale, and rotation. The pipeline includes preprocessing, segmentation, feature extraction, and classification using both classical machine learning and deep learning (CNNs).

---

## 🛠 Techniques Used

###  Image Preprocessing
- **Denoising**: Gaussian Blur, Median Blur, Bilateral Filter  
- **Contrast Enhancement**: Histogram Equalization, CLAHE  
- **Illumination Correction**: Homomorphic Filtering, Background Subtraction  
- **Evaluation Metrics**:  
  - PSNR (Peak Signal-to-Noise Ratio)  
  - SSIM (Structural Similarity Index)

###  Image Segmentation
- **Morphological Processing**
- **Hough Circle Transform**
- **GrabCut**
- **UNet (TFLite)**

###  Feature Extraction
- **Hu Moments** (Shape descriptors)
- **Haralick Features** (Texture via GLCM)
- **Local Binary Patterns (LBP)**
- **Color Statistics** (Mean & Standard Deviation across RGB and grayscale)

###  Classification Models

| Segmentation Type      | Model Type       | Accuracy |
|------------------------|------------------|----------|
| Hough                  | RF / MLP         | 40%      |
| Hough                  | CNN              | 95%      |
| GrabCut                | CNN              | 97%      |
| Raw (No Segmentation)  | CNN              | 32%      |
| Morphological          | Feature-based    | 32%      |
| UNet                   | Feature-based    | 99%      |
| UNet + MobileNetV2     | CNN (TFLite)     | 97%      |

> **Note:** SMOTE oversampling was applied to improve model performance in imbalanced datasets.

---

##  How to Run the App

### Option 1: Google Drive (APK)
1. Download and install the Android app from [Google Drive](https://drive.google.com/drive/folders/1SqM-uiKRiFgzlqyxWW7Ti3ioGFyRTymh?usp=drive_link)

### Option 2: Android Studio
1. Open Android Studio
2. Connect your Android device via USB and enable Developer Options
3. Open the project folder
4. Run the app on your connected device




---

##  Dataset
The dataset used in this project is included in the [Google Drive folder](https://drive.google.com/drive/folders/1SqM-uiKRiFgzlqyxWW7Ti3ioGFyRTymh?usp=drive_link) along with the APK.

---

##  References
- Gonzalez & Woods (2008). *Digital Image Processing*  
- Wang et al. (2004). *Image Quality Assessment using SSIM*  
- Rother et al. (2004). *GrabCut: Interactive Foreground Extraction*  
- Hu (1962). *Moment Invariants for Pattern Recognition*  
- Haralick et al. (1973). *Textural Features for Image Classification*  
- Ronneberger et al. (2015). *U-Net for Biomedical Image Segmentation*  
- Howard et al. (2017). *MobileNetV2 for Efficient Mobile Vision*  
- Chawla et al. (2002). *SMOTE: Synthetic Minority Over-sampling Technique*

---

## ✅ Conclusion

Combining robust segmentation (GrabCut, UNet) with deep learning classification (MobileNetV2) and balanced datasets provides a powerful and lightweight mobile solution for real-world coin recognition tasks. The project demonstrates high classification accuracy and practical deployability on mobile platforms.

