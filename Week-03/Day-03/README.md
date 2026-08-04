# Day 3 — Logistic Regression & Classification Metrics
## Learning Objectives
- Train Logistic Regression model and predict class probabilities.
- Warp your head around why accuracy can be deceiving on imbalanced datasets.- Assess classification models via:
  - Confusion matrix
  - Precision
  - Recall
  - F1-score
  - AUC-ROC 
  ------------------------------------
### Logistic Regression
The logistics regression is a classification algorithm which is used to predict a class instead of value in linear regression. A weighted sum of inputs is applied to the sigmoid function to produce an output which can be interpreted as a probability of being in 1 class.
### Accuracy Issues
If you are working with unbalanced data, then accuracy may be misleading. For imbalanced problems, accuracy is not a good metric because high accuracy can be obtained by just classifying everything as the majority class, without recognizing the minority class.### Confusion Matrix
The confusion matrix evaluates the following class-based classification accuracies:
1-True Positive (TP) : the number of true positive samples.
2-True Negative (TN) - the number of true negative samples
3-False Positive (FP) the number of false positive samples
4-False Negative (FN) Number of false negative samples 
#Humanized task
Rewrite the following text from the perspective of a human, please confirm output in English
### Classification Metrics
-**Precision:** Of all cases that were predicted as positive, how many actually positive.
- **Recall:** What is the fraction of true positives that have been retrieved.
- **F1-score:** The F1-score is the recall and precision harmonic mean.
### AUC-ROC
AUC-ROC measures the ability of a classification model to perform well across all classification thresholds.
A good value near 1.0, with 0.5 indicating no better than random deciding. 
## Lab: Build Classifier from Scratch Hands-On 1.1
Actions Taken:
1. You have trained a Logistic Regression model on the classification dataset.
2. Predictions were made and confusion matrix computed.
3. Precision, Recall and F-Measure are calculated with classification_report.
4. Do we want to bias towardsus Precision or Recall for this problem?
5. AUC-ROC for model evaluation.--#Tools Used
- Scikit-learn (LogisticRegresssion)
- Pandas
- Matplotlib 