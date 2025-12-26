# 🦝 Computer Vision II: ViT & Grounded-SAM Raccoon Detection

This repository contains an end-to-end Computer Vision project featuring advanced image classification and an automated object detection pipeline. 

The project is divided into two primary technical phases:
1. **Vision Transformer (ViT)**: A modern approach to image classification using self-attention mechanisms.
2. **Grounded-SAM to YOLO**: A zero-shot automated labeling pipeline for custom raccoon detection and segmentation.

---

## 🛠️ Project Architecture

### 1. Image Classification with ViT
Instead of standard Convolutional Neural Networks (CNNs), this project implements a **Vision Transformer**. 
* **Convolutional Patch Embedding**: The model treats image patches as "words" in a sequence.
* **Self-Attention**: Captures global context and relationships between different parts of the image simultaneously.

### 2. Automated Raccoon Detection Pipeline (Grounded-SAM)
To avoid manual annotation of the raccoon dataset, I implemented a "Zero-Shot" labeling workflow:
* **Grounding DINO**: Uses text prompts (e.g., "raccoon") to detect objects without prior training.
* **Segment Anything Model (SAM)**: Generates high-fidelity segmentation masks based on the DINO bounding boxes.
* **YOLO Training**: The resulting auto-generated labels are used to train a YOLO model for real-time inference.

---

## 📂 Repository Structure

```text
├── DSAI544_Assignment_2.ipynb  # Core project logic and experiments
├── requirements.txt            # Environment dependencies
├── .gitignore                  # Excludes heavy datasets and weights
└── README.md                   # Project documentation
```

---

## 🚀 Getting Started

### Prerequisites
* Python 3.9+
* GPU with CUDA support (Recommended for Grounded-SAM and YOLO training)

### Installation
1. **Clone the repository**:
   ```bash
   git clone https://github.com/Ahmet-Yusuf-Ozturk/Computer_Vision_2.git
   cd Computer_Vision_2
   ```

2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

### Data Preparation
To keep this repository lightweight, raw datasets are excluded. 
* Place your raccoon images in a folder named `images/`.
* Download the CIFAR-10 dataset into the `data/` directory.
* Run the Grounded-SAM cells in the notebook to generate the `labeled_data/` folder automatically.

---

## 📊 Results
* **Classification**: ViT performance on CIFAR-10.
* **Detection**: YOLO detection results on the custom Raccoon dataset labeled via SAM.

---
## 📜 License
This project is for educational purposes as part of the DSAI Assignment 2.
```
