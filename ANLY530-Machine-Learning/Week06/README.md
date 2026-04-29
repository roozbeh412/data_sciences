# Week 06: Naive Bayes Classifiers

## Lecture Materials

### Viewing the Presentations

This week has an HTML tutorial and lecture slides available online:

#### 1. Naive Bayes Classifiers (Hands-on Tutorial)

**Option 1: View Online (GitHub Pages - Recommended)**
- [View Tutorial Online](https://roozbeh412.github.io/data_sciences/ANLY530-Machine-Learning/Week06/Week06-NaiveBayes-Tutorial.html)

**Option 2: Alternative Online Viewer**
- [View via htmlpreview](https://htmlpreview.github.io/?https://github.com/roozbeh412/data_sciences/blob/main/ANLY530-Machine-Learning/Week06/Week06-NaiveBayes-Tutorial.html)

**Option 3: Download and Open Locally**
- Download `Week06-NaiveBayes-Tutorial.html` and open it in your web browser

#### 2. Lecture Slides

- Download `Lecture07-NB.pdf` from this directory.

---

## Course Content

This week covers:

### Lecture Topics
- Bayes' Theorem and conditional probability
- Prior, likelihood, evidence, and posterior
- The naive independence assumption
- Gaussian, Multinomial, and Bernoulli Naive Bayes
- Applications: spam filtering, text classification

### Hands-on Tutorial Topics
- Bayes' Theorem — updating beliefs with evidence (spam email example)
- The four components: prior, likelihood, evidence, posterior
- The "Play Tennis" dataset — Naive Bayes by hand
  - Frequency tables and manual probability computation
  - Step-by-step prediction walkthrough
- The naive independence assumption and why it works despite being wrong
  - Feature correlation heatmap showing violated assumptions
- Types of Naive Bayes classifiers
  - Gaussian NB for continuous features (bell curves per class)
  - Multinomial NB for count data (text classification)
  - Bernoulli NB for binary features
- Building Gaussian NB in R with `e1071::naiveBayes()`
  - Learned parameter visualisation (bell curves per feature × species)
  - Posterior probability heatmap
  - Decision boundary on Iris petal features
- The zero-frequency problem and Laplace smoothing
- Naive Bayes for text classification (spam filtering from scratch)
- Model comparison: Decision Tree vs. Random Forest vs. SVM vs. Naive Bayes
  - 4-panel decision boundary comparison
  - Training speed benchmark
- Learning curves: test accuracy vs. training set size
- Advantages, disadvantages, and practical tips

---

## Materials

- **HTML Tutorial**: `Week06-NaiveBayes-Tutorial.Rmd` → `Week06-NaiveBayes-Tutorial.html` (Interactive RMarkdown tutorial)
- **Lecture Slides**: `Lecture07-NB.pdf`

---

## Reading

- **Textbook**: *Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow* (Géron, 2019)
  - Chapter 3: Classification
- **scikit-learn documentation**: [1.9. Naive Bayes](https://scikit-learn.org/stable/modules/naive_bayes.html)
- **Wikipedia**: [Naive Bayes classifier](https://en.wikipedia.org/wiki/Naive_Bayes_classifier)

---

## Learning Path

### Step 1: Theory
1. Review the lecture slides (`Lecture07-NB.pdf`)
2. Read Chapter 3 in the Géron textbook
3. Understand the intuition: Bayes' Theorem, the naive assumption, and why it works

### Step 2: Practice
1. Work through the tutorial (`Week06-NaiveBayes-Tutorial.html`)
2. Follow along with the code chunks — observe how the bell curves, decision boundaries, and probabilities change
3. Compare Naive Bayes decision boundaries with Decision Tree, Random Forest, and SVM from previous weeks

### Step 3: Apply
1. Try Naive Bayes on a dataset with more features
2. Experiment with the `laplace` smoothing parameter
3. Build a simple text classifier using the bag-of-words approach
4. Verify you can compile the `.Rmd` file to HTML on your own machine

---

## Key Concepts

### Naive Bayes Classification
- **Bayes' Theorem**: posterior ∝ likelihood × prior — update beliefs as evidence arrives
- **Prior P(C)**: How common each class is before seeing features
- **Likelihood P(X|C)**: How probable the features are under each class
- **Posterior P(C|X)**: Updated probability of each class given the features
- **Naive Assumption**: All features are conditionally independent given the class
- **Gaussian NB**: Assumes continuous features follow normal distributions per class
- **Multinomial NB**: For count/frequency data (e.g., word counts in text)
- **Bernoulli NB**: For binary features (present/absent)
- **Laplace Smoothing**: Adds pseudo-counts to prevent zero probabilities
- **Log-Probabilities**: Avoids numerical underflow when multiplying many small probabilities

---

## Tools & Packages

### Required R Packages
```r
install.packages(c("tidyverse", "e1071", "caret", "gridExtra", "scales", "rpart", "randomForest", "knitr", "kableExtra", "seedhash"))
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
