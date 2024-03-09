# Sentiment Analysis on Product Review Data Using Google BERT

Author: Giuseppe Cappella

This project demonstrates a comprehensive approach to sentiment analysis on customer reviews, leveraging the powerful BERT model within a TensorFlow framework. From mounting the dataset to training and evaluating the model, the project encapsulates an end-to-end process, culminating in the application of the trained model to classify unseen customer reviews into sentiment categories.

## Dataset Description

The project utilizes an extensive dataset containing 462,744 labeled customer reviews, each associated with a sentiment label (negative, neutral, positive). Due to the considerable size of the dataset's CSV file, it is not included directly within the repository. 
The dataset features 3 key columns:

- labelled_reviews_index: A unique identifier for each review in the dataset.
- review_text: The text content of the customer review.
- sentiment_label`: The sentiment of the review categorized as negative, neutral, or positive.

## Project Overview

The project is structured into distinct phases, starting with data preparation, followed by model training and evaluation, and concluding with the application of the model to predict sentiments of new reviews.

### Data Preparation and Feature Engineering

The initial phase involves loading the dataset into a pandas DataFrame, followed by label encoding to convert sentiment labels into numerical form. This encoded dataset is then transformed into a Hugging Face Dataset object, allowing for easy manipulation and split into training, testing, and validation sets. A tokenizer is initialized to prepare the review texts for BERT, ensuring inputs are in the correct format for model training.

### Model Training and Evaluation

The core of the project lies in training the BERT model for sequence classification. The TensorFlow implementation of BERT is utilized, with the model being trained to classify reviews into the three sentiment categories. This process involves setting up a training pipeline, including tokenization, data collation, and the creation of TensorFlow datasets for training, validation, and testing. The model's performance is evaluated using various metrics, with results visualized through confusion matrices and classification reports.

### Application to New Data

With the model trained, the project demonstrates its application to new customer reviews. The process involves tokenizing unseen reviews, predicting their sentiments with the trained model, and appending these predictions to the dataset. This showcases the model's practical utility in analyzing customer sentiments, providing valuable insights for business strategies.

## Results:

The model's performance on sentiment analysis of customer reviews has been evaluated using a confusion matrix, which serves to illustrate the accuracy of the model by displaying the number of true positive, false positive, true negative, and false negative predictions for each class.

<img width="708" alt="Schermata 2024-03-09 alle 23 20 03" src="https://github.com/peppecappella/Sentiment-Analysis-on-Product-Review-Data-Using-Google-BERT/assets/124899610/5df215dd-0b9d-43e9-8880-34d75d6fb53b">

The results obtained from the Google BERT-based model for sentiment analysis of customer reviews demonstrate overall high performance.

The confusion matrix results suggest the model excels at correctly identifying positive reviews, evidenced by a high precision rate of 94% and a recall rate of 98%. These metrics imply a high level of reliability in tagging a review as positive when it indeed is, with very few positive reviews being misclassified.

When considering negative reviews, the model demonstrates an 85% precision and 93% recall. Although this indicates a slightly higher rate of false positives for this category as compared to positive reviews, it still maintains a robust ability to recognize negative comments.

Neutral reviews pose a greater challenge for the model, showing a 92% precision and 79% recall. The difficulty in accurately identifying neutral reviews is common across many sentiment analysis models due to the intrinsic subtlety of the neutral category. Nevertheless, the performance here remains commendable.

The confusion matrix further corroborates the model's performance. Most errors occur within the neutral category, where some instances have been misclassified as negative or positive. This could suggest a need for further refinement of the model to better handle the nuances of these reviews.

The F1-score, balancing precision and recall, is outstanding for positive reviews and very good for the other categories, reflecting an effective compromise between the two metrics.

Finally, the aggregated metrics (accuracy, macro average, and weighted average) all exceed 90%, underscoring the overall efficacy of the model in sentiment analysis. These performances make the model a reliable tool for large-scale analysis of customer sentiment.
