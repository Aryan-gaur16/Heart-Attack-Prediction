# Heart-Attack-Prediction
This project reproduces the stacking ensemble from Bhagat, Sharma & Agarwal (2025), "An efficient stacking-based ensemble technique for early heart attack prediction", published in Multimedia Tools and Applications, 84:36351–36375. It then tests the reliability of the paper's results and develops a more reliable evaluation pipeline.

#What this project does

Part 1: Reproduction. Trains the paper's six classifiers: Logistic Regression, Decision Tree, Random Forest, XGBoost, Naive Bayes and KNN. It then combines them using a 5-fold stacking ensemble and reports Accuracy, Precision, Recall, F1, Specificity, MCC and AUC.

Part 2: Leakage-aware pipeline. Finds that 723 of the 1,025 rows are duplicates, leaving only 302 unique patients, and that 154 rows appear in both the training and test sets. Part 2 removes the duplicates, scales the data within each cross-validation fold, tunes hyperparameters using nested cross-validation, and compares three different meta-classifiers for the stacking ensemble.

# How to install

1. Install Python 3.9 or newer from [Python.org](https://www.python.org?).
2. Download or clone this repository.
3. Open a terminal in the repository folder and run:

```bash
pip install pandas numpy scikit-learn xgboost matplotlib seaborn scipy jupyter
```

# How to run

1. In the same terminal, start Jupyter Notebook:

```bash
jupyter notebook
```

2. Open the project notebook.
3. Make sure `heart.csv` is in the same folder as the notebook.
4. Click **Kernel > Restart & Run All** to run the complete analysis.
