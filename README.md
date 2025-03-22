# ADHD-Diagnosis-Model
# GitHub Kaggle Project README Template
---

### **👥 Team Members**

| Name | GitHub Handle | Contribution |
| ----- | ----- | ----- |
| Saloni Jain | @saloni-jain-code | Led EDA and preprocessing, finetuned XGBoost Model |
| Pooja Ginjupalli | @MelRam |  |
| Charlie Nguyen | @CharlieN |  |

---

## **🎯 Project Highlights**

**Example:**

* Built a \[insert model type\] using \[techniques used\] to solve \[Kaggle competition task\]
* Achieved an F1 score of \[insert score\] and a ranking of \[insert ranking out of participating teams\] on the final Kaggle Leaderboard
* Used \[explainability tool\] to interpret model decisions
* Implemented \[data preprocessing method\] to optimize results within compute constraints

🔗 [Equitable AI for Dermatology | Kaggle Competition Page](https://www.kaggle.com/competitions/bttai-ajl-2025/overview)
🔗 [WiDS Datathon 2025 | Kaggle Competition Page](https://www.kaggle.com/competitions/widsdatathon2025/overview)

---

## **👩🏽‍💻 Setup & Execution**

**Provide step-by-step instructions so someone else can run your code and reproduce your results. Depending on your setup, include:**

* How to clone the repository
* How to install dependencies
* How to set up the environment
* How to access the dataset(s)
* How to run the notebook or scripts

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
We loaded all the excel and csv files into dataframes and looked at the shape of the dataframes, the number of null values for each of the columns, the value counts for each of the categorical variables, and the numerical distribution of all the quantitative variables. We also looked at the correlation between each of the variables and the labels. Lastly, we also looked at the labels and observed class imbalance. 
To do preprocessing, we one-hot encoded the categorical variables. We then filled in the missing values using the median/mean/kNN imputer. Additionally, to address class imabalance, we attempted to do undersampling.

**Challenges / Assumptions we worked with**
There were a lot of missing values in both the training and test sets, so we had to figure out the best way to handle them– depending on the column and the type of feature it was, we tried the following strategies: mean imputation, median imputation, and kNN imputation. For the test data, 30 of the rows contained missing values for all of the parent questionnaire columns. Instead of dropping those rows or those columns, we decided to use a kNN imputer to best fill in the data according to the rows that were the most similar.   

**Potential visualizations to include:**

---

## **🧠 Model Development**

**Describe (as applicable):**

* Model(s) used (e.g., CNN with transfer learning, regression models)
* Feature selection and Hyperparameter tuning strategies
* Training setup (e.g., % of data for training/validation, evaluation metric, baseline performance)

---

## **📈 Results & Key Findings**

**Describe (as applicable):**

* Performance metrics (e.g., Kaggle Leaderboard score, F1-score)
* How your model performed overall
* How your model performed across different skin tones (AJL)
* Insights from evaluating model fairness (AJL)

**Potential visualizations to include:**

* Confusion matrix, precision-recall curve, feature importance plot, prediction distribution, outputs from fairness or explainability tools

---

## **🖼️ Impact Narrative**

**Answer the relevant questions below based on your competition:**

**WiDS challenge:**

1. What brain activity patterns are associated with ADHD; are they different between males and females, and, if so, how?
2. How could your work help contribute to ADHD research and/or clinical care?

**AJL challenge:**

As Dr. Randi mentioned in her challenge overview, “Through poetry, art, and storytelling, you can reach others who might not know enough to understand what’s happening with the machine learning model or data visualizations, but might still be heavily impacted by this kind of work.”
As you answer the questions below, consider using not only text, but also illustrations, annotated visualizations, poetry, or other creative techniques to make your work accessible to a wider audience.
Check out [this guide](https://drive.google.com/file/d/1kYKaVNR\_l7Abx2kebs3AdDi6TlPviC3q/view) from the Algorithmic Justice League for inspiration!

1. What steps did you take to address [model fairness](https://haas.berkeley.edu/wp-content/uploads/What-is-fairness_-EGAL2.pdf)? (e.g., leveraging data augmentation techniques to account for training dataset imbalances; using a validation set to assess model performance across different skin tones)
2. What broader impact could your work have?

---

## **🚀 Next Steps & Future Improvements**

**Address the following:**

* What are some of the limitations of your model?
* What would you do differently with more time/resources?
* What additional datasets or techniques would you explore?

---

## **📄 References & Additional Resources**

* Cite any relevant papers, articles, or tools used in your project

---

