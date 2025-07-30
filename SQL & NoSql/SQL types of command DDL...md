# Types of SQL commands: DDL, DML, DQL, DCL, and TCL

### -DDL(Database Definition Language)
> These commands are used to define the structure of database objects by creating, altering, and dropping the database objects
<bR><br>
-CREATE
<br><br>
-ALTER(Modifies(change) an existing database object),change table structure(columns,data type ,structur)
<BR><br>
-DROP(Deletes an entire table or database like Scholl database / students table) 
<br><br>
-TRUNCATE: remove all rows but keep the table,columns
<br><br>
-RENAME: Rename the table name

### -DML(Database Manipulation Language)

> A relational database can be updated with new data using data manipulation language (DML) statements
<BR><BR>
-INSERT:Add a new Data
<BR><BR>
-UPDATE:Change existing data(values update in (row) columns) EX:UPDATE students SET age = 21 WHERE name = 'Raj';
<BR><BR>
-DELETE:Delete (remove) selected data like DELETE FROM students WHERE id = 1; using filter method in django


### DQL (Data Query Language)

> It's used to Fetch(read) data from database,don't change and delete ,you only ask(query) for it
<br><br>
SELECT:To fetch data from table 
<br>
<br>
EX:SELECT * FROM ,students; , FETCH SELECTED DATA like SELECT name FROM students WHERE age > 18;(✔️ Only students above 18.)


## DCL(data Control language)

> dcl is manage user acces to the database by granting or revoking permission.Dcl use for control and security
<br><br>
GRANT: give permission to users
<br><br>
Exmple:GRANT SELECT, INSERT ON students TO 'raj'@'localhost';
<br><br>
REVOKE: TAck back (remove) permission from user
<br><br>
Exmple:REVOKE INSERT ON students FROM 'raj'@'localhost';

## TCL(Transaction Control Language)

> TCL command manage  transection in relational database ,You can undo or confirm a group of actions
<br><br>
BEGIN: Starts a transaction. It marks the beginning of a series of operations that should be treated as one unit.
<br><br>
COMMIT: Save all changes permanently during transaction
<br><br>
ROLLBACK: This command undoes all changes made during the current transaction, restoring the database to its state before the transaction began. any tansection feil of any step they restart to step 1 (it mean rollback)
<br><br>
SAVEPOINT: This command allows you to set a point within a transaction to which you can roll back later, without affecting the entire transaction

