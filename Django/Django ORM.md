# ORM 

### <u>Object-Relational Mapping:</u>

ORMs automatically create a database from defined models or scheme which meant that the developer need not have knowledge of the SQL used in the database.

It translates Python object operations into SQL queries, allowing developers to manipulate database data using familiar Python syntax.

The main purpose of these is to make query retrieval faster and easier.

### <u> Relationship between fields of tables </u>

Abstraction is a major concern when working with data, Django ORM provides a level of abstraction that is easy to work with. 
 ORM will relate the object's attributes to the corresponding table fields automatically.

 ### <u> There are 3 kinds of relationships between fields of tables. </u>

<u> One to one </u> ---->  here, there exists a one-to-one relationship between two tables. For each row in table1, there exists a row in table2.

<u>One-to-many:</u>
One record in Table A can be linked to multiple records in Table B, but each record in Table B is linked to only one record in Table A. Example: One customer can place multiple orders.

<u>Many-to-many:</u>
One record in Table A can be linked to multiple records in Table B, and vice versa. Example: One product can be in multiple orders, and one order can contain multiple products. Many-to-many relationships are typically implemented using a third table (junction or linking table) with one-to-many relationships to the original two tables. 


### <u>Why Use Django ORM? </u>

No need to write raw SQL.

Avoids SQL injection.

Portable across different databases (SQLite, PostgreSQL, MySQL).

Cleaner, Pythonic syntax.



