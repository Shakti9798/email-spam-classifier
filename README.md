# 📧 Email Spam Classifier

A Machine Learning project that uses **Natural Language Processing (NLP)** and **Multinomial Naive Bayes** to automatically classify SMS/Email messages as **Ham (legitimate)** or **Spam**.

The project includes data exploration, text vectorization, model training, evaluation, real-time inference, and model serialization using `joblib`.

---

## 📌 Project Overview

Spam messages are unwanted and potentially harmful messages that can contain misleading offers, advertisements, or fraudulent content.

This project builds an automated spam detection system that learns patterns from historical SMS messages and predicts whether a new message is **Ham** or **Spam**.

### 🎯 Objective

* Analyze an SMS/Email dataset using Exploratory Data Analysis (EDA)
* Convert text messages into numerical features
* Train a Machine Learning classification model
* Evaluate the model using multiple performance metrics
* Test the model on unseen messages
* Save and reload the trained model for future deployment

---

## 📊 Dataset

The project uses the **SMS Spam Collection Dataset**.

* **Total Messages:** 5,572
* **Ham Messages:** 4,825
* **Spam Messages:** 747
* **Features:** Category, Message
* **Missing Values:** None

The target variable contains two classes:

| Category | Description           |
| -------- | --------------------- |
| `Ham`    | Legitimate message    |
| `Spam`   | Unwanted/spam message |

---

## 🔎 Exploratory Data Analysis

The dataset was analyzed to understand its structure and class distribution.

The following checks were performed:

* Dataset information
* Statistical summary
* Missing-value detection
* Class distribution
* Number of unique messages

A count plot was also created to visualize the distribution between Ham and Spam messages.

---

## ⚙️ Machine Learning Pipeline

The project uses an end-to-end **Scikit-learn Pipeline** consisting of:

### 1. CountVectorizer

`CountVectorizer` converts the text messages into numerical **Bag-of-Words** features that can be processed by the Machine Learning model.

### 2. Multinomial Naive Bayes

`MultinomialNB` is used as the classification algorithm because it is well suited for text classification problems.

### 3. Train-Test Split

The dataset was divided into:

* **80% Training Data**
* **20% Testing Data**
* `random_state = 42`

The target labels were encoded as:

```text
Ham  → 0
Spam → 1
```

---

## 📈 Model Performance

The trained model achieved an overall **99.19% accuracy** on the test dataset.

### Classification Report

| Class                | Precision | Recall |   F1-Score |
| -------------------- | --------: | -----: | ---------: |
| Ham                  |      0.99 |   1.00 |       1.00 |
| Spam                 |      1.00 |   0.94 |       0.97 |
| **Overall Accuracy** |           |        | **99.19%** |

### Evaluation Metrics

The model was evaluated using:

* Accuracy
* Precision
* Recall
* F1-Score
* Confusion Matrix

A confusion matrix was also generated to analyze correct and incorrect predictions.

---

## 🧪 Testing & Inference

The trained model was tested on previously unseen messages.

### Example 1

**Input:**

```text
Hey, are we still meeting for lunch today?
```

**Prediction:**

```text
Ham
```

### Example 2

**Input:**

```text
CONGRATULATIONS! You've won a $1,000 gift card. Click here to claim now!
```

**Prediction:**

```text
Spam
```

---

## 💾 Model Serialization

The trained Scikit-learn pipeline was saved using **Joblib**.

```text
spam_classifier_pipeline.joblib
```

The saved model was then loaded back and tested successfully, demonstrating that the trained pipeline can be reused without retraining.

This makes the model suitable for future integration with applications such as:

* Streamlit
* Flask
* Web applications
* API-based services

---

## 🛠️ Technologies & Libraries

* **Python**
* **Pandas**
* **Seaborn**
* **Matplotlib**
* **Scikit-learn**
* **Joblib**
* **Natural Language Processing (NLP)**
* **Machine Learning**

### Machine Learning Concepts

* Exploratory Data Analysis
* Text Classification
* Bag-of-Words
* Train-Test Split
* Naive Bayes Classification
* Model Evaluation
* Confusion Matrix
* Model Serialization

---

## 📂 Project Structure

```text
Email-Spam-Classifier/
│
├── email_spam_classifier.ipynb
├── spam_classifier_pipeline.joblib
├── spam.csv
└── README.md
```

> The exact files in the repository may vary depending on which dataset and model files you choose to upload.

---

## 🚀 How to Run the Project

### 1. Clone the Repository

```bash
git clone https://github.com/Shakti9798/Email-Spam-Classifier.git
```

### 2. Install Required Libraries

```bash
pip install pandas seaborn matplotlib scikit-learn joblib
```

### 3. Open the Notebook

Open:

```text
email_spam_classifier.ipynb
```

using **Jupyter Notebook** or **Google Colab**.

### 4. Run the Cells

Run the notebook sequentially to:

1. Load the dataset
2. Perform EDA
3. Prepare the data
4. Train the model
5. Evaluate performance
6. Test new messages
7. Save and reload the trained model

---

## 🔮 Future Improvements

Possible improvements for this project include:

* Text preprocessing such as stopword removal and stemming/lemmatization
* TF-IDF vectorization
* Comparing multiple Machine Learning algorithms
* Hyperparameter tuning
* Handling class imbalance
* Building a Streamlit web application
* Deploying the classifier as an API
* Adding a user interface for real-time message classification

---

## 📌 Key Takeaways

* Built an end-to-end NLP classification pipeline.
* Used `CountVectorizer` to transform text into numerical features.
* Implemented **Multinomial Naive Bayes** for spam classification.
* Achieved **99.19% test accuracy**.
* Evaluated the model using Precision, Recall, F1-Score, and Confusion Matrix.
* Tested the model on unseen messages.
* Serialized the trained pipeline using Joblib for potential deployment.

---

## 👨‍💻 Author

**Shakti Bhushan Mishra**

*Aspiring Data Analyst | Data Science Enthusiast*

### Connect with Me

* 📧 Email: [shaktibhushanmishra@gmail.com](mailto:shaktibhushanmishra@gmail.com)
* 💼 LinkedIn: https://www.linkedin.com/in/shakti-bhushan-mishra
* 🐙 GitHub: https://github.com/Shakti9798

---

⭐ If you found this project useful, consider giving the repository a star!
