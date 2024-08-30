# Organ Segmentation using Hounsfield Scale

This repository contains a project focused on organ segmentation in medical images using the Hounsfield scale.

## Project Overview

The project is organized into a folder structure containing input images and various processed images. The main code is implemented in the notebook `main.ipynb`. The program reads input from two `.in` files and converts them to grayscale images using Min-Max Scaling. It then identifies cells corresponding to specific organs, with a focus on detecting lungs in DICOM CT images. 

## Functionality

1. **Input Data Processing**: The program preprocesses the input images, converting them to grayscale and scaling them using Min-Max Scaling.
   
2. **Lung Segmentation**: It identifies cells that may belong to a lung near the lung segmentation provided by medical professionals.

3. **Overlay with Ground Truth**: The identified lung cells are overlaid with the segmentation provided by medical experts.

4. **Custom K Nearest Neighbor Algorithm**: A custom K Nearest Neighbor algorithm is applied for clusterization. It uses the nearest pixels in slides of various dimensions to determine if a pixel belongs to the lung based on the majority vote of its neighbors.

5. **Segmentation Visualization**: The segmentation results produced by the algorithm are saved in the "compare3.png" file within each input folder.

## Folder Structure

The folder structure is organized as follows:

- `input/`: Contains input images.
- `processed/`: Contains processed images.
- `output/`: Contains segmentation results and other output images.
- `notebooks/`: Contains the notebook `main.ipynb` which contains the main code.

## Usage

1. Clone the repository to your local machine.
   
2. Open and run the `main.ipynb` notebook using Jupyter or any compatible environment.

3. The notebook will process the input images, perform organ segmentation, and generate segmentation results.

## Requirements

The project requires the following dependencies:

- Python 3.x
- Jupyter Notebook
- `numpy`
- `matplotlib`
- `scikit-image`

Install the dependencies using `pip` or any package manager before running the notebook.
