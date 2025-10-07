# Overview

Our business problem is that SyriaTel, a telecommunications company, would like to reduce monetary losses related to customer churn, meaning losses related to customers who do not use the company's services for very long. Our goal with this project is to look for any predictable patterns we can ascertain from available data which might help pinpoint cause(s) of customer churn. Then, we will make recommendations for action SyriaTel might take to reduce customer churn based on our findings.

# Business and Data Understanding

We are working with a dataset from SyriaTel providing records for over 3,300 accounts. We have basic information like account numbers and length, and location information in state and area code. It includes some plan type information and the number of customer service calls, as well as minutes, calls and charges broken down by time of day and whether domestic or international.

Day charge, customer service calls, and international plan all seem to play a role in churn.



https://github.com/sfp13VA/SyriaTel_Customer_Churn/blob/main/images/churn_by_CScalls.jpeg


# Modeling and Evaluation

Our best model was a decision tree with a recall score of .76, meaning the model successfully identified 76% of all positive cases.

We chose recall to evaluate our models as it minimizes false negative outcomes, the least desirable outcome type for our business purposes.

Our model confirmed that charges and customer service calls were important features for churn.

https://github.com/sfp13VA/SyriaTel_Customer_Churn/blob/main/images/importance.jpeg

# Conclusion

We analyzed Syriatel's data to identify any patterns which might indicate that a customer may soon churn. We prioritized minimizing false negatives, meaning we want to avoid incorrectly predicting a customer will not churn, when in fact the customer did churn. This scenario represents the most expensive outcome, since retaining current customers is well known to be less costly than acquiring new customers. While me may mistakenly identify a customer would churn when in fact they would not have, any resources deployed to keep that customer would still serve to improve their loyalty to the company, even if it was technically a waste of resources. Losing a current customer comes at a much hugher cost to the company.
We deployed Logistic Regression and Decision Tree models on our data, finding the decision tree model to perform best by recall score.
The model helped us confirm the top factors determining customer churn: charges with day charges in particular being significant, as well as customer service calls.

## Limitations

It is difficult to account for the possibility that customer behavior was impacted by outside variables not represented in the data. SyriaTel promotions or lack thereof, or policy changes could impact customers' tendency to churn. Promotions of competitor telecom companies might impact churn as well.

## Recommendations

We would recommend a customer retention strategy which targets current customers who are heavy users of daytime minutes in particular, but one that addresses the key feature of call charges broadly. This could include personalized promotional offers like discounts on day charges which improve loyalty and therefore minimize revenue loss while still being cost effective.
Customer service quality should be evaluated for improvement since customers who made 4 or more customer service calls show higher potential to churn. Evaluate the reasons for these calls and address this key factor driving customer churn.
Make use of predictive modeling to predict churn in real time, and flag high risk customers to apply retention stategy.

## Next Steps

It would be worth collecting additional data by way of customer satisfactions surveys.
Evaluating churn by location could be worthwhile if we have time to dedicate.
