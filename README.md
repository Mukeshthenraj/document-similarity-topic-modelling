# Document Similarity and Topic Modelling

A Python project that demonstrates document similarity measurement and topic modeling techniques using **NLTK** and **Gensim** libraries. This project processes a dataset of text paraphrases, computes similarity scores, and extracts latent topics.

---

## 🚀 Project Overview

This project covers:

- **Preprocessing text data** (tokenization, lemmatization, stop word removal)
- **WordNet-based semantic similarity**
- **TF-IDF vectorization**
- **Topic modeling** with LDA (Latent Dirichlet Allocation)
- Evaluation of document similarity for paraphrase detection

It is designed to help you understand and practice core NLP techniques for comparing and analyzing documents.

---

## 📂 Project Structure

```
.
├── assets/
│   └── paraphrases.csv
├── LICENSE
├── README.md
├── document_similarity_topic_modelling.py
└── .gitignore
```

- **assets/paraphrases.csv**: Dataset of sentence pairs labeled as paraphrases or not.
- **document_similarity_topic_modelling.py**: Main script containing all processing and analysis steps.
- **LICENSE**: MIT License.
- **README.md**: Project description and usage instructions.

---

## 📝 Dataset

The dataset `paraphrases.csv` contains pairs of sentences and labels indicating whether the sentences are paraphrases:

| sentence1               | sentence2              | is_paraphrase |
|-------------------------|------------------------|---------------|
| "The cat sat on the mat"| "A cat was sitting there"| 1 |
| ...                     | ...                    | ... |

Each record helps evaluate whether your similarity functions correctly predict semantic equivalence.

---

## ⚙️ Requirements

Install the required libraries using pip:

```bash
pip install pandas numpy nltk gensim scikit-learn
```

Also, ensure you have downloaded the NLTK resources (run this in Python once):

```python
import nltk
nltk.download('punkt')
nltk.download('wordnet')
nltk.download('stopwords')
```

---

## 🧩 How to Run

1. Clone this repository or download the files.
2. Make sure `assets/paraphrases.csv` and `document_similarity_topic_modelling.py` are in the same folder structure.
3. Run the script:

```bash
python document_similarity_topic_modelling.py
```

Each function in the script processes the data step by step, computes similarity scores, and trains a topic model.

---

## ✨ Features Implemented

- **Document Preprocessing:**
  - Lowercasing, tokenization, lemmatization
  - Stopword removal
- **Semantic Similarity:**
  - WordNet synset similarity
  - Path similarity between words
- **Vectorization:**
  - TF-IDF transformation of documents
- **Topic Modeling:**
  - Gensim LDA to identify latent topics
- **Evaluation:**
  - Similarity scoring and comparison against labels

---

## 📈 Example Outputs

- **Similarity Scores:**  
  Values between 0 and 1 indicating semantic closeness.
- **Top Topics:**  
  List of keywords representing discovered topics.
- **Model Accuracy:**  
  Basic metrics showing how well similarity scores align with paraphrase labels.

---

## 📝 License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.

---

## 🙌 Acknowledgements

This project demonstrates core NLP workflows using open-source libraries:

- [NLTK](https://www.nltk.org/)
- [Gensim](https://radimrehurek.com/gensim/)
- [scikit-learn](https://scikit-learn.org/)

Feel free to use and adapt it for your learning or research projects!
