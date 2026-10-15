# 📈 Financial News Sentiment Analyzer (FinBERT & Streamlit)

[![Python](https://img.shields.io/badge/Python-3.10%2B-blue.svg)](https://www.python.org/)
[![HuggingFace](https://img.shields.io/badge/Model-FinBERT%20(ProsusAI)-yellow.svg)](https://huggingface.co/ProsusAI/finbert)
[![Streamlit](https://img.shields.io/badge/UI-Streamlit-red.svg)](https://streamlit.io/)
[![License](https://img.shields.io/badge/License-MIT-purple.svg)](LICENSE)

An intelligent Natural Language Processing (NLP) web application that analyzes financial news headlines, earnings call excerpts, and market commentary to predict financial market sentiment (**Positive**, **Negative**, or **Neutral**) with high confidence scores.

---

## 🧠 Model Architecture & Details

* **Underlying Model:** **FinBERT** (`ProsusAI/finbert`)
  * FinBERT is a pre-trained NLP model specifically fine-tuned on **Financial PhraseBank** (a large-scale financial domain corpus).
  * Unlike general-purpose BERT, FinBERT understands financial jargon, market sentiment shifts (e.g., *"revenue dropped"* vs *"costs reduced"*), and domain-specific semantic nuances.
* **Pipeline:** Built using the Hugging Face `transformers` pipeline for fast tokenization and sequence classification.
* **Inference Output:**
  * Sentiment Classification: `Positive`, `Negative`, or `Neutral`
  * Confidence Score: Calibrated softmax probability score (0.0000 to 1.0000).

---

## 📊 Dataset

* **Dataset:** Financial PhraseBank (`all-data.csv`)
* **Description:** A benchmark financial sentiment analysis dataset containing thousands of sentences extracted from financial news releases, classified by finance professionals.

---

## 🚀 Getting Started

### 1. Prerequisites
* Python 3.10 or higher
* Internet access (to automatically download the pre-trained weights from Hugging Face on the first run)

### 2. Installation
```bash
# Clone the repository
git clone https://github.com/asawirrr/financial-sentiment-analyzer-finbert.git
cd financial-sentiment-analyzer-finbert

# Create and activate virtual environment
python -m venv venv
# Windows:
venv\Scripts\activate
# Linux / macOS:
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt
```

### 3. Launch Web Application
```bash
streamlit run app.py
```
Open your browser at `http://localhost:8501`.

---

## 🖥️ Usage Example

1. Enter a financial headline such as:
   > *"Operating profit rose by 14% to EUR 3.2 million, beating analyst estimates."*
2. Click **"Analyze Sentiment"**.
3. **Result Output:**
   * **Sentiment:** `Positive`
   * **Confidence Score:** `0.9842`

---

## 📁 Repository Structure

```
├── app.py              # Streamlit Web Application & Inference Pipeline
├── all-data.csv        # Financial PhraseBank Dataset
├── report.docx         # Project Documentation & Experimental Analysis Report
├── requirements.txt    # Python Dependencies
├── .gitignore          # Cache and environment exclusion rules
└── README.md           # Project Documentation
```

---

## 📄 License
This project is open-source and available under the MIT License.