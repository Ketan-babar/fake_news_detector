flowchart LR
    subgraph Data_Layer["🗂️ Data Layer"]
        A1[Fake.csv<br/>(Fake News)]
        A2[True.csv<br/>(Real News)]
    end

    subgraph Ingestion["📥 Data Ingestion"]
        B[Load CSV Files<br/>Assign Labels<br/>Merge Dataset]
    end

    subgraph Preprocessing["🧹 Text Preprocessing"]
        C1[Lowercasing]
        C2[Regex Cleaning]
        C3[Stopword Removal]
    end

    subgraph Feature_Engineering["🧠 Feature Engineering"]
        D[TF-IDF Vectorization]
    end

    subgraph Model["🤖 ML Model"]
        E[Logistic Regression Classifier]
    end

    subgraph Evaluation["📊 Evaluation Layer"]
        F1[Accuracy]
        F2[Confusion Matrix]
        F3[F1-Score]
    end

    %% Flow connections
    A1 --> B
    A2 --> B
    B --> C1 --> C2 --> C3
    C3 --> D
    D --> E
    E --> F1
    E --> F2
    E --> F3




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
