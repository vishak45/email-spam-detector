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


---

## 🚀 Usage
Clone the repository:


```
git clone https://github.com/vishak45/email-spam-detector
cd email-spam-detector
```

Install dependencies:


```
pip install -r requirements.txt
```

