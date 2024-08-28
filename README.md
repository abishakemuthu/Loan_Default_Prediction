### Loan Default Prediction

![dataset-cover](https://github.com/user-attachments/assets/65f9ac80-3342-4be0-9af1-5ced99333c15)

### Problem Statement

In the competitive realm of financial lending, businesses grapple with diverse customer profiles. Understanding the key factors influencing loan repayment is crucial in minimizing risk and ensuring profitability. To strategically reduce loan defaults, businesses need precise insights and targeted strategies that address specific risk factors identified through data analysis.

### Business Objective

The business objective is to leverage various machine learning techniques to identify key factors influencing loan defaults. By uncovering these influential factors, the project aims to propose targeted strategies to improve the decision-making process, reduce risk, and enhance profitability for lending institutions.

### Data Collection

We have sourced the "Credit Risk Analysis" loan dataset from kaggle.

https://www.kaggle.com/datasets/rameshmehta/credit-risk-analysis

The dataset contains complete loan data for all loans issued through the year 2007 - 2015 with 73 Columns and 8.5 Lakhs Records.

### Key Variables

- Loan characteristics: Amount, Term, Interest Rate and Grade.
- Borrower Information: Income, Employment and Credit History.
- Loan Performance: Payment History and Current Status.

### Challenges

- High-dimensional data with complex relationships.
- Imbalanced classes (defaulted vs. non-defaulted loans).
- Data quality (Missing values, outliers and inconsistencies identified).
- Temporal aspects of loan performance.

### Data Cleaning

- Removed duplicate records.
- Dropped columns with >30% missing values.
- Encoded categorical variables (e.g., Term,  Grade and Verification Status, etc.)
- Standardized date formats and created derived features.

### Data Preprocessing

- One-hot encoding: Created binary features for categorical variables.
- Feature scaling: Standardized numerical features to ensure comparability.
- Handling imbalanced data: Applied SMOTE (Synthetic Minority Over-sampling Technique).
- Dimensionality reduction: Performed Principal Component Analysis (PCA).
- Feature binning: Grouped discrete numerical variables into meaningful categories.

### EDA and Feature Engineering

#### Term

![term](https://github.com/user-attachments/assets/0cfe1e1d-41dd-4f21-b81f-3bf65b77c584)

- we can infer that People who got Loan in the term of '36 months' are less prone to default compared to '60 months'.

#### Grade

![grade](https://github.com/user-attachments/assets/0f296fd5-011a-449e-ba00-9aa2ec589ff2)

- We can infer that Customers who belong to grade 'A', 'B' and 'C' are less Prone to default.
- We can also see that Grade 'A' customers defaulted the Least.
- We can see that Customers who belong to grade 'D', 'E', 'F' and 'G' are More Prone to default.

#### Employee Length

![emp_length](https://github.com/user-attachments/assets/1cf2e42b-fcb4-47d2-97cd-fa1fcf7305b2)

- We can infer that most of the Loan were given to the people who has more than 10 years of experiance.
- The people who have Experiance more than 10 years has defaulted less compared to others.

#### Home Ownership

![home_ownership](https://github.com/user-attachments/assets/1cee5747-b8e5-484a-81c4-d62c5268b78f)

- We can infer that customers who have home and customers who have mortgaged their home are less defaulted.
- Customers who live on rent are more defaulted.

#### Verification Status

![verification status](https://github.com/user-attachments/assets/3ebf2115-6645-4b25-a2b6-c193edb368c0)

- We can see that Verification Status does not have a significant impact on Loan defaulters.

#### Purpose

![purpose](https://github.com/user-attachments/assets/8bb9f2e4-afca-46c1-8651-6c780af92726)

- We can see that Credit Card and Debit Consolidation are the major Purpose for the Loan.

#### No of Deliquent

![no_of_deliquent](https://github.com/user-attachments/assets/4c44ec19-6e9b-457c-9143-4f43de620386)

- We can infer that people who tend to make late Payments are more prone to Default.

### Model Scores

![model_scores](https://github.com/user-attachments/assets/99e609be-b1af-46cc-8937-9a13e62220ff)

- We have tried various classification models with different approaches and got the best "f1 score" in XGBoost with SMOTE Analysis.

### Key Variables in Loan Default

- Outstanding Principal
- Last Payment Date
- Total Principal Received
- Recoveries
- Loan Issue Date
- Interest Rate
- Installment

### Business Insights

- Implement risk-based pricing: Adjust Interest rates based on predicted default probability.
- Enhance credit policy: Focus on key risk factors identified by the model.
- Develop early warning system: Monitor ongoing loan performance using model predictions.
- Optimize loan portfolio: Balance risk and return across different loan grades and purposes.
- Personalized loan offers: Tailor loan terms based on individual borrower risk profiles
- Clustering technique: Helps to identify delinquent cases having high risk associated with them, so that primitive steps can be initiated at early stages in order to save losses and mitigating the risk associated with such cases.
