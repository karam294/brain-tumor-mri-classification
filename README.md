# Brain Tumor MRI Classification with Deep Learning

Course project for **MLAI 504 – Neural Networks and Deep Learning** (2026–2027).

This project classifies brain MRI slices into four classes (**glioma, meningioma, pituitary tumor, no tumor**) using a systematic deep learning workflow: data cleaning, step-by-step CNN design, hyperparameter tuning, and transfer learning with a pretrained model.

> ⚠️ This is an academic project. The model is not a medical device and must not be used for diagnosis.

## Highlights

- **Leakage audit:** duplicate images found with perceptual hashing (23% of the original test images had a copy in the training set), and near-duplicates (neighbouring slices of the same patient) grouped so they never cross the train / validation / test split
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

The full list is in Section 9 of the notebook.

- Nickparvar, M. (2021). *Brain Tumor MRI Dataset* (version 2). Kaggle. Combines the Figshare (Cheng et al., 2015), SARTAJ (Bhuvaji et al., 2020) and Br35H (Hamada, 2020) datasets.
- He, K., Zhang, X., Ren, S., & Sun, J. (2016). Deep residual learning for image recognition. *CVPR*.
- Bergstra, J., & Bengio, Y. (2012). Random search for hyper-parameter optimization. *JMLR*, 13.
- Paszke, A., et al. (2019). PyTorch: An imperative style, high-performance deep learning library. *NeurIPS*, 32.
- Buchner, J. *ImageHash*. https://github.com/JohannesBuchner/imagehash

## Authors

Karam Jammal & Yorgo Bou Fayad · MLAI 504, 2026–2027
