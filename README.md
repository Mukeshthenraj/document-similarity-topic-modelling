# Document Similarity and Topic Modelling

A Python project that demonstrates document similarity measurement and topic modeling techniques using **NLTK** and **Gensim** libraries. This project processes a dataset of text paraphrases, computes similarity scores, and extracts latent topics.

---

## 🚀 Project Overview

This project covers:

- **Preprocessing text data** (tokenization, POS tagging)
- **WordNet-based semantic similarity**
- **Symmetrical similarity scoring between sentence pairs**
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

| Quality | D1                                    | D2                                    |
|---------|---------------------------------------|---------------------------------------|
| 1       | "Ms Stewart, the chief executive..." | "Ms Stewart, 61, its chief executive..." |
| 0       | "And it's going to be a wild ride..."| "Now the rest is just mechanical..." |
| ...     | ...                                   | ...                                   |

- **Quality**: 1 if the sentences are paraphrases, 0 otherwise
- **D1 / D2**: Text of the two sentences

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
nltk.download('averaged_perceptron_tagger')
nltk.download('wordnet')
nltk.download('omw-1.4')
```

---

## 🧩 How to Run

1. Clone this repository or download the files.
2. Make sure `assets/paraphrases.csv` and `document_similarity_topic_modelling.py` are in the same folder structure.
3. Run the script:

```bash
python document_similarity_topic_modelling.py
```

---

## ✨ Features Implemented

- **Document Preprocessing:**
  - Tokenization
  - POS tagging
  - WordNet synset mapping
- **Semantic Similarity:**
  - Path similarity between synsets
  - Symmetrical similarity scoring (`document_path_similarity`)
- **Evaluation:**
  - `most_similar_docs()` returns the most similar pair of sentences.
  - `label_accuracy()` computes classification accuracy against labels.
- **Topic Modeling:**
  - Gensim LDA to identify latent topics in text corpus.
  - `lda_topics()` to list top words per topic.
  - `topic_distribution()` to get topic probabilities for a new document.
  - `topic_names()` to label topics with descriptive names.

---

## 📈 Example Outputs

- **Most Similar Documents:**

```
('"Indeed, Iran should be put on notice that efforts to try to remake Iraq in their image will be aggressively put down," he said.',
 '"Iran should be on notice that attempts to remake Iraq in Iran\'s image will be aggressively put down," he said.',
 0.9590643274853801)
```

- **Similarity Accuracy:**
```
0.7
```

- **Top Topics:**

```
(9, '0.068*"space" + 0.036*"nasa" + 0.021*"science" + ...')
```

- **Topic Distribution:**
```
[(3, 0.496), (9, 0.343), ...]
```

---

## 📝 License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.

---

## 🙌 Acknowledgements

This project demonstrates core NLP workflows using open-source libraries:

- [NLTK](https://www.nltk.org/)
- [Gensim](https://radimrehurek.com/gensim/)
- [scikit-learn](https://scikit-learn.org/)

Feel free to use and adapt it for your learning or research projects.
