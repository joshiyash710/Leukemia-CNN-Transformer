Leukemia Classification Using Hybrid CNN–Transformer
Overview

This repository contains an end-to-end deep learning pipeline for automated leukemia detection from microscopic blood smear images. The model leverages a hybrid CNN–Transformer architecture, combining local feature extraction from a CNN backbone (ResNet/EfficientNet) with global context modeling using a Transformer encoder.

The system achieves high accuracy by training on the C-NMC leukemia dataset and using k-fold cross-validation with hyperparameter optimization via Optuna.

Key Features

Hybrid architecture: CNN for feature extraction + Transformer for global context

Supports multiple backbones: ResNet18, ResNet50, EfficientNet-B0

Uses Focal Loss and Cross-Entropy Loss for robust training

K-fold cross-validation for reliable evaluation

Optuna hyperparameter tuning for optimal performance

Provides ensemble predictions across trained folds

Generates confidence scores and identifies low-confidence samples

Installation
# Clone the repository
git clone https://github.com/your-username/Leukemia-CNN-Transformer.git
cd Leukemia-CNN-Transformer

# Create and activate a virtual environment
python -m venv leukemia_env
source leukemia_env/bin/activate  # Linux/Mac
leukemia_env\Scripts\activate     # Windows

# Install dependencies
pip install -r requirements.txt

Dataset

Training and validation data: D:\C-NMC_Leukemia\training_data and D:\C-NMC_Leukemia\validation_data

Testing data: D:\C-NMC_Leukemia\testing_data

The dataset contains two classes:

ALL (Acute Lymphoblastic Leukemia)

HEM (Normal Hematopoietic cells)

Note: Update dataset paths in the code according to your environment.

Usage
1. Train Model with Optuna Hyperparameter Tuning
python train_optuna.py

2. Train Final Model with Best Hyperparameters
python train_final_model.py

3. Load Ensemble Models and Predict on Test Set
python predict_test_set.py

4. Visualize Predictions
python visualize_predictions.py

Results

Achieved best validation accuracy across folds using ResNet50 backbone

Provides prediction probabilities for each test image

Identifies low-confidence samples for further review

Folder Structure
Leukemia-CNN-Transformer/
├─ data/
│  ├─ training_data/
│  ├─ validation_data/
│  └─ testing_data/
├─ notebooks/                  # Jupyter notebooks (optional)
├─ src/                        # Source code
│  ├─ dataset.py
│  ├─ model.py
│  ├─ train.py
│  ├─ predict.py
│  └─ utils.py
├─ requirements.txt
└─ README.md

Citation

If you use this repository for research or projects, please cite:

Your Name, "Hybrid CNN–Transformer Model for Leukemia Detection", 2025.

License

This project is licensed under the MIT License.
