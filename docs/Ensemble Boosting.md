# Ensemble: Boosting Technique

In Boosting, multiple weak models are combined to generate a strong predictive model.
In boosting, we train multiple weak models, and in subsequent steps focus on correcting the mistakes made by the previous models. This is done till there is no noticeable change in accuracy of the final result.

### Steps of Boosting
1. Weak Model Training:
   Select a weak learning algorithm as base model.
2. Training:
   Train the model on training data. In subsequent runs, the model should focus more on the data points that were misclassified. 
3. Instance Weighting
   Boosting assigns weights to the various models to focus on more difficult examples. First we start with equal weights, and as training progresses we assign higher weights to misclassified examples to have subsequent models focus more on them.
4. Model Combination
   After each weak model is trained, the predictions are combined with the predictions of the previous models. The models are all assigned weights according to their performance. Higher weights are assigned to more accurate models.
5. Iterative Process
   Steps 1-4 are repeated for some number of cycles or till no noticeable change in accuracy is seen.
6. Final Prediction
   The final prediction is acquired by combining the individual predictions of the weak models. This is done by using weighted voting where each model is assigned a weight based on its performance and importance.
   
### Two Types of Boosting
Adaptive Boosting (AdaBoost):
- Trains models by assigning weights to examples based on accuracy of weak models
- Has the subsequent models focus more no misclassified examples

Gradient Boosting:
- Trains the models on residuals of the previous models
- Optimises the model by minimising loss function