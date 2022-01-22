File Input and output-I
R provides various functions for reading and writing data to/ from files. We shall look at some commonly used read and write commands in R.

Create your text file in tab separated format and import it into R.
```R
Name	Age	Weight
Raj	12	30
Seena	24	47
Rekha	5	23
Priya	28	65
Meena	30	62
Suni	30	65
Raju	19	57
Remya	33	71
Vidya	30	60
```

Now try
```R
test<- read.table("C:/Users/Swathi/Desktop/sept06/my_test.txt", header=T)
```
Most of these arguments are common to almost all input/output commands. A brief description of the important arguments are listed in the below table.

# Cat ( )
Cat ( ) function simply exports data to the file specified. It can also be considered as concatenating the items given as input. The syntax is 
cat(…, file=”", sep=” “, append=FALSE)
See the following example:

Try 
```R
x<-c(1,2,3,4,5,6,7)
cat(x, file="/home/umesh/Desktop/new_created.txt", sep="\t")
```

Here the argument header is set to T (true) which tells that the first row of the data is column names.
Now using the function write.table( ) we can write this data into a file.
```R
write.table(data, "/home/umesh/Desktop/new_filewrote.txt", sep='\t', quote=FALSE)
```
This statement will write the dataframe in the variable in to a new file named “new”. If the file is not there in the directory, it will be created automatically with the execution of the write.table ( ) statement. sep=’\t’ indicates that the data is tab separated. 

# Reading and writing Excel spreadsheets
Spreadsheets can be read and written in two ways: either as comma separated values (CSV) or as tab-delimited files (TXT). 
For CSV files we can use the functions read.csv( ) and write.csv( ) for reading from and writing to CSV files respectively. 
```R
write.csv(sample(1:10), "samplecsv.csv")
```

This statement will create a vector of random numbers from 1 to 10 using the sample () function and write it to the file samplecsv.csv.  We can read the data in the file through the read.csv() statement below: 
```R
x<-read.csv("samplecsv.csv")
```
# For Excel File 
```R
library(readxl)
time_table <- read_excel("C:/Users/Swathi/Desktop/time table.xlsx")
View(time_table)
```
