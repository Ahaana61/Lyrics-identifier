# 🎵 Song & Artist Identification from Lyrics Snippet

## 📌 Project Overview
This project implements a text-based identification system that predicts the **song title** and **artist name** when given a **small snippet of lyrics or text**.  
The system uses Natural Language Processing (NLP) techniques and a similarity-based retrieval model to match the input snippet with songs in a large Spotify lyrics dataset.

---

## 🎯 Objective
To build a model that:
- Accepts a short lyrics snippet as input
- Identifies the most relevant **song title** and **artist**
- Demonstrates prediction accuracy using standard evaluation metrics

---

## 🗂 Dataset
**Spotify Million Song Dataset (Lyrics Version)**

**Columns used:**
- `artist` – Artist name
- `song` – Song title
- `text` – Song lyrics

---

## ⚙️ Technologies Used
- Python
- Pandas, NumPy
- NLTK (text preprocessing)
- Scikit-learn (TF-IDF, Cosine Similarity)
- Google Colab / Jupyter Notebook

---

## 🧠 Methodology

### 1. Text Preprocessing
- Lowercasing
- Removal of punctuation and numbers
- Tokenization
- Stop-word removal

### 2. Feature Extraction
- TF-IDF (Term Frequency–Inverse Document Frequency) vectorization
- Character and word-level features for lyric matching

### 3. Similarity Model
- Cosine Similarity is used to measure closeness between the input snippet and stored lyrics
- The song with the highest similarity score is selected as the prediction

---

## 🔍 Model Prediction
Given a lyrics snippet, the model:
1. Cleans and preprocesses the text
2. Converts it into a TF-IDF vector
3. Computes similarity with all songs in the dataset
4. Returns the most similar song and artist with a confidence score

---

## 📊 Model Evaluation (Prediction Accuracy)

Since lyric snippets can be ambiguous, the model is evaluated using **Top-K Accuracy**, a standard metric in information retrieval systems.

### Evaluation Method:
- Random songs are selected
- A short snippet is extracted from their lyrics
- A prediction is considered correct if the original song appears in the Top-K retrieved results

### Results:
| Metric | Accuracy |
|------|---------|
| Top-1 Accuracy | ~88% |
| Top-3 Accuracy | ~90% |
| Top-5 Accuracy | ~95% |

---

## ✅ Conclusion
The model successfully identifies songs and artists from partial lyric snippets using NLP-based similarity matching.  
While short snippets may be ambiguous, the Top-K retrieval approach ensures robust and realistic performance.

---

## 🚀 Future Improvements
- Use transformer-based embeddings (BERT / Sentence-BERT)
- Build a web interface using Streamlit
- Improve semantic understanding of lyrics

---

## 👤 Author
**Ahana Mukhopadhyay**
