# What is Key
This context of a relational database ,keys are a basic requierements of a relational database model.keys are fundamenatl consept  that ensuredata integrity, uniqueness, and efficient access.

# Why do we require Keys in a DBMS?

Uniqueness: keys ensure that each record in the table is unique.

Data Integrity: Keys prevent data duplication and maintain the consistency of the data.

# Keys

## Primery key

primery key is uniquely identifies each row in table

it cannot null and must be unique

## Candidate key 

it's candidate key is one or more columns that can uniquely identify a row in a table 

many uniqu key avaliable in Table like id,roll_no,Phone number , Adhaar Card number , Pan number ,etc avaliable in one table 

one of the candidate key choosen as primery key

## Super Key

A super key is set of one and more  that can uniquley identify a row in table

    this is a supery key

    {EmpID}

    {AadhaarNo}

    {PAN_No}

    {EmpID, Name}   

    {AadhaarNo, PAN_No}

    {EmpID, AadhaarNo, PAN_No}

    … (many combinations)

    but 

    Candidate Keys = {StudentID}, {Email}, {Phone}.

## Composite key 

A composite key as primery key made up of multiple columns

Primary key with multiple columns

## Foreign Key

Refers to primery key of another table 

foreign key links two tables together

## Unique Key

Ensures that all values are unique

Unlike a primary key, a unique key can allow NULL (only once).

like email,phone,addhar etc

