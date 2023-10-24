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

## Suggestion for Further Research
- **Incorporate Additional Data**: 
  - Leveraging other types of medical data can provide a more comprehensive understanding of the cases. Including data such as patient symptoms, medical history, and other relevant scans can enhance the model's diagnostic ability.
  
- **Balanced Dataset**:
  - It's imperative to ensure a balanced dataset, where the number of images representing healthy and pneumonia-infected lungs are equal. This will prevent the model from being biased towards the class with a higher number of samples.
  
- **Anomaly Detection**:
  - Medical images can sometimes present rare or unseen anomalies. Incorporating anomaly detection techniques will aid in identifying such unique cases and ensure that they are not misclassified.
  
- **Incorporate Expert Feedback**:
  - Collaboration with medical experts, especially radiologists, can prove invaluable. Their insights and validation of the model's predictions can steer the model's evolution in a direction that is both technically sound and clinically relevant.
 
## Reflection
Upon reflection, embarking on a data mining project in lung X-ray image classification was initially a daunting endeavor for both Jason and myself. As International Business students with a focus on Finance, the intricate nuances of such a technical undertaking were beyond the realms of our conventional academic experience.

At the onset, we grappled with the vast terminologies, methodologies, and techniques inherent to the project. The initial struggles stemmed from our attempts to navigate the labyrinth of Convolutional Neural Networks (CNN) and logistic regression models without a solid foundation in the subject.

However, with the timely intervention of our lecturer and the invaluable support from ChatGPT, our trajectory changed dramatically. ChatGPT acted as a reservoir of knowledge, seamlessly bridging our finance-oriented backgrounds with the technological intricacies of the project. From explaining complex concepts in layman's terms to generating essential code segments, ChatGPT became an integral companion in our journey.

Our newfound confidence was underscored when two other teams approached us, seeking guidance on logistic regression and ChatGPT's code generation capabilities. The transformation was evident: from being novices in the domain, we had evolved to a position where we could impart our learnings to our peers. It was particularly gratifying to witness their progress and know that our assistance had played a part in their achievements.

In conclusion, this project has been a testament to the philosophy that boundaries in learning are often self-imposed. With determination, the right guidance, and the willingness to seek assistance when needed, even the most challenging endeavors become surmountable. This experience has not only enriched our academic repertoire but has also instilled a deeper appreciation for interdisciplinary collaboration. As finance students, we have come to realize that in today's interconnected world, an openness to learn and adapt is the linchpin of success.
