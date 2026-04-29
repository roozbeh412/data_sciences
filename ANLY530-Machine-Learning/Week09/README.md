# Week 09: Dimensionality Reduction — PCA, Factor Analysis & LDA

## Access Week 09 Tutorials

### Quick Links

| Resource | Link |
|---|---|
| **Hands-on Tutorial** (HTML, recommended) | **[Open Week 09 Tutorial](https://roozbeh412.github.io/data_sciences/ANLY530-Machine-Learning/Week09/Week09-DimensionalityReduction-Tutorial.html)** |
| Tutorial source (RMarkdown) | [Week09-DimensionalityReduction-Tutorial.Rmd](./Week09-DimensionalityReduction-Tutorial.Rmd) |
| Tutorial (alternative viewer) | [htmlpreview.github.io](https://htmlpreview.github.io/?https://github.com/roozbeh412/data_sciences/blob/main/ANLY530-Machine-Learning/Week09/Week09-DimensionalityReduction-Tutorial.html) |
| Lecture Slides (PowerPoint) | [ANLY530Lecture10_PFetureEngineering2.pptx](./ANLY530Lecture10_PFetureEngineering2.pptx) |
| Course Home (all weeks) | [roozbeh412.github.io/data_sciences/#530](https://roozbeh412.github.io/data_sciences/#530) |

### Access Options

#### 1. Dimensionality Reduction (Hands-on Tutorial)

**Option 1: View Online (GitHub Pages — Recommended)**
- [View Tutorial Online](https://roozbeh412.github.io/data_sciences/ANLY530-Machine-Learning/Week09/Week09-DimensionalityReduction-Tutorial.html)

**Option 2: Alternative Online Viewer**
- [View via htmlpreview](https://htmlpreview.github.io/?https://github.com/roozbeh412/data_sciences/blob/main/ANLY530-Machine-Learning/Week09/Week09-DimensionalityReduction-Tutorial.html)

**Option 3: Download and Open Locally**
- Download [`Week09-DimensionalityReduction-Tutorial.html`](./Week09-DimensionalityReduction-Tutorial.html) and open it in your web browser

#### 2. Lecture Slides

- Download [`ANLY530Lecture10_PFetureEngineering2.pptx`](./ANLY530Lecture10_PFetureEngineering2.pptx) from this directory.

---

## Course Content

This week covers:

### Lecture Topics
- The curse of dimensionality
- Feature extraction vs. feature selection
- Principal Component Analysis (PCA)
- Factor Analysis (FA)
- Linear Discriminant Analysis (LDA)

### Hands-on Tutorial Topics
- The curse of dimensionality — why more features can hurt
  - Average pairwise distance growth visualisation
- Principal Component Analysis (PCA)
  - Step-by-step PCA on 2D data with eigenvector visualisation
  - Variance explained and scree plots
  - PCA on Iris: 4D → 2D projection coloured by species
  - Loadings bar chart and biplot
- Factor Analysis (FA)
  - PCA vs. FA comparison table
  - Factor loadings with varimax rotation
  - Communality analysis
  - Parallel analysis for choosing number of factors
- Linear Discriminant Analysis (LDA)
  - Between-class vs. within-class scatter
  - LDA on Iris: maximising class separation
  - PCA vs. LDA head-to-head comparison
- Impact on classification accuracy (RF with all features vs. PCA vs. LDA)
- PCA for high-dimensional visualisation (mtcars, 11 → 2)
- Reconstruction error analysis
- Practical decision guide

---

## Materials

- **HTML Tutorial**: `Week09-DimensionalityReduction-Tutorial.Rmd` → `Week09-DimensionalityReduction-Tutorial.html` (Interactive RMarkdown tutorial)
- **Lecture Slides**: `ANLY530Lecture10_PFetureEngineering2.pptx`

---

## Reading

- **Textbook**: *Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow* (Géron, 2019)
  - Chapter 8: Dimensionality Reduction
- **Encord**: [Top 12 Dimensionality Reduction Techniques](https://encord.com/blog/dimentionality-reduction-techniques-machine-learning/)
- **Medium**: [Mastering Feature Extraction: PCA, t-SNE, and LDA](https://medium.com/@abhaysingh71711/mastering-feature-extraction-pca-t-sne-and-lda-in-machine-learning-part-1-0da5c3d978ad)

---

## Learning Path

### Step 1: Theory
1. Review the lecture slides (`ANLY530Lecture10_PFetureEngineering2.pptx`)
2. Read Chapter 8 in the Géron textbook
3. Understand the intuition: PCA = max variance, FA = latent factors, LDA = max class separation

### Step 2: Practice
1. Work through the tutorial (`Week09-DimensionalityReduction-Tutorial.html`)
2. Follow along with the code chunks — observe how scree plots, biplots, and LDA projections reveal data structure
3. Compare PCA and LDA projections on the Iris dataset

### Step 3: Apply
1. Try PCA on a high-dimensional dataset (e.g., wine, breast cancer)
2. Experiment with different numbers of components and observe the reconstruction error
3. Apply LDA before a classifier and compare accuracy with and without dimensionality reduction
4. Verify you can compile the `.Rmd` file to HTML on your own machine

---

## Key Concepts

### Dimensionality Reduction
- **Curse of Dimensionality**: High dimensions → sparse data, overfitting, slow computation
- **PCA**: Unsupervised; finds orthogonal axes (principal components) that maximise variance
- **Eigenvalues/Eigenvectors**: Eigenvalues measure variance along each PC; eigenvectors define the directions
- **Scree Plot**: Plot eigenvalues to find the elbow — determines how many PCs to keep
- **Loadings**: Weights showing each feature's contribution to each PC
- **Biplot**: Overlay feature arrows on the PC scatter to see what drives each axis
- **Factor Analysis**: Assumes observed variables are caused by latent factors + noise
- **Communality**: Proportion of a variable's variance explained by the factors
- **Varimax Rotation**: Rotate factors to make loadings more interpretable (sparse)
- **LDA**: Supervised; finds linear combinations that maximise between-class / within-class scatter
- **Reconstruction Error**: MSE between original data and data reconstructed from k PCs

---

## Tools & Packages

### Required R Packages
```r
install.packages(c("tidyverse", "gridExtra", "scales", "corrplot", "MASS", "psych", "caret", "randomForest", "knitr", "kableExtra", "seedhash"))
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
