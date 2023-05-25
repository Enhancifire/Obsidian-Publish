### What are Counterfactual Explanations?

Counterfactual Explanations (CFEs) are causal relationships in the prediction process of ML Models. It is a process of creating hypothetical scenarios and generating predictions under those scenarios.

Let's take an example. Suppose a model was supposed to predict whether a person will get a cookie or not. It would take a look at various factors like how many chores that person did, how much did they play, etc.

Now, let's assume the model did not give someone a cookie. You might wonder what would have happened if that person might have done more chores and played less. CFEs are a way to understand this. We would create a pretend scenario where the person did more work or played less, and then we would see whether the model would give them a cookie or not. In this way, we can create scenarios to figure out which features are important to get the desired predictions and what changes would make a difference.

By generating counterfactual explanations, XAI techniques attempt to provide a better understanding of the decision-making process of machine learning models.

Counterfactual Explanations can be generated for both Regression and Classification tasks.

### CFE using Alibi Library

CFEs can be generated using Alibi library in Python. Alibi library requires a trained model and a new dataset for which predictions need to be generated.

*Read From Page 298 of **CMB Practical Explainable AI using Python** for Example*
