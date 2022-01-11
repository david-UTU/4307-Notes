# Chapter 2


### Terms

- Tuple
  - in mathematical terminology, a sequence of values
- Relation Instance
  - a specific set of rows
- Domain
  - the set of permitted values for an attribute (column)
  - considered atomic if the elements are considered to be indivisible units
- Null Value
  - signifies that the value in question does not exist or is not recognized
- Database Schema
  - Logical design of the database
- Database Instance
  - a snapshot of the data in the database at a given instant in time
- Superkey
  - a set of one or more attributes that, when taken collectively, allow us to uniquely identify a tuple in the relation
- Candidate Keys
  - superkeys for which no proper subset is a superkey
- Primary Key
  - a candidate key that is chosen by the database designer as the principal means of identifying tuples within a relation
- Schema Diagrams
  - graphical depictions of database schema, along with primary key and foreign-key constraints
- Query Language
  - a language in which a user requests information from a database
- Imperative Query Language
  - a query language where the user instructs the system to perform a sequence of operations on the database to cmputer the desired result
  - usually have a notion of state variables that are updated in the course of the computation
- Functional Query Language
  - the computation is expressed as the evaluation of functions that may operate on data in the database or on the results of other functions
- Declarative Query Language
  - the user describes the information without giving a specific sequence of steps or function calls for obtaining that information, usually done using mathematical logic


### Important Concepts

#### Relational Database Intro

- Structure of a Relational Database
  - Consists of a collection of uniquely named tables
  - Rows represent a relationship among a set of values
  - Columns are referred to as attributes; rows are referred to as tuples
  - Relationship between n values is represented mathematically as an n-tuple of values
- Database Schema
  - Composed of a list of attributes and their corresponding domains
- Arity
  - the number of attributes of a relation

#### Keys

- What are keys?
  - used to specify how tuples within a given relation are distinguished
  - expressed in terms of their attributes
  - attribute values of a tuple must uniquely identify the tuple
- Foreign-Key Constraints
  - on any database instance, the value of the attribute for each tuple in the referencing relation must also be the value of the primary-key for some tuple in the referenced relation
  - Essentially, when one database references another, the dependent values of these relations must match... duh
- Referential Integrity Constraint
  - requires the values appearing in specified attributes of any tuple in the referencing relation also appear in specified attributes of at least one tuple in the referenced relation

#### Relational Algebra

- What is relational algebra?
  - a set of operations that take one or two relations as input and produce a new relation as their result
  - this is a functional query language
  - forms the theoretical basis of SQL
- Operation Types and Rules
  - Unary operations
    - operate on one relation
    - include select, project, and rename
  - Binary operations
    - operate on pairs of relations
    - includes Cartesian product, union, and set difference
  - Relations cannot contain duplicate tuples in formal relational algebra
- Specific Operations
  - Select
    - selects tuples that satisfy a given predicate
  - Project
    - returns its argument relation with specific attributes left out
  - Cartesian-Product
    - combines information from any two relations
    - requires naming schemas to avoid similarly named attributes, which is done by attaching an attribute to the name of the relation from which the attribute originally came
  - Intersection
    - allows us to find tuples that are in both of the input relations
  - Set-Difference
    - fins tuples that are in one relation but not in another
  - Assignment
    - assigns input components to temporary relation variables
  - Rename
    - allows us to define names that refer to the results of relational-algebra expressions

