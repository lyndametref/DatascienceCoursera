#04 Exploratory Data Analysis
####Note
Personal notes, not meant to be accurate or understood by others

##Copy plot window to file
```
dev.copy(png, file = "geyserplot.png")  ## Copy my plot to a PNG file
dev.off()
```
WARNING when scaling to copy, placement of legend can be modified (remember exercise week 1)

## ggplot plot limits
```{r}
testdat <- data.frame(x = 1:100, y = rnorm(100))
testdat[50,2] <- 100  ## Outlier!
g <- ggplot(testdat, aes(x = x, y = y))
```
Outliers are not plotted (~hole)
```{r}
g + geom_line() + ylim(-3, 3)
```
Outlier are drawn
```{r}
g + geom_line() + coord_cartesian(ylim = c(-3, 3))
```
