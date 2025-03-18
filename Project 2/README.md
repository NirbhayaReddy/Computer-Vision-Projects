## Overview
This folder contains **Project 2**, which focuses on implementing and analyzing advanced computer vision techniques using Python. The project explores:
1. **Image Transformation and Stitching**: Combining multiple images into a single panorama using feature detection and homography estimation.
2. **Hough Transform**: Detecting lines on a runway and circles on a landing pad for navigation purposes.
3. **Segmentation**: Implementing Mean Shift Segmentation and Normalized Graph Cut Segmentation for object detection.
4. **Creative Section**: Using the Watershed Algorithm for segmentation and comparing its performance with other methods.

For detailed explanations of the methods, results, and discussions, please refer to the accompanying [Documentation.pdf](./Documentation.pdf).

---

## Features
### 1. Image Transformation and Stitching
- **Description**: Combines two images into a single stitched panorama using ORB feature detection, Brute-Force matching, RANSAC homography estimation, and perspective warping.
- **Key Functions**:
  - `ORB_create`: Detects keypoints and computes descriptors.
  - `BFMatcher`: Matches features between images.
  - `compute_homography`: Estimates homography matrix using RANSAC.
  - `warpPerspective`: Warps images to align them in a common plane.

### 2. Hough Transform
#### Runway Detection
- **Description**: Detects lines on a runway using edge detection (Sobel filters, Non-Maximum Suppression, Hysteresis Thresholding) followed by custom Hough Transform implementation.
- **Key Functions**:
  - `image_gradients`: Computes gradient magnitude and angle using Sobel filters.
  - `nms`: Applies Non-Maximum Suppression to thin edges.
  - `threshold_edges`: Implements Hysteresis Thresholding for edge refinement.
  - `Hough Transform`: Maps edge pixels to parameter space for line detection.

#### Landing Pad Detection
- **Description**: Detects concentric circles on a landing pad using custom Hough Transform for circles.
- **Key Functions**:
  - `generate_gaussian_kernel`: Creates Gaussian kernel for blurring.
  - `find_strongest_circle`: Implements circle detection using accumulator array in Hough space.

### 3. Segmentation
#### Mean Shift Segmentation
- **Description**: Smooths the image using spatial and color filtering, followed by Canny edge detection to highlight boundaries.
- **Key Functions**:
  - `pyrMeanShiftFiltering`: Applies Mean Shift filtering to enhance regions.
  - `detect_edges`: Detects edges using the Canny algorithm.

#### Normalized Graph Cut Segmentation
- **Description**: Uses superpixels (SLIC) and spectral clustering to segment objects based on color similarity.
- **Key Functions**:
  - `slic`: Generates superpixels for efficient segmentation.
  - `SpectralClustering`: Performs clustering based on affinity matrix constructed from color similarity.

### 4. Creative Section (Watershed Algorithm)
- **Description**: Implements the Watershed Algorithm to segment objects based on intensity gradients, followed by evaluation using Intersection over Union (IoU).
- **Key Functions**:
  - `distanceTransform`: Computes distance from background pixels to foreground pixels.
  - `watershed`: Applies Watershed segmentation to separate overlapping objects.

---

## Dependencies
To run the code in this folder, you need the following Python libraries:
- `numpy`
- `matplotlib`
- `opencv-python`
- `scipy`
- `skimage`

Install them using:
```bash
pip install numpy matplotlib opencv-python scipy scikit-image
```

---

## How to Use
1. Open or download the Notebook (`Project_2.ipynb`) and run in google collab for seamless outputs.
2. Ensure input images are correctly referenced in the code (e.g., `runway.jpeg`, `SpaceXmap.jpg`, etc.).
3. Execute each section of the code sequentially to run all tasks and visualize results.

---

## Refer to Documentation
For detailed explanations of each method, their implementation, results, and comparative discussions, please refer to [Documentation.pdf](./Documentation.pdf).