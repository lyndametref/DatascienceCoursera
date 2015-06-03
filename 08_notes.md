##Carte Package

```r
inTrain <- createDataPartition(y=spam$type, p=0.75, list=FALSE)
training <- spam[inTrain,]
testing <- spam[-inTrain,]
modelFit <- train(type ~.,data=training, method="glm")
predictions <- predict(modelFit,newdata=testing)
confusionMatrix(predictions,testing$type)
```
