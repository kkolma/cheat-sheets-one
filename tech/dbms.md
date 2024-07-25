This cheat sheet provides a concise overview of Database Management Systems (DBMS). It covers fundamental concepts, including the advantages of DBMS over file systems, the Entity-Relationship (ER) model, database design principles, various keys in DBMS, normalization, SQL commands, and more. It serves as a quick reference for essential DBMS topics, ideal for students and professionals alike.

## The Basics
### What is a DBMS?
A Database Management System (DBMS) is an organized collection of interrelated data designed to facilitate quick access, efficient insertion, and deletion of data. It organizes data in the form of tables, schemas, and records, ensuring a structured and systematic approach to data management. Additionally, DBMS supports data integrity, security, and concurrency control, making it a critical tool for handling large volumes of data in various applications.
### Issues with File System
- **Data Redundancy:** Same data stored in multiple places.
- **Data Inconsistency:** Different copies of the same data may have different values.
- **Data Access:** Difficult and insecure data access; no concurrent access.
- **No Backup and Recovery:** Risk of data loss due to lack of backup and recovery mechanisms.

## ER-Model
### ER Diagram Components
- **Entity:** Real-world object, represented by a rectangular box.
- **Strong Entity:** Has a primary key to identify tuples uniquely.
- **Weak Entity:** Lacks sufficient attributes for a primary key; depends on a strong entity.
- **Attribute:** Property or characteristic of an entity, represented by an oval.
- **Key Attribute:** Uniquely identifies an entity, represented by an oval with an underlying line.
- **Composite Attribute:** Made up of multiple attributes (e.g., Address).
- **Multivalued Attribute:** Can have multiple values (e.g., Phone numbers).
- **Derived Attribute:** Derived from other attributes (e.g., Age from Date of Birth).
- **Relationship:** Association between entities, represented by a diamond.

### Cardinality of DBMS
- **One-to-One:** One entity in A is related to at most one entity in B.
- **One-to-Many:** One entity in A is related to one or more entities in B.
- **Many-to-One:** Many entities in A are related to one entity in B.
- **Many-to-Many:** Any number of entities in A can relate to any number of entities in B.

### Specialization and Generalization
- **Specialization:** Top-down approach dividing an entity into sub-entities.
- **Generalization:** Bottom-up approach combining sub-entities into a higher-level entity.

### Aggregation
- **Aggregation:** Represents relationships as higher-level entity sets.

### Participation Constraint
- **Total Participation:** Every entity in the set participates in at least one relationship.
- **Partial Participation:** Some entities may not participate in any relationship.

## Database Design
### Goals
- **Zero Redundancy:** Avoid data duplication.
- **Loss-less Join:** Ensure data integrity.
- **Dependency Preservation:** Maintain data dependencies.
- **Overcome File System Shortcomings:** Ensure efficient data management.

### Keys in a Relation
- **Candidate Key:** Minimal set of attributes uniquely identifying a tuple.
- **Super Key:** Set of attributes uniquely identifying a tuple; can include candidate keys.
- **Primary Key:** Chosen candidate key for unique identification.
- **Foreign Key:** Set of attributes in one table referring to a primary key in another.

### Functional Dependency
- **Trivial:** If B is a subset of A.
- **Non-Trivial:** If B is not a subset of A.

### Armstrong’s Axioms
Armstrong's axioms are used to infer all functional dependencies on a relational database schema. They form the basis of a sound and complete axiomatization of functional dependencies.
- **Reflexivity:** If B is a subset of A, then A → B.
- **Augmentation:** If A → B, then A C → B C for any set of attributes C.
- **Transitivity:** If A → B and B → C, then A → C.

### Attribute Closure
Attribute closure is a method to determine all attributes that can be functionally determined by a given set of attributes.
- **Attribute Closure(X+):** All attributes that are functionally determined by X.

### Example
If the relation R(ABCD) has the functional dependencies {A→B, B→C, C→D}, then:
- Attribute closure of A (A+): {A, B, C, D}
- Attribute closure of B (B+): {B, C, D}
- Attribute closure of C (C+): {C, D}
- Attribute closure of D (D+): {D}

## Normalization
Normalization is a process to eliminate redundancy and dependency by organizing fields and tables of a database. It ensures that the database is free from undesirable characteristics like insertion, update, and deletion anomalies.

### First Normal Form (1NF)
- A relation is in 1NF if it contains only atomic (indivisible) values.

### Second Normal Form (2NF)
- A relation is in 2NF if it is in 1NF and every non-prime attribute is fully functionally dependent on the primary key.

### Third Normal Form (3NF)
- A relation is in 3NF if it is in 2NF and there is no transitive dependency.

### Boyce-Codd Normal Form (BCNF)
- A relation is in BCNF if it is in 3NF and for every functional dependency A → B, A is a super key.

## Data Retrieval (SQL, RA)
### SQL Commands
- **DDL (Data Definition Language):** CREATE, ALTER, DROP, COMMENT, TRUNCATE
- **DML (Data Manipulation Language):** SELECT, INSERT, DELETE, UPDATE, LOCK TABLE, MERGE, CALL, EXPLAIN PLAN
- **DCL (Data Control Language):** GRANT, REVOKE

### Relational Algebra
- **σ (Selection):** Select rows based on a given condition.
- **π (Projection):** Project some columns.
- **X (Cross Product/Cartesian Product):** Cross product of relations.
- **U (Union):** Return tuples in either relation.
- **- (Minus):** Return tuples in the first relation but not in the second.
- **ρ (Rename):** Rename a relation.
- **∩ (Intersection):** Return tuples in both relations.
- **⋈ (Conditional Join):** Join based on a condition.
- **⋈ (Equi Join):** Special case of conditional join with equality condition.
- **⋈ (Natural Join):** Join with equality on common attributes and remove duplicates.
- **⟕ (Left Outer Join):** Include all tuples from the left relation.
- **⟖ (Right Outer Join):** Include all tuples from the right relation.
- **⟗ (Full Outer Join):** Include all tuples from both relations.
- **/ (Division):** Return tuples in the first relation associated with every tuple in the second.

### Relational Calculus
- **Tuple Relational Calculus:** Based on specifying tuple variables. `{t | cond(t)}`
- **Domain Relational Calculus:** Based on specifying domain variables. `{x1, x2, ..., xn | cond(x1, x2, ..., xn)}`

## File Structure and Organization
### File Organization Types
- **Sequential File Organization:** Records stored sequentially.
- **Heap File Organization:** Unordered records.
- **Hash File Organization:** Records stored based on hash functions.
- **B+ Tree File Organization:** Balanced tree structure for efficient searching.
- **Clustered File Organization:** Grouping related records.

### Indexing Types
- **Primary Index (Sparse):** Ordered file with key field; single entry for a set of database records.
- **Secondary Index (Dense):** Secondary access; entry for every database record.
- **Clustered Index (Sparse):** Created on a non-key field; records ordered by clustering field.

### Multilevel Index
- **Second Level Index:** Sparse; multiple levels of indexing for efficient searching.

### B-Tree and B+ Tree
- **B-Tree:** Balanced tree with keys and data pointers.
- **B+ Tree:** Similar to B-Tree; all records at leaf level, allows sequential and random access.

## Transaction and Concurrency Control
### Transaction Properties
- **Atomicity:** Complete or no execution.
- **Consistency:** Maintain database integrity.
- **Isolation:** Transactions do not interfere.
- **Durability:** Changes persist after commit.

### Schedule Types
- **Serial Schedule:** Transactions execute one by one.
- **Non-Serial Schedule:** Concurrent transactions; better throughput.

### Serializability
- **Conflict Serializability:** Equivalent to a serial schedule by swapping non-conflicting operations.
- **View Serializability:** Equivalent to a serial schedule considering the view of data.

### Concurrency Control with Locks
Locks are mechanisms to control access to database resources by multiple transactions. Locking protocols ensure consistency and isolation by following specific rules.

#### Types of Locks
- **Binary Locks:** A simple lock/unlock mechanism.
- **Shared/Exclusive Locks:** 
  - **Shared Lock (S):** Allows read-only access.
  - **Exclusive Lock (X):** Allows read/write access and prevents other locks.

#### Two-Phase Locking (2-PL)
- **Growing Phase:** Acquire locks, but cannot release any lock.
- **Shrinking Phase:** Release locks, but cannot acquire any lock.

#### Locking Protocols
- **Basic 2-PL:** Ensures serializability, but may lead to deadlocks.
- **Strict 2-PL:** All exclusive locks held until commit/rollback; prevents cascading rollbacks.
- **Rigorous 2-PL:** All locks held until commit; ensures strict serializability.

#### Timestamp Ordering Protocols
- **Timestamp Protocols:** Assign timestamps to transactions to order their operations.
- **Thomas Write Rule:** Allows transactions to ignore obsolete writes, enhancing concurrency.

### Types of Schedule Based Recoverability
- **Irrecoverable Schedule:** A transaction that commits cannot be rolled back.
- **Recoverable Schedule:** A schedule where a

 transaction reads only after the commit of the transaction that wrote the data.
- **Cascadeless Schedule:** Transactions read only committed data, avoiding cascading rollbacks.
- **Strict Recoverable Schedule:** No operation allowed on uncommitted data.

## Tips and Sources
### Useful Tips
- Always design your database with normalization in mind to reduce redundancy.
- Use ER diagrams to visualize the database structure.
- Regularly backup your database to prevent data loss.
- Implement proper locking mechanisms to handle concurrency control.

### Reliable Sources
- [Last Minute Notes – DBMS](https://www.geeksforgeeks.org/last-minute-notes-dbms/)
- [Database Systems: The Complete Book by Hector Garcia-Molina](https://www.amazon.com/Database-Systems-Complete-Hector-Garcia-Molina/dp/0131873253)
- [SQL: The Complete Reference by James R. Groff](https://www.amazon.com/SQL-Complete-Reference-Third-Edition/dp/0071592555)
- [Fundamentals of Database Systems by Ramez Elmasri and Shamkant B. Navathe](https://www.amazon.com/Fundamentals-Database-Systems-Ramez-Elmasri/dp/0133970779)
