mermaid

flowchart TD
    A[Fake.csv / True.csv<br/>(Raw News Data)]
    B[Data Ingestion<br/>• Load CSV files<br/>• Assign labels]
    C[Text Preprocessing<br/>• Lowercasing<br/>• Regex cleaning<br/>• Stopword removal]
    D[Feature Engineering<br/>TF-IDF Vectorization]
    E[ML Model<br/>Logistic Regression]
    F[Evaluation Layer<br/>Accuracy • Confusion Matrix • F1-score]

    A --> B
    B --> C
    C --> D
    D --> E
    E --> F



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
