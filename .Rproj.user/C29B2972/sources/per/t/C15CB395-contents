library(dplyr)
library(earth)
data(etitanic)
summary(etitanic)
?etitanic
#1.How many male passengers were on the Titanic? Female passengers? Please show the R code.
glimpse(etitanic)
table(etitanic$sex)
#2.What was the survival rate for male passengers? Female passengers? Please show the R code
ServeR <- table(etitanic$survived, etitanic$sex)
prop.table(ServeR)
#3.Visualize survival rates by gender. Please show the R code.
barplot(ServeR)
#4.Run the following code in RStudio:
set.seed(123)
train.index <- sample(1:nrow(etitanic), size=0.7*nrow(etitanic))
train.data <- etitanic[train.index,]
test.data <- etitanic[-train.index,]
### Two Competing Models
mod.1 <- glm(survived ~ ., data=train.data, family=binomial)
mod.2 <- glm(survived ~ sex, data=train.data, family=binomial)

#The above are two competing models, without any test data can you comment on which model is
#better? Use model params/output metrics to support.