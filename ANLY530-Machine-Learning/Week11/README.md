# Week 11: Ensemble Modeling — When Many Heads Are Better Than One

## Access Week 11 Tutorials

### Quick Links

| Resource | Link |
|---|---|
| **Hands-on Tutorial** (HTML, recommended) | **[Open Week 11 Tutorial](https://roozbeh412.github.io/data_sciences/ANLY530-Machine-Learning/Week11/Week11-EnsembleModeling-Tutorial.html)** |
| Tutorial source (RMarkdown) | [Week11-EnsembleModeling-Tutorial.Rmd](./Week11-EnsembleModeling-Tutorial.Rmd) |
| Tutorial (alternative viewer) | [htmlpreview.github.io](https://htmlpreview.github.io/?https://github.com/roozbeh412/data_sciences/blob/main/ANLY530-Machine-Learning/Week11/Week11-EnsembleModeling-Tutorial.html) |
| Lecture Slides (HTML) | [lecture_12_ensemble_modeling-1.html](./lecture_12_ensemble_modeling-1.html) |
| Course Home (all weeks) | [roozbeh412.github.io/data_sciences/#530](https://roozbeh412.github.io/data_sciences/#530) |

### Access Options

#### 1. Ensemble Modeling (Hands-on Tutorial)

**Option 1: View Online (GitHub Pages — Recommended)**
- [View Tutorial Online](https://roozbeh412.github.io/data_sciences/ANLY530-Machine-Learning/Week11/Week11-EnsembleModeling-Tutorial.html)

**Option 2: Alternative Online Viewer**
- [View via htmlpreview](https://htmlpreview.github.io/?https://github.com/roozbeh412/data_sciences/blob/main/ANLY530-Machine-Learning/Week11/Week11-EnsembleModeling-Tutorial.html)

**Option 3: Download and Open Locally**
- Download [`Week11-EnsembleModeling-Tutorial.html`](./Week11-EnsembleModeling-Tutorial.html) and open it in your web browser

#### 2. Lecture Slides

- View [`lecture_12_ensemble_modeling-1.html`](./lecture_12_ensemble_modeling-1.html) directly in your browser.

---

## Course Content

This week covers:

### Lecture Topics
- The intuition behind ensemble learning — wisdom of the crowd
- Three conditions for a good ensemble (diversity, accuracy, independence)
- Voting ensembles — hard voting and soft voting
- Bagging (Bootstrap Aggregating) and Random Forests
- Boosting — AdaBoost and Gradient Boosting Machines (GBM)
- Stacking and meta-learning
- Bagging vs. Boosting trade-offs
- Picking the right ensemble for the right problem

### Hands-on Tutorial Topics
- The coin-flip thought experiment — why majority voting works
- Visualising the wisdom of the crowd as ensemble size grows
- Diversity demo — Decision Tree vs. Logistic Regression decision boundaries
- Voting classifiers from scratch (DT + RF + SVM on Iris)
  - Hard voting vs. soft voting accuracy comparison
- Bagging step-by-step
  - Bootstrap sampling visualisation (with/without replacement)
  - Out-of-Bag (OOB) sample explanation
  - Variance-reduction demo on `sin(x)` regression
- Random Forests
  - OOB error vs. number of trees
  - Feature importance from Mean Decrease in Gini
- Boosting
  - AdaBoost weight-evolution visualisation across rounds
  - Gradient Boosting on Iris with multinomial deviance curve
- Bagging vs. Boosting comparison table
- Stacking with K-fold out-of-fold predictions
  - Architecture diagram (base learners → meta-learner → output)
  - Multinomial logistic regression as meta-learner
- Head-to-head comparison on Iris (single + 7 ensemble methods)
  - Accuracy ranking bar chart
  - Side-by-side confusion matrices
- Regression ensembles on Boston Housing
  - Linear, Tree, RF, GBM, and a simple averaged ensemble
  - Predicted-vs-actual scatter and residual histograms
- Decision guide — which ensemble to use when

---

## Materials

- **HTML Tutorial**: `Week11-EnsembleModeling-Tutorial.Rmd` → `Week11-EnsembleModeling-Tutorial.html` (Interactive RMarkdown tutorial)
- **Lecture Slides**: `lecture_12_ensemble_modeling-1.html`

---

## Reading

- **Textbook**: *Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow* (Géron, 2019)
  - Chapter 7: Ensemble Learning and Random Forests
- **scikit-learn**: [1.11. Ensembles: Gradient boosting, random forests, bagging, voting, stacking](https://scikit-learn.org/stable/modules/ensemble.html)
- **GeeksforGeeks**: [Ensemble Learning — A Comprehensive Guide](https://www.geeksforgeeks.org/machine-learning/a-comprehensive-guide-to-ensemble-learning/)
- **Breiman, L.** (1996). Bagging predictors. *Machine Learning*, 24(2), 123–140.
- **Breiman, L.** (2001). Random forests. *Machine Learning*, 45(1), 5–32.
- **Freund, Y. & Schapire, R. E.** (1997). A decision-theoretic generalization of on-line learning and an application to boosting. *J. Computer and System Sciences*, 55(1), 119–139.
- **Friedman, J. H.** (2001). Greedy function approximation: A gradient boosting machine. *Annals of Statistics*, 29(5), 1189–1232.
- **Wolpert, D. H.** (1992). Stacked generalization. *Neural Networks*, 5(2), 241–259.

---

## Learning Path

### Step 1: Theory
1. Open the lecture slides (`lecture_12_ensemble_modeling-1.html`)
2. Read Chapter 7 in the Géron textbook
3. Internalise the three conditions: diversity, better-than-random, independence

### Step 2: Practice
1. Work through the tutorial (`Week11-EnsembleModeling-Tutorial.html`)
2. Follow each visualisation — observe how OOB error decays, how AdaBoost reweights points, and how predicted-vs-actual scatter tightens with ensembles
3. Compare voting, bagging, boosting, and stacking accuracies side-by-side

### Step 3: Apply
1. Take the same Iris models you trained in Weeks 02–06 and combine them into a hard- and soft-voting ensemble
2. Train a Random Forest and a Gradient Boosting model on a real dataset of your choice; compare against a single Decision Tree baseline
3. Build a stacked ensemble using out-of-fold predictions and a simple meta-learner (logistic regression)
4. Verify you can compile the `.Rmd` file to HTML on your own machine

---

## Key Concepts

### Ensemble Foundations
- **Wisdom of the Crowd**: Many independent estimators averaged together beat any individual estimator (Galton, 1907)
- **Diversity**: Models that make *different* errors are essential — identical models give no extra information
- **Better than Random**: Each model must be at least slightly above 50% accuracy or voting **amplifies** errors
- **Independence**: The lower the correlation of errors, the bigger the gain from voting

### Voting
- **Hard Voting**: Majority of class labels wins
- **Soft Voting**: Average of predicted probabilities — usually beats hard voting when probabilities are well-calibrated

### Bagging
- **Bootstrap Sample**: A sample of size N drawn *with replacement* from the original training set
- **OOB Sample**: The ~36.8% of rows not selected — used as a built-in test set
- **Random Forest**: Bagging + random feature subset at each split; reduces variance with no tuning
- **Variance Reduction**: Averaging cancels out the random fluctuations of high-variance learners

### Boosting
- **Sequential Training**: Each model is built on the *re-weighted* errors of the previous model
- **AdaBoost**: Re-weights misclassified rows so the next stump focuses on them
- **Gradient Boosting**: Each new tree fits the *residuals* of the current ensemble — gradient descent in function space
- **Bias Reduction**: Many weak learners combined into a strong one — but at higher overfitting risk

### Stacking
- **Meta-Learner**: A second-level model trained on the predictions of base models
- **Out-of-Fold Predictions**: Required to prevent the meta-learner from overfitting to base-model memorisation
- **Diversity Matters**: Base models must produce different mistake patterns for stacking to help

---

## Tools & Packages

### Required R Packages
```r
install.packages(c("tidyverse", "caret", "e1071", "rpart", "rpart.plot",
                   "randomForest", "gbm", "MASS", "pROC", "gridExtra",
                   "scales", "knitr", "kableExtra", "RColorBrewer", "seedhash"))
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
