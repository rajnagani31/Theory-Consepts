# what is Query set

### In Django, a QuerySet is an object that represents a collection of database objects. It is essentially a list of objects of a given Model, retrieved from the database or ready to be retrieved.it is query translater usin ORM (python code --> SQL query ----> create,update,delete,read in data base)

# Filtering and Ordering:

### QuerySets provide powerful methods to filter, order, and slice data. You can use methods like filter(), exclude(), order_by(), distinct(),id,union,intersection and slice() to refine the data you retrieve from the database.



# Represents SQL Queries:

###  In essence, a QuerySet translates to a SQL SELECT statement behind the scenes. Filtering and ordering methods correspond to WHERE, ORDER BY, and LIMIT clauses in SQL.


# lookups Method

### argumant_name__(after doubul underscore use lookups value)

# many method are avalibel

### gt(<), lt(>), gte(<=) ,lte(>=), __month details, year details __year, __range(quterly,custom monthe and year), __in=[1,2,3,4,][0:10:2]sliceing,data Create,bilk creat and update,data update,data delete in means give data thisdata_in etc more show dj folder 44_queryset

### secouns,minits,hours(24h),day,week,month,year all lookups is available