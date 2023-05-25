### What is Contrastive Explanations for ML?

Contrastive Explanations are explanations that compare and highlight the differences between two or more scenarios. They aim to explain why a certain prediction was made by emphasizing the contrasting factors or features between different scenarios.

They provide insights into how changing specific attributes or conditions leads to different outcomes, similar to [[What If Tool]].

Let's take an example. We have a robot that sorts apples and oranges by using a camera depending on their color and shape. Sometimes, it misclassifies apples as oranges and vice versa.

To explain the robots decision and highlight the differences, a CE would show two images side by side, one being a correctly identified apple and other being mistakenly identified as orange. The explanation would point out the specific color and shape differences between the two images that caused the robot to make the wrong prediction. By demonstrating the contrasting factors that influenced the decision, it helps us identify potential areas of improvement or sources of error.

Various approaches may be used to generate CE, such as feature importance analysis, similarity metrics, highlighting feature variations between data instances, etc.

There are two concepts associated with contrastive explanations:
1. **Pertinent Positives (PP):** Pertinent positives refer to the features or factors that are present in instances that receive a positive prediction or outcome but are absent or different in instances that receive a negative prediction or outcome. These features highlight the factors that contribute to a positive outcome or prediction.
2. **Pertinent Negatives (PN):** Pertinent negatives, on the other hand, refer to the features or factors that are absent or different in instances that receive a positive prediction or outcome compared to instances that receive a negative prediction or outcome. These features highlight the factors that contribute to a negative outcome or prediction.

### CEM using Alibi

Contrastive Explanations for Models (CEMs) can be implemented using Alibi, a Python Library.

### Use Cases of Contrastive Explanations
#### Comparison of Original vs Autoencoder Generated Image

Autoencoder is a ML model that can compress and decompress images. When comparing to an original image, the autoencoder attempts to decompress/reconstruct the original image from a compressed representation. 
By comparing the differences between the two images, we can assess the quality of the decompression and how well the autoencoder captures the essential features of the original image.

#### CEM for Tabular Data Explanations
CEMs can be applied to tabular data to generate [[Counterfactual Explanations]] for individual instances. By altering the input values of a specific data instance, CEM can find alternate values that would lead to a different prediction. This helps provide explanations for individual predictions in tabular data sections.