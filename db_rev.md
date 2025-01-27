# Database Concepts

1. Relational Model
<br><br>
    1. Overview
    <br><br>
        1. The relational model is an approach to managing data where all data 
        are represented in terms of _Database Relation Tuples_ grouped into 
        _Database Relations._
        <br><br>
            1. __Database Relation Tuple__
            <br><br>
                1. A set of _Attribute Values_ in which no two distinct 
                _Data Domain Elements_ have the same _Attribute Name._
                <br><br>
                    1. __Attribute Value__
                    <br><br>
                        1. An _Attribute Name_ paired with a
                        _Data Domain Element._
                        <br><br>
                    1. __Data Domain Element__
                    <br><br>
                        1. An element of a _Data Domain._
                        <br><br>
                            1. __Data Domain__
                            <br><br>
                                1. Data type, e.g. Integer.
                                <br><br>
                        1. For the _Data Domain_ example Integer, a 
                        _Data Domain Element_ example would be 1.
                        <br><br>
                    1. __Attribute Name__
                    <br><br>
                        1. Table column name.
                        <br><br>
                1. You can think of a _Database Relation Tuple_ as a function
                mapping names to values.
                <br><br>
            1. __Database Relation__
            <br><br>
                1. A set of _Database Relation Tuples_
                (d<sub>1</sub>,d<sub>2</sub>,...,d<sub>n</sub>), where each 
                _Database Relation Tuple Element_ d<sub>j</sub> is a member of 
                D<sub>j</sub>, a _Data Domain._
                <br><br>
                    1. __Database Relation Tuple Element__
                    <br><br>
                        1. See: _Attribute Value_.
                <br><br>
1. Database View
<br><br>
    1. A database view is a subset of a database and is based on a query that 
    runs on one or more database tables. 
    <br><br>
    1. Database views are saved in the database as named queries and can be used 
    to save frequently used, complex queries.
    <br><br>
1. Data Integrity

Ensuring Data Accuracy and Consistency

Key Constraints:
Entity Integrity:
No primary key value in a table can be null.
This ensures that each row in a table is uniquely identified.
Referential Integrity:
Foreign key values must either match a primary key value in another table or be null.
This maintains consistency between related tables.
Other Integrity Constraints:
Domain Constraints: Restrict the values that can be entered in a column.
Check Constraints: Enforce specific conditions on the data within a table.

3. Normalization

Organizing Tables for Efficiency and Integrity
Goals:
Reduce data redundancy (minimize data duplication).
Improve data integrity (make data more consistent and accurate).
Enhance data flexibility (make it easier to modify the database schema).
Normalization Stages:
1NF (First Normal Form): Eliminate repeating groups of columns.
2NF (Second Normal Form): Remove partial dependencies.
3NF (Third Normal Form): Remove transitive dependencies.
Higher Normal Forms (4NF, 5NF, 6NF): Address more complex dependencies.

4. SQL (Structured Query Language)

The Standard Language for Relational Databases
Key Categories:
DDL (Data Definition Language):
CREATE TABLE, ALTER TABLE, DROP TABLE: Define and modify table structures.
DML (Data Manipulation Language):
INSERT, UPDATE, DELETE: Manipulate data within tables.
DQL (Data Query Language):
SELECT: Retrieve data from the database based on specific criteria.
Other SQL Commands:
GRANT, REVOKE: Control user access privileges.
COMMIT, ROLLBACK: Manage transactions.

5. Primary Key

Uniquely Identifies Each Row in a Table
Characteristics:
Must be unique for every row.
Cannot contain null values.
Examples:
CustomerID in a Customers table
OrderID in an Orders table

6. Foreign Key

Establishes Relationships Between Tables
Represents:
A column in one table that references the primary key of another table.
Example:
In an Orders table, the CustomerID column would be a foreign key referencing the CustomerID (primary key) in the Customers table.

7. Indexes

Speed Up Data Retrieval
How they work:
Create a sorted data structure that allows the database system to quickly locate specific rows.
Types:
B-tree indexes: Efficient for both range queries and equality searches.
Hash indexes: Optimized for equality searches.
Benefits:
Faster query execution.
Improved overall database performance.

8. Views

Virtual Tables that Represent a Subset of Data
Created from:
One or more base tables.
Benefits:
Data Abstraction: Simplify complex queries by providing a simplified view of the underlying data.
Data Security: Restrict access to specific data by creating views that only show authorized information.
Data Independence: Changes to the base tables may not affect the view.

9. Transactions

A Unit of Work Treated as a Single, Indivisible Operation
Key Properties (ACID):
Atomicity: All operations within a transaction are executed as a single unit. Either all operations succeed, or all operations fail.
Consistency: A transaction must leave the database in a consistent state.
Isolation: Concurrent transactions do not interfere with each other.
Durability: The effects of a committed transaction are permanent and will not be lost in case of system failure.

10. Database Security

Protecting Data from Unauthorized Access, Modification, or Destruction
Key Measures:
User Authentication and Authorization:
Verify user identities and grant appropriate permissions.
Data Encryption:
Convert data into an unreadable format to protect it during transmission and storage.
Access Control Lists (ACLs):
Define which users or groups have specific privileges (read, write, execute) on database objects.
Regular Backups and Recovery Procedures:
Minimize data loss in case of hardware or software failures.
