Week 03 - Day 05: End-to-End Supervised Learning Workflow #Abstrat Summary This notebook includes a concise run through the life cycle of a work of supervised learning. This notebook contains a terse walk-through to-to the entire 'work' cycle for a work of supervised learning. Now that we have piplines, we can:
1. SPC (statistical process control)
2. Data −<Processing>
3. Train/Test Split
4. Model Training
5. Model Evaluation
## ENCAPSULATING LEARNING OBJECTIVES
- And all the learning-pipeline was to be run in this very way.
- Processing methods.
- You Can also leverage Scikit-learn if you are interested in building your own supervised learning model(s).
- Apply the appropriate model evaluation metric (s).
- Benchmark the results.
## Supervised Learning Pipeline
### 1. Exploratory Data Analysis (EDA)
Explore the data:
- look at distributions, for example.
- Find correlations.
Wiki Remove missing values, problem.
### 2. Preprocessing
This Is How You Do The Data Processing:
- Filling in missing values.
- Encoding categorical features.
- Scaling numerical features.
Example:
```python
from sklearn.preprocessing import StandardScaler

scaler = StandardScaler()

X_train_scaled = scaler.fit_transform(X_train)
X_test_scaled = scaler.transform(X_test) ِ