# Predictive Analytics with Python

Author: Joel Ligma

Date: May 2020 - July 2020

**Executive Summary**

*Context*

This end-to-end machine learning project revolved around a Starbucks mobile app reward program. The goal of the project was to improve the marketing campaign effectiveness of the reward program to ultimately increase the organization’s profitability.

This goal was achieved through the creation of a comprehensive data set derived from three data sources, subsequent data analysis and lastly the development of a classification prediction model that aims to accurately predict customers with a high likelihood of completing an offer. In the context of this project, completing an offer refers to a customer receiving a promotional offer, viewing the offer, and using it to complete a purchase. The data for this project was sourced from Kaggle, collected between the years 2014 and 2018 and contained customer demographics and campaign details.

*Predictive Analytics Value for Businesses*

The value of a predictive analytics model lies in analytical results which are free of emotion and bias. The model is based on statistical algorithms which can derive future outcomes based on historical data. With the help of a prediction model a firm is provided with consistent and unbiased insights that support better decision-making.

*Results*

In summary, the data analysis findings, and the development of the classification prediction model resulted in the following insights. Out of all customers, only 40.02% completed a purchase in the past. Women tend to react more positively toward promotions since the proportion of female customers who completed an offer is higher than male customers (46.04% and 35.69%). Despite the fact that women only make up around 40% of the total customer base in dataset, the number of women who completed an offer is almost equal to the number of male customers who did the same (13,260 women and 14,254 men). When comparing the four contact methods used (email, mobile, social, web), most customers were contacted via email and mobile device. However, both contact methods showed a lower success rate (50.53% and 50.30%) of completing an offer compared to social media (54.31%) and web (56.09%). Among the three promotional offer types (discount, BOGO, informational), discounts were the most effective (66.58%). Lastly, a total of three classification models were built and tuned with the aim to predict customers with a high likelihood of completing a purchase. The final model selected for deployment was the Extreme Gradient Boosting (XGBoost) model which showed a test accuracy of 96.51%.

*Recommendations*

Finally, with the aim of improving the company's marketing campaign effectiveness, the following three recommendations were derived based on the analysis findings described above. First, Starbucks should employ the XGBoost model to identify its target customers and increasingly target women. Second, once the customers are identified, the firm should increase the usage of social media and web as communication channels to send the promotional offers due to their high success rates. Third, it is advised that the promotional offer send to target customers is customized in a way which yields the highest success rate of customers using the promotion to complete a purchase. This entails making increased use of discounts, tailoring the offer’s expiration period around 7 to 10 days, and setting the minimum purchase value between $5 to $10.  


Source: https://www.kaggle.com/blacktile/starbucks-app-customer-reward-program-data


## Table of Contents
**1) Data Preprocessing and Merging Multiple Datasets** 
- Data Cleaning
- Feature Engineering
- Merging/Concatenating/Joining
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
- Neural Network Classifier
- XGBoost Classifier
- Model Comparison
<br>

**5) Saving the Model**
- Saving the Best Performing Model for Future Deployment
<br>

**6) Conclusion**
- Business Implications and Recommendations

# Detailed Summary of Findings

In summary, the data analysis findings and the development of the classification prediction model, aiming to accurately predict customers with a high likelihood of completing an offer, resulted in the following insights described below.

**Demographics**

- Most customers are roughly aged between 40 and 75 years with an average age of around 54 years
- 41.9% female and 58.1% male customers
- Average customer income equals 65,388.01 US dollars
- Only 40.02% of customers did complete an offer in the past
- Average income of customers who did complete an offer in the past: 69,398.28 US dollars (vs. 62,711.8 US dollars of those who did not)
- Average age of customers who did complete an offer in the past: 55.8 years (vs. 53.37 years of those who did not)
- The proportion of female customers who completed an offer is higher than male customers (46.04% vs. 35.69%)
- Based on these findings, women tend to react more positively towards the promotions than men. Despite the fact that women only make up around 40% of the customers in the dataset provided, they almost contribute the same number of completed offers than men. (13,260 women vs. 14,254 men).

**Offers**

- Customers who received Discount: 31.74%
- Customers who received BOGO: 31.65%
- Customers who didn't receive an offer: 20.79%
- Customers who received Informational: 15.82%
- The offer type with the highest success rate is Discount (66.58%), followed by BOGO (59.69%)
- Informational offers cannot be traced to any sales.

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

**Predictive Model**

We built and tuned 3 classification prediction models with the goal to accurately predict our target customers. Our target customer sare defined as customers who have a high likelihood of completing an offer. The 3 models are Random Forest, Neural Network and eXtreme Gradient Boosting (XGBoost). After training and validating the model performance the following results were geneated:

- The Random Forest Classifier showed a predictive accuracy of 96.19%
- The Neural Network Classifier showed a predictive accuracy of 94.04%
- The **XBGoost** Classifier showed a predictive accuracy of **96.51%**

Based on these results, we selected XGBoost as the final classifiaction prediction model with which we managed to predict our target customers with 96.51% accuracy.

## Recommendations

In order to increase the company's marketing strategy effectiveness, we derived the following 3 recommendations based on the analysis findings above.

**1) Predicting Target Customers**

- Identify target customers using the XGBoost model

**2) Choosing the right Contact Method(s)**

Increase the usage of the following communication channel(s) to send offers:

- Web (because it showed the highest success rate among the 4 contact methods)
- Social media (because it showed the second highest success rate among the 4 contact methods)

**3) Customizing the Offer Appropriately**

- Send out more discounts because they show the highest success rate
- Keep the amount of BOGO the same because they still show a decent success rate
- Tailor the period an offer is valid around 7 - 10 days because this period showed the highest completed offers
- Avoid making offers valid for only 3 - 4 days because these offers didn't result in any completed offers

The goal is to decrease the total number of customers who did not receive an offer (20.79%) and to increase the success rate of offers sent out (currently 40.02%). This can be done by increasingly targeting female customers who match the target customer profile of customers with slightly above average income (69,398.28 US dollars) and age (55.8 years).

Following these recommendations will ensure a more efficient allocation of resources, an increase in the marketing success rate and ultimately growth in profitability for the organization.
