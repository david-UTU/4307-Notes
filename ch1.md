# Chapter 1


### Terms
- Database Management System
  - A collection of interrelated data and a set of programs to access those data
- Instance
  - the collection of information stored in the database at a particular moment
- Schema
  - the overall design of the database, divided into physical and logical levels
- Data-definition Language (DDL) 
  - provided by the database system, specifies the schema and a data-manipulation language to express queries and updates
- Data-manipulation Language (DML) 
  - language used to move, delte, and modify data in the database
- Metadata 
  - data about data
- Query
  - a statement requesting the retrieval of information
- Application programs
  - programs that are used to interact with the database appropriately
- Normalization
  - the term used for the collection of algorithms used to turn the set of all attributes into a set of tables
- Storage Manager
  - component of a database system that provides the interface between low-level data stored and the application programs and submitted queries
- Two-tier Architecture
  - application resides at the client level but invokes the database at the server level
  - used in early generation database applications
- Three-tier Architecture
  - client machine merely acts as a front-end
  - application resides on an application server, which communicates with a database system
  - 


### Important Concepts
- Modern databases must be able to account for complex, unrelated data while still functioning efficiently
  - The key to this is effective abstraction in consideration of the data available
- Two main modes in which databases are used
  - Online transaction processing: large number of users interact with the database and retrieve relatively small amounts of data. 
  - Data analytics: processing data, drawing conclusions, and inferring rules or decision procedures that drive business decisions
- Types of Data Models
  - Relational model: a collection of tables to represent both the data and the relationships among those data
  - Entity-relationship model: uses a collection of basic objects (called entities) and relationships among these objects.
  - Semi-structured data model: permits the specification of data where individual data items of the same type may have different sets of attributes
  - Object-based data model: An extension of the relational model that allows notions of encapsulation, methods, and object identity to better accommodate object oriented programming
- Levels of data abstraction
  - Physical: lowest level; describes how data are actually stored, describes complex, low-level data structures in detail
  - Logical: middle level;  describes what data are stored in the database and what relationships exist among those data.
  - View: highest level; describes only part of the entire database; exists to simplify interaction for the logical level
- In practice, DDL and DML work together to form parts of a complete database language
- DDL details
  - Domain Constraints: a domain of possible values must be associated with every attribute; acts as a constraint on its intake values
  - Referential Integrity: ensuring that intake values match only ones that existed in the current relationships established in the database system
  - Authorization: differentiation among users by what they are allowed to do with data in the database
- DML details
  - Types of access:
    1. Retrieval
    2. Insertion
    3. Deletion
    4. Modification
  - Type types of DMLs
    1. Procedural: require a user to specify what data are needed and how to get them
    2. Declarative: require a user to specify what data are needed without specifying how to get those data
  - DML and query language are, in practice, synonymous, but this is technically incorrect
- Database design phases
  1. Logical:
    - designer maps the high-level conceptual schema onto the implementation data model of the database system that will be used
  2. Physical:
    - physical features are specified
    - think file organization and internal storage structures
- Components of the storage manager
  1. Authorization and integrity manager
    - tests for integrity satisfaction and constraints; also checks user authority
  2. Transaction manager
    - ensures the database remains consistent despite system failures; ensures concurrent transactions do not cause conflict
  3. File manager
    - manages the allocation of space on disk storage and the data structures used to represent information
  4. Buffer manager
    - responsible for fetching data from disk storage into main memory; also decides cache usage
- The storage manager also implements several data structures as a part of the physical system
  1. Data files
    - store the database itself
  2. Data dictionary
    - stores metadata about the structure of the database
  3. Indices
    - pointers to specific data items for fast access
- Components of the query processor
  1. DDL interpreter
    - interprets ddl statements and records definitions in the data dictionary
  2. DML compiler
    - translates dml statements to a plan of low-level instructions
  3. Query evaluation engine
    - executes instructions from the dml compiler
- Transaction management principles
  - Atomicity
    - ensuring that when modifying multiple value with a set relationship, the extent of the full relationship is either executed fully or not at all
    - Think of a money transfer. If I pay you 5 dollars, that money needs to be taken from me and given to you. It cannot be taken from me and not received by you, and it cannot be left in my account but also given to you
  - Consistency
    - Prevention of anomalous, incorrect data disruptions or deviations across all components of a database
  - Persistence/Durability
    - updated values remain what they should be, even despite system failure
