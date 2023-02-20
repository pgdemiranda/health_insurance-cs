# Health Insurance Cross-Validation
<p align="center">
  <img src="./reports/figures/1.png" />
</p>

## Overview
This is a Learning to Rank (LTR) project in which the objective is to classify and rank clients interested in purchasing vehicle insurance. The company SafeHarbor Insurance is a fictitious insurance company made up by us, in order to provide a business context for our problem. The data have been acquired in the challenge [Health Insurance Cross Sell Prediction](https://www.kaggle.com/datasets/anmolkumar/health-insurance-cross-sell-prediction) from Kaggle, We perform a exploratory data analysis, train different classification Machine Learning models, evaluate the metrics, and test their results.
#### This project was made by Pablo Miranda

# 1. Business Problem
## 1.1. Business Context
SafeHarbor Insurance is a big company that offers health insurance for an annual fee to insure its clients on a yearly basis. Their product team is developing the resources to offer vehicle insurance to SafeHarbor clients, and they already have a survey in which, their 381.109 insured clients, have indicated their willingness to purchase this new product. However, there is a new portion of clients (127.037 clients) who have subsequently purchased the SafeHarbor health insurance and it is not known if they are willing to also purchase the new vehicle insurance.
The product team needs to know how viable is to sell this vehicle insurance for the new customers, because the sales team also has a challenge: the offer of the new product will be made directly by phone calls, and they are limited to a total of 20,000 phone calls. We must therefore train a Machine Learning model that ranks and sorts the new customers according to their propensity to buy the product, so that they can be prioritized by the sales team.
## 1.2. Objectives
- Which variables are more relevant to an understanding of the conditions under which customers are interested in purchasing vehicle insurance?
- What percentage of customers interested in purchasing vehicle insurance can the sales team reach by making 20,000 phone calls?
- If the sales team's limit of phone calls is increased to 40,000, what percentage of customers interested in purchasing vehicle insurance will be contacted by the sales team?
- How many phone calls does it take for the sales team to contact 80% of the customers interested in purchasing vehicle insurance?
# 2. Business Assumptions
## 2.1. General 
The context in Kaggle brings up values in Rupees, a common term for the currency of different Southeast Asian countries. Assuming we are talking about Indian Rupees, we can perform a direct conversion of these values to American Dollars, however the value resulting from this conversion may not represent the reality of business other than Indian. This, of course, will not affect the data exploration or the construction of the Machine Learning models.
We are also assuming that the sales team has knowledge in handling the functionalities of Google Sheets.
## 2.2. Variables
- id: Unique ID for the customer.
- Gender: Gender of the customer.
- Age: Age of the customer.
- Driving_License: 	0 = Customer does not have DL, 1 = Customer already has DL.
- Region_Code: Unique code for the region of the customer.
- Previously_Insured: 1 = Customer already has Vehicle Insurance, 0 = Customer doesn't have Vehicle Insurance.
- Vehicle_Age: Age of the Vehicle.
- Vehicle_Damage: 1 = Customer got his/her vehicle damaged in the past, 0 = Customer didn't get his/her vehicle damaged in the past.
- Annual_Premium: The amount customer needs to pay as premium in the year.
- PolicySalesChannel: Anonymized Code for the channel of outreaching to the customer ie. Different Agents, Over Mail, Over Phone, In Person, etc.
- Vintage: Number of Days, Customer has been associated with the company.
- Response: 1 = Customer is interested, 0 = Customer is not interested.

For the description of these variables, we consulted the link below:
https://www.kaggle.com/datasets/anmolkumar/health-insurance-cross-sell-prediction
# 3. Solution Planning
## 3.1. Final Product
A Google Sheets file, sorting all customers by their propensity to buy the new product according to our Machine Learning Model, and that can be easily handed by the sales team.
## 3.2. Tools Used
- Python 3.9.15;
- VS Code;
- Jupyter Notebook;
- PostgreSQL;
- Git and Github;
- Render Cloud;
- Regression and Classification logarithms;
- Scikit-learn ML library;
- Flask;
- Google Sheets Apps Script.
# 4. Solution Strategy

My strategy to solve this challenge was:

**Step 01. Data Description:**

Here we will do the first exploration on the data. It would be the moment to split the data between test, train and validation sets, but there is no need to do so, because Kaggle is already available to us with the split done.
- Examine the dataset variables;
- Rename the columns to lower case;
- Check the data types; 
- Check for missing data (and what strategies should be adopted to deal with the absence of such data);
- Descriptive statistics exploration.

**Step 02. Feature Engineering:**

This is the time to inquire not only about the relationships between the features, but also to create new features that may better serve the training of our ML models.
- Questioning the relationship of the features with the help of a mindmap;
- Developing of new features.

**Step 03. Data Filtering:**

For this project there was no need to perform data filtering.

**Step 04. Exploratory Data Analysis:**

In this step univariate, bivariate and multivariate analyses of the dataset features were performed in order to generate business insights and validate the hypotheses previously raised. The insights generated here will help to select which features may be relevant for the ML models.
- Univariate analysis of each feature;
- Bivariate analysis with the purpose of validating our hypotheses;
- Multivariate analysis with the help of a heatmap;
- Evaluation of the hypothesis validations.

**Step 05. Data Preparation:**

In this step we use the scikit-learn library for data preprocessing work.
- Standardization was simple, and the StandardScaler() was applied to 'annual_premium' feature;
- Rescaling was done applying MinMaxScaler to 'age' and 'vintage' features, because we didn't have outliers;
- Encoding was done in different ways: one hot enconding to 'vehicle_age' feature, target encoding to 'gender' and 'region_code', and finally, frequency encoding was applied to 'policy_sales_channel'.

**Step 06. Feature Selection:**

The selection of the features was performed with the help of the Boruta algorithm.
- Selection with Boruta algorithm was performed with the help of the ExtraTreesClassifier model;
- Feature Importance was also considered using the feature_importances_ attribute from ExtraTreesClassifer. Then, a graph was ploted, displaying which features was ranking best, making easy for the feature selection.

**Step 07. Machine Learning Modelling:**

**Step 08. Hyperparameter Fine Tunning:**

**Step 09. Convert Model Performance to Business Values:**

**Step 10. Deploy Model to Production:**


# 5. Top 3 Data Insights

**Hypothesis 01:**

**True/False.**

**Hypothesis 02:**

**True/False.**

**Hypothesis 03:**

**True/False.**

# 6. Machine Learning Model Applied

# 7. Machine Learning Model Performance

# 8. Business Results

# 9. Conclusions

# 10. Lessons Learned

# 11. Next Steps to Improve