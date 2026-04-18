
# SMS Spam Classifier 📩

A machine learning system that classifies SMS messages as Spam or Ham
(legitimate) using Natural Language Processing and an ensemble Voting
Classifier combining multiple ML models.

## The Problem
Spam messages are one of the most persistent problems in digital
communication. With billions of SMS messages sent daily, automated
spam detection is critical to protect users from scams, phishing
attacks, and unwanted promotions. In India, spam SMS is a growing
concern with millions of fraudulent messages sent daily targeting
bank customers, job seekers, and general users.

## Dataset
[SMS Spam Collection Dataset — UCI Machine Learning](https://www.kaggle.com/datasets/uciml/sms-spam-collection-dataset)
- 5,572 SMS messages
- Binary classification: Ham (0) or Spam (1)
- Real SMS messages collected for spam research

## Project Workflow
- Loaded and explored the SMS spam dataset
- Dropped unnecessary columns and renamed for clarity
- Applied Label Encoding (ham → 0, spam → 1)
- Checked and removed duplicate messages
- Text preprocessing using NLTK:
  - Tokenization
  - Stopword removal
  - Stemming using PorterStemmer
- Feature extraction using TF-IDF Vectorizer
- Trained and compared multiple ML models
- Built a Voting Classifier combining best performing models
- Evaluated using Accuracy and Precision metrics

## Models Compared
| Model | Accuracy | Precision |
|---|---|---|
| Extra Trees Classifier (ETC) | 97.77% | 99.14% |
| SVC (Sigmoid Kernel) | 97.00% | 99.08% |
| AdaBoost | 97.29% | 97.41% |
| XGBoost | 96.22% | 95.41% |
| Gradient Boosting (GBDT) | 97.19% | 95.04% |
| Bagging Classifier (Bgc) | 95.16% | 94.00% |
| Multinomial Naive Bayes | 95.16% | 93.13% |

## Final Model — Voting Classifier
```python
voting_clf = VotingClassifier(estimators=[
    ('svc', SVC(kernel='sigmoid', gamma=1.0)),
    ('mnb', MultinomialNB()),
    ('etc', ExtraTreesClassifier())
], voting='hard')
```
Combines SVC, Naive Bayes, and Extra Trees through hard voting
for the most robust final prediction.

## What I Learned
- Full NLP preprocessing pipeline (clean → tokenize → stem → vectorize)
- TF-IDF vectorization to convert raw text into ML-ready features
- Training and comparing 7 different classification models
- Ensemble learning using Voting Classifier
- Why precision matters more than accuracy for spam detection
- Effect of feature scaling on different model performances

## How To Run
```bash
pip install numpy pandas scikit-learn nltk xgboost
jupyter notebook spam-classifier.ipynb
```

## Tech Stack
Python | Pandas | NumPy | Scikit-learn | NLTK | TF-IDF | XGBoost |
SVC | ExtraTrees | AdaBoost | Voting Classifier

## Future Improvements
- Add Streamlit web interface for real-time spam detection
- Fine-tune BERT for higher precision
- Deploy as public web app on Streamlit Cloud