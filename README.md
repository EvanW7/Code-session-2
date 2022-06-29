# Code-session-2
library(ggplot2)
Titanic$Pclass = factor(Titanic$Pclass)
Titanic$Survived = factor(Titanic$Survived)
#Titanic$Sex = factor(Titanic$Sex)
#Descriptive Statistics
summary(Titanic)
str(Titanic)
ggplot(Titanic, aes(x=Pclass)) + geom_bar()
ggplot(Titanic, aes(x=Pclass, color=Sex, fill = Sex)) + geom_bar() + theme_bw() + theme(legend.position = 'top"')
# Create box plot using ggplot2
ggplot(Titanic, aes(Sex, Age)) + geom_boxplot()
ggplot(Titanic, aes(x=Pclass, y=Age, fill = Sex)) + geom_boxplot(outlier.color = "dark orange", outlier.shape = 4, notch = TRUE) + coord_flip() + theme_bw() + ggtitle("Boxplot to plot Age vs Passenger Class")
# Create histogram using ggplot2
ggplot(Titanic, aes(x=Age)) + geom_histogram(binwidth = 10)
## load in-built dataset from r mtcars
mydata = mtcars[, c(1,3,4,5,6,7)]
head(mydata)
cormat = round(cor(mydata),2)
head(cormat)
g_base = ggplot(mpg, aes(displ, hwy))
g_aes = g_base + geom_point(aes(color = drv))
library(readxl)
# Preform the one tailed t test
t.test(Dominos$Time, alternative = "less" , mu=173.62)
t.test(Dominos$Time) = "less" 
