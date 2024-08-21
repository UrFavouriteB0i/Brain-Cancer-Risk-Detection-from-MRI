# Brain Tumor Risk Detection Using MRI Images
This repository contains the implementation of a Brain Tumor Risk Detection system using MRI images. The project is part of a research initiative conducted for Jawa Timur Hospital and utilizes the Faster R-CNN architecture implemented in PyTorch.

## Overview
Brain tumors are one of the most serious and life-threatening forms of cancer, requiring early detection and precise treatment planning. This project aims to develop an automated system for detecting and assessing the risk of brain tumors using MRI images. The Faster R-CNN (Region-based Convolutional Neural Networks) model is employed for detecting and localizing tumors within the MRI scans.

## Features
Automated Tumor Detection: Identifies the presence and location of tumors in MRI images. <br/>
Risk Assessment: Classifies the tumor based on its risk level.<br/>
PyTorch Implementation: Leverages the PyTorch deep learning framework for efficient model training and inference.<br/>
Customizable Architecture: The Faster R-CNN model can be fine-tuned or modified according to specific requirements.<br/>

## Dataset
The dataset used in this project consists of MRI images collected from open source dataset of Brain cancer Patient. The images were annotated by medical professionals, indicating the presence and location of brain tumors.

**Input**: MRI images in JPEG format. <br/>
**Annotations**: Bounding boxes around tumor regions.

### Installation
To run this project locally, follow these steps:

### Clone the repository:
```
git clone https://github.com/yourusername/brain-tumor-risk-detection.git
cd brain-tumor-risk-detection
```
### Set up a virtual environment and activate it:
```
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### Install the required packages:
```
pip install -r requirements.txt
```

## Usage
To train the model on your own dataset: <br/>
Prepare your MRI images and annotations in the required format. <br/>
Modify the configuration file to specify the dataset paths, model parameters, and training options. <br/>

### Run the training script:
```
python train.py
```

### To perform inference using a pre-trained model:
Place the MRI images you want to test in the test_images/ directory. <br/>

### Run the inference script:
```
python inference.py --model-path path/to/your/model.pth
```
The detected tumors and their risk levels will be saved in the output/ directory.<br/>

## Model Architecture
The project utilizes the Faster R-CNN architecture, a popular object detection model that combines the advantages of region proposal networks (RPN) with fast R-CNN. This allows the model to efficiently detect tumors in MRI images while maintaining high accuracy.
<br/>
Backbone: ResNet-50, pre-trained on ImageNet. <br/>
Region Proposal Network (RPN): Generates region proposals.<br/>
ROI Pooling: Extracts fixed-size feature maps from proposals.<br/>
Bounding Box Regression & Classification: Predicts bounding boxes and tumor risk levels.<br/>

## Results
The model achieved promising results: <br/>

1. Precision: 0.87
2. Recall: 0.85
3. F1 Score: 0.86
<br/>

Visual examples of tumor detection are available in the results/ directory.

# Contributing
Contributions are welcome! If you have any suggestions, feel free to open an issue or submit a pull request.
