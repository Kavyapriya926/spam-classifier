# spam-classifier
# 📧 SMS Spam Classifier

A machine learning model to classify SMS messages as Spam or Ham.

## How it works
- Preprocesses messages (cleaning + TF-IDF)
- Trains a Naive Bayes model
- Predicts whether new messages are spam or not

## How to Use
```python
# Load model and vectorizer
model = joblib.load('spam_classifier_model.pkl')
vectorizer = joblib.load('tfidf_vectorizer.pkl')

# Predict
msg = "You’ve won ₹10,000! Claim now!"
vect = vectorizer.transform([msg])
print(model.predict(vect))  # 1 means Spam
