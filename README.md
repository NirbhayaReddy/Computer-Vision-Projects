# Computer Vision Projects

## Overview
This repository contains solutions to two computer vision projects, each focusing on different aspects of image processing and analysis. The projects are organized into separate folders:

1. **Project 1: Computer Vision Assignment 1**  
   Focuses on basic image processing techniques such as histogram equalization, thresholding, template matching, and creative implementations like Sum of Absolute Differences (SAD).

2. **Project 2: Computer Vision Assignment 2**  
   Explores advanced computer vision techniques, including image stitching, Hough Transform for line and circle detection, segmentation methods (Mean Shift and Normalized Graph Cut), and Watershed Algorithm for object segmentation.

---

## Repository Structure
```
.
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   ├── bug_report.md
│   │   ├── feature_request.md
├── Project_1/
│   ├── Documentation.pdf
│   ├── Data/
│   │   ├── detective.png
│   │   ├── snow.png
│   │   ├── snowtemp.jpg
│   │   ├── TEM cell.jpg
│   │   ├── WaldoBeach.jpg
│   │   └── WaldoBeachtemp.jpg
│   ├── Project1.ipynb
│   └── README.md
├── Project_2/
│   ├── Documentation.pdf
│   ├── Data/
│   │   ├── 1.jpeg
│   │   ├── 2.jpg
│   │   |── 3.jpg
│   │   ├── runway.jpeg
│   │   ├── SpaceXmap.jpg
│   │   └── stop.jpg
│   ├── Project2.ipynb
│   └── README.md
├── .gitignore
└── README.md (this file)
```

---

## Projects

### **Project 1: Computer Vision Assignment 1**
This project demonstrates foundational computer vision techniques:
- **Histogram Equalization**: Enhances image contrast by redistributing pixel intensities.
- **Image Thresholding**: Implements Otsu's and Ni-Black's methods for binary segmentation.
- **Template Matching**: Locates templates within larger images using Normalized Cross-Correlation.
- **Creative Section (SAD)**: Implements the Sum of Absolute Differences method for faster template matching.

Refer to the [Project 1 README](./Project_1/README.md) for more details.  
For a detailed explanation of the methods and results, see [Documentation.pdf](./Project_1/Documentation.pdf).

---

### **Project 2: Computer Vision Assignment 2**
This project explores advanced image processing techniques:
- **Image Transformation and Stitching**: Combines two images into a panorama using ORB feature detection and homography estimation.
- **Hough Transform**:
  - Detects lines on a runway to assist in navigation.
  - Identifies circles on a landing pad for rocket landing.
- **Segmentation Methods**:
  - Mean Shift Segmentation for noise reduction and boundary enhancement.
  - Normalized Graph Cut Segmentation using superpixels and spectral clustering.
- **Creative Section (Watershed Algorithm)**: Segments objects in an image based on intensity gradients and evaluates performance using IoU metrics.

Refer to the [Project 2 README](./Project_2/README.md) for more details.  
For a detailed explanation of the methods and results, see [Documentation.pdf](./Project_2/Documentation.pdf).

---

## Dependencies
Both projects require the following Python libraries:
- `numpy`
- `matplotlib`
- `opencv-python`
- `scipy`
- `scikit-image`

Install them using:
```bash
pip install numpy matplotlib opencv-python scipy scikit-image
```

---

## How to Use the Repository
1. Clone the repository:
   ```bash
   git clone https://github.com/NirbhayaReddy/Computer-Vision-Projects.git
   cd computer-vision-repo
   ```

2. Navigate to the respective project folder (`Project_1` or `Project_2`) to access code, images, and documentation.

3. Open the Jupyter Notebook (`.ipynb` files) in your preferred environment (e.g., Jupyter Lab or Google Colab). Ideally in Google Collab as the work was done in Google Collab.

4. Execute the notebook cells sequentially to run all tasks.

---

## About the .github Folder
The .github folder contains templates and configurations specific to this repository:

Issue Templates: Predefined templates for reporting bugs or requesting features are located in .github/ISSUE_TEMPLATE/.

bug_report.md: Template for submitting bug reports.

feature_request.md: Template for requesting new features or enhancements.

These templates help maintain consistency in communication and collaboration within the repository.

---

## Git Ignore File
The `.gitignore` file ensures that unnecessary files are excluded from version control. It includes:
- macOS system files (`.DS_Store`)
- Python bytecode (`__pycache__/`, `*.pyc`)
- Virtual environments (`env/`, `.venv/`)
- Jupyter Notebook checkpoints (`.ipynb_checkpoints/`)
- Logs, temporary files, and editor-specific settings (`*.log`, `.vscode/`)

---

## License
This repository is licensed under the MIT License.