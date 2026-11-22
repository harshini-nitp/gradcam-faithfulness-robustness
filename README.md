# Evaluating Faithfulness and Robustness of Grad-CAM Explanations in Vision Transformers

A comparative research study investigating how faithful and robust Grad-CAM explanations are across different Vision Transformer architectures.

## Overview

Explainable AI (XAI) helps us understand the reasoning behind predictions made by deep learning models. However, a visually convincing explanation is not necessarily a faithful or reliable one.

This project evaluates Grad-CAM explanations across three image classification models using faithfulness and robustness experiments.

## Models Evaluated

| Model                  | Architecture                                         |
| ---------------------- | ---------------------------------------------------- |
| Partial Fine-Tuned ViT | Vision Transformer                                   |
| Deep-Head ViT          | Vision Transformer with a deeper classification head |
| Swin Transformer       | Hierarchical Vision Transformer                      |

## Dataset

**Indian Medicinal Leaves Image Dataset**

- 6,900 images
- 80 medicinal plant classes
- Image resolution: 224 × 224

Dataset source: [Kaggle – Indian Medicinal Leaves Dataset](https://www.kaggle.com/datasets/aryashah2k/indian-medicinal-leaves-dataset)

## Methodology

### 1. Classification Evaluation

Models were evaluated using accuracy and macro F1-score.

### 2. Faithfulness Evaluation

Grad-CAM explanations were evaluated using:

- Deletion tests
- Insertion tests
- Area Under the Curve (AUC)

### 3. Robustness Evaluation

Explanation stability was evaluated under:

- Brightness changes
- Gaussian noise
- Gaussian blur

Structural Similarity Index (SSIM) was used to compare explanation maps. Prediction consistency was also measured.

### 4. Statistical Analysis

Paired Wilcoxon tests, bootstrap confidence intervals, exact McNemar tests, and Holm correction were used for statistical comparisons.

## Key Results

| Model            | Accuracy (%) | Macro F1 (%) | Deletion AUC | Insertion AUC |
| ---------------- | -----------: | -----------: | -----------: | ------------: |
| Partial ViT      |        95.22 |        92.71 |       0.4600 |        0.3279 |
| Deep-Head ViT    |        94.06 |        91.81 |       0.4891 |        0.4219 |
| Swin Transformer |        97.10 |        97.30 |       0.6730 |        0.6772 |

**Key observation:** Higher classification performance does not necessarily imply better explanation faithfulness. The models showed different strengths across deletion, insertion, and robustness evaluations.

## Repository Structure

```text
gradcam-faithfulness-robustness/
│
├── notebooks/
│   └── Research implementation notebook
│
├── results/
│   ├── figures/
│   └── tables/
│
├── report/
│   └── Research project report
│
├── README.md
└── .gitignore
```

## Limitations

- Faithfulness and robustness experiments used a selected sample of 50 images correctly classified by all three models.
- The architectures have different native feature-map resolutions.
- Robustness findings depend on the selected transformations and their parameters.
- The study uses existing model checkpoints and does not investigate their original training procedures.

## Technologies Used

- Python
- PyTorch
- Vision Transformers
- Swin Transformer
- Grad-CAM
- NumPy
- Pandas
- Matplotlib
- scikit-image
- SciPy

## Project Status

Research experiments and report completed.

## Author

Harshini
