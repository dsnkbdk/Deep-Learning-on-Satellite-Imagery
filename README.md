# Deep Learning on Satellite Imagery

## Overview
This repository contains the project "Deep Learning on Satellite Imagery," which explores the use of deep learning techniques to enhance satellite imagery analysis for pasture management on slope farms. The project aims to improve the accuracy of dry matter estimates by incorporating slope information derived from LiDAR data.

## Files in the Repository
- `Project.ipynb`: The Jupyter Notebook containing the project's code.

## Project Background
Satellite imagery services provide detailed pasture data to farmers, reducing the need for manual measurements. However, these services have shown limitations on slope farms. This project integrates slope information with satellite imagery to address this issue.

## Objectives
1. Incorporate slope information into satellite imagery to improve pasture dry matter estimates.
2. Develop and compare two machine learning models:
   - Linear Regression
   - Convolutional Neural Network (CNN)
3. Analyze the performance of these models and provide recommendations for future improvements.

## Methodology
### Data Collection
- **Satellite Imagery**: Sourced from 'Planet', containing 13 spectral bands, with four bands (Blue, Green, Red, Nir) used in this project.
- **LiDAR Imagery**: Provided by Land Information New Zealand (LINZ), containing high-accuracy elevation data used to calculate slope.

### Data Preprocessing
1. **Reprojection and Resampling**: Aligning the coordinate reference systems (CRS) and resolutions of the satellite and LiDAR images.
2. **Slope Band Calculation**: Extracting slope information and integrating it with the satellite imagery.
3. **Data Cleaning**: Removing images affected by weather conditions (e.g., clouds, shadows).
4. **Padding**: Ensuring consistent image sizes for neural network input.

### Models
1. **Linear Regression**:
   - Used as a baseline model.
   - Analyzes the linear relationship between spectral bands, slope, and dry matter.
2. **Convolutional Neural Network (CNN)**:
   - Implements a 3-layer CNN using PyTorch.
   - Trains on both slope and flat farm data to improve model accuracy.

## Analysis and Results
- The linear regression model showed that slope significantly affects dry matter estimates, though the model's outcomes were unstable due to lack of orientation data.
- The CNN model improved linear feature capture after incorporating flat farm data, reducing overfitting and enhancing prediction accuracy.

## Recommendations for Future Work
1. **Data Improvements**:
   - Standardize resolution and CRS across datasets.
   - Collect more ground truth data from slope farms.
2. **Model Enhancements**:
   - Tune existing model parameters and explore additional deep learning models (e.g., DenseNet, AlexNet).
3. **Methodological Adjustments**:
   - Incorporate slope orientation information.
   - Develop algorithms to mitigate weather-related image quality issues.

## Conclusion
The project successfully demonstrated the integration of slope information with satellite imagery to enhance pasture management on slope farms. Further research and data collection are required to refine the models and extend their applicability.
