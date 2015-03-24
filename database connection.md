#connect MySQL using R & other simple commands
```
library(DBI)
library(RMySQL)
conn=dbConnect(MySQL(),user='root',password='',host='',dbname='moodle')
dbGetQuery(conn,"show databases") # dbGetQuery(conn, "a character vector of length 1 containing SQL", ...)

dbListTables(conn) #show tables from database
dbReadTable(conn,"mdl_user")  #all the list and read things can use GetQuery to achieve
```
We can store the table as a data frame in R using 

`test=dbGetQuery(conn,"select * from  mdl_user") `
or 
`test=dbReadTable(conn,"mdl_user")`

next step is dealing with all data frame
