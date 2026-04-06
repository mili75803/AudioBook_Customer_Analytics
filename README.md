# AudioBook_Customer_Analytics - WIP
I built a machine learning model to predict customer purchase behavior using an audiobook dataset. The goal was to identify users most likely to convert within the next six months, enabling targeted marketing and improving revenue.

I developed an end-to-end pipeline in Python using NumPy, Pandas, and scikit-learn. The workflow included data cleaning, feature engineering, and statistical feature selection using ANOVA F-tests (f_classif) to retain the most predictive variables (e.g., engagement metrics, purchase history, and average listening duration). I split the dataset into training, validation, and test sets to ensure unbiased evaluation.

As a baseline, I implemented a logistic regression model, then built a feedforward neural network using TensorFlow/Keras to capture non-linear relationships. The model outputs were probabilities, and I optimized classification thresholds based on business objectives (precision at top-K rather than overall accuracy).

To evaluate performance, I used accuracy, precision, lift, and a two-proportion z-test to validate that model-driven targeting significantly outperformed random selection. The neural network achieved ~81% accuracy and improved conversion rates from ~49% to ~86% in the top-ranked segment, generating measurable revenue uplift.

To do:
Upload the Tableau Figures.
