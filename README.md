# Sentiment-Analysis-on-product-review-data-using-Google-BERT-

Author: Giuseppe Cappella

This project demonstrates a comprehensive process for implementing a sentiment analysis model utilizing Google's BERT architecture and TensorFlow, focusing on analyzing customer reviews. The project is structured into several key parts, encompassing data preparation, preprocessing, modeling, training, evaluation, and finally, labeling customer reviews with their sentiment predictions.

Dataset Description

The project begins with mounting a dataset stored in a Google Drive folder, followed by importing necessary libraries such as pandas, TensorFlow, and Hugging Face's transformers. The dataset, initially in a CSV format, contains customer reviews alongside their sentiment labels, which are crucial for training the sentiment analysis model.

Project Structure and Methodology

Part I: Data Preparation and Preprocessing

    Loading the Dataset: The script reads a CSV file containing customer reviews and their associated sentiment labels (negative, neutral, positive) into a pandas DataFrame.
    Label Encoding: Sentiment labels are encoded into numerical values (0, 1, 2) to facilitate processing.
    Dataset Preparation: Utilizing Hugging Face's dataset library, the DataFrame is converted into a dataset and subsequently split into training, validation, and testing sets.
    Tokenization and Encoding: An AutoTokenizer from the "bert-base-uncased" model is employed to tokenize the text reviews. A custom function applies this tokenization and encoding to the dataset, preparing it for the model.

Part II: Modeling and Training

    Model Initialization: A TensorFlow model for sequence classification is initialized with the BERT architecture, configured to classify three sentiment labels.
    Training Preparation: The script prepares the datasets for TensorFlow, employing data collation for batch processing and defining a custom metric for accuracy.
    Model Training: The BERT model is trained using the training set, with performance monitored via TensorBoard. This phase leverages a GPU for acceleration, if available.

Part III: Evaluation and Insight Generation

    Evaluation: The trained model is evaluated against the test dataset, with metrics such as accuracy, confusion matrix, and classification reports providing insights into its performance.
    Labeling Customer Reviews: The model is then used to predict sentiments on a new set of customer reviews, adding a column to the dataset with these predictions.
    Exporting Results: Predicted sentiments are exported to a CSV file, demonstrating the model's application in analyzing and understanding customer sentiments based on their reviews.

This project exemplifies the end-to-end implementation of a sentiment analysis model using advanced NLP techniques and deep learning, showcasing the potential of BERT for understanding customer feedback and sentiments from textual data.
