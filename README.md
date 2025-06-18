Land Cover Classification in Texas 🌎🛰️
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/samrakshanadhikari/landcovertexas.repo/blob/main/landcover_texas.ipynb)

This project aims to classify different land cover types across Texas using satellite imagery and  Fully Convolutional Neural Network (FCNN). Land cover classification identifies the type of surface in each pixel of satellite images, such as water, grass, trees, urban areas, bare ground, etc.

Land cover data is important for many applications such as climate modeling, agriculture, conservation, urban planning, and disaster management.

Overview
Data source: Sentinel-2 or Landsat satellite images over Texas region.

Labels: Land cover classes from datasets like ESA WorldCover or similar.

Input: Image patches (e.g., 128x128 pixels) with multiple spectral bands (e.g., RGB + Near Infrared).

Output: Pixel-wise land cover class predictions (semantic segmentation).

Model: A CNN-based semantic segmentation network.

Goal: Train the model to predict land cover type for each pixel.

Workflow
1. Data Preparation
Collect satellite imagery: Use Google Earth Engine (GEE) or other sources to download Sentinel-2 or Landsat images over Texas.

Generate labeled patches: Extract image patches (e.g., 128x128 pixels) along with corresponding land cover labels for supervised training.

Preprocess data: Normalize pixel values, convert labels to categorical classes.

2. Model Architecture
Use a simple CNN or U-Net architecture to perform pixel-wise classification.

Input: 128x128x4 image patch (R, G, B, NIR bands).

Output: 128x128xN where N = number of land cover classes.

3. Training
Use cross-entropy loss for multi-class pixel classification.

Use TensorFlow/Keras for model building and training.

Monitor validation accuracy and loss.

4. Evaluation
Evaluate pixel-level accuracy and other metrics such as IoU (Intersection over Union).

Visualize prediction maps on test regions.
