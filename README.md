# Malicious URL Detection Model using Machine Learning

This repository contains a machine learning model designed to detect malicious URLs, classifying them into categories such as **benign**, **phishing**, **defacement**, or **malware**. The model leverages various features extracted from URLs and employs powerful classification algorithms for accurate prediction.

---

## 📚 Table of Contents

* [Introduction](#introduction)
* [Features](#features)
* [Installation](#installation)
* [Usage](#usage)
* [Data](#data)
* [Model Training](#model-training)
* [Prediction](#prediction)
* [Dependencies](#dependencies)
* [Contributing](#contributing)
* [License](#license)
* [Contact](#contact)

---

## 🧠 Introduction

In today's digital landscape, malicious URLs pose a significant threat, leading to phishing attacks, malware infections, and website defacement. This project builds a robust machine learning model capable of identifying and categorizing these harmful URLs, thereby enhancing online security.

The model is developed using **Python** and various ML libraries, demonstrating the pipeline from data loading and preprocessing to model training, evaluation, and prediction.

---

## 🔍 Features

The model uses the following URL-based features:

* **URL Length**
* **Hostname Length**
* **Path Length**
* **Query Length**
* **Fragment Length**
* **Number of Dots**
* **Number of Hyphens**
* **Number of @ Symbols**
* **Number of ? (Query Symbols)**
* **Number of & (Ampersands)**
* **Number of = (Equal Signs)**
* **Number of ! (Exclamations)**
* **Number of / (Slashes)**
* **Number of # (Hashtags)**
* **Number of Digits**
* **Number of Letters**
* **Number of Subdomains**
* **Entropy (Randomness Measure)**
* **Presence of 'www'**
* **Presence of 'http' and 'https'**
* **Shortening Service Detection**
* **IP Address in Hostname**

---

## ⚙️ Installation

To set up locally:

```bash
git clone https://github.com/Tareq905/Malicious-URL-Detection-Model-using-Machine-Learning.git
cd Malicious-URL-Detection-Model-using-Machine-Learning
```

Create a virtual environment (optional but recommended):

```bash
# Windows
python -m venv venv
venv\Scripts\activate

# macOS/Linux
python3 -m venv venv
source venv/bin/activate
```

Install required dependencies:

```bash
pip install pandas numpy scikit-learn xgboost lightgbm matplotlib seaborn wordcloud
```

> ⚠️ Note: The original notebook used absolute Python executable paths. In virtual environments, the standard `pip install <package>` is sufficient.

---

## 🚀 Usage

1. Launch the notebook:

```bash
jupyter notebook
```

2. Open `Malicious URL Detection.ipynb`.

3. Execute cells sequentially to:

   * Load the dataset (`malicious_phish.csv`)
   * Perform feature engineering
   * Train models (LightGBM, XGBoost, Random Forest)
   * Evaluate performance
   * Make predictions

---

## 📊 Data

The dataset used is `malicious_phish.csv`, which should be in the project root.

**Required columns:**

* `url`: The actual URL
* `type`: The label (`benign`, `malware`, `phishing`, or `defacement`)

---

## 🧪 Model Training

The notebook demonstrates training using:

* `RandomForestClassifier`
* `LGBMClassifier`
* `XGBClassifier`

The training process involves:

* Train-test split
* Feature extraction
* Model fitting
* Evaluation using:

  * Classification report
  * Confusion matrix
  * Accuracy score

---

## 🔮 Prediction

To predict new URLs, use the provided function:

```python
urls = ['titaniumcorporate.co.za', 'en.wikipedia.org/wiki/North_Dakota']
for url in urls:
     print(get_prediction_from_url(url))
```

**Expected output:**

```
MALWARE  
SAFE
```

---

## 📦 Dependencies

* Python 3.x
* pandas
* numpy
* scikit-learn
* xgboost
* lightgbm
* matplotlib
* seaborn
* wordcloud

---

## 🤝 Contributing

Contributions are welcome!
Please open an issue or submit a pull request for any suggestions, features, or fixes.

---

## 📄 License

This project is licensed under the **MIT License**.

---

## 📬 Contact

For questions or collaboration, contact:

**Md Tareq Shah Alam**
📧 [tareqshah.027@gmail.com](mailto:tareqshah.027@gmail.com)

---
