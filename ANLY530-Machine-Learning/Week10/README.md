# Week 10: Model Evaluation — How Good Is Your Model, Really?

## Lecture Materials

### Viewing the Presentations

This week has an HTML tutorial and lecture slides available online:

#### 1. Model Evaluation (Hands-on Tutorial)

**Option 1: View Online (GitHub Pages - Recommended)**
- [View Tutorial Online](https://roozbeh412.github.io/data_sciences/ANLY530-Machine-Learning/Week10/Week10-ModelEvaluation-Tutorial.html)

**Option 2: Alternative Online Viewer**
- [View via htmlpreview](https://htmlpreview.github.io/?https://github.com/roozbeh412/data_sciences/blob/main/ANLY530-Machine-Learning/Week10/Week10-ModelEvaluation-Tutorial.html)

**Option 3: Download and Open Locally**
- Download `Week10-ModelEvaluation-Tutorial.html` and open it in your web browser

#### 2. Lecture Slides

- Download `ANLY530Lecture11_Model_evaluation.pptx` from this directory.

---

## Course Content

This week covers:

### Lecture Topics
- Why accuracy alone is not enough
- The confusion matrix and its derived metrics
- Precision, recall, specificity, and the F1 score
- ROC curves and AUC
- Regression error metrics (MAE, MSE, RMSE, R², Adjusted R²)
- Cross-validation and overfitting detection

### Hands-on Tutorial Topics
- The Accuracy Paradox — how 99% accuracy can be useless
- Two types of errors: False Positives vs. False Negatives (fire alarm analogy)
- Confusion Matrix as a heatmap on Iris with Random Forest
- Per-class metrics from the confusion matrix
- Precision — "When the model says yes, is it right?"
- Recall (Sensitivity) — "Of all the real positives, how many did we catch?"
- The Precision-Recall trade-off (threshold visualisation)
- F1 Score — harmonic mean vs. arithmetic mean comparison
- F-beta score for weighted emphasis
- Metric selection decision guide
- ROC Curves — four classifiers (DT, RF, NB, SVM) compared
- AUC interpretation and grading table
- Precision-Recall Curves for imbalanced data
- Log Loss — penalising confident wrong answers
- Regression metrics on Boston Housing (Linear Regression vs. Random Forest)
  - Actual vs. Predicted scatter plots
  - Residual plots and pattern detection
- K-Fold Cross-Validation diagram and implementation
  - Boxplot comparison across folds
  - Choosing K: bias-variance trade-off
- Multi-model classification comparison (radar chart, multi-CM heatmap)
- Complete metrics reference table

---

## Materials

- **HTML Tutorial**: `Week10-ModelEvaluation-Tutorial.Rmd` → `Week10-ModelEvaluation-Tutorial.html` (Interactive RMarkdown tutorial)
- **Lecture Slides**: `ANLY530Lecture11_Model_evaluation.pptx`

---

## Reading

- **Analytics Vidhya**: [12 Important Model Evaluation Metrics for Machine Learning](https://www.analyticsvidhya.com/blog/2019/08/11-important-model-evaluation-error-metrics/)
- **scikit-learn**: [3.4. Metrics and scoring: quantifying the quality of predictions](https://scikit-learn.org/stable/modules/model_evaluation.html)
- **Fawcett, T.** (2006). An Introduction to ROC Analysis. *Pattern Recognition Letters*, 27(8), 861–874.
- **Powers, D. M. W.** (2011). Evaluation: From Precision, Recall and F-Measure to ROC, Informedness, Markedness and Correlation. *Journal of Machine Learning Technologies*, 2(1), 37–63.

---

## Learning Path

### Step 1: Theory
1. Review the lecture slides (`ANLY530Lecture11_Model_evaluation.pptx`)
2. Read the Analytics Vidhya article on evaluation metrics
3. Understand why different problems demand different metrics

### Step 2: Practice
1. Work through the tutorial (`Week10-ModelEvaluation-Tutorial.html`)
2. Follow along with the code chunks — observe how confusion matrices, ROC curves, and residual plots reveal model behaviour
3. Compare classification metrics across Decision Tree, Random Forest, Naive Bayes, and SVM

### Step 3: Apply
1. Train a classifier on an imbalanced dataset and compare accuracy vs. F1 vs. AUC
2. Experiment with different decision thresholds and observe the precision-recall trade-off
3. Run 10-fold cross-validation on your own model and check for overfitting
4. Verify you can compile the `.Rmd` file to HTML on your own machine

---

## Key Concepts

### Classification Metrics
- **Confusion Matrix**: 2D table of TP, TN, FP, FN — the foundation of all classification metrics
- **Accuracy**: Fraction correct — misleading with imbalanced classes
- **Precision**: Of predicted positives, how many are truly positive?
- **Recall (Sensitivity)**: Of actual positives, how many were caught?
- **Specificity**: Of actual negatives, how many were correctly identified?
- **F1 Score**: Harmonic mean of precision and recall — punishes extreme imbalance
- **ROC Curve**: TPR vs. FPR at all thresholds
- **AUC**: Area under the ROC curve — threshold-independent quality measure
- **Log Loss**: Penalises confident wrong predictions exponentially

### Regression Metrics
- **MAE**: Average absolute error — treats all errors equally
- **RMSE**: Root of average squared error — punishes large errors more
- **R²**: Fraction of variance explained vs. the mean-baseline model
- **Adjusted R²**: R² penalised for unnecessary features

### Model Selection
- **Cross-Validation**: Train/test on every fold to estimate generalisation error
- **Overfitting**: High training score, low test score — model memorises rather than learns
- **Bias-Variance Trade-Off**: Simpler models (high bias) vs. complex models (high variance)

---

## Tools & Packages

### Required R Packages
```r
install.packages(c("tidyverse", "caret", "e1071", "naivebayes", "rpart", "randomForest", "pROC", "gridExtra", "scales", "knitr", "kableExtra", "MASS", "kernlab", "seedhash"))
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
