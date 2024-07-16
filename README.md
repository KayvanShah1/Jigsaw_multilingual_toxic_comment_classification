# Rate Severity & Toxicity Classification of Social Media Comments

![Header image](/Images/header.png)

The objective was to rate the severity of toxic social media comments and classify them as toxic or not across more than seven languages. My approach involved leveraging advanced multilingual modeling techniques, utilizing Kaggle's TPU support, and incorporating innovative strategies to address the challenges of cross-lingual toxicity detection.

### Data Preparation and Preprocessing

1. **Data Collection**: 
   - I utilized the English training data provided from the previous competitions, which included comments labeled with varying degrees of toxicity.
   - The test data comprised Wikipedia talk page comments in multiple languages.

2. **Text Cleaning and Tokenization**:
   - Implemented text preprocessing steps to handle special characters, punctuation, and emojis.
   - Used language-specific tokenizers to ensure that the nuances of each language were preserved during tokenization.

### Model Development

1. **Multilingual Transformer Models**:
   - Leveraged state-of-the-art multilingual models like BERT, XLM-RoBERTa, T5, etc which are designed to handle multiple languages.
   - Fine-tuned these models on the English training data, employing transfer learning to adapt the models to recognize toxicity in other languages.

2. **Few-Shot and Zero-Shot Learning**:
   - Explored few-shot and zero-shot learning techniques to improve model performance on languages not seen during training.
   - Implemented strategies like meta-learning to enhance the model's ability to generalize across different languages.

3. **Model Architecture**:
   - Developed multi-headed models to handle the main task of toxicity detection and sub-tasks such as classifying different types of toxicity (e.g., obscene, threat, insult).
   - Employed ensemble learning by combining predictions from multiple models to achieve robust performance.

### Training and Optimization

1. **TPU Utilization**:
   - Took advantage of Kaggle's TPU support for faster training and fine-tuning of large transformer models.
   - Optimized training pipelines to handle large-scale data efficiently, reducing training time and improving model scalability.

2. **Hyperparameter Tuning**:
   - Conducted extensive hyperparameter tuning using grid search and Bayesian optimization to identify the best configurations for model performance.
   - Focused on parameters such as learning rate, batch size, and number of training epochs.

### Evaluation and Bias Mitigation

1. **Performance Metrics**:
   - Evaluated model performance using metrics like F1-score, precision, recall, and ROC-AUC to ensure a balanced assessment of toxicity detection.
   - Conducted cross-validation to validate model performance across different data splits.

2. **Bias Detection and Mitigation**:
   - Implemented techniques to detect and mitigate unintended bias in toxicity classification.
   - Used fairness-aware learning approaches to ensure that the model operated fairly across diverse conversation contexts.

### Model Deployment and Inference

1. **Real-Time Inference**:
   - Deployed the models using Jigsaw's Perspective API to serve toxicity predictions in real-time.
   - Implemented efficient inference pipelines to handle large volumes of comments, ensuring quick and accurate toxicity detection.

2. **Multilingual Support**:
   - Ensured that the deployed models supported toxicity detection across all target languages.
   - Continuously monitored and evaluated model performance in different languages to make iterative improvements.

# Results:

| #   | Model Name          | Accuracy (%) |
|-----|---------------------|--------------|
| 1   | Roberta             | 90.49        |
| 2   | Electra             | 89.90        |
| 3   | AlBERTa             | 88.80        |
| 4   | BERT                | 88.46        |
| 5   | Distil-BERT         | 87.41        |
| 6   | XLM-RoBERTa         | 85.83        |
| 7   | Embeddings+Conv     | 85.00        |
| 8   | Simple Embeddings   | 65.68        |

### Conclusion

By combining advanced multilingual modeling techniques, leveraging few-shot and zero-shot learning, and utilizing TPU support for efficient training, my approach aimed to develop a robust and fair toxicity classification system. This approach not only achieved high performance in detecting toxic comments but also contributed to the broader goal of fostering healthier and more collaborative online conversations across multiple languages.


# Notebooks
1. [`Roberta-Large`](https://www.kaggle.com/code/kayvanshah/roberta-large-2)

# Contributors:
1. **Kayvan Shah**
2. **Abneet Wats**
3. **Rahil Merchant**

## Link to the dataset: 
1. [Jigsaw Multilingual Toxic Comment Classification](https://www.kaggle.com/c/jigsaw-multilingual-toxic-comment-classification/data) 
2. [Jigsaw Multilingual Toxic Test Translated](https://www.kaggle.com/kashnitsky/jigsaw-multilingual-toxic-test-translated)

*Description from [competition page](https://www.kaggle.com/c/jigsaw-multilingual-toxic-comment-classification/overview/description)*
