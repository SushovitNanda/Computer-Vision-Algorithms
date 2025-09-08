# Computer Vision  Basic Algorithms

A comprehensive implementation of fundamental computer vision algorithms from scratch using Python and NumPy. This project demonstrates various image processing techniques including RGB to grayscale conversion, noise analysis, edge detection methods, and a complete Canny edge detector implementation.

## Overview

This repository covers four main computer vision tasks:

1. **RGB to Grayscale Conversion & Channel Analysis** - Implement luminance formula and analyze individual color channels
2. **Gaussian Noise Addition & Analysis** - Add noise to images and study its effects on processing
3. **Edge Detection Comparison** - Compare Sobel and Laplacian operators with different filter sizes
4. **Canny Edge Detector** - Complete implementation from scratch with all intermediate steps

## Technologies Used

- **Python 3.x** - Core programming language
- **NumPy** - Numerical computations and array operations
- **Matplotlib** - Visualization and plotting
- **OpenCV** - Limited to image loading and color space conversion only
- **Math** - Mathematical functions and kernel generation

**Note**: All algorithms are implemented from scratch. OpenCV is used only for image loading and preprocessing.

## Features Implemented

### 1. RGB to Grayscale Conversion
- **Luminance Formula**: `Y = 0.299×R + 0.587×G + 0.114×B`
- Individual color channel extraction and analysis
- Statistical analysis of color channels (mean, standard deviation)
- Histogram computation and visualization

### 2. Gaussian Noise Analysis
- Gaussian noise addition with configurable parameters (μ=0, σ²=20)
- SNR calculation and analysis
- Clean vs noisy image comparison
- Histogram analysis of noise effects

### 3. Edge Detection Methods
- **Sobel Edge Detector**:
  - Horizontal and vertical gradient detection
  - Combined gradient magnitude computation
  - Support for 3×3, 5×5, and 7×7 kernel sizes
- **Laplacian Edge Detector**:
  - Second derivative-based edge detection
  - Multiple kernel size support
  - Zero-crossing detection

### 4. Canny Edge Detector (Complete Implementation)
- **Step 1**: Gaussian smoothing (σ=1.4)
- **Step 2**: Gradient magnitude and orientation computation
- **Step 3**: Non-maximum suppression for edge thinning
- **Step 4**: Hysteresis thresholding with dual thresholds
- **Step 5**: Final edge map generation

## Key Results

### Image Statistics
- **Original Image**: 1280×914×3 pixels, 3,509,760 total pixels
- **Color Channel Analysis**:
  - Red: Mean=128.55, Std=57.12
  - Green: Mean=122.03, Std=53.25
  - Blue: Mean=116.81, Std=50.92

### Edge Detection Performance
- **3×3 filters**: Optimal edge detection quality with clear, well-defined edges
- **5×5 filters**: Moderate performance with some edge degradation
- **7×7 filters**: Poor edge detection with incomplete and disturbed results

### Canny Algorithm Parameters
- **Gaussian σ**: 1.4 (optimal noise reduction without excessive blurring)
- **High threshold**: 15% (strong edge detection)
- **Low threshold**: 5% (weak edge connection)

## Key Findings

1. **Filter Size Impact**: Smaller filters (3×3) provide superior edge detection quality compared to larger filters
2. **Noise Sensitivity**: The implemented algorithms show varying sensitivity to Gaussian noise
3. **Canny Superiority**: The Canny edge detector provides the most robust edge detection among all tested methods
4. **Parameter Optimization**: Careful parameter tuning is crucial for optimal edge detection performance

## Visualizations

The project includes comprehensive visualizations for:
- Original image and color channel histograms
- Grayscale conversion results
- Noise addition effects and comparisons
- Edge detection results across different methods and filter sizes
- Complete Canny algorithm step-by-step visualization


## Report

A detailed PDF report is included with:
- Mathematical formulations
- Algorithm explanations
- Results analysis
- Performance comparisons
- Visual documentation

*This implementation demonstrates a thorough understanding of fundamental computer vision algorithms and their practical applications in image processing.*
