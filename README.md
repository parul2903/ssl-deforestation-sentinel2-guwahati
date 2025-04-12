# Self-Supervised Learning for Deforestation Prediction using Sentinel-2 Data in Guwahati

## Project Overview
This project explores self-supervised learning techniques for spatiotemporal forecasting of environmental changes, specifically deforestation prediction in Guwahati. We leverage contrastive learning frameworks like MoCo and SimCLR to extract feature representations from Sentinel-2 satellite imagery.

## Dataset
- **Source**: Google Earth Engine and Copernicus Ecosystem
- **Format**: Sentinel-2 satellite images in `.tif` format
- **Years Covered**: 2019–2024
- **Bands Used**: RGB (Bands 2, 3, 4), NIR, SWIR

## Models Used
We implemented and trained contrastive learning models to learn feature representations from the Sentinel-2 dataset:

### 1. **Momentum Contrast (MoCo)**
- Implemented MoCo v2 with a ResNet50 backbone.
- Used pre-trained MoCo models (800 epochs and 200 epochs) for transfer learning.
- Trained on Sentinel-2 images to extract temporal feature representations.
- Implemented a more complex architecture to minimize contrastive loss.

### 2. **Simple Contrastive Learning (SimCLR)**
- Implemented SimCLR with a ResNet50 backbone.
- Augmented Sentinel-2 images with transformations such as random cropping, flipping, and Gaussian blurring.
- Extracted high-dimensional embeddings to analyze changes in forest cover over time.

## Training Pipeline
- Data Preprocessing: Resized and normalized Sentinel-2 images.
- Augmentations applied for SimCLR-style training.
- Training performed using PyTorch with CUDA acceleration.
- Contrastive loss visualization to track learning efficiency.

## Results & Analysis
- Extracted feature embeddings from Sentinel-2 imagery.
- Demonstrated the effectiveness of MoCo and SimCLR for learning representations without labeled data.
- Used learned embeddings to build a downstream model for deforestation prediction.
- Analyzed deforestation patterns in Guwahati from 2019–2024.

## Future Scope
- Experiment with additional self-supervised methods like BYOL and SwAV.
- Extend the dataset to include more spectral bands.
- Develop a real-time monitoring tool for deforestation tracking.

## References
- [Facebook AI Research - MoCo](https://arxiv.org/abs/1911.05722)
- [Google Brain - SimCLR](https://arxiv.org/abs/2002.05709)
- [Copernicus Open Access Hub](https://scihub.copernicus.eu/)
- [Google Earth Engine](https://earthengine.google.com/)

---
Feel free to contribute, open issues, or suggest improvements!
