# SQL JOIN

### bascically join mean's combine rowa two or more tables

## INNER JOIN

#### given same type data (matching value) in both tabules 

## Left join

#### given all  right side table data to match left side table,table show empty(0) it's mean any data of right side it not match left side data table

#### T1(left) - 1,2,3,4,5,6,7,8,9,10
#### T2(right) - 1,2,3,4,5
#### data show : 1,2,3,4,5

## Right Join

#### given all  left side table data to match Right side table ,Table is empty it means any left side data no match right side data table

#### T1(left):1,2,3,4,5
#### T2(right):1,2,3,4,5,6,7,8,9,10
#### DATA SHOW :1,2,3,4,5

## full join

#### it give all data t1,t2,matching data,no match data all means all
#### it mean commbine result LEFT and RIGHT join

## self join
#### show all rows from both table,wher no match data they retun NULL 

#### it give all data according your need no cheaking left join,right join,data  match or not

#### EX T1:customer name ,T2:Customer name ,city etc