# Analog clock reader
A Computer Vision project built with Python and OpenCV that automatically detects and reads the time from images of analog clocks using line and circle detection algorithms.

## Features

* **Image preprocessing:** Uses blurring and thresholding to clean up the input images.
* **Circle detection:** Finds the clock face boundary to isolate the region of interest.
* **Line detection:** Employs edge detection and skeletonization (`skimage.morphology`) to find the exact positions of the clock hands.
* **Mathematical conversion:** Calculates the spatial angles of the detected lines (`skspatial.objects`) and maps them to standard clock hours and minutes.
* **Error analysis:** Includes accuracy testing against a dictionary of true values to calculate the mean absolute error across a dataset of test clocks.

## Tech stack

This project is written in Python and relies on the following libraries:
* `OpenCV` (`cv2`) - for core image processing and computer vision tasks;
* `NumPy` - for array and matrix operations;
* `Matplotlib` - for visualizing the step-by-step image transformations;
* `scikit-image` (`skimage`) - specifically for the `skeletonize` morphological operation;
* `scikit-spatial` (`skspatial`) - for geometric and spatial calculations (lines and angles).

## Prerequisites & installation

To run the Jupyter Notebooks locally, ensure you have Python installed along with Jupyter and the required libraries. 

You can install all dependencies via pip:
```bash
pip install opencv-python numpy matplotlib scikit-image scikit-spatial jupyter
