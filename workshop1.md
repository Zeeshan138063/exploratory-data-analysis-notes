
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
**[Link to Workshop #1 Resources](#)**

---

## **6. Workshop Video**
**[Watch the Workshop Video Here](https://example.com)**  

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
