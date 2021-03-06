# Predicting Loan Defaults
This repository is about a structured approach to building predictive models for binary classification.


## Task Definition

- Build a machine learning model that can predict a loan default, i.e. a failure to repay a loan. 
- Use the loan data from the Lending Club: https://www.kaggle.com/wendykan/lending-club-loan-data


## Approach

Generally building any predictive model involves going along the path:
    • Understand the business problems and opportunities well.
    • Explore available data sources, extract and clean the data.
    • Select the algorithms to use for machine learning, prepare the data and train the models.
    • Evaluate the models against the held-out data.
    • Present the pros and cons to the business of the predictive model.
    • Deploy the model and monitor its performance.


## Business Understanding

We need clear answers to some of the business questions.

First, what are the business objectives?
- Most often, it's profit. However, after careful consideration other issues may come to light. Increasing profits comes through increasing the price and/or decreasing costs, improving the product features or quality, changing the product mix, starting new promotions or better utilizing sales channels. The objectives may be short- or long-term. They should take into account financial risks, better assets utilization and liabilities management, impact on employees, society, and environment. And finally, they must abide by the regulators rules.

What does "predicting loan defaults" mean for the business people?
- Limiting the losses, hence improving the bottom line, and at the same time, not impacting adversely the revenue generated by granting loans.


## Data Exploration and Cleaning
What data sources are available, and what are they like?
- Data sources are often given at the outset. Here, only one data source is used. However, frequently new data sources may be added that may significantly enhance the results. Usually, they are messy and inconsistent. So, some preliminary cleaning and standardization are required.


## Model Selection and Training

How to choose predictive models?
- The task at hand usually determines the model type. If the expected outcome is to Give or Deny the loan, then the task is for the classification models. But, if the expectation is to give a prediction about some continuous value of gain or loss, then regression-based models are called for. And, if we want to understand better how to differentiate the good vs the bad loans using the data features, then clustering methods may come in useful.

How to train the models?
- Once the models have been selected, they need to be trained. Often the data must still be preprocessed for particular models, as often they have specific requirements, eg. some models can handle categorical data, but others must have the data transformed, eg. by on-hot-encoders. A few different types of algorithms are tried in here, including Generalized Linear Models, Support Vector Machines, Random Forest Tress, Gradient Boosting Decision Trees, Deep Neural Nets. The scikit-learn library is used, as well as XGBoost, LightGBM, and Keras.


## Model Evaluation

How to evaluate the predictive models?
- At the very outset, some available data must be set aside as a held-out data and they must not be used for training. The purpose of the held-out data is to perform the final model evaluation after which the model cannot be tweaked any more lest the model gets over-fitted to the held-out data, thus skewing the evaluation results. The evaluation is usually based on metrics, such as accuracy, precision, recall, F1, ROC, PRC. However, for many business people, more business-oriented metrics, such as Expected Profit (or Gain/Loss) and Uncertainty/Risk may be a better fit.


## Business Presentation 

How to present the results to the business?
- The models and the evaluation results must be presented so that business people can make informed decisions. The important step is to go over the objectives and check how different models, or alternative options, measure up. It may happen that new findings shed a new light and new opportunities arise, and as a consequence many performed tasks/process steps need to be revisited. In any case, due to complexity and ambiguity it is always good to give a summary presentation, whereby every important aspect for the decision is explained.


## Model Deployment and Performance Monitoring

How models are deployed?
- Generally, there are 3 deployment modes: a) offline, where models make predictions in a database; b) online, where models are deployed as HTTP-services or micro-services in a cloud; c) embedded, where models are embedded in some devices. Models  can be stored in a low-level format, like Python pickle, or using only their succinct configuration, like the PMML format.

Do models need to be monitored in production?
- It's always a good idea to have safety checks and keep thing under control. There might be bugs in software, and the models may start behaving erratically. There might be new data arriving that are in some way much different than the data on which the models were trained, and as a result the models' performances may deteriorate. Also, the models' internal rules or patterns need to be adapted to ever changing external conditions.

