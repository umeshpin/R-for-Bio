# Plotting with ggplot
Apart from the R's plot() function, ggplot2 allows you to create more complex graphs and plots. ggplot2 allows composing a set of independent components- such as scales and layers, in different ways to get variety of graphs.
To make ggplot2 available for our application, first install the package and load it into the R environment: (If you are using RStudio, use GUI to do this as in the figure given below)

If you are comfortable with commands, type:

```R
install.packages("ggplot2")
library(ggplot2)
```
A typical ggplot() function takes two  primary arguments – data and aes. “data” indicates the data frame contacting the data that is to be plotted and aes itself is like a function to pass arguments to the plot. 
Now let us try ggplot ( ) with an example.
The distinctive feature of the ggplot2 framework is the way you make plots through adding ‘layers’. The process of making any ggplot is as follows.

```R
x=1:10
y=seq(1,5.5, by=0.5)
df=data.frame(x,y)
```
Now lets plot the first simple plot by using ggplot 
```R
ggplot(df, aes(x,y))+geom_line()
```
Lets plot as points (dots)
```R
ggplot(df, aes(x,y))+geom_point()
```
See more custumizarion
```R
ggplot(df, aes(x,y))+geom_point(alpha = 0.1, color = "blue")
```
Add a theme 
```R
ggplot(data=df, aes(x,y))+geom_point(alpha = 0.5, color = "blue")+theme_light()
```
Lest add some labels
```R
ggplot(data=df, aes(x,y))+geom_point(alpha = 0.5, color = "blue")+theme_light()+labs(title="This is a trial", x="somme value", y="y-value")
```
