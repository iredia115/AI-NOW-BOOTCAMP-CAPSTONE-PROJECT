# AI-NOW-BOOTCAMP-CAPSTONE-PROJECT
Predicting building insurance claims using machine learning

## Project Overview
This project builds a machine learning model to predict the probability that a building will experience at least one insurance claim during its insured period.

## Target Variable
- Claim = 1 → At least one claim occurred
- Claim = 0 → No claim occurred

## My Workflow
- I broke this project down into five main phases:

- Exploration & Cleaning: I dug into the raw data to handle messy entries. For example, the NumberOfWindows column was being read as text due to some >=10 values—I cleaned these and turned them into usable numbers.

- Smart Imputation: Instead of throwing away rows with missing values, I filled in the blanks using the median for numbers and the mode for categories. This kept my dataset robust without skewing the trends.

- Visual Insights (EDA): I spent time visualising the data to see the "story" it was telling. The most obvious takeaway? Larger buildings and specific locations have a much higher probability of claims.

- Multi-Model Testing: I didn't just stick to one algorithm. I trained Logistic Regression, Random Forest, and Gradient Boosting to see which one could best navigate the complexity of the data.

- Performance Evaluation: Since claims are relatively rare (imbalanced data), I used ROC-AUC as my primary metric. It gave me a much clearer picture of how well the model actually separates high-risk buildings from low-risk ones.

## What the Data Taught Me
After training the models, I looked at the "Feature Importance" to see what really drives claims.

Building Size: As expected, larger buildings are more likely to have claims.

Location (Geo_Code): Where the building is situated is a massive factor, likely due to regional risks.

Age/Occupancy: Older buildings or those with specific occupancy dates showed distinct risk patterns.

## The Results
The Gradient Boosting model was the winner, achieving an AUC score of 0.6953. This tells us the model is significantly better than random guessing at identifying buildings that will eventually file a claim.

## Files in This Repository
- CAPSTONE_PROJECT.ipynb: Main analysis notebook
- Train_data.csv: Training dataset
- Variable Description.csv: Feature definitions

## Tools & Libraries
- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn
