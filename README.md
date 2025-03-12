# Phishing Website Detection using Machine Learning

## 📌 Overview

This project focuses on detecting phishing websites using **Machine learning models**. We implemented multiple algorithms and selected **XGBoost** as the best-performing model for real-time detection in a **Streamlit web application**.

## 🚀 Project Workflow

1. **Dataset**
- File: `urldata.csv`
- Contains **10,000 URLs** (5,000 legitimate, 5,000 phishing)
2. **Feature Extraction**:
   - Extracted **17 key features**, categorized into:
     - **Address Bar Features** (IP presence, URL length, HTTPS, etc.)
     - **Domain Features** (DNS records, domain age, web traffic, etc.)
     - **HTML & JavaScript Features** (iFrame, right-click disabling, redirection, etc.)
3. **Exploratory Data Analysis (EDA)**:
   - Analyzed dataset trends.
   - Visualized feature importance for phishing detection.
4. **Data Preprocessing**:
   - Removed duplicates and irrelevant features.
   - Split data into **training (80%)** and **testing (20%)** sets.
5. **Machine Learning Model Training**:
   - Implemented and evaluated five models:
     - **Decision Tree**
     - **Random Forest** 
     - **Multilayer Perceptrons (MLP)**
     - **XGBoost**
     - **Support Vector Machines (SVM)**

## 📂 Implementation

### **Model Training**

- Stored the trained **XGBoost model** as `XGBoostClassifier.pickle.dat`
- Users enter a URL, and the trained XGBoost model predicts if it is **legitimate or phishing**.

### Installation
1. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```
2. Run the application:
   ```bash
   streamlit run app.py
   ```
3. Access the app in your web browser at the specified URL (usually http://localhost:8501).

### **Web Application**

- Code in `app.py`
- Runs using:
  ```bash
  streamlit run app.py
  ```

## 📊 Model Performance Comparison

| ML Model                | Train Accuracy | Test Accuracy |
|-------------------------|---------------|--------------|
| Decision Tree          | 0.812         | 0.818        |
| Random Forest         | 0.818         | 0.818        |
| Multilayer Perceptrons | 0.865         | 0.863        |
| XGBoost               | 0.867         | 0.863        |
| SVM                   | 0.802         | 0.800        |


## 🔍 Key Findings

- **XGBoost outperformed all other models**, making it the best choice for phishing detection.
- **Domain-based features** (age, DNS, traffic) played a crucial role in classification.
- **Random Forest** showed competitive accuracy but required more computational resources.
- The **Streamlit web app** provides an easy-to-use interface for real-time phishing detection.


