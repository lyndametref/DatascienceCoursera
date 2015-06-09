####Note
Personal notes, not meant to be accurate or understood by others

#knitr
##Input a value in a text chunk
```
Some text, my variable is: `r nameofthevariable`. Some more text
```
##Cache
```{r nameofchunk, cache=TRUE}
....
```
!!!!If libraries are called in a cached chunk, they won't be loaded if the chunk is not run!!!!!
