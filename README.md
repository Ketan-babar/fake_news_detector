<img width="1536" height="1024" alt="image" src="https://github.com/user-attachments/assets/0af71e14-cff3-4d65-b0e2-a9bd96a9571e" />



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
