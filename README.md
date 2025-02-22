# Image Processing and Feature Extraction with ResNet50

## Overview

This project utilizes a combination of deep learning, OCR, and machine  
learning techniques to process images, extract features, and predict  
entity attributes. The pipeline includes image preprocessing, feature  
extraction using ResNet50, text extraction with EasyOCR, and the  
application of Random Forest models for regression and classification tasks.

## Workflow

### Data Preprocessing:

1) Converted the `.xlsx` dataset to `.csv` format.  
2) Downloaded and saved images from the dataset.  
3) Preprocessed the images by resizing and converting them to grayscale.

### Text Extraction:

1) Applied **EasyOCR** to extract text from the images.  
2) Processed and filtered important content from the OCR results.

### Feature Extraction:

1) Leveraged **ResNet50** (a pre-trained CNN model) to extract image features.  
2) Performed feature engineering to reduce the dimensionality of the feature set.

### Modeling:

1) Combined image features and text data into a unified dataset.  
2) Implemented **Random Forest Regression** to predict `entity_value` (e.g., weight, height, depth, power).  
3) Applied **Random Forest Classification** to predict the unit of the entity value (e.g., gram, kilogram).

### Evaluation:

1) Achieved a **Mean Squared Error (MSE)** of **2.4567** for the regression model.  
2) The classification model attained an **accuracy of 64.67%**.

## Model Details

1) **ResNet50**: Pre-trained Convolutional Neural Network used for feature extraction from images.  
2) **EasyOCR**: Optical Character Recognition (OCR) tool for text extraction.  
3) **Random Forest Models**: Applied for both regression and classification:  
   - **Regression** to predict `entity_value`.  
   - **Classification** to predict the unit (e.g., grams, kilograms, watt, volt, kilometre, meter, centimetre).

## Results

1) **MSE** for the Random Forest regression model: **2.4567**  
2) **Accuracy** for the Random Forest classification model: **64.67%**
