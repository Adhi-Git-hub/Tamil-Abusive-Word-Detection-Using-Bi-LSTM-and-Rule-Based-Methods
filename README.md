# Tamil-Abusive-Word-Detection-Using-Bi-LSTM-and-Rule-Based-Methods

## Project Overview
In this project, we addressed the challenge of detecting abusive words in Tamil text, focusing particularly on low-frequency abusive words that are often missed by standard models. We utilized a hybrid approach combining deep learning (Bi-LSTM) with a rule-based method to enhance the model's ability to detect abusive content even in subtle or rare cases. LIME was incorporated to provide interpretability for each prediction.

## Problem Faced
Detecting abusive content in Tamil language is challenging due to:
1. **Low Occurrence of Abusive Words**: Some abusive words appear rarely in datasets, making it difficult for models to detect them effectively.
2. **Fuzzy Matching of Abusive Words**: Many abusive words in Tamil might appear in different forms or with slight variations, requiring more robust detection mechanisms.
3. **Interpretability of Model Predictions**: It's critical to not only detect abusive words but also understand why a certain comment was classified as abusive or non-abusive.

## Solution Implemented
We tackled these problems with the following solutions:
- **Bi-LSTM Model**: A deep learning model with Bidirectional LSTM layers was used to predict abusive or non-abusive content in a sequence of text. The model is designed to handle sequential data, making it effective for language modeling tasks.
- **Rule-Based Post-Processing**: After the initial prediction, a rule-based post-processing step was introduced to identify low-frequency abusive words using fuzzy matching. This step enhances the model’s performance by addressing edge cases that the model might otherwise miss.
- **LIME for Interpretability**: LIME (Local Interpretable Model-agnostic Explanations) was used to explain individual predictions. By breaking down the contribution of each word to the final prediction, we made the model’s decisions more transparent and interpretable.

## FastText Embedding Model
For this project, we used pre-trained FastText embeddings specific to the Tamil language. These embeddings, which capture semantic relationships between words, were loaded using the FastText `cc.ta.300.vec.gz` model. The FastText model provides an effective way of representing words as dense vectors that capture context and meaning, which significantly improves the performance of our Bi-LSTM model.

## Files and Datasets
- **Dataset**: We created a custom abusive word dataset for Tamil comments, containing labeled examples of abusive and non-abusive content.
- **FastText Embedding**: We attached Tamil FastText vector embeddings to train the Bi-LSTM model.
- **Model**: The Bi-LSTM model is trained on this dataset and enhanced using the rule-based fuzzy matching method.
- **LIME Explanations**: We used LIME to provide explanations for the model’s predictions.

## Steps to Run the Project
1. Install the necessary dependencies.
2. Prepare the data and pre-trained FastText embeddings.
3. Train the model using the provided scripts.
4. Use LIME to visualize and interpret the model's predictions.
5. Evaluate the model on the test set and observe improvements with the rule-based enhancements.

## Conclusion
This project highlights the benefits of combining machine learning models with rule-based techniques to improve accuracy and handle edge cases in abusive word detection for Tamil text. By integrating LIME, we ensured that the model’s decisions are transparent and interpretable.



