# NewsGuard

NewsGuard is a project aimed at providing tools and resources for evaluating the credibility of news sources. Built with Streamlit, scikit-learn and NLTK.

## Features


- Preprocess text by removing non-letters, lowercasing, filtering out stopwords and applying Porter stemming  
- Convert cleaned text into TF-IDF vectors  
- Train a logistic regression classifier on a labeled news dataset  
- Interactive Streamlit UI for live “REAL” or “FAKE” predictions

## Installation

```bash
git clone https://github.com/yourusername/newsguard.git
cd newsguard
Install Depedencies: 
    pip install streamlit pandas numpy nltk scikit-learn
```

## Usage

```bash
python -m streamlit run app.py
```
*Your browser will open at http://localhost:8501. Paste or type your article text and receive a “REAL” or “FAKE” verdict.*

## How it Works
1. Data loading

    - Reads train.csv

    - Fills missing fields with blanks

2. Text preprocessing

    - Concatenates author and title

    - Strips out non-letters

    - Converts to lowercase

    - Removes NLTK stopwords

    - Applies Porter stemming

3. Vectorization

    - Fits a TfidfVectorizer on the cleaned text

4. Model training

    - Splits data into 80% train and 20% test sets

    - Trains a LogisticRegression classifier

5. Prediction

    - Applies the same preprocessing and vectorization to new input

    - Outputs the model’s label