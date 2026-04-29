# Week 08: Data Preprocessing & Feature Engineering

## Lecture Materials

### Viewing the Presentations

This week has an HTML tutorial and lecture slides available online:

#### 1. Data Preprocessing & Feature Engineering (Hands-on Tutorial)

**Option 1: View Online (GitHub Pages - Recommended)**
- [View Tutorial Online](https://roozbeh412.github.io/data_sciences/ANLY530-Machine-Learning/Week08/Week08-FeatureEngineering-Tutorial.html)

**Option 2: Alternative Online Viewer**
- [View via htmlpreview](https://htmlpreview.github.io/?https://github.com/roozbeh412/data_sciences/blob/main/ANLY530-Machine-Learning/Week08/Week08-FeatureEngineering-Tutorial.html)

**Option 3: Download and Open Locally**
- Download `Week08-FeatureEngineering-Tutorial.html` and open it in your web browser

#### 2. Lecture Slides

- View `lecture_09_preprocessing_and_feature_selection.html` from this directory (slidy presentation).

---

## Course Content

This week covers:

### Lecture Topics
- Pre-processing data: "Garbage In, Garbage Out"
- Subsetting ignoble (irrelevant) variables
- Handling missing data (imputation strategies)
- Detecting and treating outliers
- Normalization and feature scaling
- Feature selection via correlation
- Feature selection via variable importance

### Hands-on Tutorial Topics
- Why preprocessing matters — visualising messy data
  - Missing value heatmaps and box plots
- Handling missing values
  - Mean, median, mode, and KNN imputation
  - Before/after distribution comparison
- Outlier detection and treatment
  - IQR method with box plots and scatter plots
  - Z-score method
  - Capping (Winsorisation) and log-transform comparison
- Feature scaling
  - Min-max normalisation [0, 1]
  - Z-score standardisation (mean 0, SD 1)
  - Robust and MaxAbs scalers
  - Side-by-side scaling comparison visualizations
- Encoding categorical variables
  - Label encoding for ordinal variables
  - One-hot encoding for nominal variables
  - Dummy encoding (drop-first) for linear models
- Feature engineering
  - Interaction features (rooms x size)
  - Binning (continuous to categories)
  - Log and square-root transforms for skewed data
- Feature selection
  - Correlation heatmap and `findCorrelation()`
  - Variable importance with Random Forest and Decision Tree
  - Accuracy comparison across different feature subsets
- Handling imbalanced data
  - Oversampling, undersampling, and SMOTE (ROSE)
  - Class distribution and scatter plot visualizations
- Train/test splitting and data leakage prevention
  - Correct preprocessing workflow
  - Correct vs. leaked scaling comparison
- Complete pipeline: preprocessing + model training + evaluation

---

## Materials

- **HTML Tutorial**: `Week08-FeatureEngineering-Tutorial.Rmd` → `Week08-FeatureEngineering-Tutorial.html` (Interactive RMarkdown tutorial)
- **Lecture Slides**: `lecture_09_preprocessing_and_feature_selection.html` (Slidy presentation)
- **Data**: `data/data.csv` (Iris dataset used in lecture examples)

---

## Reading

- **Textbook**: *Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow* (Géron, 2019)
  - Chapter 2: End-to-End Machine Learning Project (data cleaning and preprocessing sections)
- **Pure Storage**: [What Is Data Preprocessing for Machine Learning?](https://www.purestorage.com/knowledge/what-is-data-preprocessing.html)
- **Medium**: [Data Preprocessing in Machine Learning: A Detailed Guide](https://nicks-cheke44.medium.com/data-preprocessing-in-machine-learning-a-detailed-guide-c710df69073f)

---

## Learning Path

### Step 1: Theory
1. Review the lecture slides (`lecture_09_preprocessing_and_feature_selection.html`)
2. Read Chapter 2 in the Géron textbook (focus on data cleaning sections)
3. Understand why preprocessing matters and the "Garbage In, Garbage Out" principle

### Step 2: Practice
1. Work through the tutorial (`Week08-FeatureEngineering-Tutorial.html`)
2. Follow along with the code chunks — observe how distributions change after scaling, how missing values are filled, and how feature importance ranks features
3. Pay special attention to the data leakage section

### Step 3: Apply
1. Take a messy dataset (e.g., from Kaggle) and apply the full preprocessing pipeline
2. Experiment with different imputation strategies and compare model performance
3. Try creating interaction features on a regression dataset
4. Verify you can compile the `.Rmd` file to HTML on your own machine

---

## Key Concepts

### Data Preprocessing & Feature Engineering
- **Missing Values**: Handle with deletion (rows/columns) or imputation (mean, median, mode, KNN)
- **Outliers**: Detect with IQR or Z-score; treat by removing, capping, or transforming
- **Min-Max Scaling**: Rescale features to [0, 1] — good for neural networks, bounded data
- **Z-Score Standardisation**: Centre to mean 0, SD 1 — good for SVM, PCA, linear models
- **Label Encoding**: Map ordinal categories to integers preserving order
- **One-Hot Encoding**: Create binary columns for nominal categories
- **Feature Engineering**: Create new features (interactions, binning, transforms) to improve model learning
- **Correlation Analysis**: Identify and remove redundant features (|r| > 0.85)
- **Variable Importance**: Use Random Forest or Decision Tree to rank feature contributions
- **Imbalanced Data**: Address with oversampling, undersampling, or SMOTE
- **Data Leakage**: Always fit preprocessing on training data only; apply to test data

---

## Tools & Packages

### Required R Packages
```r
install.packages(c("tidyverse", "gridExtra", "scales", "caret", "corrplot", "GGally", "randomForest", "rpart", "e1071", "ROSE", "knitr", "kableExtra", "seedhash"))
```

### Recommended Software
- **R**: Latest stable version
- **RStudio/Posit**: Latest version

---

## Quick Links

- [← Back to Course Home](../README.md)

---

<div align="center">

**ANLY 530 - Principles & Applications of Machine Learning**  
*Harrisburg University*

</div>
