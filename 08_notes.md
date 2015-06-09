####Note
Personal notes, not meant to be accurate or understood by others

##Caret Package

```r
inTrain <- createDataPartition(y=spam$type, p=0.75, list=FALSE)
training <- spam[inTrain,]
testing <- spam[-inTrain,]
modelFit <- train(type ~.,data=training, method="glm")
predictions <- predict(modelFit,newdata=testing)
confusionMatrix(predictions,testing$type)
dummies <- dummyVars(wage ~ jobclass,data=training)
nsv <- nearZeroVar(training,saveMetrics=TRUE)
library(splines)
bsBasis <- bs(training$age,df=3) 
```
## Caret tutorials:
 * http://www.edii.uclm.es/~useR-2013/Tutorials/kuhn/user_caret_2up.pdf
 * http://cran.r-project.org/web/packages/caret/vignettes/caret.pdf
 * http://topepo.github.io/caret/training.html
 * http://topepo.github.io/caret/visualizations.html
 
## A paper introducing the caret package
        http://www.jstatsoft.org/v28/i05/paper

## Preprocessing with PCA + Prediction
```
preProc <- preProcess(training[,-c('result')]),method="pca",thresh=0.9) ## thresh=0.9 or pcaComp=2
trainPC <- predict(preProc,training[,-c('result')])
modelFit <- train(training$result ~ .,method="glm",data=trainPC)
testPC <- predict(preProc,testing[,-c('result')])
confusionMatrix(testing$result,predict(modelFit,testPC))
```
