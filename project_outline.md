# Lung X-ray Image Classification Project

## Objective
In the aftermath of the COVID-19 pandemic, there has been a notable increase in pneumonia cases globally. This surge is further exacerbated in regions like Indonesia, which has recently experienced heightened pollution levels, leading to an increased risk of pneumonia and other Acute Respiratory Infections. In light of these challenges, our research project emerges with a specific objective.

To harness advanced technological approaches, specifically Convolutional Neural Networks (CNN) and logistic regression models, for the classification of lung X-ray images. The model is envisioned to distinguish between 'normal' and 'pneumonia-infected' categorizations.

This initiative holds profound implications:

1. **Prompt Diagnosis**: In an era where swift medical responses are paramount, our model endeavors to provide immediate insights based on X-ray examinations.
  
2. **Alleviating Medical Workload**: The healthcare sector, already under significant strain, can benefit from automated initial diagnoses, allowing professionals to concentrate on complex cases and expedite treatments.
  
3. **Optimized Healthcare Operations**: Efficient diagnosis can lead to streamlined operations, ensuring that a larger number of patients receive timely medical attention.
  
4. **Economic Efficiency**: Accurate and immediate diagnoses could potentially reduce the need for redundant tests, resulting in cost savings for both medical institutions and patients.

In essence, our research merges technological innovation with healthcare demands, aspiring to offer tangible solutions in regions grappling with heightened medical challenges.

## Dataset
We used a publicly available dataset containing a large collection of chest X-ray images from kaggle https://www.kaggle.com/datasets/paultimothymooney/chest-xray-pneumonia. The dataset is divided into two classes:
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
