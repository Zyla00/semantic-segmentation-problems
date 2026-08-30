# Breast Cancer Detection using Semantic Segmentation Models

**Author:** Angelika Żyła  
**Date:** June 19, 2024  

## Project Overview

This project focuses on developing an effective machine learning model for the early detection and diagnosis of breast cancer. By utilizing the Breast Ultrasound Dataset, the objective is to create a robust and accurate semantic segmentation model to identify and classify breast tissue conditions. 

## Dataset

The Breast Ultrasound Dataset consists of ultrasound images from 600 female patients, aged between 25 and 75 years, collected in 2018. The dataset includes:

- **Total Images:** 780, in PNG format with an average resolution of 500x500 pixels.
- **Classes:** The images are divided into three categories:
  - **Normal:** 133 images with corresponding 133 masks.
  - **Benign:** 437 images with 454 masks.
  - **Malignant:** 210 images with 211 masks.
<p>
<img width="368" height="146" alt="image" src="https://github.com/user-attachments/assets/ed8efbee-f221-4832-b0d0-910aad5ba41d" />
</p>
<p>
<img width="368" height="146" alt="image" src="https://github.com/user-attachments/assets/c24ffd36-2543-4ca7-a34a-a64a67441d07" />
</p>
<p>
<img width="368" height="146" alt="image" src="https://github.com/user-attachments/assets/7a417125-62e8-4bdb-99cf-1a5a793b9df7" />
</p>

## Models Explored

Several state-of-the-art models for semantic segmentation were analyzed and tested for their applicability in medical imaging, specifically for breast cancer detection:

1. **U-Net**
2. **Fully Convolutional Network (FCN)**
   - Added layers for encoding (downsampling) and decoding (upsampling).
   - Skip connections to retain spatial features across layers.
   - Bottleneck layer for dense feature extraction.
3. **SegNet**
4. **PSPNet**

## Results
<p>
<img width="433" height="197" alt="image" src="https://github.com/user-attachments/assets/22c072df-550a-4462-a9fb-9be5687853f3" />
</p>

<p>
<img width="433" height="197" alt="image" src="https://github.com/user-attachments/assets/0469bdec-52d7-4056-9171-1db5340fb917" />
</p>
<p>
<img width="269" height="157" alt="image" src="https://github.com/user-attachments/assets/8389603d-0001-4eef-825a-8c99fa4a505a" />
</p>
<p>
<img width="433" height="197" alt="image" src="https://github.com/user-attachments/assets/d01a9f12-4d59-45a7-a006-b37637f84d9e" />
</p>
<p>
<img width="383" height="155" alt="image" src="https://github.com/user-attachments/assets/1b18433a-ccb4-42ce-bdaf-78696ec90142" />
</p>

<p>
<img width="146" height="257" alt="image" src="https://github.com/user-attachments/assets/54acbccd-d472-44c7-ba01-ce98cfb21287" />
</p>

### Performance Analysis

The performance of the models was evaluated based on accuracy and loss metrics:

- **FCN Model:** Showed the best results in terms of metrics. The architecture, which includes an encoder for downsampling, a dense bottleneck layer, and a decoder for upsampling, demonstrated effective learning on training data.
- **Accuracy Comparison (Fig. 4):** FCN achieved higher accuracy compared to other models.
- **Loss Comparison (Fig. 5):** FCN maintained lower loss values during training and validation.

### Observations

- Predictions using the FCN model generally matched ground truth masks in shape and size, achieving high accuracy in identifying regions of interest.
- Slightly blurry edges were noted in predictions, with instances of false positives due to over-prediction.
- Validation accuracy showed minor fluctuations, indicating possible overfitting which was mitigated by using regularization and early stopping.

## Summary

The FCN model, with its advanced architecture and skip connections, achieved impressive accuracy and low loss rates, proving its efficacy in breast cancer detection tasks. Despite occasional over-prediction and some variability in validation loss, the model’s overall performance indicates it is well-suited for segmenting abnormal tissue in breast ultrasound images.
