# 🛒 SmartCart Segmentation System

## 📌 Project Overview

SmartCart Segmentation System is an Unsupervised Machine Learning project that identifies different customer groups based on their demographic information, income, spending habits, and purchasing behavior.

The goal of this project is to help businesses understand their customers better and create personalized marketing strategies for different customer segments.

---

## 🚀 Problem Statement

Businesses often have thousands of customers with different purchasing patterns.

Treating every customer the same can reduce marketing effectiveness.

This project uses clustering techniques to divide customers into meaningful groups so that businesses can:

- Improve customer targeting
- Increase customer retention
- Optimize marketing campaigns
- Identify high-value customers

---

## 📊 Dataset Information

The dataset contains customer information such as:

- Income
- Education
- Marital Status
- Recency
- Product Spending
- Number of Purchases
- Website Visits
- Campaign Responses

Total Records: **2240 Customers**

---

## 🛠 Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn
- PCA
- K-Means Clustering
- Agglomerative Clustering
- Jupyter Notebook

---

## ⚙️ Project Workflow

### 1️⃣ Data Cleaning

- Handled missing values in Income column
- Replaced null values using Median Imputation

```python
df["Income"] = df["Income"].fillna(df["Income"].median())
```

### 2️⃣ Feature Engineering

Created new features:

#### Age

```python
Age = 2026 - Year_Birth
```

#### Customer Tenure

```python
Customer_Tenure_Days
```

#### Total Spending

```python
Total_Spending =
MntWines +
MntFruits +
MntMeatProducts +
MntFishProducts +
MntSweetProducts +
MntGoldProds
```

#### Total Children

```python
Total_Children =
Kidhome + Teenhome
```

---

### 3️⃣ Data Transformation

#### Education Simplification

| Original | Converted |
|-----------|-----------|
| Basic | Undergraduate |
| 2n Cycle | Undergraduate |
| Graduation | Graduate |
| Master | Postgraduate |
| PhD | Postgraduate |

#### Living Status Creation

| Original | Converted |
|-----------|-----------|
| Married | Partner |
| Together | Partner |
| Single | Alone |
| Divorced | Alone |
| Widow | Alone |

---

### 4️⃣ Outlier Removal

Removed unrealistic values:

```python
Age < 90
Income < 600000
```

---

### 5️⃣ Categorical Encoding

Applied One-Hot Encoding on:

- Education
- Living_With

---

### 6️⃣ Feature Scaling

Used StandardScaler to normalize features.

```python
StandardScaler()
```

This ensures all features contribute equally during clustering.

---

### 7️⃣ Dimensionality Reduction

Applied Principal Component Analysis (PCA).

```python
PCA(n_components=3)
```

Benefits:

- Reduced dimensionality
- Faster clustering
- Better visualization
- Reduced noise

---

### 8️⃣ Customer Segmentation

#### K-Means Clustering

Used Elbow Method to determine optimal number of clusters.

Result:

```python
Optimal K = 4
```

#### Agglomerative Clustering

Applied Hierarchical Clustering for comparison and final segmentation.

---

## 📈 Visualizations

### Elbow Method

Used to identify the optimal number of clusters.

### 3D PCA Projection

Visualized customer groups in three-dimensional space.

### Cluster Distribution

Used Countplot and Scatterplot to analyze cluster behavior.

---

## 🎯 Cluster Insights

### Cluster 0

- Low Income
- Low Spending
- Family Customers

### Cluster 1

- High Income
- High Spending
- Premium Customers

### Cluster 2

- Low Income
- Low Spending
- Mostly Individual Customers

### Cluster 3

- High Income
- High Spending
- High Campaign Response Rate

---

## 📌 Business Impact

This solution can help businesses:

✅ Identify premium customers

✅ Improve customer retention

✅ Design personalized campaigns

✅ Increase marketing ROI

✅ Understand customer purchasing behavior

---

## 🔮 Future Improvements

- Deploy using Streamlit
- Add real-time customer prediction
- Build interactive dashboard
- Integrate recommendation system

---

## 👨‍💻 Author

**Lalit Kumar Saraswat**

- Electrical & Electronics Engineering
- Aspiring Data Scientist / AI Engineer

GitHub:
https://github.com/lalitkumar180503

---

## ⭐ If you found this project useful, don't forget to star the repository!