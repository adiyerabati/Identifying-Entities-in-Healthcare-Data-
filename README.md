# Identifying-Entities-in-Healthcare-Data-
‘BeHealthy’ has a web platform that allows doctors to list their services and manage patient interactions and provides services for patients such as booking interactions with doctors and ordering medicines online. Here, doctors can easily organise appointments, track past medical records and provide e-prescriptions.

BeHealthy Medical Named Entity Recognition (NER)
Overview
BeHealthy is a hypothetical health tech platform connecting doctors and patients nationwide. The platform generates a large volume of medical text data daily, such as clinical notes and therapy reviews, containing complex medical terminology like diseases and treatments.

This project aims to build a custom Named Entity Recognition (NER) model to automatically extract disease names and their corresponding treatments from unstructured medical text. Since these entities are not explicitly labeled in the text, the model learns to identify and classify them from the dataset.

Dataset
The project uses four datasets:

train_sent: Training sentences with one word per line. Blank lines separate sentences.

train_label: Corresponding labels for each word in train_sent with tags:

D = Disease

T = Treatment

O = Other (non-entity)

test_sent: Test sentences in the same format as train_sent.

test_label: Labels corresponding to test_sent.

Note: Sentences must be reconstructed by grouping words between blank lines.

Project Workflow
The following steps outline the complete pipeline:

Data Preprocessing

Convert word-level data and labels into sentence-level format for both training and testing.

Concept Identification

Understand the labels and entity types (Disease, Treatment, Other) used in the dataset.

Feature Engineering

Define features for each word to train the Conditional Random Field (CRF) model.

Feature Extraction

Extract the features for all words in each sentence for training and testing.

Input and Target Preparation

Prepare feature vectors and target labels for model training.

Model Training

Build and train a CRF model for disease and treatment entity recognition.

Model Evaluation

Evaluate the model on the test set and measure its performance.

Entity Extraction and Mapping

Use the trained model to identify diseases and their predicted treatments in the text, and organize these as a dictionary where diseases are keys and treatments are values.

How to Use
Clone the repository.

Download the datasets (train_sent, train_label, test_sent, test_label) and place them in the data/ directory.

Run the preprocessing script to convert word-level data into sentence-level lists.

Extract features and train the CRF model.

Evaluate the model and extract disease-treatment pairs.

Technologies Used
Python 3.x

sklearn-crfsuite (CRF implementation)

pandas, numpy (data processing)

License
This project is for educational purposes only.
