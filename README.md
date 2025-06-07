# Identifying-Entities-in-Healthcare-Data-
‘BeHealthy’ has a web platform that allows doctors to list their services and manage patient interactions and provides services for patients such as booking interactions with doctors and ordering medicines online. Here, doctors can easily organise appointments, track past medical records and provide e-prescriptions.

# BeHealthy Medical Named Entity Recognition (NER)

---

## 🚀 Project Overview

**BeHealthy** is a conceptual health tech platform designed to connect doctors and patients across the country. It generates large volumes of medical text data daily, including clinical notes and therapy reviews containing complex medical terminology such as diseases and treatments.

This project focuses on building a **custom Named Entity Recognition (NER)** model to automatically extract **disease names** and their corresponding **treatments** from unstructured medical text. Since these entities are not explicitly labeled, the model learns to identify and classify them from the dataset.

---

## 📂 Dataset Description

You will work with four datasets:

| Dataset      | Description                                                   |
|--------------|---------------------------------------------------------------|
| `train_sent` | Training sentences with one word per line; blank lines separate sentences. |
| `train_label`| Labels for each word in `train_sent` (`D`=Disease, `T`=Treatment, `O`=Other). |
| `test_sent`  | Test sentences in the same format as `train_sent`.            |
| `test_label` | Labels corresponding to `test_sent`.                           |

**Note:** Sentences need to be reconstructed by grouping words between blank lines.

---

## 🛠️ Project Workflow

1. **Data Preprocessing**  
   Convert word-level data and labels into sentence-level structures for both training and testing sets.

2. **Concept Identification**  
   Understand the dataset’s entity labels and their meanings (`Disease`, `Treatment`, `Other`).

3. **Feature Engineering**  
   Define and extract features for each word to use in the Conditional Random Field (CRF) model.

4. **Feature Extraction**  
   Extract features for all words in every sentence (train and test).

5. **Input & Target Preparation**  
   Prepare input feature vectors and target labels to train the model.

6. **Model Building**  
   Train a CRF model to recognize disease and treatment entities in text.

7. **Model Evaluation**  
   Evaluate model performance using the test dataset.

8. **Entity Extraction & Mapping**  
   Use the trained model to extract diseases and treatments, organizing them into a dictionary where diseases are keys and treatments are values.

---

## ⚙️ How to Use

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/BeHealthy-NER.git
   cd BeHealthy-NER
