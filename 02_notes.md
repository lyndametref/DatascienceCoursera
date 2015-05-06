#Note
*Personal notes, not meant to be accurate or understood by others*

# Week 1

# Week 2

# Week 3
* anonymous function = function unamed (defined in the call of another function for ex)
* MARGIN= number representing the dimension (for ex 1 = row, 2=col, etc...)
* in apply the margin can be a list of number if the object on which it is applied habe more dimension. If 3 dimensions the c(1,2) represent the row and col. so the result will have the length of the depth
* mapply: apply a function on multiple list with each list being an argument to the function. Allows to vectorise a function that does not allow for a vector input.
* tapply apply function on a subset of a vector given by INDEX (Can specify a factor level for ex).
* split = tapply without applying the function. Creat a *list* with each element being the content of each factor level. ?Can select some element by droping unselected levels ?
* traceback : print call stack only in case of error 
```
>Afunction
Error...
>traceback()
```
* recover: error handler fire when an error occurs. Global R option to activate. Open function call stack and allow browsing the environnement of a given function level.
```{r}
options(error=recover)
```
#Week4

#Other
* R is a one based indexing system!
* vapply() allows you to specify the format explicitly. If the | result doesn't match the format you specify, vapply() will throw an error
* Piping a result on a function. WARNING operator must stay at the end of the line else the command line thinks the command is over.
```{r}
data <- unz("activity.zip","activity.csv") %>% 
    read.csv(as.is =TRUE,na.strings = "NA") %>% 
    tbl_df
```
