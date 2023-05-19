### What are Categorical Boosting Models?

Categorical Boosting Models, also called Gradient Boosting Machines (GBM) are a type of [[Ensemble Models|Ensemble Learning Method]] specifically designed to handle *categorical* or *discrete* features in input data. 

### Algorithms of Categorical Boosting Model

1. One Hot Encoding
   The first step is converting the categorical data into numerical format. This is done by converting n unique categories in the features into binary form, by turning them into whether the category is present or not.
   Ex. In a feature of disease symptoms, we can convert the various symptoms into binary format by converting them into columns and assigning them values of 0 if not present and 1 when present
2. Gradient Boosting for Categorical Variables
   Categorical boosting models employ diff. strategies to handle categorical splits in the data
3. Categorical Splitting Strategies
   1. Ordinal Encoding
      Assigning a numerical value to each category based on order. This allows the algo to treat categorical variables as continuous data.
   2. One Versus All Encoding
      Create binary features by encoding each category as a separate binary feature
   3. Frequency Encoding
      Replace each category with its frequency in the training dataset.
4. Tree Construction
   The algorithm then generates a series of decision trees based on the features. Each tree is made using Gradient Boosting technique. It takes into account both the numerical and categorical data.
5. Model Ensemble
   The final prediction is obtained by combining the predictions of the generated trees, generally done through weighted voting.