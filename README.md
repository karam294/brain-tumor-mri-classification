# Brain Tumor MRI Classification with Deep Learning

Course project for **MLAI 504 – Neural Networks and Deep Learning** (2026–2027).

This project classifies brain MRI slices into four classes (**glioma, meningioma, pituitary tumor, no tumor**) using a systematic deep learning workflow: data cleaning, step-by-step CNN design, hyperparameter tuning, and transfer learning with a pretrained model.

> ⚠️ This is an academic project. The model is not a medical device and must not be used for diagnosis.

## Highlights

- **Leakage audit:** duplicate images found with perceptual hashing (23% of the original test images had a copy in the training set), followed by a duplicate-free re-split of the data
- **Step-by-step CNN development:** from a fully connected baseline to a deeper CNN with batch normalization, data augmentation and dropout
- **Hyperparameter tuning:** random search over learning rate, batch size, dropout and model size
- **Transfer learning:** ResNet50 pretrained on ImageNet, first as a frozen feature extractor, then fine-tuned
- **Evaluation:** per-class precision, recall and F1, confusion matrix and misclassified examples

## Dataset

[Brain Tumor MRI Dataset](https://www.kaggle.com/datasets/masoudnickparvar/brain-tumor-mri-dataset) by Masoud Nickparvar (Kaggle, version 2, CC0: Public Domain), which combines the Figshare, SARTAJ and Br35H datasets. See [`data/README.md`](data/README.md).

## Tech stack

Python · PyTorch · torchvision · scikit-learn · OpenCV · ImageHash · VS Code with a Google Colab GPU

## Repository structure

```
brain-tumor-mri-classification/
├── README.md            # project overview (this file)
├── requirements.txt     # Python dependencies
├── notebooks/           # the main Jupyter notebook (graded deliverable)
├── data/                # dataset information and the train / validation / test split
└── results/             # experiment results
```

## Roadmap

- [x] Phase 0: Repository and environment setup
- [x] Phase 1: Dataset selection and description
- [x] Phase 2: Data exploration and preprocessing
- [ ] Phase 3: Step-by-step model building
- [ ] Phase 4: Hyperparameter tuning
- [ ] Phase 5: Transfer learning
- [ ] Phase 6: Integration of course topics
- [ ] Phase 7: Final evaluation and interpretation
- [ ] Phase 8: Final notebook and submission

## How to run

1. Create a virtual environment and install the dependencies: `pip install -r requirements.txt`
2. Open `notebooks/main.ipynb` in VS Code or Jupyter. The dataset downloads automatically with `kagglehub`.
3. For training, connect the notebook to a GPU, for example with the Google Colab extension for VS Code (**Select Kernel → Colab → New Colab Server → GPU**).
4. Run all cells.

## Results

_To be completed at the end of the project._

## References

_To be completed._

## Authors

Karam Jammal & Yorgo Bou Fayad · MLAI 504, 2026–2027
