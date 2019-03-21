# Dummy Variable
Using categorical data in Multiple Regression Models is a powerful method to include non-numeric data types 
into a regression model.
<br />
For example, use "0" represents "Female" and "1" represents "Male", and vice-versa.
<br />
Linear Model: y ~ b + {0|1} male + {0|1} female

### What is dummy variable trap?
The Dummy Variable trap is a scenario in which the independent variables are multicollinear - a scenario in which 
two or more variables are highly correlated. In simple terms one variable can be predicted from the others. 
<br />
For instance, as mentioned above, we create a regression mode y ~ b0 + b1 * D1 + b2 * D2, which D1: {0|1} male and 
D2: {0|1} female. However D2 = 1 - D1. So  the model will be:
<br />
**y ~ b0 + b1 * D1 + b2 * (1 - D1)**
<br />
Thus the model is nothing related with D2, which means we don't need D2.

### Solution
The solution to the dummy variable trap is to drop one of the categorical variables (or alternatively, drop the 
intercept constant) - if there are m number of categories, use m-1 in the model, the value left out can be thought 
of as the reference value and the fit values of the remaining categories represent the change from this reference.

### Reference
https://www.algosome.com/articles/dummy-variable-trap-regression.html
