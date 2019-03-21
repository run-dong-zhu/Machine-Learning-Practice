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
3. Conside the predictor with the highest P-value. If P > SL, go to STEP 4, otherwise go to FIN (Final model)
4. Remove the predictor
5. Fit model without this variable (Refit model)

After STEP 5 go back to STEP 3 until the highest P-value smaller than Significance Level.

## Forward Selection
Steps:
1. Select a significance level to stay in the model (e.g. SL = 0.05)
2. Fit all simple regression models y ~ Xn select the one with the lowest P-value
3. Keep this variable and fit all possible models with one extra predictor added to the one(s) you already have
4. Consider the predictor with the lowest P-value. if P < SL, go to STEP 3, otherwise go to FIN (the previous model)

After STEP 4 go back to STEP 3 until the lowest P-value greater than Significance Level.

## Bidirection Elimination
Steps:
1. Select a significance level to enter and to stay in the model. e.g. SL_ENTER = 0.05, SL_STAY = 0.05
2. Perform the next step of Forward Selection (new variables must have : P < SL_ENTER to enter)
3. Perform ALL steps of Backward Elimination (old variables must have: P < SL_STAY to stay)
4. No new variables can enter and no old variables can exit

After STEP 3 go back to STEP 2 until no new variables can enter and no old variables can exit.

## All Possible Models
Steps:
1. Select a criterion of goodness of fit (e.g. Akaike criterion)
2. Construct All Possible Regression Models: 2^n - 1 total combinations.
3. Select the one with the best criterion

Finally, your model is Ready.
