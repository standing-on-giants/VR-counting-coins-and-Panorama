# VR Assignment: Coin Detection, Segmentation, and Panorama Creation

## Overview
This repository contains the implementation of two computer vision tasks:
1. Detection, segmentation, and counting of Indian coins from an image
2. Creation of a stitched panorama from multiple overlapping images

## Repository Structure
```
VR-counting-coins-and-Panorama/
├── countCoins.ipynb                  # Jupyter notebook for coin detection and counting
├── Image stitching panorama.ipynb    # Jupyter notebook for stitching two images
├── Multiple image.ipynb              # Jupyter notebook for stitching multiple images
└── README.md                         # This file
```

## Part 1: Coin Detection, Segmentation, and Counting

### Methods Used
- **Edge Detection**: Canny edge detection algorithm to identify coin boundaries
- **Region-based Segmentation**: Watershed algorithm for isolating individual coins
- **Contour Detection**: For identifying and counting distinct coins

### Results
- Successfully detected all coins in the input images
- Segmented each coin individually
- Accurately counted the total number of coins present in the images

### How to Run
1. Open `countCoins.ipynb` in Jupyter Notebook or Google Colab
2. Make sure the input image path is correctly set to your image containing Indian coins
3. Run all cells sequentially to:
   - Detect coins using edge detection
   - Segment individual coins
   - Count and display the total number of coins

## Part 2: Panorama Creation

### Methods Used
- **SIFT (Scale-Invariant Feature Transform)**: For detecting key points in overlapping images
- **Homography Estimation**: For determining the transformation between images
- **Image Warping**: For creating the final panorama

### Results
- Successfully detected key points in overlapping images
- Matched corresponding features across images
- Created seamless panoramas from both two and multiple images

### How to Run
For two-image panorama:
1. Open `Image stitching panorama.ipynb` in Jupyter Notebook or Google Colab
2. Set the paths to your two overlapping images
3. Run all cells to:
   - Extract and visualize SIFT features
   - Match key points between images
   - Generate and display the final panorama

For multi-image panorama:
1. Open `Multiple image.ipynb` in Jupyter Notebook or Google Colab
2. Set the paths to your multiple overlapping images
3. Run all cells to create a panorama from multiple images

## Dependencies
- Python 3.x
- OpenCV (cv2)
- NumPy
- Matplotlib
- Jupyter Notebook

To install all required dependencies:
```
pip install opencv-python numpy matplotlib jupyter
```

## Observations
- Edge detection parameters need to be carefully tuned based on the lighting conditions and contrast of the coin images
- SIFT feature detection works best when there is significant overlap between images (30-50%)
- The quality of the panorama depends on the stability of the camera during image capture
- Proper image alignment is crucial for creating seamless panoramas

## Author
Shashank Devarmani
IMT2022107, IIIT-Bangalore
