# Semaine 04 - Jour 03 Ajustement du Modèle : Diagnostic biais variance
##  Ce que vous allez apprendre
Reconnaître sous-apprentissage et sur-apprentissage.
Apprenez à savoir raisonner dans un contexte de compromis biais-variance.
Comparez des modèles sur les scores d'entraînement et de validation.
Comment peuvent être utilisés pour prévenir et corriger le sur-apprentissage dans les modèles RL2Lassoization methods regulari (L1QLITY RTH IN your TOUR.PLATOn espace:c):).
---
## Important Topics
* High Bias: Underfitting
* High Variance (Overfitting)
* Bias-Variance Tradeoff
* Train-Validation Gap
* Regularization (Ridge & Lasso)
---
##  Summary
### Underfitting (High Bias)
Lorsque nous disons (comme dans le sous-ajustement) qu'un modèle est trop simple et n'est pas vraiment capable de capter le moindre signal dans les données.
SYMPTOMS
* Mauvaises performances d'apprentissage.
* Test poor results.
Potential solutions:
* Better model.
* More informative features.
* Rewrite Too much on the regulation.
---
### Overfitting (High Variance)
Surajustement est le cas où un modèle a été ajusté trop étroitement aux données d'entraînement (y compris le bruit), donc, il n’est pas très bon pour généraliser aux nouvelles données.
SYMPTOMS
* Extremely high train performance.
* Much worse performance on test sets.
Fixes:
Simplify the model?
Get more training samples.
Regularize the estimates.
---
##  Bias-Variance Trade-off
There’s a bias-variance tradeoff to be had:
Bias-Variance Do I need to balance this up two things under: in every model? Bias decreases with model complexity. Getting variance to increase with model complexity, so. We want to find the “Goldilocks” point where your model well generalizes to new unseen data. 
Check Model Fit
Training Score Validation Score What It Means
Low Low Under Underfitting (model is too simple)
High Much Lower Overfitting (too complex a model)
Good Fit High (Small Gap) High (Small Gap)
The delta between training and validation performance is the most informative model "goodness" statistic.
Regularization
Model complexity is regularized by penalizing with the magnitude of the coefficients, which deters fitting the noise.
Hence, all coefficients but none are moved towards zero by Ridge Regression (or L2).
Pulls all coefficients toward zero.
Add all features to the model.
from sklearn.linear_model import Ridge

ridge = Ridge(alpha=1.0, [set your parameters here])
Lasso Regression (L1)
Shrinks coefficients.
It can have irrelevant feature coefficients be exactly zero.
handle the feature selection for you.
from sklearn.linear_model import Lasso

lasso = Lasso(alpha=0.1)
Alpha Parameter

The alpha determines the amount of regularization.
Small alpha → Less regularization and less bias.
More alpha = more regularization, more simple model.

There is also a "best"\alpha choice for a hyperparameter optimization, e.g† via GridSearchCV. So it's easy to over-interpret here
Summarize
You should know the bias-variance tradeoff if you want to create ml models that generalize. Underfitting → the model is too simple. Underfitting → Too Simple Model. Overfitting → Model Too Complicated. Overfitting → Too Complex Model. Since they are working with L1 regularizations, as well as Ridge & Lasso regularization, they also increase the generalizability of the model by penalizing the model’s “spread” (variance) of the model [7]
A good model is one in which both training and validation performance are fairly good, and the gap between the two curves of performance is really very small.