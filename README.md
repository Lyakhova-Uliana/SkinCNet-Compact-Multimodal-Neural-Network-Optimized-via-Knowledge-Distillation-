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
