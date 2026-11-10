#Subject: Database Management System (B.Tech CSE Core)
## Topic 1: DBMS vs RDBMS

A Database Management System (DBMS) is software that allows users to create, store, retrieve, update, and manage data efficiently. It acts as an interface between the database and the user or application. DBMS reduces data redundancy, improves data security, and provides controlled access to stored information.

A Relational Database Management System (RDBMS) is an advanced type of DBMS that stores data in the form of tables consisting of rows and columns. Different tables can be connected using relationships through Primary Keys and Foreign Keys. RDBMS supports SQL (Structured Query Language) to perform database operations. Examples include MySQL, Oracle, PostgreSQL, and Microsoft SQL Server.

## Topic 2: Primary Key and Foreign Key

A Primary Key is a special attribute or combination of attributes that uniquely identifies each record (row) in a database table. It does not allow duplicate or NULL values, ensuring entity integrity within the database. Every table can have only one Primary Key, although it may consist of multiple columns (Composite Primary Key).

A Foreign Key is an attribute or combination of attributes in one table that refers to the Primary Key or a unique key of another table. It establishes relationships between two tables and maintains Referential Integrity by preventing invalid references. Unlike a Primary Key, a Foreign Key can contain duplicate values and may contain NULL values if permitted by the database constraints.

## Topic 3: SQL and Its Types

SQL (Structured Query Language) is a standard programming language used to communicate with relational databases. It allows users to create database structures, retrieve information, insert new records, modify existing data, and control database access. SQL provides an efficient way to manage and manipulate structured data.

SQL commands are divided into five major categories:

DDL (Data Definition Language): Used to define or modify database structures. Examples: CREATE, ALTER, DROP, TRUNCATE.
DML (Data Manipulation Language): Used to insert, update, and delete records in database tables. Examples: INSERT, UPDATE, DELETE.
DQL (Data Query Language): Used to retrieve data from database tables. Example: SELECT.
DCL (Data Control Language): Used to control database permissions and access. Examples: GRANT, REVOKE.
TCL (Transaction Control Language): Used to manage database transactions. Examples: COMMIT, ROLLBACK, SAVEPOINT.
## Topic 4: Normalization and Its Types

Normalization is a systematic process of organizing data in a relational database to reduce data redundancy and eliminate insertion, deletion, and update anomalies. It involves dividing large tables into smaller related tables and establishing relationships using Primary Keys and Foreign Keys. Normalization improves data consistency, integrity, and database efficiency.

The major normal forms are:

First Normal Form (1NF): A table must contain atomic (indivisible) values, and each column must contain values of a single domain. There should be no repeating groups or multivalued attributes.
Second Normal Form (2NF): A table must satisfy 1NF, and every non-prime attribute must be fully functionally dependent on the entire candidate key. It eliminates partial dependency.
Third Normal Form (3NF): A table must satisfy 2NF and should not contain transitive dependencies of non-prime attributes on candidate keys.
Boyce-Codd Normal Form (BCNF): A stronger version of 3NF in which every determinant must be a super key. It eliminates certain types of redundancy that may remain in 3NF.
## Topic 5: ACID Properties of Transactions

A Transaction is a logical unit of work performed on a database that consists of one or more operations, such as INSERT, UPDATE, DELETE, or SELECT. A transaction must be executed reliably to maintain database consistency, even in cases of system failure or concurrent access. ACID properties ensure the correctness and reliability of database transactions.

The four ACID properties are:

Atomicity: A transaction is treated as a single indivisible unit. Either all operations are completed successfully or none of them are applied.
Consistency: A transaction must take the database from one valid state to another while maintaining all predefined constraints and rules.
Isolation: Multiple transactions executing simultaneously should not interfere with each other. Each transaction should behave as if it is executing independently.
Durability: Once a transaction is successfully committed, its changes are permanently stored in the database, even if a system crash occurs.
## Topic 6: Deadlock in DBMS

A Deadlock in DBMS is a situation where two or more transactions are permanently blocked because each transaction holds a lock on a resource and waits for another resource locked by a different transaction. As a result, none of the transactions can proceed, causing the database system to become stuck until the deadlock is detected and resolved.

A deadlock can occur if all four Coffman conditions hold simultaneously:

Mutual Exclusion: A resource or lock must be held in a non-shareable mode, allowing only one transaction to access it at a time.
Hold and Wait: A transaction must hold at least one lock while waiting to acquire another lock held by a different transaction.
No Preemption: Locks cannot be forcibly taken away from a transaction; they are generally released when the transaction voluntarily releases them or is rolled back.
Circular Wait: A circular chain of transactions must exist in which each transaction waits for a resource held by the next transaction in the chain.
## Topic 7: Database Indexing

Indexing is a database optimization technique used to improve the speed of data retrieval operations. An index is a special data structure that stores selected column values along with pointers to their corresponding records. Instead of scanning the entire table, the database uses the index to locate required records more efficiently. However, indexing requires additional storage space and can slow down INSERT, UPDATE, and DELETE operations because indexes must also be maintained.

The major types of indexing are:

Primary Index: An index created on the primary key of a table, generally associated with an ordered data file.
Secondary Index: An additional index created on a non-ordering attribute to improve data retrieval.
Clustered Index: An index that determines the physical or logical ordering of records according to the indexed key.
Non-Clustered Index: An index that stores key values and pointers to the actual data records without determining the physical ordering of the table.
## Topic 8: DBMS vs File System

A File System is a traditional method of storing and managing data in separate files on a computer. It provides basic operations such as creating, reading, updating, and deleting files. However, it often suffers from data redundancy, inconsistency, limited security, and difficulties in accessing and managing large amounts of data.

A Database Management System (DBMS) is specialized software designed to store, organize, retrieve, and manage large amounts of structured data efficiently. It provides features such as data security, concurrency control, transaction management, backup, and recovery. Unlike a traditional file system, DBMS supports structured querying and controlled access to shared data.