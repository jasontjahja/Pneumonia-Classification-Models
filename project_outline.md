# Lung X-ray Image Classification Project

## Objective
The primary objective of this data mining project is to develop a robust and accurate model for classifying lung X-ray images into two categories: normal and pneumonia-infected. Leveraging Convolutional Neural Networks (CNN) and logistic regression models, this project aims to assist medical professionals in the timely diagnosis of pneumonia based on X-ray images, potentially reducing the workload and improving the efficiency of healthcare providers.

## Dataset
We used a publicly available dataset containing a large collection of chest X-ray images. The dataset is divided into two classes:
- Normal: Lung X-ray images of individuals with no signs of pneumonia.
- Pneumonia: Lung X-ray images of individuals diagnosed with pneumonia.

## Data Preprocessing
- Data Loading: We loaded and preprocessed the X-ray images, including resizing, normalization, and data augmentation.
- Data Splitting: The dataset was split into training and testing sets (80:20 ratio) to train and evaluate the models.

## Model Architecture
### Convolutional Neural Network (CNN)
- Architecture: We designed a CNN with layers for image feature extraction and classification.
  1. Convolutional Layer with 32 filters, each of size (3, 3), and ReLU activation.
  2. Max Pooling Layer with a pool size of (2, 2).
  3. Convolutional Layer with 32 filters, each of size (3, 3), and ReLU activation.
  4. Max Pooling Layer with a pool size of (2, 2).
  5. Dropout Layer with a dropout rate of 25%.
  6. Flatten Layer to convert the 2D feature maps to a 1D vector.
  7. Fully Connected (Dense) Layer with 128 units and ReLU activation.
  8. Dropout Layer with a dropout rate of 50%.
  9. Output Layer with 2 units (for binary classification) and softmax activation.

### Logistic Regression
- Architecture: A logistic regression model was used as a baseline for comparison.
- Input Features: The preprocessed images were flattened and normalized, then used as input features.
- Evaluation: The logistic regression model's performance was evaluated using cross-validation and test set accuracy.

## Model Training and Evaluation
- CNN Training: The CNN model was trained using the training dataset with optimization techniques, including the SGD optimizer and categorical cross-entropy loss.
- Logistic Regression Training: The logistic regression model was trained using cross-validation and the test set accuracy was reported.
