# Week 04 - Day 01: - Training/Validation/Test  Splitting
## Overview
In this lab, I learned How to partition a data set into train, validation and test sets using Scikit-learn. I trained k-Nearest Neighbours (KNN) on the training set, selected the best hyperparameter with help of validation set, and test the final model on the test set only once.
## What You’ll Learn
* Know why you need training, validation, and test sets.
* 60/20/20 data split with `train_test_split .`
* Tune a model with the validation set.
* Test the final model on the test set.
* Explain why tuning on the test set produces a foiled performance.
## Tools Used
* Python - Version 2.7.16
* Pandas
* Scikit-learn
* Jupyter Notebook
## Steps Performed
1. Loaded the Iris dataset.
2. Bulk of the data were divided into --
   * 60% for the training set
   * 20% for the validation set
   * 20% for the test set
3. Trained several KNN models by varying `k`.
4. Best k value is selected for the validation accuracy.
5. Training the final model over the tuned hyperparameter.
6. Oncethe model is evaluated on the test set.
## Results
* Created three-way data set split successfully.
* Used the validation set to tune the KNN classifier.
* Final model was then evaluated with the previously unexercised test set. * Noted that using a validation set gives a more accurate estimate of model performance. 
Why Not Tune on the Test Set?
The test set is kept separate until the end, for final evaluation. If used for model tuning, "the model may become indirectly optimized for that particular test data, resulting in leakage of data and overly optimistic performance estimates." This way, the final test accuracy will better simulate the real-world performance.
Conclusion
A three-way split is a necessary component for a sound ML workflow. It is crucial for preventing overfitting during model building and for providing a realistic assessment of model performance on novel data. 