# Model Inheritance 

# 1.Abstract

#### Abstract mean perent model inheritance in chiled model ,all perent model field show in child model

#### you can also use 

    class Meta:
        abstract=True

#### how to not show perent child field in other child class
> Field_name = None // they not show perent field in this perticuler class

#### don't try never delete manuylee table and databse diracli in database
#### remove data in model then migrate they auto delete row,cloums,database table etc...

# 2 multi Table Inheritance

#### multi table inheritance is vidly use for spret data in defren tables(data base)

#### perent class use not all child class and accses data but all child class access perent class data

#### use case it's use one to one relation ship you add any child class data they autometically add data in perent class

    class center:
        name=models...

    class child(center):
        age=models...

    > make to difrrent tables after migrations
    >you show child name and age / center table only show name
    >you name add in center no show child table but you add name and age in child bydefuilt add center table 

    > live exmple in django 45 file no


    Dont use abstract=true method in multi table inheritance         


# 3.Proxy model  

# change python level behavior of model

    user class Meta:
            proxy=True
            ordring=['id']

    "ordrint" mean they show data in orderd by in adminal panel without tuch admin panel seetting 
    ex:1,2,3,4,5
    noreml(withour proxy data):5,4,3,2,1        

# conclusion

### Abstract base clas: sharing a commen field to another class

### multi-table inheritance : own table share data to child table

### Proxy : modifying model behavior in python without impeacting the database structur