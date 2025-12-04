# Object Detection and Image Analysis README
This notebook performs comprehensive image analysis using deep learning object detection models and traditional image processing techniques.

## Overview
The code is organized into three main parts:

### Part A-0: Image File Loading and Feature Engineering
- Loads images from the "Image Files" folder
- Displays basic image properties (dimensions, color mode, file size)
- Visualizes sample images in a grid
- Analyzes RGB color channels individually
- Demonstrates image resizing while maintaining aspect ratio

### Part A-1: Deep Learning Object Detection
- Implements two object detection algorithms:
  - Faster R-CNN (with ResNet50 backbone)
  - YOLOv8 (nano version)
- For each image, both algorithms detect objects and provide:
  - Number of objects detected
  - List of detected object names
  - Confidence scores (max and average)
  - Processing time
- Creates comparison visualizations showing:
  - Objects detected per image
  - Average confidence scores
  - Processing times
  - Overall performance metrics
- Generates side-by-side visualizations of detection results with bounding boxes
- Saves results to object_detection_results.csv

### Part A-2: Additional Image Analysis (Without Deep Learning)
- Extracts traditional image features:
  - Brightness: Average pixel intensity
  - Contrast: Standard deviation of grayscale values
  - Color Analysis: Mean RGB values and dominant color channel
  - Color Variance: Variability across color histograms
  - Texture Score: Laplacian variance measuring image complexity
- Creates bar charts and pie charts visualizing feature distributions
- Saves feature analysis to image_features_analysis.csv

#### Requirements
- Python packages: numpy, pandas, PIL, matplotlib, opencv-python, torch, torchvision, ultralytics
- Pre-trained models will be automatically downloaded on first run

#### Usage
1. Place your images in a folder named Image Files
2. Run all cells sequentially
3. Review generated visualizations and CSV output files

#### Output Files
- object_detection_results.csv: Detection results from both algorithms
- image_features_analysis.csv: Traditional image feature measurements

#### Changes & Limitations
- Needed to strip some information from original image filenames to meet GitHub filelength restriction.
- Limited detection comparison visualizations to 3 images (of 31 total) to shorten processing time.

#### Image Sourcing Information
Image files were collected from the "Picture of the Day" page for the month of December from Wikimedia Commons. The link can be found here: https://commons.wikimedia.org/wiki/Commons:Picture_of_the_day . 
Licensing of these images is not copyrighted and is made available through the Creative Commons CC0 License. More information regarding this license can be found here: https://creativecommons.org/publicdomain/zero/1.0/ .

