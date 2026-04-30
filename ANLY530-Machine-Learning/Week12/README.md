# Week 12: Neural Networks — Layers, Signals, and Learning from Examples

## Access Week 12 Tutorials

### Quick Links

| Resource | Link |
|---|---|
| **Hands-on Tutorial** (HTML, recommended) | **[Open Week 12 Tutorial](https://roozbeh412.github.io/data_sciences/ANLY530-Machine-Learning/Week12/Week12-NeuralNetworks-Tutorial.html)** |
| Tutorial source (R Markdown) | [Week12-NeuralNetworks-Tutorial.Rmd](./Week12-NeuralNetworks-Tutorial.Rmd) |
| Tutorial (alternative viewer) | [htmlpreview.github.io](https://htmlpreview.github.io/?https://github.com/roozbeh412/data_sciences/blob/main/ANLY530-Machine-Learning/Week12/Week12-NeuralNetworks-Tutorial.html) |
| Lecture Slides (PowerPoint) | [ANLY530Lecture13_NeuralNetworks.pptx](./ANLY530Lecture13_NeuralNetworks.pptx) |
| Course Home (all weeks) | [roozbeh412.github.io/data_sciences/#530](https://roozbeh412.github.io/data_sciences/#530) |

### Access Options

#### 1. Neural Networks (hands-on tutorial)

**Option 1: View online (GitHub Pages — recommended)**

- [View tutorial online](https://roozbeh412.github.io/data_sciences/ANLY530-Machine-Learning/Week12/Week12-NeuralNetworks-Tutorial.html)

**Option 2: Alternative online viewer**

- [View via htmlpreview](https://htmlpreview.github.io/?https://github.com/roozbeh412/data_sciences/blob/main/ANLY530-Machine-Learning/Week12/Week12-NeuralNetworks-Tutorial.html)

**Option 3: Download and open locally**

- Knit `Week12-NeuralNetworks-Tutorial.Rmd` to HTML in RStudio, or download [`Week12-NeuralNetworks-Tutorial.html`](./Week12-NeuralNetworks-Tutorial.html) from this folder after it is generated and open it in your browser.

#### 2. Lecture slides

- Download [`ANLY530Lecture13_NeuralNetworks.pptx`](./ANLY530Lecture13_NeuralNetworks.pptx) from this directory.

---

## Course content

This week covers:

### Lecture topics

- Neurons, layers (input, hidden, output), weights, and biases  
- Forward propagation and activation functions (sigmoid, tanh, ReLU)  
- Why nonlinearity matters (XOR intuition)  
- Loss functions, gradients, backpropagation, and gradient descent  
- Capacity, overfitting, and interpretability trade-offs  

### Hands-on tutorial topics

- Plain-English vocabulary table  
- Activation-function comparison plots  
- Feedforward network schematic  
- Numeric forward pass (spam-keyword style, aligned with readings)  
- XOR: logistic regression vs. neural network decision regions  
- Loss landscape + gradient-descent intuition  
- Iris: `multinom` vs. `nnet`, confusion matrices, hidden-unit sweep  

---

## Materials

- **HTML tutorial**: `Week12-NeuralNetworks-Tutorial.Rmd` → `Week12-NeuralNetworks-Tutorial.html`  
- **Lecture slides**: `ANLY530Lecture13_NeuralNetworks.pptx`  

---

## Reading

- **GeeksforGeeks**: [Neural Networks — A beginner’s guide](https://www.geeksforgeeks.org/deep-learning/neural-networks-a-beginners-guide/)  
- **Victor Zhou**: [Introduction to Neural Networks](https://victorzhou.com/blog/intro-to-neural-networks/)  
- **Géron**: *Hands-On Machine Learning*, neural net / deep learning chapters  
- **Goodfellow et al.** (2016). *Deep Learning*. MIT Press (reference).  

---

## Learning path

### Step 1: Theory

1. Follow `ANLY530Lecture13_NeuralNetworks.pptx`  
2. Read the GeeksforGeeks and Victor Zhou articles above  

### Step 2: Practice

1. Work through `Week12-NeuralNetworks-Tutorial.html`  
2. Pay special attention to the XOR plots and the Iris comparisons  

### Step 3: Apply

1. Re-knit the `.Rmd` on your machine after installing missing packages  
2. Experiment with `size` (hidden units) and `decay` on a small tabular dataset  

---

## Tools and packages

### Required R packages

```r
install.packages(c(
  "rmarkdown", "pacman", "ggplot2", "dplyr", "tibble", "purrr",
  "scales", "knitr", "RColorBrewer", "nnet", "remotes"
))
remotes::install_github("roozbeh412/seedhash", subdir = "R")
```

### Recommended software

- **R**: 4.2 or newer (recommended for CRAN binaries)  
- **RStudio / Posit**: current release  

---

## Quick links

- [← Back to course home](../README.md)

---

<div align="center">

**ANLY 530 — Principles & Applications of Machine Learning**  
*Harrisburg University*

</div>
