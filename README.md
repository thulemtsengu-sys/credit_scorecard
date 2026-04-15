# Credit Risk Scorecard Model
This project demonstrates the development of a credit risk scorecard using logistic regression and Weight of Evidence (WOE) transformation.
The goal is to predict the Probability of Default (PD) and translate it into an interpretable credit scorecard for decision-making.

## Key Features
- WOE (Weight of Evidence) transformation
- Information Value (IV) for feature selection
- Logistic Regression for PD modelling
- Model evaluation using AUC and KS
- Scorecard generation for business use

## Dataset
- German Credit Dataset (via scorecardpy)
- Binary target:
-  1 = Default (Bad)
- 0 =  Non-default (Good)

## Methodology
1. Data Preprocessing
- Missing value handling
- Feature binning
  
2. WOE Transformation
- WOE is used to transform variables into a form suitable for logistic regression:
WOE = ln(%Good / %Bad)

3. Information Value (IV)
- IV is used to measure predictive strength of features:
IV = Sum(%Good-%Bad) x WOE
4. Model Building
- Logistic Regression used to estimate Probability of Default (PD)

5. Model Evaluation
- AUC (ROC Curve)
- KS Statistic

6.Scorecard Generation
- Model coefficients are converted into a points-based scorecard

## Business Interpretation
- Customers with high-risk WOE profiles receive lower scores
- Scorecards allow easy decision rules (approve/decline)
