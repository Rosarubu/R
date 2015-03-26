###connect MySQL using R & other simple commands
```
library(DBI)
library(RMySQL)
conn=dbConnect(MySQL(),user='root',password='',host='',dbname='moodle')
dbDisconnect(conn) #disconnect
dbGetQuery(conn,"show databases") # dbGetQuery(conn, "a character vector of length 1 containing SQL", ...)

dbListTables(conn) #show tables from database
dbListFields(conn, 'mdl_user') #list table names
dbReadTable(conn,"mdl_user")  #all the list and read things can use GetQuery to achieve
```
We can store the table as a data frame in R using 

`test=dbGetQuery(conn,"select * from  mdl_user") `
or 
`test=dbReadTable(conn,"mdl_user")`

next step is dealing with all data frame
```
Select mdl_user.*,mdl_role _assignments.roleid from mdl_user join
mdl_role _assignments on mdl_user.id=mdl_role _assignments.userid
```
