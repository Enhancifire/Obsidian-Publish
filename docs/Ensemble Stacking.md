# Ensemble: Stacking Technique
In Stacking, a *Meta Model* is trained on the outputs of various models. This method is used to find the best way to combine the outputs of various ML models into one accurate result.

### Steps in Stacking
1. Base Model Training
   In this step, many models are trained on the base dataset. These may be based on any algorithm like regression, random forest, etc.
2. Creating Stacking Dataset
   In this step, the predictions of the various models are used to create a *stacking* dataset that contains the predictions of each model per example.
3. Meta Model Training
   In this step, a model is trained on the stacking dataset, generally using the base dataset as label or target. Any algorithm can be used for the final meta model. This meta model results in accurate predictions
4. Prediction
   In this step, the input is given to the base models to generate predictions. The predictions made by the base models are fed into the meta model and it's prediction is treated as the final result