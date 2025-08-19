# Normal forms in Dbms

### what is Normal forms?

Normal forms is inportent for ensuring that data is structured logically,reducing redundancy, and maintaining data integrity. it's importen whan you work with relationall data base they help to  normalization techniques that help to eliminate unnecessary duplication, improve performance, and minimize the risk of anomalies in database.

### Why is Normalization Important in Databases?

1.Reduces Data Redundancy(duplicate data) : they reduse dublicate data 

2.semplifies database design : they give simple and clear stucture 


## Type of normal Form

### 1NF (one normal form)

user order many items in one teble(dining table) they data stord always add single row like 
    1NF
    1  raj  supp
    2  raj  dosa
    3  raj  idly
    4  keshave panipri
    4 keshave vadapave

    they spreat data and transfer into esy way

    NoN-1NF
    1 raj  supp,dosa,idly
    2 keshave panipri,vadapave

    this way not good alway order stord in database..

- use a foreignkey 
-  Each row is unique and can be identified by a primary key.

- All entries are atomic—no lists or nested records.





