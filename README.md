# Brain Tumor MRI Classification with Deep Learning

Course project for **MLAI 504 – Neural Networks and Deep Learning** (2026–2027).

This project classifies brain MRI slices into four classes (**glioma, meningioma, pituitary tumor, no tumor**) using a systematic deep learning workflow: data cleaning, step-by-step CNN design, hyperparameter tuning, and transfer learning with pretrained models.

> ⚠️ This is an academic project. The model is not a medical device and must not be used for diagnosis.

## Highlights (planned)

- **Leakage audit:** exact and near-duplicate image detection, followed by a duplicate-aware re-split of the data
- **Step-by-step CNN development:** from a simple baseline to a residual network, with every change justified and measured
- **Hyperparameter tuning:** grid search and random search / Hyperband with Keras Tuner
- **Transfer learning:** ResNet50 plus a comparison model, with feature extraction followed by fine-tuning
- **Evaluation:** per-class precision, recall and F1, confusion matrix, ROC-AUC and Grad-CAM heatmaps

## Dataset

[Brain Tumor MRI Dataset](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset) by Masoud Nickparvar (Kaggle, CC0: Public Domain), which combines the Figshare, SARTAJ and Br35H datasets. See [`data/README.md`](data/README.md).

## Tech stack

Python · TensorFlow / Keras 3 · Keras Tuner · scikit-learn · OpenCV · ImageHash · Kaggle Notebooks (GPU)

## Repository structure

```
brain-tumor-mri-classification/
├── README.md            # project overview (this file)
├── requirements.txt     # Python dependencies
├── notebooks/           # the main Jupyter notebook (graded deliverable)
├── data/                # dataset instructions and split manifest (raw images not committed)
├── results/             # experiment and tuning logs (CSV)
├── figures/             # key plots exported from the notebook
└── models/              # saved model weights (git-ignored)
```

## Roadmap

- [ ] Phase 0: Repository and environment setup
- [ ] Phase 1: Dataset selection and description
- [ ] Phase 2: Data exploration and preprocessing
- [ ] Phase 3: Step-by-step model building
- [ ] Phase 4: Hyperparameter tuning
- [ ] Phase 5: Transfer learning
- [ ] Phase 6: Integration of course topics
- [ ] Phase 7: Final evaluation and interpretation
- [ ] Phase 8: Final notebook and submission

## How to run

1. Open the notebook from `notebooks/` in Kaggle.
2. Add the dataset: **Add Input → search "Brain Tumor MRI Dataset" (Masoud Nickparvar) → Add**.
3. Under **Session options**, turn **Internet** on and select a **GPU** accelerator.
4. Run all cells.

## Results

_To be completed at the end of the project._

## References

_To be completed._

## Author

karam jammal  · MLAI 504, 2026–2027