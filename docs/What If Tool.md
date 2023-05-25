### What is the WIT?

Developed by Google, What If Tool is an open source tool to probe and understand ML models. It was used to understand the relationship between the independent variables and the outcomes. Due to it being easy to use and easy to generate visualizations with, it is widely used for explainability.

We can use WIT in three formats:
- Regular Jupyter Notebook
- Google Colab Notebook
- Tensorboard based Visualizations

#### Checking for Bias in Model using WIT

![[attachments/Pasted image 20230525202232.png]]

The What If Tool is very useful for checking whether our ML Model contains any biases regarding a particular feature such as gender, race, age, etc.

1. **Prepare your data and Train your Model:** Prepare your data and ensure that it is properly cleaned and labeled. Train your model on the dataset and save it.
   
2. **Loading into WIT:** Load your model into WIT interface by importing it into your python environment and connecting it to the WIT tool
   
3. **Define Sensitive Features:** Identify features in your data that may lead to biases. It may be related to gender, race, age or any other sensitive attribute.
   
4. **Explore data using WIT:** Using WIT's interface, we can explore and interact with the data instances. We can filter, sort and group the instances based on features.
   
5. **Analyze model behavior:** Use WIT to evaluate the models predictions and observe how they vary across various subgroups defined by the sensitive features. Look for patterns that indicate potential biases in the model's predictions/decisions. An example might be some groups getting consistently higher or lower predictions than others.
   
6. **Mitigate Biases:** If you identify biases, you can use WIT to experiment with various mitigations strategies. You can try manipulating the input parameters to check how the models predictions change or apply fairness techniques like reweighting or bias-correction methods