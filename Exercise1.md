


R Project 

ggplot(RA_data, aes(RA_data$Patient)) + geom_line(aes(y= RA_data$Systolic_BP), colour="green") 
+  geom_line(aes(y= RA_data$RBC), colour="red")
+geom_line(aes(y= RA_data$Neutrophil), colour="blue")
+geom_line(aes(y= RA_data$Cholesterol), colour="red") 
+ annotate("text", x = 15, y = 25, label = "Parameters :: various of patient ")


RA3 = melt(RA_data, id = 'Patient')

Exploratory analysis 
ggplot(data = RA3, mapping = aes(x =variable, y = value, colour = variable)) +geom_line() 

Boxplot 

ggplot(RA3, aes(x=variable, y=value, fill=Patient)) + geom_boxplot() + facet_wrap(~variable, scale="free")



Regression Line
plot(RA_data4$RA_intensity ~ RA_data4$Pulse_rate, main="RA_intensity ~ Pulse_rate")
abline(RA_model, col="red")
