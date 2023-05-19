### Ensemble Models
Ensemble Models: Complex Models that are made up of multiple smaller, less accurate models.
Three types of Ensemble Models:
	1. [[Ensemble Bagging|Bagging]]
	2. [[Ensemble Boosting|Boosting]]
	3. [[Ensemble Stacking|Stacking]]

### Using SHAP for Ensemble Models

Explainability for Ensemble models is very important because we need to be able to understand about how the models are being combined.

We can use SHAP for understanding the output of an ensemble model.

#### Steps for Applying SHAP to Ensemble Models
1. Understanding the Ensemble Model
   Begin by understanding the model. Explore which models are being used as the base, as well as the type of ensemble method used
2. Individual Model Predictions
   To use SHAP, we need to obtain the individual results from each of the base models. This involves running the data through the individual models and recording the predictions
3. Apply SHAP to the Individual Prediction
   Apply SHAP to the predictions of the individual models. Use the appropriate SHAP algorithm for the model.
4. Combine SHAP Values
   Combine the SHAP values for the individual models based on the ensemble technique used. 
   - For Bagging, take the average of the SHAP values
   - For Boosting, take the weighted average depending on the weights assigned to the individual models in the boosting model
   - For Stacking, you can use the meta-models coefficients to generate the final SHAP value
5. Interpret the SHAP Values
   Interpret the final SHAP values to understand the feature importance and various other stuff that you do using SHAP
   
### Using SHAP for Categorical Boosting Models