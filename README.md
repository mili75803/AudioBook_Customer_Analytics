# AudioBook_Customer_Analytics - WIP
**Overview**
This project develops an end-to-end machine learning pipeline to predict which customers are most likely to purchase an audiobook subscription within the next six months. A baseline linear classification model, logistic regression, used for comparison and a fully connected feedforward neural network implemented using TensorFlow/Keras to capture non-linear relationships. The model outputs probabilities, and the classification thresholds are optimized based on business objectives (precision at top-K rather than overall accuracy). The predictive model is then evaluated through an offline A/B testing framework to quantify its business impact compared with a random marketing strategy. The project demonstrates how machine learning can improve customer targeting by increasing conversion rates, revenue, and profit while maintaining the same marketing budget.

**Objectives**
* Predict future audiobook purchasers using customer behavioral data.
* Compare Logistic Regression and Neural Network classifiers.
* Evaluate business performance using offline A/B testing.
* Build interactive Tableau dashboards for model evaluation and business insights.

**Dataset**
The dataset contains customer demographic and behavioral information collected from an audiobook platform.
- Target Variable
0 → Customer did not purchase within six months
1 → Customer purchased within six months

* Total records: 14,084
* Total features: 11 input features + 1 target variable
Data Dictionary
* Features	| Description	| Type
* ID	| Unique customer identifier |	Integer
* Book length (minutes)_overall |	Total audiobook duration purchased by the customer	| Numeric
* Book length (minutes)_avg	| Average audiobook duration per purchase	| Numeric
* Price_overall	| Total amount spent on audiobooks	| Numeric
* Price_avg	| Average audiobook purchase price	| Numeric
* Review	| Indicates whether the customer submitted a review	| Binary 
* Review 10/10	| Review rating score given by the customer	| Numeric
* Completion	| Fraction of audiobook completed by the customer	| Numeric
* Minutes listened	| Total listening time in minutes	| Numeric
* Support Request	| Number of customer support requests submitted	| Numeric
* Last visited minus purchase date	| Number of days between the last platform visit and the purchase date	| Numeric
* Targets	| Target variable: 1 = customer likely to purchase again within next 6 months, 0 = otherwise | binary

**Project Workflow:**
Data Collection -> Data Cleaning & Preprocessing -> Feature Selection -> Model Training ( Logistic Regression, Neural Network) -> Model Evaluation -> Offline A/B Testing -> Business Impact Analysis -> Interactive Tableau Dashboard
                                                                         
**Model Evaluation Metrics**
Accuracy, Precision, Recall, F1 Score, Precision@TopK, Lift@TopK, Confusion Matrix

**Offline A/B Testing**
To estimate real-world business value, the trained neural network was compared against a random targeting strategy.

Control Group: Randomly selected customers.
Treatment Group: Customers ranked by predicted purchase probability from the neural network.

**Business Metrics**
Number of targeted users, Number of conversions, Conversion rate, Revenue, Marketing cost, Profit, Absolute lift, Relative lift, Incremental profit

**Results**
* NN outperformed LR overall: NN achieved 79.7% accuracy, 66.3% recall, and higher F1, while LR had slightly higher precision (89.9% vs. 87.0%).
* At the top 10% target group, NN achieved 100% conversion versus 46% for random targeting.
* At 50% targeting, NN generated $3,825 revenue and $3,490 profit, compared with $2,220 revenue and $1,885 profit for random targeting.
* NN delivered up to $1,605 incremental profit with the same marketing cost.
* All targeting improvements were statistically significant (p < 0.001).

**Dashboard**
Tableau dashboard link: https://public.tableau.com/views/Audiobook_Customer_analysis/ModelMetricsComparison?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link
