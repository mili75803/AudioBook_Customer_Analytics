# AudioBook_Customer_Analytics - WIP
I built machine learning models to predict customer purchase behavior using an audiobook dataset. The goal was to identify users most likely to convert within the next six months, enabling targeted marketing and improving revenue.

I developed an end-to-end pipeline in Python using NumPy, Pandas, and scikit-learn. The workflow included data cleaning, feature engineering, and statistical feature selection using ANOVA F-tests (f_classif) to retain the most predictive variables (e.g., engagement metrics, purchase history, and average listening duration). I split the dataset into training, validation, and test sets to ensure unbiased evaluation.

As a baseline, I implemented a logistic regression model, then built a feedforward neural network using TensorFlow/Keras to capture non-linear relationships. The model outputs were probabilities, and I optimized classification thresholds based on business objectives (precision at top-K rather than overall accuracy).

To evaluate performance, I used accuracy, precision, lift, and a two-proportion z-test to validate that model-driven targeting significantly outperformed random selection. The neural network achieved ~81% accuracy and improved conversion rates from ~49% to ~86% in the top-ranked segment, generating measurable revenue uplift.



Dataset Size
Total records: 14,084
Total features: 11 input features + 1 target variable
Data Dictionary
Column Name	| Description	| Type
ID	| Unique customer identifier |	Integer
Book length (minutes)_overall |	Total audiobook duration purchased by the customer	| Numeric
Book length (minutes)_avg	| Average audiobook duration per purchase	| Numeric
Price_overall	| Total amount spent on audiobooks	| Numeric
Price_avg	| Average audiobook purchase price	| Numeric
Review	| Indicates whether the customer submitted a review	| Binary 
Review 10/10	| Review rating score given by the customer	| Numeric
Completion	| Fraction of audiobook completed by the customer	| Numeric
Minutes listened	| Total listening time in minutes	| Numeric
Support Request	| Number of customer support requests submitted	| Numeric
Last visited minus purchase date	| Number of days between the last platform visit and the purchase date	| Numeric
Targets	| Target variable: 1 = customer likely to purchase again within next 6 months, 0 = otherwise | binary


To do:
Upload the Tableau Figures.
