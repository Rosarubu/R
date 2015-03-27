[http://www.r-tutor.com/r-introduction/data-frame]
[http://joe11051105.gitbooks.io/r_basic/content/variable_and_data/data_frame.html]
[http://oz.berkeley.edu/classes/s133/Db3.html]


###COLUMN

show name(header,column name) of data frame `names(test)`

change column name `names(test) <- c("n", "a", "g",...)`

number of column `ncol(test)`

Data Frame Column Vector : get vector 

`test$deleted` or  `test[[5]]` or `test[["deleted"]] #it's a vector instead of frame`

Data Frame Column Slice :  get data frame

`id=test[1]` or `id=test["id"]` or 
`id=test[c(1,2)]  # first two colums of frame`
`id=test[c("id","auth")] # first two colums of frame`

----------------

###ROW

show row name `row.names(test)`

change row name `row.names(test) <- c("r1", "r2", "r3",...)`

number of row `nrow(test)`

Data Frame Row Slice : get data frame
```
test[1,] # first row
test[c(1,3),] # first & third row
test[c(1,3),] # first to third row
head(test,1) # first two rows
```

----------------

summary  `summary(test)`

remove dataframe  `remove(test)`


