### What are [[Ensemble Models]]?
Ensemble Models are Complex Models built using a combination of multiple small/weak models. They boast superior accuracy as compared to their base models.

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
   
### Using SHAP for [[Categorical Boosting Models]]
1. Train the [[Categorical Boosting Models]]
   Train the model on the training data.
2. Convert Categorical Features
   Since SHAP works on Numerical Features, we need to convert the categorical data into numerical form. We can use many techniques like One-Hot Encoding
3. Calculate SHAP Values
   Once we have converted the categorical data into numerical form, we can calculate the SHAP values for them. There exist specific implementations of SHAP for the various models, such as LightGBM SHAP for LightGBM, etc
4. Interpret SHAP Values
   We can now interpret the SHAP values to understand feature importance, etc