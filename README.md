# 🏥 Healthcare Chatbot using NLP Models  
### *Disease Prediction • Symptom Extraction • Model Performance Comparison*

This project is an end-to-end **NLP-based Healthcare Chatbot** designed to identify symptoms from user input and predict the most likely disease using trained machine-learning and deep-learning models.  
It also includes a **performance comparison** of multiple NLP models trained on the same medical dataset.

---

## 📌 Project Overview

This chatbot analyses the text entered by a user, extracts medical symptoms, validates them using WordNet (synonyms check), and forwards valid symptoms to a trained classification model.  
The system then predicts the most probable disease and responds with a helpful explanation.

The chatbot is built to:
- Understand symptom-based queries  
- Map user language to structured medical intents  
- Predict diseases using multiple ML/DL models  
- Compare model accuracy, training behaviour, and reliability  
- Provide actionable outputs based on extracted symptoms  

---

## 🧠 High-Level Workflow

The chatbot pipeline works through four main stages:

1. **User enters text**  
2. **NLP Engine extracts symptoms**  
   - Tokenization  
   - Lemmatization  
   - Synonym matching with WordNet (Synset)  
3. **Validation of extracted symptoms**  
   - If valid → forward to classifier  
   - If invalid → user receives an “Invalid symptom” message  
4. **Disease Classification**  
   - Trained model predicts the most likely disease  
   - Chatbot returns the disease response  

---

### 📘 Flow Diagram

Below is the visual workflow used in the project:

<img src="/mnt/data/eeb44942-9229-4509-b166-a02fbdcc23c2.png" width="450"/>

---

---

## 🗂 Dataset Format (Training Data)

All models were trained using the same dataset structure.  
Below is the simplified pattern used in `intents.json`:

```json
{
  "intents": [
    {
      "name": "Acne",
      "description": "Acne is a common skin condition...",
      "symptoms": ["Blackheads", "Whiteheads", "Pimples"],
      "treatments": ["Topical creams", "Oral medication"],
      "response": ["You may have Acne"]
    }
  ]
}

---
Each disease includes:

Name

Description

Symptoms

Treatments

Responses used by chatbot

Purpose of This Project
- Build a medical symptom-based prediction chatbot
- Compare modern NLP approaches with classical ML techniques
- Understand how different text-processing models behave on the same dataset
- Provide a clean modular implementation for research or educational use

Technologies Used
- Python
- TensorFlow / Keras
- NLTK (Tokenization, Lemmatization, WordNet)
- Scikit-learn
- BERT (Transformers)
- NumPy, Pandas

## 📂 Project Structure

