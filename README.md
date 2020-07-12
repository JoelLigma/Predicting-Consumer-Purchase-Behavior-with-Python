# Predicting Customer Behavior with Python

Author: Joel Ligma

Date: July 2020

**Context**

This project revolves around a Starbucks App Reward Program. The goal of the project is to increase the marketing promotion effectiveness. This is achieved through data analysis and the development of a classifiaction prediction model that aims to accurately predict customers with a high likelihood of completing an offer. In the context of this project, completing an offer refers to to customer receiving a promotional offer, viewing the offer and using it to perform a purchase.

## Table of Contents
**1) Preprocessing and Combining Multiple Datasets** 
- Data Clearning
- Feature Engineering
- Merging, Concatenating, Joining
<br>

**2) Exploratory Data Analysis (EDA)**
- Summary Statistics
- Univariate Analysis
- Bivariate Analysis
<br>

**3) Data Preparation**
- Feature Correlation
- Dummy Coding
- Training, Validation and Test Split
- Scaling Data
<br>

**4) Model Building & Validation**
- Baseline Accuracy
- Random Forest Classifier
- Random Forest Classifier with Grid Search and Addressing Class Imbalance
- Neural Network Classifier
- Neural Network Classifier with Grid Search and Addressing Class Imbalance
- XGBoost Classifier
- XGBoost Classifier with Grid Search and Addressing Class Imbalance
- Model Comparison
<br>

**5) Saving the Model**
- Saving the Best Performing Model for Future Deployment
<br>

**6) Conclusion**
- Business Implications and Recommendations

# Executive Summary of Findings

**Demographics**

- Most customers are roughly aged between 40 and 75 years with an average age of around 54 years
- 41.9% female and 58.1% male customers
- Average customer income equals 65,388.01 US dollars
- Only 40.02% of customers did complete an offer in the past
- Average income of customers who did complete an offer in the past: 69,398.28 US dollars (vs. 62,711.8 US dollars of those who did not)
- Average age of customers who did complete an offer in the past: 55.8 years (vs. 53.37 years of those who did not)
- The proportion of female customers who completed an offer is higher than male customers (46.04% vs. 35.69%)
- Based on these findings, women tend to react more positively towards the promotions than men. Despite the fact that women only make up around 40% of the customers in the dataset provided, they almost contribute the same number of completed offers than men. (13,260 women vs. 14.254 men).

**Offers**

- Customers who received Discount: 31.74%
- Customers who received BOGO: 31.65%
- Customers who didn't receive an offer: 20.79%
- Customers who received Informational: 15.82%

The offer type with the highest success rate is Discount (66.58%), followed by BOGO (59.69%)

Informational offers can not be traced to any sales.
Generally, discounts show the highest success rate among the 3 offer types and are also the most frequent promotion sent to customers. Furthermore, out of all offers sent out to customers, informational promotions make up approx. 15% of offers. 20.79% of customers did not receive any promotion.

In terms of difficulty and duration, one can infer that a difficulty level of 10 USD leads to the most completed offers, followed by a level of 5 USD. Further, most offers were completed for promotions that were only valid for 7 days, followed by 10 days and 5 days respectively. No offers were completed for offers that are only valid for 3 or 4 days.

**Contact Methods**

When comparing the 4 contact methods used (email, mobile, social, web), most customers were contacted via email and mobile device. However, both of these contact methods showed a lower success rate of customers completing an offer compared to social media and web.

- Customers contacted via email: 79.21%
- Customers contacted via mobile device: 71.2%
- Customers contacted via web: 63.33%
- Customers contacted via social media: 47.48%

- Web success rate: 56.09%
- Social media success rate: 54.31%
- Email success rate: 50.53%
- Mobile success rate: 50.3%
- Predictive Model

We built and tuned 3 classifiaction prediction models with the goal to accurately predict our target customers. Our target customer sare defined as customers who have a high likelihood of completing an offer. The 3 models are Random Forest, Neural Network and eXtreme Gradient Boosting (XGBoost). After training and validating the model performance the following results were geneated:

- The Random Forest Classifier showed a predictive accuracy of 87.88%
- The Neural Network Classifier showed a predictive accuracy of 86.29%
- The **XBGoost** Classifier showed a predictive accuracy of **88.65%**
Based on these results, we selected XGBoost as the final classifiaction prediction model with which we managed to predict our target customers with approximately 88.65% accuracy.

**Recommendations**
In order to increase the company's marketing strategy effectiveness, we derived the following 3 recommendations based on the analysis findings above.

1) Predicting Target Customers
- Identify target customers using the XGBoost model

2) Choosing the right Contact Method(s)

Increase the usage of the following communication channel(s) to send offers:

- Web (because it showed the highest success rate among the 4 contact methods)
- Social media (because it showed the second highest success rate among the 4 contact methods)

3) Customizing the Offer Appropriately

- Send out more discounts beacuse they show the highest success rate
- Keep the amount of BOGO the same beacuse they still show a decent success rate
- Tailor the period an offer is valid around 7 - 10 days because this period showed the highest completed offers
- Avoid making offers valid for only 3 - 4 days because these offers didn't result in any completed offers

The goal is to decrease the total number of customers who did not receive an offer (20.79%) and to increase the success rate of offers sent out (currently 40.02%). This can be done by increasingly targeting female customers who match the target customer profile of customers with slightly above average income (69,398.28 US dollars) and age (55.8 years).

Following these recommendations will ensure a more efficient allocation of resources, an increase in the marketing success rate and ultimately growth in profitability for the organization.
