# Vectors
Vectors are the simplest data structure in R. Vector stores a collection of elements with same data type.  Like most of the modern computing languages like Matlab or Scilab, ‘colon’ operator can be used to create a vector with elements as a sequence of numbers with an interval 1. For generating sequences with custom interval seq() function can be used. 

Try 
```R
1:10
```

```R
seq(1,5, by = 0.5)
```

```R
seq(1,10, length=3)
```

A vector can be created and assigned to a variable using a simple command: 
```R
k<-c (10,20,30,40,50,60,70,80,90)
k
```

The function c() stands for concatenate/combine, but for simplicity, it can be read as create. In order to access a specific object in the vector we can use the symbol name and the index number within square brackets. In R, the index starts with 1. 
Try
```R
k[1]
k[2]
k[3]
k[-1]
k[-2]
```
You can use the rep command for creating objects with repeating numbers. To create a list with 8 repeating 100 times, you may use the following code:
```R
rep(8,100)
```
You can create a character vector or string, using the create function and write the character/strings inside double quote 

```R
s="I am a string"
```
Combining vectors
To combine two vectors try:
```R
a=c(2,4,6,8)
b=c(1,2,3,4)
combine=c(a,b)
```
Try the following
```R
a=c(1,2,3)
a+1
```
```R
b=c(4,2,7,1,5,9,2,3,4,6)
sort(b)
sort(b, decreasing = TRUE)
```

To know the data type of object that we created just type:
```R
typeof(x)
```

# b) Matrices
Matrix is a collection of objects arranged in rows and columns. R provides the function matrix () along with the create function to create a matrix. The number of rows and columns of the matrix has to be given as attribute- nrow and ncol. Try the example below:
```R
x = matrix(c(10,20,30,40,50,60,70,80,90,100), nrow=5, ncol=2)
```

The functions nrow(x) and ncol(x) will give the number of rows and columns of the matrix, x. 
To retrieve elements of a matrix, we can use the indices. For example, from the matrix x, to retrieve the element in the fourth row and first column, we can use x [4,1].
```R 
nrow(x) 
```


```R
ncol(x)
```


```R
x [4,1]
```

Lets see some more method to create a matrix
Method 2
```R
mat=cbind(c(1,2,3),c(4,5,6))
```
Method 3
```R
mat2=1:10
dim(mat2)=c(2,5)
```

cbind and rbind
You can add row or columns by using the following method
```R
rbind(mat2,c(2,3))
cbind(mat2,c(1,2,3,4,5,6))
```

c) Arrays
Arrays are yet another data structure in R. Arrays can be created using the array() function in a similar manner like matrix. Matrix can have only two dimensions- rows and columns. But arrays can have more than two dimensions. 
To create an array in R, first the data vector has to be given. Then dimension of the array has to be written in the dim attribute. Let’s see how a three dimensional array is created in R :
```R
i <- array(c(1:24), dim=c(3,4,2))
```
Factors
Factors have a particular way called as levels to represent category of elements. Levels will help user to represent the data in a compact manner. 

A factor is created using the factor() function. Even though we can create factors with numeric and character data, the levels of the factor will always be character values. Levels will be displayed automatically when we print the data elements or can be displayed using the levels() function with the symbol that stores the factor data as the argument, as below
```R
P<-factor(c(1,3,2,1,1,3,4,2,3,2,1,3,4))
```

```R
> P
 [1] 1 3 2 1 1 3 4 2 3 2 1 3 4
Levels: 1 2 3 4
> Q<-factor(c("aaa", "bbb", "ccc", "aaa", "bbb", "aaa", "ccc"))
> Q
[1] aaa bbb ccc aaa bbb aaa ccc
Levels: aaa bbb ccc
```

# Lists
List is another data structure in R which handles multiple data types with different length. For creating a list we can use list() function with the data elements or the vectors as the arguments. In the given example, the two factor data given above with different data types are stored in a single list:
```R
listdata<-list(P=c(1,3,2,1,1,3,4,2,3,2,1,4,3,4),Q=c("aaa","bbb","eee","aaa","bbb","aaa","eee","eee"))
```

Each object/vector in R will have a specific name/symbol. The data can be accessed using that name and the $ operator preceded by the list name.  Data in list can also be accessed by using the list name and the index of the particular object/ vector

# Data frame
Data frame is like a spreadsheet or table; it is most widely used for representing experimental data.  A data frame can be created using data.frame() function with arguments as the vector names that it represent. 
```R
SlNo<-c(1,2,3,4)
Name<-c("Raju", "Radha", "Mayavi", "Luttapi") 
Age<-c(18,17,20,18)
table<-data.frame(SlNo,Name,Age)
```
The Data frame will look like 
```R
> table
  SlNo    Name Age
1    1    Raju  18
2    2   Radha  17
3    3  Mayavi  20
4    4 Luttapi  18
```
Objects in a data frame can be accessed in the same manner as used for accessing list items.
Now try the following 
```R
table$Name
table[1]
```
