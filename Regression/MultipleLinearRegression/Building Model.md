# Building A Model
To build a precise regression model, it is important to construct the model with selecting right variables. There are five 
methods of building models:

1. All-in
2. Backward Elimination
3. Forward Selection
4. Bidirectional Elimination
5. Score Comparison

## All-in
Put all variables in model. Suitable case: You have prior knowledge, or you have to.

## Backward Elimination
Steps:
1. Select a significance level to stay in the model (e.g. SL = 0.05)
2. Fit the full model with all possible predictors
3. Conside the predictor with the highest P-value. If P > SL, go to STEP 4, otherwise go to FIN (Final model).
4. Remove the predictor
5. Fit model without this variable (Refit model)

After STEP 5 go back to STEP 3 until the highest P-value smaller than Significance.
