# Decision Tree Classification – Iris Dataset

A simple machine learning project that trains and visualizes a **Decision Tree Classifier** using the Iris dataset provided by scikit-learn.

## Overview

This project demonstrates how a decision tree can learn to classify iris flowers from their measurements. The notebook loads the built-in Iris dataset, trains a `DecisionTreeClassifier`, and plots the resulting decision tree.

## Dataset

The project uses `sklearn.datasets.load_iris()`, a built-in dataset containing:

- **150 samples** of iris flowers
- **4 input features**:
  - Sepal length
  - Sepal width
  - Petal length
  - Petal width
- **3 target classes**:
  - Setosa
  - Versicolor
  - Virginica

The measurements are provided in the dataset's standard units (centimetres).

## Technologies and Libraries

- Python
- Jupyter Notebook
- pandas
- Matplotlib
- scikit-learn

## Project Structure

```text
.
├── DecisionTree.ipynb   # Notebook containing data loading, model training, and visualization
└── README.md            # Project documentation
```

## Getting Started

### 1. Clone the repository

```bash
git clone <your-repository-url>
cd <repository-folder>
```

### 2. Install the dependencies

```bash
pip install pandas matplotlib scikit-learn jupyter
```

### 3. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open `DecisionTree.ipynb` and run the cells from top to bottom.

## How It Works

1. **Import libraries** – Imports pandas, Matplotlib, and the required scikit-learn dataset, model, and tree-visualization utilities.
2. **Load the dataset** – Loads the Iris dataset using `load_iris()`.
3. **Inspect the features** – Accesses `iris.data` to view the flower measurements.
4. **Train the classifier** – Creates a `DecisionTreeClassifier` and fits it using `iris.data` and `iris.target`.
5. **Visualize the model** – Uses `tree.plot_tree()` with filled nodes to display the learned decision tree.

## Model

The notebook uses the default scikit-learn configuration:

```python
from sklearn.tree import DecisionTreeClassifier

classifier = DecisionTreeClassifier()
classifier.fit(iris.data, iris.target)
```

The tree is visualized with Matplotlib:

```python
import matplotlib.pyplot as plt
from sklearn import tree

plt.figure(figsize=(15, 10))
tree.plot_tree(classifier, filled=True)
plt.show()
```

## Current Scope and Notes

- The notebook trains the model on the **entire Iris dataset**.
- Although `train_test_split` is imported, it is not used in the current notebook.
- The notebook does not currently calculate test accuracy or other evaluation metrics.
- The model uses scikit-learn's default decision-tree settings; no hyperparameter tuning is performed.

For a more complete evaluation, a future version could split the data into training and testing sets, use a fixed `random_state`, and report metrics such as accuracy, precision, recall, and a confusion matrix.

## Purpose

This notebook is intended as a beginner-friendly demonstration of decision tree classification and model visualization using scikit-learn.

## License

No license is specified in the notebook. Add a license file if you intend to distribute or reuse this project publicly.
