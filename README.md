# OngoBoost_Insight_Project

As a part of the Insight Data Science fellowship, I consulted for a fitness app manufacturer to build a gradient-boosted classifier to predict the probability of customers subscribing to their app, which was built from 4+ data sources (including AppleHealthKit) with 27M+ observations (>10GB).

When a customer joins the app, they can sync their historic data from 3rd party integration such as AppleHealthKit or FitBit. By segmenting those users who sync their historic data, the fitness app manufacturer will have the insights to send personalized fitness recommendations from the start of the customer onboarding experience (prior to collecting a single observation within the fitness platform itself). Building on these segments, the fitness app manufacturer isolates the meaningful data from the user’s historic fitness behavior and couples it with their behavior in the fitness platform to predict conversion rate to the paid subscription model.



## Overall steps in the project:
1. Third-party integration and in-app behavior analysis, which required a massive amount of data cleaning, data wrangling, data aggregation based on each individual, and feature engineering. Packages used: python, pandas, postgreSQL, pySpark, and AWS.

2. Customer segmentation of those who synced their historic data to the fitness app. Packages used: Scikit-learn.

3. Created a classification model to decipher which features are essential for assigning an individual to a particular cluster. Packages used: Scikit-learn.

4. Coupling previous findings with the user’s in-app behavior to predict subscription rate. Subscription data was highly imbalanced (Unpaid customers: 93, Paid subscribers: 7), so SMOTE and ADASYN were used to balance the training data. Additional subscriber data was added to improve the gradient-boosted trees to a precision of 78 and recall of 81.

For further information on the data analysis pipeline that I built, please check out these 
[Slides](https://docs.google.com/presentation/d/e/2PACX-1vRZfuQaQSz6L5F23l_E6SmhuNUJLGYOUdL4QYtwPplWfnhijze0ZteVXZkx8jWhD2BxJGn6WznXY_co/embed?start=false&loop=false&delayms=3000)




## The outcome of the project:
An interactive web app [link](https://ongoboost.herokuapp.com) was built using Streamlit and Heroku to predict the subscription conversion probability for the new customers. Corporate decision-makers can use the provided slider bar in the web app to select a range of customers that have the highest probability to subscribe. Several benefits of identifying and isolating customers on the fence:

1. This information will facilitate targeted marketing, such as offering discounts only to customers that have the highest probability to subscribe and not losing money by providing discounts randomly to a customer who might have a way low likelihood to subscribe. 

2. Identifying customers with no to low subscription probability. Sending a discount code could be considered as spam and rather alienate these customers, causing them to quit the platform and Ongo will lose the entire lifetime value of these customers.

3. Lift is a metric that the subscription industry aims to increase. Lift generally suggests how much more subscribers a company can get by targeting customers with the highest likelihood to subscribe.
By selecting the top 10% of the customers with the highest likelihood to subscribe, Ongo can achieve a 5x lift, and targeting the top 20% will generate a 3.21x lift. 

I hope you enjoy the project as much as I enjoyed building it!



[Slides](<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vRZfuQaQSz6L5F23l_E6SmhuNUJLGYOUdL4QYtwPplWfnhijze0ZteVXZkx8jWhD2BxJGn6WznXY_co/embed?start=false&loop=false&delayms=3000" frameborder="0" width="480" height="329" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>)""",unsafe_allow_html=True)


[Slides]("""https://docs.google.com/presentation/d/e/2PACX-1vRZfuQaQSz6L5F23l_E6SmhuNUJLGYOUdL4QYtwPplWfnhijze0ZteVXZkx8jWhD2BxJGn6WznXY_co/pub?start=false&loop=false&delayms=3000""",unsafe_allow_html=True)



