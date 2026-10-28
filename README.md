# SkinCNet: Compact Multimodal Neural Network Optimized via Knowledge Distillation for Skin Lesion Classification

This repository contains the official implementation of the research paper:

**"SkinCNet: Compact Multimodal Neural Network Optimized via Knowledge Distillation for Skin Lesion Classification"**

The study proposes a multimodal neural network system based on the specialized convolutional architecture SkinCNet that simultaneously analyzes dermatological images of pigmented skin neoplasms and statistical metadata of patients. Knowledge distillation from heavy teacher models (DenseNet_201, ResNeXt_101, Inception_v4) to the compact SkinCNet student model provides up to 98.99 times parameter reduction with only 1.98 percentage points accuracy loss.

## Key Results

| Metric | Value |
|--------|-------|
| SkinCNet parameters | 0.27 million |
| Parameter reduction vs. DenseNet_201 | 98.99 times |
| Inference time reduction | 19.19 times |
| Network depth reduction | 10.44 times |
| Accuracy loss vs. teacher | 1.98 percentage points |
| Inference time on mobile device | less than 110 ms |
| Energy per inference | 0.039 mJ |

## Repository Structure
SkinCNet/
├── MNN based on DenseNet_201 as a model teacher.ipynb # Training of DenseNet_201 teacher model
├── MNN based on DenseNet_201 as a model teacher test/ # Test results for DenseNet_201 teacher
├── MNN based on Inception_v4 as a model teacher.ipynb # Training of Inception_v4 teacher model
├── MNN based on Inception_v4 as a model teacher test/ # Test results for Inception_v4 teacher
├── MNN based on ResNeXt_101 as a model teacher.ipynb # Training of ResNeXt_101 teacher model
├── MNN based on ResNeXt_101 as a model teacher test/ # Test results for ResNeXt_101 teacher
├── MNN based on specialized CNN/ # SkinCNet student model implementation
├── Ablation Study SkinCNet.ipynb # Ablation study experiments
└── README.md # This file


## Software Requirements

The experiments were conducted using the following software environment:

- **Operating System**: Windows 11
- **Python**: 3.11.11
- **Deep Learning Framework**: PyTorch 2.x
- **CUDA**: Required for GPU acceleration
- **GPU**: NVIDIA RTX 4070 Ti SUPER

## Installation

### Option 1: Using Conda (recommended)

```bash
conda env create -f environment.yml
conda activate NN_3_11_11

### Option 2: Using pip

python -m venv venv
# On Windows:
venv\Scripts\activate
# On Linux/macOS:
source venv/bin/activate

pip install -r requirements.txt
