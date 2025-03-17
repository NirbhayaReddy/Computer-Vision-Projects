# Computer Vision Assignment 1

## Overview
This repository contains implementations of various image processing techniques in Python, including:
- **Histogram Equalization** for enhancing image contrast.
- **Image Thresholding** using Otsu's and Ni-Black's methods for binary segmentation.
- **Template Matching** using Normalized Cross-Correlation.
- **Creative Section** implementing Sum of Absolute Differences (SAD) for efficient template matching.

The project demonstrates the practical application of these techniques in computer vision.

---

## Features
### 1. Histogram Equalization
Enhances image contrast by redistributing pixel intensities using Probability Density Function (PDF) and Cumulative Distribution Function (CDF).
- Input: Grayscale image (e.g., `detective.png`).
- Output: Contrast-enhanced grayscale image with equalized histogram.

### 2. Image Thresholding
Implements two thresholding methods:
- **Otsu's Thresholding**: Global thresholding to separate foreground and background.
- **Ni-Black's Thresholding**: Adaptive thresholding for non-uniform illumination.
- Input: Grayscale image (e.g., `TEM cell.png`).
- Output: Binary segmented images.

### 3. Template Matching
Locates a template within an image using Normalized Cross-Correlation.
- Input: Original image and template (e.g., `snow.jpg` and `snowtemp.jpg`).
- Output: Location of the best match with visual markers.

### 4. Creative Section
Implements the Sum of Absolute Differences (SAD) method for faster template matching.
- Input: Original image and template (e.g., `WaldoBeach.jpg` and `WaldoBeachtemp.jpg`).
- Output: Location of the best match with bounding box visualization.

---

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/cv-assignment.git
   cd cv-assignment
   ```

2. Install dependencies:
   ```bash
   pip install numpy matplotlib scikit-image scipy
   ```

3. Place input images in the appropriate directory.

---

## How to Run
Run the Python script to execute all tasks:
```bash
python cv_assignment_1_ng3033.py
```
Ensure input images are correctly referenced in the script.

---

## Code Explanation

### Histogram Equalization
1. **PDF Function**: Computes pixel intensity distribution.
2. **CDF Function**: Calculates cumulative sum of PDF.
3. **Equalization**: Remaps pixel values using CDF for improved contrast.
4. **Visualization**: Displays original vs equalized images and their histograms.

### Image Thresholding
1. **Otsu's Method**:
   - Calculates inter-class variance to find optimal global threshold.
2. **Ni-Black's Method**:
   - Computes local thresholds based on mean and standard deviation within a window size.
3. **Visualization**:
   - Displays segmented binary images for different methods.

### Template Matching (Normalized Cross-Correlation)
1. Converts images to grayscale if necessary.
2. Slides the template over the image, calculating correlation scores at each position.
3. Identifies global peak and additional matches above defined thresholds.
4. Visualizes results with heatmaps and bounding boxes.

### Creative Section (SAD Method)
1. **Integral Image**: Computes cumulative sums for efficient region calculations.
2. **SAD Calculation**:
   - Measures similarity by summing absolute differences between template and image regions.
3. Visualizes matched region with bounding box.

---

## Results & Discussion

### Histogram Equalization
Improves contrast by redistributing pixel intensities, revealing hidden details in darker regions.

### Image Thresholding
- Otsu's method works well for uniform lighting but struggles with complex structures.
- Ni-Black's method adapts to local variations, providing better segmentation for non-uniform illumination.

### Template Matching
Normalized Cross-Correlation accurately identifies templates, compensating for brightness/contrast variations.

### Creative Section (SAD)
SAD is faster than cross-correlation but less robust to lighting variations, making it suitable for simpler scenarios.

---

## Limitations & Future Work
1. Histogram equalization may amplify noise in some cases.
2. Otsu's method is less effective for non-uniform illumination; adaptive methods like Ni-Black perform better but are computationally intensive.
3. SAD is faster but less robust compared to Normalized Cross-Correlation; hybrid approaches could improve accuracy.

---

## Dependencies
- `numpy`
- `matplotlib`
- `scikit-image`
- `scipy`

---

## License
This project is licensed under the MIT License.