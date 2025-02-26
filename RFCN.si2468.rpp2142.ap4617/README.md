# Faster R-CNN Object Detection on PASCAL VOC Dataset

## Overview
This project implements Faster R-CNN for object detection using the PASCAL VOC dataset. The model is based on a pre-trained Faster R-CNN with a ResNet-50 backbone and Feature Pyramid Network (FPN) from PyTorch's `torchvision` module. The project includes training, validation, and inference steps. 

There is also an associated presentation with google slides. The pdf version is available in this folder. 

## Features
- Uses the PASCAL VOC 2012 dataset for training and validation.
- Implements Faster R-CNN with ResNet-50 backbone and Feature Pyramid Network.
- Performs training and validation loops.
- Conducts inference on random test images and visualizes bounding boxes.
- Evaluates the model using Mean Average Precision (mAP) scores.

## Requirements
Make sure you have the following dependencies installed:

```bash
pip install torch torchvision matplotlib numpy
```

## Dataset
The project uses the PASCAL VOC dataset, which is automatically downloaded and stored in `./data/pascal`.

## Usage

### 1. Train the Model
The model is trained on the training set of PASCAL VOC 2012.

### 2. Validate the Model
Validation loss is computed at each epoch to monitor performance.

### 3. Perform Inference
To test the model, random images from the validation dataset are passed through the model, and the detected bounding boxes are visualized.

### 4. Evaluate Performance with mAP
To generate Mean Average Precision (mAP) curves for the model:
- Compute precision-recall curves for each class.
- Calculate the mAP score across all classes.

## Visualization
Bounding boxes from the predictions are drawn on sample images, with class labels and confidence scores.

## Future Improvements
- Implement training on additional datasets like COCO.
- Optimize the model for faster inference.
- Fine-tune hyperparameters for improved accuracy.

## Acknowledgments
- The implementation is based on PyTorch’s `torchvision.models.detection.fasterrcnn_resnet50_fpn`.
- The PASCAL VOC dataset is publicly available for object detection tasks.

### Other Reading
1. original RFCN paper: https://arxiv.org/pdf/1605.06409
2. OverFeat paper: https://arxiv.org/pdf/1312.6229
3. Segmentation: https://arxiv.org/pdf/1506.06204
4. Instance-Sensitive Segmentation: https://arxiv.org/pdf/1603.08678


