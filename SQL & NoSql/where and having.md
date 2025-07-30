# what is Where

Where use in aql query for filtering specific data and show in the table they work brfor group by

    Ex:
    SELECT * FROM Customers
    WHERE Country='Mexico';

    They write befor group by

NOTE:where coundition is cannot be used aggregate function    

# what is group by

group by use they give same value of rows into summary ,like find number of customers in each country

    SELECT COUNT(CustomerID), Country
    FROM Customers
    GROUP BY Country;

    summary query:

    they coutn all same country from customers table and give group by coutry details

    ex:
    count          coutry
      3             india
      4             america
      2              NZ
      1             aus
      6             south affrica

NOTE : they user aggregate function COUNT(),SUM(),MIN(),MAX(),AVG()      


# Having 

Having coundition use aggregate function for filtering a data

    SELECT COUNT(CustomerID), Country
    FROM Customers
    GROUP BY Country
    HAVING COUNT(CustomerID) > 5;

    Query summary:
    count all customer id from cuntry coulmns
    and from customers table after they culeact and make group by coutry details they give data above 5 no of country in one group

    count               country
        7                 AUS
        8                 usa
        6                  india
        12              china

# NOTE: Where use befor group by and having use after group by
