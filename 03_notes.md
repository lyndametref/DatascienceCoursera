#Note
*Personal notes, not meant to be accurate or understood by others*

#Week1

#Week2
##Download from URL
```
fileUrl <- "https://data.baltimorecity.gov/api/views/dz54-2aru/rows.csv?accessType=DOWNLOAD"
download.file(fileUrl, destfile = "./data/cameras.csv", method = "curl")
list.files("./data")
```
