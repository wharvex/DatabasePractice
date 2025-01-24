# Database Concepts

1. Relational Model
<br><br>
    1. Overview
    <br><br>
        1. The relational model is an approach to managing data using a structure and language consistent with first-order predicate logic, where all data are represented in terms of tuples, grouped into relations.
        <br><br>
            1. First-order (predicate) logic
            <br><br>
                1. First-order logic is a collection of formal systems used in mathematics, philosophy, linguistics, and computer science.
                <br><br>
                1. First-order logic uses quantified variables over non-logical objects, and allows the use of sentences that contain variables.
                <br><br>
                1. Rather than propositions such as "all men are mortal", in first-order logic one can have expressions in the form "for all x, if x is a man, then x is mortal"; where "for all x" is a quantifier, x is a variable, and "... is a man" and "... is mortal" are predicates.
                <br><br>
                1. The term "first-order" distinguishes first-order logic from higher-order logic, in which there are predicates having predicates or functions as arguments, or in which quantification over predicates, functions, or both, are permitted.
                <br><br>
                1. In first-order theories, predicates are often associated with sets. In interpreted higher-order theories, predicates may be interpreted as sets of sets.
                <br><br>
            1. Tuple
            <br><br>
                1. In mathematics, a tuple is a finite sequence or ordered list of numbers or, more generally, mathematical objects, which are called the elements of the tuple.
                <br><br>
            1. Relation
            <br><br>
                1. In database theory, a relation is a set of tuples (d<sub>1</sub>,d<sub>2</sub>,...,d<sub>n</sub>), where each element d<sub>j</sub> is a member of D<sub>j</sub>, a data domain.
                <br><br>
                1. Each tuple element is called an attribute value.
                <br><br>
                1. An attribute is a name paired with a domain (nowadays more commonly referred to as a type or data type). 
                <br><br>
                1. An attribute value is an attribute name paired with an element of that attribute's domain.
                <br><br>
                1. A tuple is a set of attribute values in which no two distinct elements have the same name. 
                <br><br>
                1. Thus, in some accounts, a tuple is described as a function, mapping names to values.
                <br><br>
    1. Key Concepts:
Tables: Consist of rows (tuples) and columns (attributes).
Attributes: Represent specific characteristics of the entities being described.
Relationships: Defined between tables using primary and foreign keys.

Benefits:
Data independence: Changes to data structure don't necessarily affect the applications.
Flexibility: Easily adaptable to changing requirements.
Data integrity: Ensures consistency and accuracy of data.

2. Data Integrity

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
