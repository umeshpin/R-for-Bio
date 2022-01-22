# RA and Physioco chemical parameter 


```R
ggplot(RA_data, aes(RA_data$Patient)) 
+geom_line(aes(y= RA_data$Systolic_BP), colour="green") 
+geom_line(aes(y= RA_data$RBC), colour="red")
+geom_line(aes(y= RA_data$Neutrophil), colour="blue")
+geom_line(aes(y= RA_data$Cholesterol), colour="red") 
+ annotate("text", x = 15, y = 25, label = "Parameters :: various of patient ")
```
