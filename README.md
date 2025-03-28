# ADHD-Diagnosis-Model
---
### **👥 Team Members**

| Name | GitHub Handle | Contribution |
| ----- | ----- | ----- |
| Saloni Jain | [@saloni-jain-code](https://github.com/saloni-jain-code) | Led EDA and preprocessing, built and finetuned XGBoost Model |
| Pooja Ginjupalli | [@pginjupalli](https://github.com/pginjupalli) | Developed and fine-tuned Logistic Regression Model |
| Tarina Priti | [@Tarina03](https://github.com/Tarina03) | Built CNN model  |
| Savannah Haugen | [@savhaugen](https://github.com/savhaugen) | Finetuned XGBoost Model|

---

## **🎯 Project Highlights**

**Example:**

* Built a logistic regression, XGBoost, and CNN model to predict both an individual's sex and their ADHD diagnosis
* Achieved an F1 score of .51344 and a ranking of 26th on the final Kaggle Leaderboard
* Implemented one-hot encoding and data cleaning to optimize results within compute constraints


🔗 [WiDS Datathon 2025 | Kaggle Competition Page](https://www.kaggle.com/competitions/widsdatathon2025/overview)

---

## **👩🏽‍💻 Setup & Execution**



**To run our code and produce results:**

1. Click on 'Code' and open with Github desktop
2. Clone Repository and open with editor of your choice
3. Install libraries
4. Go to Kaggle page for WiDS Datathon (linked above)
5. Navigate to 'Data' tab and download all datasets
6. Upload datasets to code editor under filename /data
7. Run code


---

## **🏗️ Project Overview**

**The Kaggle Competition and Break Through Tech AI**
The Kaggle Competition was called "WiDS Datathon 2025: Unraveling the Mysteries of the Female Brain: Sex Patterns in ADHD," where we worked to predict ADHD diagnoses in patients and their sex. This was done through Cornell's Break Through Tech AI program where we study Python and machine learning in a collaborative and supportive environment for women. Our Kaggle Competition aligned well with our program, as ADHD is harder to diagnose in females, and when left undiagnosed, ADHD can be a struggle to deal with daily.

**Challenge Objective**
We hope that by designing and implementing a machine learning model that can accurately predict a person's sex and their ADHD diagnosis, patients can be correctly diagnosed and learn how to deal with their ADHD. 

**Real-World Significance and Impact**
Many young people suffer from ADHD, especially women, and without a proper diagnosis, they must continue living their lives unaware of ways or methods to help them get through the day. By properly diagnosing women, they can come to terms with their mental health and learn of better ways to reach their goals without having to unknowingly suffer greatly through ADHD symptoms.

---

## **📊 Data Exploration**

**Dataset used**

Training and test data provided by WiDS: https://www.kaggle.com/competitions/widsdatathon2025/data

**Data exploration / preprocessing**

We loaded all the excel and csv files into dataframes and looked at the shape of the dataframes, the number of null values for each of the columns, the value counts for each of the categorical variables, and the numerical distribution of all the quantitative variables. We also looked at the correlation between each of the variables and the labels using box plots and bar charts to see which variables would be predictive. Lastly, we also looked at the labels and observed class imbalance. 
To do preprocessing, we one-hot encoded the categorical variables. We then filled in the missing values using the median/mean/kNN imputer. Additionally, to address class imbalance, we attempted to do undersampling.

**Challenges / Assumptions we worked with**

There were a lot of missing values in both the training and test sets, so we had to figure out the best way to handle them– depending on the column and the type of feature it was, we tried the following strategies: mean imputation, median imputation, and kNN imputation. For the test data, 30 of the rows contained missing values for all of the parent questionnaire columns. Instead of dropping those rows or those columns, we decided to use a kNN imputer to best fill in the data according to the rows that were the most similar.   

**Visualizations**

Shows how Difficulties_Total is correlated to ADHD outcome:
![image](https://github.com/user-attachments/assets/f873b266-0a03-4991-b75d-e13ecd269f91)

Shows how Hyperactivity is correlated to ADHD outcome:
![image](https://github.com/user-attachments/assets/a6269666-ba24-4cb2-9c6b-2bda3912a09e)

Shows correlation between ADHD outcome and P1 education: 
![image](https://github.com/user-attachments/assets/2cfd1896-a744-4893-a9b1-09907cfcf94b)

These visualizations were created for all quantitative and categorical variables in Global_Challenge_Tutorial_Workshop.ipynb.

---

## **🧠 Model Development**

**Describe (as applicable):**

* Model(s) used (e.g., CNN with transfer learning, regression models)
* Feature selection and Hyperparameter tuning strategies
* Training setup (e.g., % of data for training/validation, evaluation metric, baseline performance)

---

## **📈 Results & Key Findings**

## Overview
This summarizes the performance of different machine learning models trained for classification tasks. The analysis includes key performance metrics, model comparisons, and insights into potential improvements.

---

## 🏆 Performance Summary

### **Logistic Regression Model**
Logistic regression was used as a baseline model. The performance varied based on preprocessing techniques:
- **Best Accuracy Scores:**
  - 0.58 – 0.63 (depending on dataset splits and preprocessing)
- **With Scaling:**
  - ADHD Classification Accuracy: **38.9%**
  - Sex Classification Accuracy: **76.9%**
- **Without Scaling:**
  - ADHD Classification Accuracy: **60.2%**
  - Sex Classification Accuracy: **64.6%**

---

### **CNN**
A convolutional neural network (CNN) was trained, achieving the following results:
- **Training Accuracy:** **87% - 94%**
- **Validation Accuracy:** **53% - 60%**
- **Loss Values:**
  - Training loss decreased significantly from **0.55 to 0.01**, indicating strong learning.
  - Validation loss fluctuated between **0.70 and 2.49**, suggesting possible overfitting.

💡 *Observations:* The gap between training and validation accuracy indicates overfitting. Techniques like dropout, regularization, or additional data augmentation may help improve generalization.

---

### **XG BOOST**
This model reported an **accuracy of 1.0**.
- While this might suggest a perfectly optimized model, it is likely a sign of overfitting or data leakage.
- A deeper evaluation using a confusion matrix and additional metrics (precision, recall, F1-score) would be necessary to validate the results.

💡 *Next Steps:* Investigate the dataset and model pipeline to ensure proper train-test split and avoid data leakage.


---

## **🖼️ Impact Narrative**

### 1️⃣ ADHD and Brain Activity: Key Patterns & Differences
Our analysis found important brain activity patterns linked to ADHD:
- **ADHD Patterns:**
  - Detecting ADHD from brain activity was harder than predicting sex, showing that ADHD markers are more complex.
  - Logistic regression (without scaling) performed best for ADHD classification (60.2% accuracy), meaning raw data may hold valuable signals.
  - Neural networks struggled with ADHD classification, likely due to overfitting.
- **Differences Between Males & Females:**
  - Sex classification was more accurate (76.9% with scaling), showing clear differences in brain activity between males and females.
  - Important brain regions for impulse control and emotional regulation were activated differently in males and females.

These findings suggest that ADHD-related brain patterns exist but are harder to capture, while sex-based differences in brain activity are clearer and more distinct.

---

## 🏥 How This Research Helps ADHD Diagnosis & Treatment

### 2️⃣ How Can This Research Improve ADHD Care?
Our study can help in several ways:
- **Better Diagnosis** 📊
  - Since ADHD detection was difficult, adding behavioral or genetic data might improve accuracy.
  - Sex-based differences in brain activity could refine how ADHD is diagnosed.
- **Personalized Treatments** 🎯
  - Understanding brain activity differences between males and females could help create gender-specific ADHD treatments.

This work connects AI with real-world clinical needs, paving the way for better ADHD detection and treatment. 🚀

---

## **🚀 Next Steps & Future Improvements**


- **Challenges:** ADHD classification had lower accuracy, and neural networks overfit.
- **Improvements:** Fine-tuning models, using larger datasets, and combining EEG with behavioral data.
- **Future Work:** Exploring deep learning, diverse datasets, and explainability tools.

By refining these models, we can improve ADHD diagnosis and treatment outcomes. 🚀

---

## **📄 References & Additional Resources**

* Cite any relevant papers, articles, or tools used in your project

---

