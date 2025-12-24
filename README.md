# 📧 Spam Detection with Naive Bayes

A machine learning project to classify emails as **Spam** or **Ham** using **TF-IDF** vectorization and **Multinomial Naive Bayes**. This project demonstrates text preprocessing, model training, evaluation, and predicting new emails.

---

## 🗂 Dataset

- The dataset contains email messages with labels `Spam` or `Ham`.
- CSV columns include:
  - `Message`: The text content of the email
  - `Category`: Label (`Spam` / `Ham`)

**Note:** Malformed or empty rows are skipped during preprocessing.

---

## 🧹 Data Preprocessing

1. Remove rows with missing values (`NaN`).
2. Encode `Category` labels using **LabelEncoder** (`Spam` → 1, `Ham` → 0).
3. Convert email messages into numeric features using **TF-IDF vectorization**:
   - Stop words removed (`stop_words='english'`)
   - Top 5000 features (`max_features=5000`)

---

## 🧠 Model

- **Algorithm:** Multinomial Naive Bayes
- **Reason:** Works well with discrete features like word counts or TF-IDF scores in text classification.

---

## 🧪 Train-Test Split

- 80% training, 20% testing
- `random_state=0` for reproducibility

---

## 📊 Evaluation

- **Accuracy:** Measures overall prediction correctness
- **Optional:** Use `classification_report` to check **precision, recall, and F1-score**

```python
from sklearn.metrics import classification_report
print(classification_report(y_test, y_pred, target_names=['Ham','Spam']))
```
🚀 Usage
Clone the repository:

bash
Copy code
git clone https://github.com/vishak45/email-spam-detector
cd email-spam-detector


Install dependencies:

bash
Copy code
```
pip install -r requirements.txt
```

🛠 Technology Stack

Python 3.x

Pandas

Scikit-learn

Matplotlib / Seaborn

TF-IDF Vectorization

⚡ Future Improvements
Handle imbalanced datasets with SMOTE or class weighting

Use deep learning models like LSTM or BERT for better accuracy

Deploy as a web API using Flask or FastAPI

Add GUI or CLI interface for real-time email classification

🔗 Author
Vishak45
GitHub Profile
