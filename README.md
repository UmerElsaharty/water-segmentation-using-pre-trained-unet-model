# Water Segmentation Using U-Net

This project focuses on segmenting water bodies from multi-channel images using a U-Net model. The dataset used in this project consists of TIFF images with 12 channels and corresponding binary mask labels in PNG format. The U-Net model used transfer learning from 'imagenet', and it produced impressive results.

## Table of Contents

- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Training Process](#training-process)
- [Results](#results)



## Project Overview

This project aims to accurately segment water bodies from satellite images using a pre-trained deep learning model. The U-Net architecture was chosen due to its effectiveness in image segmentation tasks, particularly when working with multi-channel inputs.

## Dataset

- **Images:** The dataset contains images in TIFF format, each with 12 channels. These images represent various spectral bands, providing detailed information for accurate segmentation.
- **Labels:** The corresponding labels are binary masks in PNG format, indicating the presence or absence of water in each pixel of the images.

## Model Architecture

The pre-trained U-Net model from segmentation_models was used to handle the unique characteristics of the multi-channel input data. The architecture consists of an encoder represented by a mobilenet architecture as a backbone for the Unet and a decoder structure with skip connections, enabling the model to capture both spatial and contextual information.


## Training Process

The model was trained on the multi-channel TIFF images but I only chose 3 channels corresponding to detect water bodies and moisture, with the binary masks serving as labels. Key details of the training process include:

- **Input Dimensions:** (128, 128, 3)
- **Loss Function:** Custome Dice loss function + BinaryCrossentropy 
- **Optimizer:** Adam
- **Data Augmentation:** random rotation was applied to increase the robustness of the model.

## Results

The U-Net model achieved remarkable results in segmenting water bodies, demonstrating its effectiveness in this task. The detailed results, including metrics such as F1-score, precision, and recall

