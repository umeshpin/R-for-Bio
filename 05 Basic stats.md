## Basic stats in R
R package is developed for statistical applications. It provides built-in functions for various statistical operations based on probability distributions, statistical tests, regression models, classification models, machine learning, time series analysis, resampling etc. Let us see how R supports basic statistical operations like mean, median, maxima, minima, standard deviation etc. 

# Mean
Arithmetic mean of a set of data values can be calculated simply using the function mean ( ). For example,
```R
dataset<-c(21,22,23,24,25,26,27,28,29,30)
M<-mean(dataset)
```

# Median
Median, which is the ordinal measure of the central location of the data values can be calculated using the function 
median ( ).
Example:
```R
median(dataset)
```

# Range
The function range ( ) gives the range of all the values given as input. In other words, it gives the maximum and minimum values in the given dataset. See the example given below which gives the range of the values given in the vector dataset.
Example:
```R
range(dataset)
```
Minima and maxima
The functions min ( ) and max ( ) can be used to obtain the minimum and maximum values of a set of input values.
```R
max(dataset)
min(dataset)
```
# Quantile
Quantile split the input data values. There are basically four quantiles for every input dataset. The first quantile is the value that cuts the first 25% of the given data set while second quantile cuts the first 50%, third quantile, the first 75% and fourth quantile, 100%. The function that achieves this is quantile( ). 
Example:
```R
quantile(dataset)
```


sample a normal distribution, with a mean of 5 and sd of 2, 100 times
```R
x <- rnorm(100, mean=5, sd=2)
```
sort in ascending order
```R
rand <- sample(x)
```
Rounding of Numbers of x
```R
trunc(x)
```
Set the seed of R‘s random number generator, which is useful for creating simulations or random objects that can be reproduced.
```R
set.seed(10)
rnorm(10)
```

# Variance
The function var ( ) calculates the variance of the input values. 
Example:
```R
var(dataset)
```

# Standard Deviation
Standard Deviation is the square root of variance. It is calculated using the function sd ( ). 
Example:
```R
sd(dataset)
```
[1] 3.02765

# Correlation Coefficient
This property measures how two variables are co-related.  Its value varies from -1 to +1. The function cor ( ) computes the correlation between two values.
Example:
```R
dataset1<-c(21,22,23,24,25,26,27,28,29,30)
dataset2<-c(0.1,0.2,0.3,0.4,0.5,0.6,0.7,0.8,0.9,1.1)
cor(dataset,dataset2)
```

# Covariance
Covariance tells how two variables are varying together. The function cov ( ) is used to find out the covariance in R.
Example:
```R
cov(dataset1,dataset2)
```

In addition to all these specific statistical functions, the function summary ( ) will provide us with all the most basic statistical properties. See the example below:
```R
summary(dataset)
```

