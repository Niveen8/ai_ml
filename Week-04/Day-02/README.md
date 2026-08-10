# Jour 2 — Validation croisée
## Aperçu
Cette journée est consacrée à la **validation croisée**, la méthode pour évaluer plus justemennt les modèles de machine learning.
Vindel et al. (2019) cross valider sous une autre forme: Au lieu de se fier à un seul séparateur train-validation, Cross-Validation segmentera les données d'entraînement en plusieurs folds, entraîn une instance du modèle pour chaque fold.
## Objectifs d'apprentissage
Rendre compte pourquoi **estime de performance K-Fold Cross-Validation** fiable.
De `Scikit-learn` utilisez `cross_val_score`.
Calculer et interpréter la **moyenne** et la **variance** de scores de cross-validation.
Approuver importance de **Stratified K-Fold** pour Classification Problèmes de.
Appréhender la façon dont Validation Croisée évalue [sic]  Modèle Plus Stable d'évaluation du modèle.
## Sujets clés
### 1. Huit plis K-Fold Cross-Validation
Le cross-validation K-Fold consiste à diviser l’ensemble de données d’apprentissage en `k` folds égaux.
Pour `k=5`, par exemple:
* The model is trained 5 times.
* Validation data is indeed used once as validation data.
* The other 4 folds are training data.
* Every sample is used for validation exactly once.
### 2. cross_val_score
Scikit-learn offers `cross_val_score` that enables us to execute Cross-Validation very easily.
```python
from sklearn.model_selection import cross_val_score
scores = cross_val_score(
model,
X_train,
y_train,
cv=5,
scoring="accuracy"
)
print(scores)
print(scores.mean())
print(scores.std())
```
### 3. Moyenne et écart type
Ensemble de la **moyenne** du modèle de fonctionnement dans tous les plis. L’**écart-type** indique dans quelle mesure les scores diffèrent entre les plis.
Un niveau moyen élevé avec un écart type faible a habituellement expliqué la performance du modèle est bon et stable. 
4. Stratified K-Fold
For this first competition, we are going to use the Stratified K-Fold , which is essentially the K-Fold but with stratification.
This is very useful when you have an unbalanced class distribution in your samples.
Be aware that if you pass a integer value (e.g. cv=5) to cross_val_score it will stratify the folds enough out-of-the-box for classifiers.
Source dataset
The demonstrated example is executed on the Iris dataset of Scikit-learn.
Following are the contents of the data set：
150 samples 4 features 3 classes Model
Cross Validation is an example of Logistic Regression classifier.
Expected Results
The notebook to compute the:
Cross validation scores for each fold Average cross-validation score Standard deviation
Test accuracy on final
Conclusion
Cross-Validation provides more reliable estimate of model performance than using just a single validation split for testing.
If a model was stable or not would be interesting in knowing." It's certainly useful to run multiple folds to get a "sense" if a model's performance is noisy. It is particularly recommended for classification problems, should always be used together with StratifiedKFold to ensure that folds are made by preserving the percentage of samples for each class of target variable as is the case with the whole set. 