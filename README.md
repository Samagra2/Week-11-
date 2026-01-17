# Customer Segmentation & Churn Prediction

## 📌 Project Overview
This project performs **customer segmentation using clustering techniques** and builds **segment-specific churn prediction models** to generate **actionable business recommendations**.  
By combining unsupervised learning (clustering) and supervised learning (classification), the project demonstrates how businesses can tailor strategies for different customer groups.

---

## 🎯 Objectives
- Segment customers using multiple clustering algorithms
- Analyze and profile each customer segment
- Build **separate churn prediction models for each segment**
- Optimize models using **hyperparameter tuning**
- Provide **business-driven insights and recommendations**

---

## 🛠️ Technologies Used
- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn
- Google Colab / Jupyter Notebook

---

## 📊 Dataset Information
- **File:** `customer_churn.csv`
- **Rows:** 500
- **Target Variable:** `Churn`
- **Features:** Demographics, service usage, contract details

---

## 🧠 Methodology

### 1️⃣ Data Preprocessing
- Removed non-predictive identifiers (CustomerID)
- Converted churn labels to binary
- One-hot encoded categorical features
- Scaled numerical features where required

---

### 2️⃣ Customer Segmentation
Implemented **three clustering algorithms**:
- **K-Means** (Elbow Method used for optimal clusters)
- **Hierarchical Clustering**
- **DBSCAN**

Final segmentation was based on **K-Means clustering**.

---

### 3️⃣ Segment Profiling
For each segment:
- Calculated numerical feature means
- Computed churn rate per segment
- Assigned intuitive business-friendly segment names:
  - Premium Spenders
  - Budget Conscious
  - Young Professionals

---

### 4️⃣ Segment-wise Prediction Models
- Built **separate Random Forest models for each segment**
- Used stratified train-test split
- Addressed class imbalance using `class_weight='balanced'`

---

### 5️⃣ Model Evaluation
Metrics calculated per segment:
- Accuracy
- Precision
- Recall
- F1-Score
- ROC-AUC

---

### 6️⃣ Hyperparameter Tuning
- Applied **GridSearchCV** independently for each segment
- Tuned:
  - `n_estimators`
  - `max_depth`
  - `min_samples_split`

---

### 7️⃣ Business Insights
Developed **segment-specific strategies**, such as:
- Loyalty programs for high-value customers
- Discount-based retention for price-sensitive users
- Digital-first engagement for young professionals

---

## 📁 Project Structure
├── customer_segmentation.ipynb
├── customer_churn.csv
├── model_evaluation_results.csv
├── segment_profiles.md
├── business_recommendations.pdf
├── README.md
├── requirements.txt

---

## ▶️ How to Run the Project

1. Clone the repository:
```bash
git clone <repository-url>
pip install -r requirements.txt
