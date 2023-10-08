# Model Comparison: Logistic Regression vs. CNN

In this analysis, we compare the performance of two different models, a **Logistic Regression** model and a **Convolutional Neural Network (CNN)** model, for a classification task. The task involves classifying instances into two classes: "NORMAL" and "PNEUMONIA."

## Logistic Regression Model

### Cross-Validation Scores
- Mean Cross-Validation Score: 0.9158

### Test Set Performance
- Test Set Accuracy: 87.2%

### Classification Report

| Class          | Precision | Recall | F1-Score |
| ---------------|-----------|--------|----------|
| **NORMAL**     | 0.91      | 0.77   | 0.83     |
| **PNEUMONIA**  | 0.85      | 0.95   | 0.90     |

- Macro Average F1-Score: 0.86
- Weighted Average F1-Score: 0.87

The logistic regression model demonstrated good overall performance with a weighted average F1-score of 0.87. It showed slightly lower recall for the **NORMAL** class compared to the **PNEUMONIA** class.

## CNN Model

### Average Validation Accuracy (5 Folds)
- Average Validation Accuracy: 0.8779

### Classification Report

| Class          | Precision | Recall | F1-Score |
| ---------------|-----------|--------|----------|
| **NORMAL**     | 0.84      | 0.95   | 0.89     |
| **PNEUMONIA**  | 0.91      | 0.73   | 0.81     |

- Macro Average F1-Score: 0.85
- Weighted Average F1-Score: 0.86

The CNN model achieved an average validation accuracy of 0.8779 and demonstrated competitive performance. Notably, it exhibited higher recall for the **NORMAL** class compared to the logistic regression model.

## Conclusion

Both models performed well, but there are key differences to consider:

- **Logistic Regression**:
  - Achieved a slightly higher weighted average F1-score (0.87).
  - Demonstrated higher recall for the **PNEUMONIA** class.
  - Test set accuracy of 87.2%.

- **CNN**:
  - Achieved a competitive weighted average F1-score (0.86).
  - Demonstrated higher recall for the **NORMAL** class.
  - Average validation accuracy of 0.8779.

The choice between these models may depend on the specific requirements of the application. The logistic regression model might be preferred when interpretability is essential, while the CNN model excelled in capturing complex patterns in the image data. Further considerations, such as computational resources and data size, should also influence the choice of model.

Ultimately, both models demonstrate strong potential for the classification task, and additional tuning or ensemble methods could potentially improve their performance further.
