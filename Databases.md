- Database: an organised collection of structured information or data that can be accessed in different ways
- Table: a structure of rows and columns for storing a group of similar data
- Entity: a living or non-living thing that can have data stored about it that can be described
- Record: one instance of an entity; a row in a table
- Attribute: a data item or a characteristic of an entity; a column in a table

## Features:

- Primary key: a field that uniquely identifies a record in a table
- Foreign key: an attribute in a table refers to the primary key in another table
- Composite keys: a set of attributes that form a primary key
- Relationship: a relation established between different tables, where the foreign key in one table refers to the primary table in another table

## Database relationships

### One to one relationship
- When there is a one-to-one relationship between two tables, that means that one record in a table is associated with exactly one record in another table: the primary key corresponds to one or no data in another table
- E.g. Each staff member of a school has one single staff ID
- Each country has exactly one capital city
- A user on a social media platform has a single user profile
- These are rare types of relationships, which would not be frequently encountered when dealing with databases
###  One-to-many relationships
- A more frequently used type of relationship, and it refers to one record in a table being associated with one or more records in another table: the foreign key of one table references the primary key of another table.
- E.g. One teacher teaches many subjects
- One tourist visits many countries
- One person owns many properties
- One person has many bank accounts
### Many-to-many relationships
- This type of relationship appears when multiple records in a table have a relation with multiple records in another table
- E.g. Many customers purchase many products
- Many actors act in many movies
- Problem with this relationship is that a foreign key attribute can only hold a single value and so it cannot handle the many references required

## Benefits of databases

#### Community support
- Questions and problems can be solved quickly
#### Concurrency control
- Many people can work on the same database, can be used by concurrent users without error using ACID properties
#### Data consistency
- Making sure that data is accurate
- A mechanism mirrors all replicas, ensures all copies of it is kept the same
#### Data integrity
- Making sure the data is correct, has certain rules and needs to be followed
#### Data retrieval
- The process of retrieving specific data from a database using SQL
#### Reduced data duplication
- Use of entities and relationship means there is less data duplication
#### Reduced redundancy
- As data is stored across entities using relationship links, there is less redundant data, use of foreign keys
#### Reliable transaction processing
- Relational databases have several checks that occur when transactions take place to ensure that the transactions are reliable
#### Scalability
- Relational databases are easier to scale than flat file databases
- Allows systems to handle increasing data volumes, user traffic, and workloads without sacrificing performance
#### Security features
- Relational databases have built-in security to support a multiuser environment
- They provide a structured, robust framework for protecting sensitive data
- Access can be controlled and restricted to specific tables or even specific columns

## Limitations of databases - ADD
### “big data” scalability issues -
### Design complexity
### Hierarchical data handling

### Rigid schema

### Object-relational impedance mismatch

### Unstructured data handling

## Database Schemes
- a database schema is a blueprint of the database, describing how data is organised and stored in a database.
- It identifies the different entities (tables), attributes (fields), and relationships (links)
- within the database, including the restraints on the data
- Doesn't contain actual data
### Conceptual Schema
- a high-level, abstract representation of the database structure
- Focusing on entities and their relationships
- Independent of the database software or hardware
- uses tools like ERDs to depict entities (e.g., Students, Courses) and relationships
- Conceptual schemas guid initial design discussions
### Logical Schema
- Defines the database structure in terms of tables, columns, datatypes, and constraints like keys
- ceebs

### Physical schema
im just adding photo
- difference is that it specifies how data is stored on hardware - numbers beside represent maximum size of the thing
![[GYDcP.png]]

# Purpose of schemas
organise data to support efficient querying, integrity and scalability
seperation of concerns

# Entity Relationship Diagrams
![[Screenshot 2026-02-27 at 15.16.00.png]