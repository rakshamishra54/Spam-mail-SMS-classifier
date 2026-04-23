
# 📩 SMS Spam Classifier

A Machine Learning project that classifies SMS messages as **Spam** or **Ham (Not Spam)** using multiple algorithms and compares their performance.

---

## 🚀 Project Overview

This project applies various machine learning models to detect spam messages from text data. It includes:

- Data preprocessing & cleaning  
- Feature extraction (text → numerical form)  
- Model training & evaluation  
- Comparison of multiple classifiers  

---

## 📂 Dataset

- Source: https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset  
- Total Messages: 5572 SMS  
- Classes:
  - ham → Not Spam  
  - spam → Spam  

---

## ⚙️ Models Used

- Random Forest  
- Extra Trees  
- Logistic Regression  
- Multinomial Naive Bayes  
- XGBoost  
- AdaBoost  
- Gradient Boosting  
- Bagging Classifier  
- Decision Tree  
- K-Nearest Neighbors  
- Support Vector Machine (SVM)  

---

## 📊 Model Performance

### Accuracy Scores

| Algorithm            | Accuracy |
|---------------------|----------|
| ExtraTrees          | 0.9787 |
| MultinomialNB       | 0.9739 |
| XGBoost             | 0.9700 |
| RandomForest        | 0.9690 |
| Bagging             | 0.9661 |
| LogisticRegression  | 0.9652 |
| AdaBoost            | 0.9642 |
| GradientBoosting    | 0.9507 |
| DecisionTree        | 0.9449 |
| KNeighbors          | 0.8859 |
| SVC                 | 0.8665 |

---

### Precision Scores

| Algorithm            | Precision |
|---------------------|----------|
| RandomForest        | 0.9818 |
| ExtraTrees          | 0.9754 |
| LogisticRegression  | 0.9554 |
| MultinomialNB       | 0.9512 |
| XGBoost             | 0.9496 |
| AdaBoost            | 0.9316 |
| GradientBoosting    | 0.9307 |
| Bagging             | 0.8992 |
| DecisionTree        | 0.8857 |
| KNeighbors          | 0.8333 |
| SVC                 | 0.0000 |

---

## 🧠 Key Insights

- ExtraTrees achieved the highest accuracy  
- RandomForest achieved the highest precision  
- MultinomialNB performed very well for text data  
- SVC failed in precision → not suitable for this task  

In spam detection, **precision is more important than accuracy** (reducing false positives).

---

## 🛠️ Tech Stack

- Python  
- Pandas, NumPy  
- Scikit-learn  
- NLTK  
- Matplotlib / Seaborn  

---

## 🔄 Workflow

1. Data Cleaning  
2. Text Preprocessing (tokenization, stopwords removal)  
3. Feature Extraction (Bag of Words / TF-IDF)  
4. Train-Test Split  
5. Model Training  
6. Evaluation (Accuracy & Precision)  

---

## 💡 Future Improvements

- Deep Learning (LSTM / Transformers)  
- Hyperparameter tuning  
- Deployment (Streamlit / Flask)  

---

