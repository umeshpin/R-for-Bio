You can just enter your simple mathematical computation now. When you press ‘enter’ after the expression in console, the interpreter returns the result preceded by ‘[1]’. Any element that we enter into the R console is considered as a vector and this ‘[1]’ in the output indicates the index of the first element in the output row. 
For example, type 3+9/3-2 in R window
```R
3+9/3-2
```



R stores information on objects. The simplest objects are scalars, you can assign values to the variables by using "<-" assignment operator 
```R
x<- 5
```
```R
> x
[1]  5
```
We can create and reuse the object for our future use as in any programming language.
```R
x <- 5
>  y <- 6
>  z <- x+y
[1]  11
```
we can see objects which we have created by typing "ls()" 
```R
> ls()
[1] "x" "y" "z" 
```
Lets us have a look into other objects- vectors and matrices,lists and data frames that is being used in R. 
Setwd and getwd
You can find your working directory by running the getwd (get working directory) function
To change your working directory, use setwd and specify the path to the desired folder.
```R
getwd()
setwd(dir)
```
