#Note
*Personal notes, not meant to be accurate or understood by others*

#dplyr
##Group by
Group ```data``` by ```date```
```{r}
data <- group_by(data,date)
```
## Summarise
```{r}
DailyTotal<-summarize(data, sum=sum(steps,na.rm = TRUE))
```
#Other
* Read a defined number of entry in csv (or other table)
```
read.csv('file.csv',skip=5,nrows=190,header=F,stringsAsFactors=F)
```
nrow=how many lines to read

* transforme a dataframe column to factor
```
data[,'foo']<-as.factor(data[,'foo'])
```

* Renaming levels of a factor
```
x <- factor(c("alpha","beta","gamma","alpha","beta"))
levels(x) <- list(A="alpha", B="beta", C="gamma")
```

* summarize each column by group: summarise_each (dplyr)

#Download from URL
```
fileUrl <- "https://data.baltimorecity.gov/api/views/dz54-2aru/rows.csv?accessType=DOWNLOAD"
download.file(fileUrl, destfile = "./data/cameras.csv", method = "curl")
list.files("./data")
```
## Same function name in different packages
*IF plyr IS LOADED BEFORE dplyr summarize() AND group_by() MIGHT NOT WORK PROPERLY*
http://stackoverflow.com/questions/26923862/group-by-summarize-in-in-dplyr-package

# Index names
```
index(foo)
```
To get the index in a variable. Good to get dates/times in a time-serie object (xts)
