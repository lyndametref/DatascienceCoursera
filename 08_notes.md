##Carte Package

```r
inTrain <- createDataPartition(y=spam$type, p=0.75, list=FALSE)
training <- spam[inTrain,]
testing <- spam[-inTrain,]
modelFit <- train(type ~.,data=training, method="glm")
predictions <- predict(modelFit,newdata=testing)
confusionMatrix(predictions,testing$type)
```
## Caret tutorials:
 * http://www.edii.uclm.es/~useR-2013/Tutorials/kuhn/user_caret_2up.pdf
 * http://cran.r-project.org/web/packages/caret/vignettes/caret.pdf
 
## A paper introducing the caret package
        http://www.jstatsoft.org/v28/i05/paper

