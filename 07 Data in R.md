# Special capacities 

Lets see some of the special capabilities of R. Try
```R
library(dplyr)
1:8 %>% sum %>% sqrt
```



match function in R with vectors
```R
v1 <- c(2,5,6,3,7)
v2 <- c(15,16,7,3,2,7,5)
match(v1,v2)
```
Join in R: How to join (merge) data frames (inner, outer, left, right) in R

```R
df1 = data.frame(CustomerId = c(1:6), Product = c("Oven","Television","Mobile","WashingMachine","Lightings","Ipad"))
```
```R
df2 = data.frame(CustomerId = c(2, 4, 6, 7, 8), State = c("California","Newyork","Santiago","Texas","Indiana")) 
```

```R
df = merge(x=df1,y=df2,by="CustomerId")
```
```R
> df
  CustomerId        Product      State
1          2     Television California
2          4 WashingMachine    Newyork
3          6           Ipad   Santiago
```

outer join in R using merge() function
```R
library(dplyr)
df = merge(x=df1,y=df2,by="CustomerId",all=TRUE)
df
```


Have a look at the data frame 
```R
my_dataframe <- data.frame(Person = c("Ramesh", "Suresh"), age = c(33, 37), origin = c("Karnataka", "Tamilnadu"), height = c(178, 183))
```

The data frame is 
```R
     Person    age     origin	   height
1 	Ramesh	 33  	Karnataka    178
2 	Suresh 	 37 	Tamilnadu    183
```
Now if you need this in a diffrent form try
```R
library(reshape2)
melt(my_dataframe, id = "Person")
```
Also try
```
melt(my_dataframe, id = c("Person", "origin"))
```
