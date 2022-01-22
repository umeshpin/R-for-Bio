## Regression
Regression Analysis

By regression analysis, we intend to find equation of the function which relates x and y. i.e., in case of linear regression, we will find equation of line that fits on the given data. A typical linear regression model will be of the form y= ax+b, where, ‘a’ is the slope of the line and ‘b’ is the y intercept. 

Now let us look into one typical data. The following is the data of samples collected from people of different ages and their cholesterol levels in mmol/L.

```R
age = c(19,22,25,30,35,41,46,48,50,53,57,60,64,70)
chol_level = c(4.1,4.3,4.3,4.4,4.5,4.6,4.7,4.6,5,5,5.1,5.3,5.5,5.6)
```

First, let us see how these values are distributed. For this, let us plot the values as a scatter plot. In R, type the following command to obtain the plot. 

```R
plot(age ~ chol_level, main="Age Vs Cholesterol Level")
```
From the graph itself, we can say that behavior of values is almost linear. Now we will find the regression model for the cholesterol levels and age. For this, R has a simple command- lm( ). 

For this, use the following code in R. Here we store the regression model in the variable, lm.out.

```R
lm.out=lm(chol_level ~ age)
lm.out
```

Call:
lm(formula = chol_level ~ age)

Coefficients:
(Intercept)          age 
   3.53714      0.02819 
So our regression function will be, Age= 0.02819*age[i])+3.53714
Now, Let us plot our regression line over the scatter plot.

To check all values try and compare with cholesterol level
```R
for (i in 1:14){
   print(paste(i<-(0.02819*age[i])+3.53714))
}
plot(chol_level ~ age, main="Age Vs Cholesterol Level")
abline(lm.out, col="red")
```
