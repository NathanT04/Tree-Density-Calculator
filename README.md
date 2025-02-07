Depth Estimation and Object Detection Pipeline

Overview

This project processes images to estimate depth and detect objects, specifically highlighting apples on the depth map. It utilizes the transformers library for AI-based depth estimation and object detection, integrating models from Hugging Face.

Features

Depth Estimation: Uses Depth-Anything-V2-base-hf to generate depth maps.

Object Detection: Implements facebook/detr-resnet-50 for detecting objects.

Apple Highlighting: Draws red borders around detected apples on the depth map.

Batch Processing: Processes multiple images within a directory.

Output Saving: Saves processed images with applied annotations.

Requirements

Ensure you have the following dependencies installed:

pip install transformers accelerate pillow matplotlib numpy

Usage

1. Single Image Processing

Modify the input_path and output_path in the script and run:

python depth_object_detection.py

2. Batch Processing

Place images in the input_folder, update the script accordingly, and execute:

python batch_depth_object_detection.py

File Structure

|-- depth_object_detection.py     # Processes a single image
|-- batch_depth_object_detection.py # Processes multiple images
|-- /kaggle/input/point-cloud-test1/  # Input image directory
|-- /kaggle/working/  # Output directory for processed images

Notes

The script ensures only images (.jpg, .jpeg, .png) are processed.

Red borders are drawn only for objects labeled as "apple" with confidence > 0.5.

If depth_map is not an image, it is visualized using Matplotlib and saved accordingly.

Output Example

The processed images will be saved with red-highlighted apple detections in the specified output directory.

