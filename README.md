🍷 Red Wine Quality Dataset - Exploratory Data Analysis (EDA)
📊 Project Overview
This project performs Exploratory Data Analysis (EDA) on the Red Wine Quality Dataset. The dataset contains physicochemical properties of red wine samples and their associated quality ratings, which range from 3 to 8. The goal of the analysis is to understand the distribution, relationships, and key influencing factors on wine quality.

📁 Dataset
File: winequality-red.csv
Rows: 1599
Columns: 12

Features:
Fixed acidity

Volatile acidity

Citric acid

Residual sugar

Chlorides

Free sulfur dioxide

Total sulfur dioxide

Density

pH

Sulphates

Alcohol

Quality (target variable)

🛠️ Technologies Used
Python 🐍

Pandas 📊

Seaborn 🎨

Matplotlib 📈

Jupyter Notebook

🔍 Commands Used
📥 Data Loading & Initial Overview
python
Copy
Edit
import pandas as pd
df = pd.read_csv("winequality-red.csv")
df.head()
df.info()
df.describe()
df.shape
df.columns
df['quality'].unique()
📈 Visualizations & Insights
🔥 Correlation Heatmap
python
Copy
Edit
import seaborn as sns
sns.heatmap(df.corr(), annot=True)
📏 Enlarged Heatmap
python
Copy
Edit
import matplotlib.pyplot as plt
plt.figure(figsize=(18, 6))
sns.heatmap(df.corr(), annot=True)
📊 Quality Distribution
python
Copy
Edit
sns.countplot(x='quality', data=df)
🧪 Feature Distribution
python
Copy
Edit
for column in df.columns:
    sns.histplot(df[column], kde=True)
🍷 Alcohol Distribution
python
Copy
Edit
sns.histplot(df['alcohol'])
🔎 Key Observations
Alcohol has a moderately positive correlation with quality.

Volatile acidity has a negative correlation with quality.

Most wines have a quality rating of 5 or 6.

Several features are skewed and may require scaling or transformation for modeling.

Highly correlated pairs:

Free and total sulfur dioxide.

Fixed acidity and citric acid.

📌 Next Steps (Optional)
Feature scaling & normalization.

Outlier detection & removal.

Predictive modeling using regression/classification.

Quality classification (binary or multi-class).

📚 References
UCI Machine Learning Repository - Wine Quality Dataset

