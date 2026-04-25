# Week 07: Unsupervised Learning — K-Means & Hierarchical Clustering

## Lecture Materials

### Viewing the Presentations

This week has an HTML tutorial and lecture slides available online:

#### 1. Unsupervised Learning (Hands-on Tutorial)

**Option 1: View Online (GitHub Pages - Recommended)**
- [View Tutorial Online](https://roozbeh412.github.io/data_sciences/ANLY530-Machine-Learning/Week07/Week07-UnsupervisedLearning-Tutorial.html)

**Option 2: Alternative Online Viewer**
- [View via htmlpreview](https://htmlpreview.github.io/?https://github.com/roozbeh412/data_sciences/blob/main/ANLY530-Machine-Learning/Week07/Week07-UnsupervisedLearning-Tutorial.html)

**Option 3: Download and Open Locally**
- Download `Week07-UnsupervisedLearning-Tutorial.html` and open it in your web browser

#### 2. Lecture Slides

- Download `ANLY530Lecture08UnsupervisedLearning.pptx` from this directory.

---

## Course Content

This week covers:

### Lecture Topics
- Supervised vs. Unsupervised Learning — the big picture
- K-Means Clustering algorithm and objective function (WCSS)
- Choosing K: Elbow Method, Silhouette Analysis, Gap Statistic
- K-Means pitfalls: initialization sensitivity, cluster shape assumptions, feature scaling
- Hierarchical Clustering: agglomerative (bottom-up) and divisive (top-down)
- Linkage methods: single, complete, average, Ward
- Dendrograms: reading, cutting, and interpreting

### Hands-on Tutorial Topics
- Supervised vs. unsupervised learning comparison
  - Side-by-side visualizations of labeled vs. unlabeled data
- K-Means Clustering
  - Step-by-step algorithm walkthrough with multi-panel iteration visualization
  - Within-Cluster Sum of Squares (WCSS / inertia) objective function
  - Voronoi-style cluster decision regions
- Choosing K
  - Elbow Method plot with annotation
  - Silhouette analysis for multiple K values
  - Average silhouette width comparison
- K-Means pitfalls and solutions
  - Initialization sensitivity (multiple random starts)
  - K-Means++ initialization
  - Failure on non-spherical data (moon-shaped clusters)
  - Feature scaling before vs. after comparison
- Hierarchical Clustering
  - Agglomerative algorithm walkthrough
  - Linkage methods explained with plain English analogies
  - Dendrogram visualization with colored branches
  - Side-by-side linkage method comparison
- Cutting the dendrogram — from tree to clusters
  - Cut height selection and resulting cluster assignments
  - K-Means vs. Hierarchical Clustering comparison on the same data
- Real data: clustering the Iris dataset
  - PCA-reduced scatter plots colored by cluster vs. true species
  - Cluster-to-species correspondence table
  - Iris dendrogram
- K-Means vs. Hierarchical Clustering comparison table
- DBSCAN — brief introduction to density-based clustering
- Practical tips and decision guide

---

## Materials

- **HTML Tutorial**: `Week07-UnsupervisedLearning-Tutorial.Rmd` → `Week07-UnsupervisedLearning-Tutorial.html` (Interactive RMarkdown tutorial)
- **Lecture Slides**: `ANLY530Lecture08UnsupervisedLearning.pptx`

---

## Reading

- **Textbook**: *Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow* (Géron, 2019)
  - Chapter 9: Unsupervised Learning Techniques
- **Wikipedia**: [Unsupervised learning](https://en.wikipedia.org/wiki/Unsupervised_learning)
- **Wikipedia**: [K-means clustering](https://en.wikipedia.org/wiki/K-means_clustering)
- **Wikipedia**: [Hierarchical clustering](https://en.wikipedia.org/wiki/Hierarchical_clustering)
- **Kaggle**: [K-means & Hierarchical Clustering](https://www.kaggle.com/code/abdallahwagih/k-means-hierarchical-clustering)

---

## Learning Path

### Step 1: Theory
1. Review the lecture slides (`ANLY530Lecture08UnsupervisedLearning.pptx`)
2. Read Chapter 9 in the Géron textbook
3. Understand the intuition: what changes when there are no labels, and how K-Means and Hierarchical Clustering discover structure in data

### Step 2: Practice
1. Work through the tutorial (`Week07-UnsupervisedLearning-Tutorial.html`)
2. Follow along with the code chunks — observe how centroids move, dendrograms form, and cluster assignments change
3. Compare K-Means and Hierarchical Clustering results on the Iris dataset

### Step 3: Apply
1. Try clustering on a new dataset (e.g., `USArrests`, `mtcars`)
2. Experiment with different values of K and linkage methods
3. Use silhouette analysis to select the best K for your data
4. Verify you can compile the `.Rmd` file to HTML on your own machine

---

## Key Concepts

### Unsupervised Learning
- **Unsupervised Learning**: Finding structure in data without labeled outcomes
- **Clustering**: Grouping similar observations together
- **K-Means**: Partition data into K clusters by minimizing within-cluster sum of squares
- **WCSS (Inertia)**: Sum of squared distances from each point to its cluster centroid
- **Elbow Method**: Plot WCSS vs. K and look for the "bend" in the curve
- **Silhouette Score**: Measures how well each point fits its own cluster vs. the nearest other cluster
- **Hierarchical Clustering**: Builds a tree (dendrogram) of progressively merged clusters
- **Agglomerative**: Bottom-up approach — start with individual points, merge the closest pairs
- **Dendrogram**: Tree diagram showing the order and distance of cluster merges
- **Linkage**: Rule for measuring distance between clusters (single, complete, average, Ward)
- **K-Means++**: Improved initialization that spreads starting centroids apart
- **DBSCAN**: Density-based clustering that finds arbitrary-shaped clusters without specifying K

---

## Tools & Packages

### Required R Packages
```r
install.packages(c("tidyverse", "gridExtra", "scales", "cluster", "factoextra", "dendextend", "dbscan", "GGally", "knitr", "kableExtra", "seedhash"))
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
