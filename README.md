Land Cover Classification in Texas 🌎🛰️
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/samrakshanadhikari/landcovertexas.repo/blob/main/landcover_texas.ipynb)
Land Cover Classification in Texas 🌎🛰️
This project uses a Convolutional Neural Network (CNN) to classify land cover types across Texas from satellite imagery.

Project Overview
Goal:
Classify each pixel in satellite images of Texas into land cover types such as water, grass, trees, bare ground, built-up areas, etc.

Applications:
Useful for climate modeling, agriculture, conservation, urban planning, water management, and more.

Data
Satellite Imagery Source:
Sentinel-2 or Landsat images over Texas region.

Labels:
Land cover classes from datasets like ESA WorldCover.

Input Data Format:

Image patches, e.g., 128×128 pixels.

Multiple bands (e.g., Red, Green, Blue, Near Infrared).

Label Data Format:

Pixel-wise class labels matching image patch size.

Workflow
1. Data Preparation

Extract satellite image patches with corresponding labeled masks.

Normalize image data.

Convert labels into integer class IDs per pixel.

2. Model Architecture

Use a CNN-based semantic segmentation model (e.g., U-Net).

Input shape: (128, 128, 4) (4 bands).

Output shape: (128, 128, NUM_CLASSES) with per-pixel class probabilities.

3. Training Setup

Loss: sparse_categorical_crossentropy (for pixel-wise classification).

Optimizer: Adam.

Metrics: Pixel accuracy, Intersection over Union (IoU).

Batch size: Example 16 patches per batch.

Number of epochs: 10 or more depending on performance.

4. Evaluation

Evaluate on test set for accuracy and IoU.

Visualize predicted land cover maps.

5. Saving Model

Save trained model for inference later.



