# Sentiment Analysis of Customer Reviews Using BERT and TensorFlow

Author: Giuseppe Cappella

This project demonstrates a comprehensive approach to sentiment analysis on customer reviews, leveraging the powerful BERT model within a TensorFlow framework. From mounting the dataset to training and evaluating the model, the project encapsulates an end-to-end process, culminating in the application of the trained model to classify unseen customer reviews into sentiment categories.

### Dataset Description

The project utilizes an extensive dataset containing 462,744 labeled customer reviews, each associated with a sentiment label (negative, neutral, positive). Due to the considerable size of the dataset's CSV file, it is not included directly within the repository. 
The dataset features 3 key columns:

- labelled_reviews_index: A unique identifier for each review in the dataset.
- review_text: The text content of the customer review.
- sentiment_label`: The sentiment of the review categorized as negative, neutral, or positive.

### Project Overview

The project is structured into distinct phases, starting with data preparation, followed by model training and evaluation, and concluding with the application of the model to predict sentiments of new reviews.

#### Data Preparation and Feature Engineering

The initial phase involves loading the dataset into a pandas DataFrame, followed by label encoding to convert sentiment labels into numerical form. This encoded dataset is then transformed into a Hugging Face Dataset object, allowing for easy manipulation and split into training, testing, and validation sets. A tokenizer is initialized to prepare the review texts for BERT, ensuring inputs are in the correct format for model training.

#### Model Training and Evaluation

The core of the project lies in training the BERT model for sequence classification. The TensorFlow implementation of BERT is utilized, with the model being trained to classify reviews into the three sentiment categories. This process involves setting up a training pipeline, including tokenization, data collation, and the creation of TensorFlow datasets for training, validation, and testing. The model's performance is evaluated using various metrics, with results visualized through confusion matrices and classification reports.

#### Application to New Data

With the model trained, the project demonstrates its application to new customer reviews. The process involves tokenizing unseen reviews, predicting their sentiments with the trained model, and appending these predictions to the dataset. This showcases the model's practical utility in analyzing customer sentiments, providing valuable insights for business strategies.

### Conclusion and Insights

In summary, this project exemplifies a sophisticated approach to sentiment analysis, from data handling and model training to practical application, illustrating the power of modern NLP techniques in extracting meaningful insights from customer reviews.
