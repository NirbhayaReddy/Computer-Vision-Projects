Here’s a clean and concise **README** file for **Project 1** in the `Project_1` folder, including dependencies and relevant details:

---

# Project 1: Computer Vision Assignment 1

## Overview
This folder contains **Project 1**, which focuses on implementing and analyzing various image processing techniques using a Jupyter Notebook (`Project1.ipynb`). The project demonstrates key concepts in computer vision, including:
- **Histogram Equalization** for enhancing image contrast.
- **Image Thresholding** using Otsu's and Ni-Black's methods for binary segmentation.
- **Template Matching** using Normalized Cross-Correlation.
- **Creative Section** implementing Sum of Absolute Differences (SAD) for efficient template matching.

For a detailed explanation of the methods, results, and discussions, please refer to the accompanying [Report.pdf](./Report.pdf).

---

## Features
### 1. Histogram Equalization
Enhances image contrast by redistributing pixel intensities using Probability Density Function (PDF) and Cumulative Distribution Function (CDF).

### 2. Image Thresholding
Implements two thresholding methods:
- **Otsu's Thresholding**: Global thresholding to separate foreground and background.
- **Ni-Black's Thresholding**: Adaptive thresholding for non-uniform illumination.

### 3. Template Matching
Locates a template within an image using Normalized Cross-Correlation.

### 4. Creative Section
Implements the Sum of Absolute Differences (SAD) method for faster template matching.

---

## Dependencies
To run the notebook and reproduce the results, you need the following Python libraries:
- `numpy`
- `matplotlib`
- `scikit-image`
- `scipy`

Install them using:
```bash
pip install numpy matplotlib scikit-image scipy
```

---

## How to Use
1. Open the Jupyter Notebook (`Project1.ipynb`) in your preferred environment (e.g., Jupyter Lab, Jupyter Notebook, or Google Colab).
2. Ensure input images are correctly referenced in the notebook.
3. Execute each cell sequentially to run all tasks.
4. Refer to the visual outputs in the notebook for results.

---

## Refer to Report
For detailed explanations of each method, their implementation, results, and comparative discussions, please refer to [Report.pdf](./Report.pdf).