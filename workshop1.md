
# **Workshop 1: Introduction to Exploratory Data Analysis (EDA)** 📊

---

## **1. Introduction to EDA**
- **What is Exploratory Data Analysis (EDA)?**  
  EDA is the process of analyzing datasets to summarize their main characteristics, often using visual methods.

- **Why is EDA Essential in Data Science?**  
  EDA helps identify patterns, detect anomalies, test hypotheses, and check assumptions to inform further analysis.

- **Approaches to Perform EDA Efficiently:**  
  - Use automation tools for repetitive tasks.  
  - Leverage visualization libraries for insights.  
  - Start with simple statistics before using advanced methods.

---

## **2. Setting Up Virtual Environments**
- **Importance of Virtual Environments in VS Code for Local Development:**  
  Virtual environments, such as MiniConda or `venv`, isolate project dependencies, ensuring compatibility and reproducibility.

---

## **3. Key EDA Concepts**
1. **Data Sourcing:** Methods for collecting data from databases, APIs, and CSV files.  
2. **Data Cleaning and Handling Outliers:** Techniques to prepare data for analysis by fixing inconsistencies.  
3. **Overview of Data Types:** Understanding numerical, categorical, and mixed data types.  
4. **Types of Analysis and Statistical Methods:**  
   - Descriptive Statistics  
   - Inferential Statistics  
5. **Visualizations and Their Role in EDA:**  
   Graphical techniques (e.g., histograms, box plots) to uncover patterns and trends.

---

## **4. Practical Notebook**
- **Hands-On with Libraries:**  
  Practical exploration using libraries like **Pandas**, **NumPy**, **Matplotlib**, and **Seaborn**.
  
- **Step-by-Step Code Explanation:**  
  Detailed walkthroughs of EDA workflows, from data cleaning to visualization.

---

## **5. GitHub Repository**
**[Link to Resources](https://github.com/muhammadibrahim313/Start-Your-Data-Science-Journey)**

---

## **6. Workshop Video**
**[Watch the Workshop Video Here](https://www.facebook.com/iCodeguru/videos/637344342386776)**  

---

## **7. Handling Missing Values**

Data cleaning is crucial in EDA, especially when dealing with missing data. Below is a guide to handle missing values based on their percentage, with examples included for better understanding.

### **Breakdown of Missing Value Handling**

#### **1. If Missing Value > 60%**  
- **Rule:** Drop the column.  
- **Reason:** Features with excessive missing data often add noise and complexity.  
- **Example:**  
  A dataset has 70% missing values in the "user_comments" column. Since this column lacks sufficient information, it should be removed. Alternatively, if the column is critical, consider collecting more data or using advanced deep learning models that inherently handle missing values.

---

#### **2. If Missing Value is Between 30% and 60%**  
- **Rule:** Use advanced imputation techniques.  
- **Techniques to Use:**  
  - **KNN Imputation:** Predict missing values based on nearest neighbors.  
  - **Regression Imputation:** Predict missing values based on correlated features.  
  - **Iterative Imputation:** Use machine learning models to iteratively predict missing values.  
- **Example:**  
  For a "salary" column with 50% missing values, use regression or KNN imputation to estimate the missing salaries based on features like "job title" and "location."

---

#### **3. If Missing Value is Between 25% and 30%**  
- **Rule:** Predict the missing values using ML models or domain-specific logic.  
- **Techniques to Use:**  
  - Train a regression model using rows without missing values to predict missing ones.  
  - Use domain expertise for logical imputations.  
- **Example:**  
  If 28% of the "age" column is missing, train a regression model using other features (e.g., "education level" and "income") to predict the missing ages.

---

#### **4. If Missing Value is Between 5% and 15%**  
- **Rule:** Use statistical methods like mean, median, or mode imputation.  
- **Techniques to Use:**  
  - For numeric columns: Use the mean (if data is normally distributed) or median (if skewed).  
  - For categorical columns: Use the mode (most frequent category).  
  - **Group-based Imputation:** Impute based on grouped categories (e.g., mean salary of people in the same job role).  
- **Example:**  
  If 10% of "height" data is missing, use the median height to fill in the missing values.

---

#### **5. If Missing Value is Between 2% and 5%**  
- **Rule:** Use simple imputation (mean, median, mode, or random imputation).  
- **Techniques to Use:**  
  Same as the 5%-15% range, but with less concern about skewness.  
- **Example:**  
  If 3% of "product price" values are missing, replace them with the mean price.

---

### **Summary Table for Missing Values Handling**

| **Percentage of Missing Values** | **Recommended Action**                                           |
|----------------------------------|------------------------------------------------------------------|
| > 60%                            | Drop the column.                                                |
| 30%-60%                          | Use advanced imputation (e.g., KNN, regression).                |
| 25%-30%                          | Predict missing values using ML models or domain-specific logic.|
| 5%-15%                           | Use statistical methods (mean, median, mode).                  |
| 2%-5%                            | Use simple imputation (mean, median, mode).                    |

---

## **8. Key Statistical Terms in EDA (with Examples)**

1. **Mean (Average):**  
   - **Definition:** Sum of all values divided by the total count.  
   - **Example:** For values [2, 4, 6], the mean is (2+4+6)/3 = 4.

2. **Median:**  
   - **Definition:** Middle value of a sorted dataset.  
   - **Example:** For [1, 3, 7], the median is 3. For [2, 4, 6, 8], the median is (4+6)/2 = 5.

3. **Mode:**  
   - **Definition:** Most frequently occurring value(s) in a dataset.  
   - **Example:** For [1, 2, 2, 3], the mode is 2.

4. **Standard Deviation (SD):**  
   - **Definition:** Measures data spread from the mean.  
   - **Example:** For [2, 4, 6], SD indicates how far each value deviates from the mean (4).

5. **Variance:**  
   - **Definition:** Square of the standard deviation.  
   - **Example:** Variance quantifies data spread in the same way SD does but in squared units.

6. **Range:**  
   - **Definition:** Difference between maximum and minimum values.  
   - **Example:** For [2, 8, 10], the range is 10 - 2 = 8.

7. **Interquartile Range (IQR):**  
   - **Definition:** Spread between the 25th (Q1) and 75th (Q3) percentiles.  
   - **Example:** For data with Q1 = 10 and Q3 = 30, IQR = 30 - 10 = 20.

8. **Skewness:**  
   - **Definition:** Measures asymmetry of data distribution.  
   - **Example:** Income data typically has a positive skew due to high-income outliers.

9. **Kurtosis:**  
   - **Definition:** Measures the "tailedness" of the distribution.  
   - **Example:** High kurtosis distributions have more extreme outliers.
   - 

## **9. What are Outliers?**

Outliers are **data points that are significantly different from other observations** in a dataset. They are extreme values that deviate from the overall pattern or distribution of the data.

### **Examples:**
1. A salary of **$1,000,000** in a dataset where most salaries range from $30,000 to $80,000.
2. A test score of **10** in a dataset where the majority of scores are between 70 and 90.

---

## **5. How to Detect Outliers**

### **Statistical Methods**
1. **Z-Score Method**:
   - Measures how many standard deviations a data point is from the mean.
   - Formula:  
     \[
     Z = \frac{x - \text{mean}}{\text{std deviation}}
     \]
   - **Rule:** If \( |Z| > 3 \), the value is considered an outlier.

2. **IQR (Interquartile Range) Method**:
   - Identifies outliers based on the middle 50% of the data.
   - Steps:
     1. Calculate \( Q1 \) (25th percentile) and \( Q3 \) (75th percentile).
     2. Compute \( \text{IQR} = Q3 - Q1 \).
     3. Determine bounds:
        - Lower Bound = \( Q1 - 1.5 \times \text{IQR} \)
        - Upper Bound = \( Q3 + 1.5 \times \text{IQR} \)
     4. Any data point outside these bounds is an outlier.

---

## **6. How to Handle Outliers**

Outlier handling is an essential part of EDA. Here are some common strategies:

### **1. Remove Outliers**
   - **When to Use:** If the outliers are due to data entry errors or irrelevant to your analysis.
   - **How:** Simply drop the rows containing outliers.
   - **Example:** In a dataset of human weights, a value of **2000 kg** can be removed.

---

### **2. Cap or Winsorize Outliers**
   - **When to Use:** When you want to reduce the impact of extreme values but not remove them entirely.
   - **How:** Replace outliers with the nearest boundary value.
     - Example: Replace \( x > \text{Upper Bound} \) with \( \text{Upper Bound} \).
   - **Example:** Cap a salary of **$1,000,000** at the 95th percentile.

---

### **3. Impute Outliers**
   - **When to Use:** When the outlier represents a valid but extreme value, and you want to smooth its effect.
   - **How:** Replace outliers with statistical measures like mean, median, or mode.
   - **Example:** Replace a missing or outlier "height" with the median height of the dataset.

---

### **4. Analyze Separately**
   - **When to Use:** When outliers represent meaningful information (e.g., fraud detection, rare events).
   - **How:** Treat them as a separate dataset for specialized analysis.
   - **Example:** A dataset of credit card transactions might treat high-value outliers as potential fraudulent activity.

---

### **5. Transform the Data**
   - **When to Use:** If outliers distort the data distribution.
   - **How:** Apply transformations to reduce the effect of outliers.
     - Example: Use log transformation or square root transformation.

---

### **6. Use Robust Statistical Methods**
   - Some algorithms are resistant to outliers (e.g., median-based regression, decision trees).

---

## **7. Example in Python: Detecting Outliers with IQR**

```python
import pandas as pd

# Dataset with outliers
data = [55, 60, 62, 65, 68, 70, 72, 95, 400]
df = pd.DataFrame(data, columns=['values'])

# Calculate Q1, Q3, and IQR
Q1 = df['values'].quantile(0.25)
Q3 = df['values'].quantile(0.75)
IQR = Q3 - Q1

# Define bounds
lower_bound = Q1 - 1.5 * IQR
upper_bound = Q3 + 1.5 * IQR

# Identify outliers
df['is_outlier'] = (df['values'] < lower_bound) | (df['values'] > upper_bound)

print(df)
```

**Output:**
```
   values  is_outlier
0      55       False
1      60       False
2      62       False
3      65       False
4      68       False
5      70       False
6      72       False
7      95       False
8     400        True  <-- Outlier
```

---

### **Concise Definitions for Outlier Handling**

#### **Quantile Method**  
- Removes outliers by defining thresholds based on specific percentiles (e.g., 1st and 99th).

#### **Interquartile Range (IQR) Method**  
- Detects outliers based on the middle 50% of the data.

#### **Machine Learning (ML) Models**
- Detect complex outliers using advanced models like Isolation Forest or DBSCAN.


