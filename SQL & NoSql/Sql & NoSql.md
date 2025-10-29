# what is SQL and NOSQL

### Full Form
#### -SQL (Structured Query Language) 
#### -NOSQL (Not Only Structured Query Language) 

# SQL

####  SQL (Structured Query Language) databases are relational and use a predefined schema to store data in tables
#### SQL databases excel in handling structured data and complex transactions

#### SQL databases are primarily called Relational Databases (RDBMS)
<!-- # SQL relational Database  -->
# Vertical 
####     It's Vertical Scaling(scale up ) means Increase resources of a single server(Add more CPU, RAM, Disk, or GPU).

# what schema in Database

#### 

#### It's a blueprint and arechitecture of database they defines structur,organization and relationship withun database it's acts(તે કાર્ય કરે છે) logical map of the database,  outlining(રૂપરેખા) how data is stored,how tables are structured,and how different parts of the database connect to one another.

#### 1.logical Structure
>>Tables: The basic units for storing data, with rows (records) and columns (attributes).

>>Columns: These specify the data types and properties of data within each table.

>>Relationships: How different tables relate to one another (e.g., one-to-many, many-to-many).

>> Constraints(અવરોધો) (Rules for Data):like uniqe,notnull ,cheak,primary key ,FOREIGN KEY – links one table to another,
Why it's useful:
To protect data from mistakes or invalid entries.

>>Views (Virtual Tables):To simplify access and protect original data
Why it's useful:Shows only what you need, Hides sensitive data ,Makes complex queries easier to reuse

>> Note : virtual table is not create mannuli using ORM ,it's create using sql query  (Use Raw SQL (Manual))
## Why is SQL important

#### -Unlike general-purpose programming languages, SQL is purpose-built for relational databases—and relational databases are, in turn, optimized for SQL. This mutual design renders SQL a highly efficient data management tool.

>> -Declarative Language
<br>
 <br>
 -User-Friendly and Accessible
 <BR>
 <br>
 -Command Structure: SQL does not require a continuation character for multi-line queries, allowing flexibility in writing commands across one or multiple lines.
 <BR>
 <br>
 -Built-in Functionality: SQL includes a rich set of built-in functions for data manipulation, aggregation, and formatting, empowering users to handle diverse data-processing needs effectively.
 <br>
 <br>
 -Open source support
Many SQL databases are open source and supported by a large, active community that contributes to continuous improvement and problem-solving.
<br>
<br>
-Scalability
SQL can effectively manage both small and large databases, adapting to growing data needs without significant performance loss.

## how does SQL work
>>-Input: The process begins when a user submits an SQL query through a database interface or application. This query typically specifies the desired operation, such as data retrieval, insertion, updating, or deletion.
<br>
<br>
-Parsing: The query is passed to the query processor, which breaks it into smaller units called tokens. These tokens represent keywords, table names, column names, and other elements of the query. The processor then validates the syntax against SQL standards and the database schema to ensure the query is well-formed and executable.
<br>
<br>
-Optimization: After parsing, the query is handed to the optimizer, which evaluates multiple ways to execute the query. The optimizer considers factors like indexes, table statistics, and available resources to generate the most efficient execution plan. This step ensures that the query runs with minimal resource consumption and maximum performance.
<br>
<br>
Execution: The execution engine follows the plan provided by the optimizer. It interacts with the storage engine, which retrieves, manipulates, or updates the required data from the database tables. During this step, SQL statements like SELECT, INSERT, UPDATE, or DELETE are translated into actions performed on the underlying data.
<BR>
<BR>
-Execution : this execution according query datatype




## How SQL Manages and Interacts with Data

#### -SQL is widely used across various relational database management systems(RDBMS) such as MySQL, PostgreSQL, Oracle, and SQL Server.

#### -data is core of every application and SQL plays key role in managing and interacting with this data.Whether you are working with a small user database or handling massive datasets like sales records, SQL allows you to efficiently query, update, and manage relational databases.

#### -SQL queries (also known as SQL commands or SQL statements) allow users to easily add, retrieve, update, delete, aggregate and otherwise manage data in a relational database (or SQL database). 



# NOSQL

#### while NoSQL databases are non-relational and offer ***more flexibility*** in data storage and retrieval

#### "Not Only SQL," is a database management system (DBMS) designed to handle large volumes of unstructured and semi-structured data.

#### Unlike traditional relational databases that use tables and pre-defined schemas, NoSQL databases provide flexible data models and support horizontal scalability, making them ideal for modern applications that require real-time data processing.


#### used own query language like mongodb (use persnol query)

## what schema in Database

#### In NoSQL databases, a flexible schema, or schema flexibility, means that the database ****does not require**** a fixed, predefined structure for the data.

>> NoSQL vs. Relational:
(means sql use schema then Nosql is not use predifune achema)
Traditional relational databases (SQL) use rigid schemas with fixed tables, columns, and data types. Data must fit this predefined structure. In contrast, NoSQL databases embrace flexibility, enabling you to easily add, modify, or remove fields in your data without impacting the overall database structure.

>> Data Model Freedom:
NoSQL databases are designed to support various data types, including unstructured and semi-structured data, where the data might not adhere to a strict, pre-defined schema. They can store different types of data in the same collection, enabling schema flexibility.

>> Adaptability and Evolution(અનુકૂલનક્ષમતા અને ઉત્ક્રાંતિ):Flexible schemas allow you to evolve your application's data structures as your requirements change without significantly impacting database operations.

in sort  does not require a schema.
## Why Use NoSQL?

#### It's Horizontal Scaling(scale out ) means multiple machines(servers)

#### Today, companies need to manage large data volumes at high speeds with the ability to scale up quickly to run modern web applications in nearly every industry. In this era of growth within cloud, big data, and mobile and web applications, NoSQL databases provide that speed and scalability, making it a popular choice for their performance and ease of use.

#### Unlike relational databases, which use Structured Query Language, NoSQL databases do not have a universal query language. In fact, each NoSQL database has its own approach to query languages. Traditional relational databases will follow ACID principles, assuring a strong consistency and a structured relationship between the data.

####  Flexibility in supporting unstructured or semi-structured data without a rigid schema.

#### Optimized for fast read/write operations with large datasets resulting in higher performance.

## Types of Nosql Database?

>> 1.Doucument DataBases:
Stored data in JSON,BSON or XML data
<br>
Exmpales:MongoDb ,couchDB ,cloudant

>> 2.Key-value stores
<br>
-Data stored in Key values pairs formet,this extremely faster to data retrieval
<br>
-Optimized for caching and session storage.
<br>
Examples:Redis,Memcached,Amazon DynamoDB

>> 3.Column-family stores
<br>
-Data stored in column formet rather then Row
<br>
-Examples: Apache Cassandra, HBase, Google Bigtable

>>4. Graph databases
<br>
-D-ata stored in Nodes and edges enabling complex relationship management
<br>
-Examples: Neo4j, Amazon Neptune, ArangoDB


## Advantages of NOSQL

>>1.Cost-effectivenes
<br>
2.Flexiblity
<br>
3.replication:NoSQL replication functionality copies and stores data across multiple servers. 
<br>
4.Speed
<br>
-In a nutshell, NoSQL databases provide high performance, availability, and scalability.

all data in IBM NOSQL website

# conclusion

-NoSQL database are flexible ,scalable and high-performance alternative to relational databases

-Make modern applications such as real-time analytics, big data processing and web applications more suitable for maintaining complex requirements.