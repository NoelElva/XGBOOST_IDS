# XGBoost Classification on Network Intrusion Dataset

This project implements a machine learning pipeline for multi-class classification using XGBoost on the **Friday-WorkingHours-Afternoon-DDos.pcap\_ISCX.csv** dataset from the CICIDS2017 dataset. The focus is on identifying different types of network intrusions, including DDoS attacks.

## 📋 Features

* Data cleaning and preprocessing
* Label encoding and downsampling
* Feature selection using variance threshold
* Train-test split and 5-fold stratified cross-validation
* Classification using XGBoost
* Performance evaluation with accuracy, confusion matrix, and classification report
* Feature importance visualization

---

## 🧪 Requirements

Install the required packages before running the script:

```bash
pip install pandas numpy scikit-learn xgboost matplotlib
```

---

## 📁 Dataset

The dataset used is:

**`Friday-WorkingHours-Afternoon-DDos.pcap_ISCX.csv`**

Place this file in the same directory as the script or update the `pd.read_csv()` path accordingly.

---

## 🚀 How It Works

1. **Load and Clean Data**

   * Reads the CSV dataset.
   * Cleans column names and handles NaN/infinite values.

2. **Label Filtering and Sampling**

   * Retains the top 4 most frequent classes (including `BENIGN`).
   * Uniformly samples 3,000 instances per class to ensure class balance.

3. **Preprocessing**

   * Encodes target labels to integers.
   * Applies variance threshold to remove near-zero variance features.

4. **Modeling**

   * Splits the data into training and testing sets (80/20 stratified).
   * Trains an `XGBClassifier` model with 5-fold stratified cross-validation.
   * Reports cross-validation accuracy.

5. **Evaluation**

   * Generates predictions on the test set.
   * Outputs a detailed classification report and confusion matrix.
   * Visualizes the top 10 most important features used by XGBoost.

---

## 📊 Outputs

* **Cross-validation accuracy scores**
* **Classification Report** (precision, recall, F1-score for each class)
* **Confusion Matrix**
* **Feature Importance Plot**

---


## 📌 Notes

* Be cautious about data leakage and test/train split when extending this project.
* You can further enhance this model with techniques like hyperparameter tuning, SMOTE, or deep learning.

---

## 📧 Contact

For questions or suggestions, feel free to open an issue or reach out!

---

