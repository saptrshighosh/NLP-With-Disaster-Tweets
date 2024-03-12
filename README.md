# NLP With Disaster Tweets

## By Saptrshi Ghosh

### Problem Statement

The task was to develop a machine learning model capable of predicting whether a given tweet is about a real disaster or not. The model should classify tweets into two categories: '1' for tweets about real disasters, and '0' for those that are not.

### Input Dataset and Its Attributes

The input dataset consists of two sets: a training set and a test set, each containing the following attributes:

- `id`: A unique identifier for each tweet.
- `keyword`: A specific keyword from the tweet (may be blank).
- `location`: The location from where the tweet was sent (may be blank).
- `text`: The actual text of the tweet.
- `target`: Present only in the training set, indicating whether a tweet is about a real disaster (1) or not (0).

### Problem-Solving Methodology

The approach involved several steps:

1. **Data Preprocessing**: Cleaning and preprocessing text data, including tokenization, normalization, and stop words removal.
2. **Feature Extraction**: Using the TF-IDF (Term Frequency-Inverse Document Frequency) technique to convert text data into numerical features.
3. **Model Selection and Training**: A Naive Bayes classifier was chosen for its effectiveness in text classification tasks. The model was trained using the training dataset.
4. **Model Evaluation**: The model was evaluated on a validation set derived from the training data.

### Results Achieved

The model achieved an accuracy of approximately 79.12% on the validation set, with detailed metrics like precision, recall, and F1-score for both classes provided in the classification report.

### Performance Metrics Employed for Evaluation

Several metrics were used to evaluate the model:

- **Accuracy**: A general measure of the model's performance.
- **Precision, Recall, and F1-Score**: Metrics that provide insights into the model's ability to correctly identify disaster-related tweets and its overall reliability.
- **Confusion Matrix**: Offers a detailed view of the model's performance in terms of true positives, false positives, true negatives, and false negatives.
- **Precision-Recall Curve**: Illustrates the trade-off between precision and recall for different threshold settings.
- **ROC Curve and AUC**: Showcases the model's ability to distinguish between the two classes.

### Merits and Limitations of the Chosen Solution

**Merits**:
- Effectiveness: The Naive Bayes classifier performed well in classifying text data.
- Simplicity and Efficiency: The method is simple to implement and computationally efficient.

**Limitations**:
- Model Bias: Potential bias due to the nature of the training data or the limitations of the Naive Bayes classifier.
- Lack of Contextual Understanding: Possible misclassifications due to not fully grasping the context or subtleties of natural language.
- Dependence on Preprocessing: The performance heavily relies on the quality of data preprocessing.
