# Evaluating Faithfulness and Robustness of Grad-CAM Explanations in Vision Transformers

A comparative research project evaluating the faithfulness and robustness of Grad-CAM explanations across three vision transformer models.

## Models Evaluated
- Partial Fine-Tuned Vision Transformer (Partial ViT)
- Deep-Head Vision Transformer
- Swin Transformer

## Dataset
Indian Medicinal Leaves Image Dataset — 6,900 images across 80 classes.

Dataset source: [Kaggle – Indian Medicinal Leaves Dataset](https://www.kaggle.com/datasets/aryashah2k/indian-medicinal-leaves-dataset)

## Evaluation Methods
- **Faithfulness:** Deletion and insertion tests.
- **Explanation robustness:** Stability of Grad-CAM heatmaps under brightness changes, Gaussian noise, and Gaussian blur.
- **Statistical analysis:** Paired statistical tests and multiple-comparison correction.

## Repository Structure
- `notebooks/` — Research implementation and experiments.
- `results/figures/` — Generated research figures.
- `results/tables/` — Experimental results in CSV format.
- `report/` — Research project report.

## Key Findings
The experiments show that model performance, explanation faithfulness, and explanation robustness do not necessarily rank models in the same order. No single model performs best across all evaluation criteria.

## Limitations
The explanation experiments use a selected sample of 50 images. The models also differ in architecture and native feature-map resolution, which should be considered when interpreting comparisons.

## Project Status
Research experiments and report completed.