PROJECT ARCHITECTURE:
┌────────────────────┐
│   Data Layer       │
│ (CSV files)        │
└─────────┬──────────┘
          ↓
┌────────────────────┐
│ Preprocessing      │
│ (cleaning text)    │
└─────────┬──────────┘
          ↓
┌────────────────────┐
│ Feature Engineering│
│ (TF-IDF)           │
└─────────┬──────────┘
          ↓
┌────────────────────┐
│ ML Model           │
│ (Logistic Reg.)    │
└─────────┬──────────┘
          ↓
┌────────────────────┐
│ Evaluation Layer   │
│ (Accuracy, CM)    │
└────────────────────┘

Logical Flow Architecture (Pipeline View)

This explains what happens when the script runs.

Step 1: Data Ingestion

Load Fake.csv and True.csv
Assign labels:
FAKE
REAL
Merge into a single DataFrame


Step 2: Text Preprocessing

For each news article:
Convert to lowercase
Remove punctuation & non-alphabetic characters
Remove stopwords (NLTK)
Normalize whitespace


Step 3: Feature Engineering (TF-IDF)

Convert cleaned text into numerical vectors
Capture:
Term importance
Frequency-based relevance
Limit features for efficiency


Step 4: Train–Test Split

Split dataset into:
Training set
Testing set


Step 5: Model Training

Algorithm: Logistic Regression
Train on TF-IDF vectors



Step 6: Evaluation

Predict on test data
Calculate:
Accuracy
Confusion Matrix
Precision, Recall, F1-score
