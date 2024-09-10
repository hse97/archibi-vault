##### Database Application 
Software that helps business users interact with database systems
##### Database Administrator 
responsible for securing the dB system against unauthorized users. dB admin enforces procedures for user access and dB system availability 
##### Authorization 
Many dB users should have limited access to specific tables, cols, and rows. 
dB systems authorize individual users to access specific data 
##### Rules
dB systems ensure data is consistent with structural and business rules 
##### Query Processor
interprets queries, creates a plan to modify or retrieve data, and returns query results to the application 
	performs **QUERY OPTIMIZATION** to ensure the most efficient instructions are executed on the data 
##### Storage Manager
Translates the query processor instructions into low-level file-system commands that modify or retrieve data. 
dB sizes frange from mB to kB so storage manager uses **INDEXES** to quickly locate data 
##### Transaction Manager
ensures transactions are properly executed 
transaction manager prevents conflicts between concurrent transactions 
Transaction manager also restores the dB to a consistent state in the event of a transaction or system failure 
##### MongoDB
noSQL, Open Source, Engine rank #5
##### INSERT
inserts rows into a table 
```
INSERT INTO table_name (column1, column2,...) 
VALUES (value1, value2,...);
```
##### SELECT
retrieves data from a table
```
SELECT Column1, Column2, ... 
FROM table_name
WHERE condition;
```
##### UPDATE
modifies data in a table 
```
UPDATE table_name
SET column1 = parameter
WHERE condition;
```
##### DELETE
deletes rows from a table
```
DELETE table_name
WHERE condition; 
```
##### CREATE TABLE
creates a new table by specifying table and column name
```
CREATE TABLE table_name (
column1 datatype,
column2 datatype,
....
);
```
##### Data Types
Set of values that column values can be derived from. Numeric, textual, or complex. 

##### INT
stores integer values 
`INT` or `INTEGER`
##### DECIMAL 
stores fractional numbers 
`DECIMAL(M,D)` 
##### VARCHAR(n)
variable length string 
`VARCHAR(n)`
##### DATE
stores date YYYY-MM-DD 
`DATE` 
##### Analysis
Specifies dB requirements without regard to specific dB system
requirements represented as entities, relationships, and attributes
An entity is a person, place, activity, or thing 
Relationship is a link between entities, and an attribute is a descriptive property of an entity 
	Also called 
	**CONCEPTUAL DESIGN**
	**ENTITY-RELATIONSHIP MODELING**
	**REQUIREMENTS DEFINITION**
##### Logical Design 
implementation dB requirements in a specific dB system. For relational dB systems, logical design converts entities, relationships, and attributes into tables, keys, and columns 
##### Physical Design 
adds indexes and specifies how tables are organized on storage media 
Effects query processing speed and performance but not results 
##### Data Independence
idea that query performance does not impact query results 
##### Application Programming Interface 
simplifies user of SQL qwith general purpose languages
##### MySQL command line
text interface included in MySQL server download
##### Error Code
when an SQL statement is syntatically incorrect or the dB cannot execute the statement 
##### Tuple
ordered collection of elements enclosed in parenthesis 

##### Table
Has a name, fixed tuple of columns, and varying set of rows
	AKA
	**FILE**
	**RELATION**
##### Column
Has name and datatype
	AKA
	**FIELD**
	**ATTRIBUTE**
##### Row
unnamed tuple of values, each value corresponding to a column with matching datatype
	AKA
	**RECORD**
	**TUPLE**
##### Cell
single column of a single cell
##### Empty Table
Tables must have at least one column but any number of rows
Table without any rows is called an Empty Table
##### Data type
named set of values from which column values are drawn from 
##### Business Rules
are based on business policy and specific to a particular dB 
##### Literals
Explicit values that are string, numeric, or binary 
	Strings must be surrounded by single or double quotes
	Literals are of the form x'0' where 0 is whatever hex value
##### Keywords
Words with special meaning in SQL
	like SELECT, WHERE, FROM
##### Identifiers
Objects from the dB like table, columns, etc 
	City, Name, Population, etc etc

##### Comments 
-- for single line 
/* * / for multi line

##### Data Definition Language (DDL)
defines structure of the database
##### Data Query Language (DQL)
retrieves data from the database 
##### Data Manipulation Language (DML)
manipulates data stored in dB 
##### Data Control Language (DCL)
controls dB user access
##### Data Transaction Language (DTL)
manages dB transactions 
##### ALTER TABLE
adds, deletes, or modifies columns of an existing table 
```
ALTER TABLE table_name
ADD/CHANGE/DROP column_name datatype;
```

##### UPDATE statement
modifies existing rows in a table 
uses the SET clause to specify new column values 
uses optional WHERE clause to specify condition, if WHERE Omitted then all rows are updated 
```
UPDATE table_name
SET column1 = value1, column2 = value2, ...
WHERE condition
```

##### DELETE statement
deletes existing rows in a table 
FROM keyword is followed by table name whose rows are to be deleted 
Optional WHERE clause to state condition, omitting the where clause results in all rows in table being deleted 
```
DELETE FROM table_name
WHERE condition;
```

##### TRUNCATE statement
deletes all rows from a table
nearly identical to DELETE with no WHERE clause
```
TRUNCATE TABLE table_name;
```

##### MERGE statement
selects data from one table, called the source, and inserts data to another table called the target 

##### Primary Key 
column, or group of columns, used to identify a row 
PK is usually first column in the table 

##### Simple Primary Key 
consists of a single column 
##### Composite Primary Key 
consists of multiple columns
##### Auto Increment Column
numeric column that is assigned an automatically increasing value when a new row is inserted
##### Common user errors when inserting PKs
Inserting values for auto-incrementing PKs
Omitting values for PKs that are not auto-incrementing 
##### Foreign Key 
Column, or group of columns, that refer to a PK 
datatypes for Foreign and PK must be the same, but names can differ
##### Foreign Key Constraint 
added to the FK declaration statement with the REFERENCE keyword 
When constraint is specified, dB rejects insert, update, and delete statements that violate referential integrity 

##### Referential Integrity actions
when referential integrity is broken, can be updated manually but is labor and error prone, can be automatically fixed with some actions
##### RESTRICT
rejects any insert, update, or delete that violates referential integrity 
##### SET NULL
set invalid foreign keys to NULL
##### SET DEFAULT 
set invalid foreign keys to default value 
##### CASCADE 
Propagates primary key changes to foreign key 
##### Constraint
rule that governs allowable values in a dB 
based on business and relational rules 
implemented with special keywords in CREATE TABLE statement 
##### BETWEEN Operator
alternative way to determine if value is between two other values 
`WHERE HIREDATE BETWEEN '2001-01-01' AND '2020-01-01`
##### LIKE Operator 
Used in a WHERE clause, matches text against a pattern using the two wild card characters % and _ 
%
	matches any number of characters
_
	matches exactly one character 
`WHERE Language LIKE 'A%'`
##### ABS(n)
returns absolute value of n
##### LOWER(s)
returns lowercase s string
##### TRIM(s)
returns string s with no leading/trailing spaces
##### HOUSE(t) MINUTE(t) SECOND(t)
returns hour, minute, second from time t 
##### Aggregate Function 
processes values from a set of rows and returns a summary value 

##### COUNT()
counts number of rows in a set 
##### MIN()
finds minimum value in the set
##### MAX()
finds all maximum value in the set
##### SUM()
sums all the values in the set 
##### AVG()
computes the arithmetic mean of all the values in the set 
##### HAVING clause 
used with the GROUP BY caluse to filter results 

##### Join
is a select statement that combines data from two talbes know as the left table and right table into a single result 
Tables are combined by comparing columns from the left and right table, usually with the = operator 
columns must have compareable datatypes

##### AS
column name can be replaced with an alias using the optional AS keyword 

##### INNER JOIN
selects only matching left and right table rows
##### FULL JOIN
selects all left and right table rows regardless of match 
##### LEFT JOIN
selects all left table rows but only matches with right table rows
##### RIGHT JOIN 
Selects all right table rows but only matches with left table rows
##### OUTER JOIN
any join that selects unmatched rows
##### UNION
keyword that combines two results into one table

##### Equijoin
compares columns of two tables with the = operator 
most joins are equijoins
##### Non-Equijoin
joins that compare with any operator other then = 
##### Self-Join
joins a table to itself
##### Cross-Join
combines two tables without comparing columns
##### Subquery
query within a query
sometimes called Inner Query or Nested Query 
##### Materialized View
view for which data is stored at all times
Whenever base table changes, corresponding view tables can also change so material view must be updated

##### WITH CHECK OPTION 
when specified, dB will reject inserts and updates that do not satisfy the view query WHERE clause 
dB generates an error message that explain the violation 

##### Entity-Relationship Model 
high-level representation of data requirements, ignoring implementation details 
##### Entity
Person, place, product, concept, or activity 
##### Relationship 
Statement about two entities 
##### Attribute 
Descriptive property of an entity 
##### Reflexive Relationship 
When an entity relates to itself 

##### Entity-Relationship Diagram/ ER Diagram
schematic picture of entities, relationships, and attributes
Entities are drawn as a rectangle 
##### Entity Type
set of things
i.e all employees in a company
##### Relationship Type
set of related things
i.e Employee-Manages-Department
##### Attribute Type
set of values 
i.e All employee salaries 

##### Entity Instance
An individual thing
i.e Sam Snead 
##### Relationship Instance 
statement about entity instance 
i.e 'Sam Snead manages IT'
##### Attribute Instance
an individual value 
i.e Salary: $35,000

##### Analysis 
develops ER model, caputring data requirements while ignoring implementation details
##### Logical Design 
converts ER model into table, columns, and keys for particular dB system
##### Physical Design 
adds indexes and specifies how tables are organized on storage media 

##### Analysis Steps
1. Discover Entities, Relationships, and Attributes
2. Determine Cardinality 
3. Distinguish Strong/Weak entities
4. Create super/subtype entities
##### Logical Design Steps
5. implement entities
6. implement relationships
7. implement attributes
8. Apply normal form 
##### Cardinality 
refers to maxima and minima of relationships and attributes
##### Relationship Maximum
greatest number of instances one entity can realte to a single instance of another entity 
##### Relationship Minimum 
the least number of instances of one entity that can relate to a single instance of another entity 
appears in parenthesis 
##### Subtype Entity 
Subset of another entity type called the supertype entity 
i.e managers is a subset of employees
##### IsA relationship 
identifies relationship between Sub/Supertype entities 
##### Partition 
a partition of a supertype entity is a group of mutual exclusive subtype entities 
##### Crows Foot Notation
depicts cardinality as a circle (zero), a short line (1), or three short lines (many)
##### Intangible Entity 
documented in the data model, but not tracked with data in the database
##### Primary Keys
Need to be 
###### STABLE 
should not change, when PK value changes statements that specify old value must also change and PK new value must cascade down to foreign keys
###### Simple
Primary Key values should be easy to type and store. Small values are easy to specify in an SQL WHERE clause and speed up query processing 
###### Meaningless 
PK should not contain descriptive information about the entity 

##### Artificial Key
single column primary key created by dB designer when no suitable single or composite PK exists 
Usually integers, generated automatically by dB as new rows are inserted
Still Simple, Stable, and Meaningless 

##### Functional Dependence
dependence of one column on another is called functional dependence 
##### Redundancy 
is the repetition of related values in a table
##### Normal Forms
rules for designing tables with less redundancy 
##### Candidate Key
simple or composite keys that are minimal and unique 
dB designer designates 1 candidate key to be the PK 
##### Minimal 
means all columns are necessary for uniqueness 
##### non-Key
column that is not contained in a candidate key
##### Third-Normal form 
whenever a non-key column A depends on column B, then B is unique
##### Boyce-Codd Normal Form
whenever column A depends on Column B then B is unique
gold standard for normalization, ideal for tables with frequent updates, deletes, and inserts 

##### Trivial Dependencies 
When the columns of A are subsets of columns of B, A always depends on B and are called Trivial
##### Normalization 
eliminates redundancy by decomposing a table into two or more tables
##### Denormalization 
means intentionally introducing redundancy 
##### Heap Table
no order imposed on rows 
optimize insert operations 
fast for bulk load of many rows since rows are stored in load order 
##### Sorted Table
has a sort column that determines physical row order
##### Hash Table 
rows are assigned to buckets based on their hash, the modulo function is common has function 
##### Table Cluster/Multi-Tables
interleave rows of two or more tables in the same storage area
##### Table Scan
dB operation that reads table blocks directly without accessing an index
##### Index Scan
dB operation taht reads index blocks sequentially in order to located needed table blocks 
##### Hit Ratio 
filter factor or selectivity
percentage of table rows selected by a query 
##### Binary Search 
dB splits the index until it finds the entry containing the search value 
##### Dense Index
contains an etnry for every table row
##### Sparse Index
Contains entry for every table block 
##### Hash index
Hashes the data and puts it in a bucket
##### Bitmap index
uses 1s and 0s to map the data 
##### Logical Index
reference to a physical index
##### Tablespace
dB object that maps one or more tables to a single file CREATE TABLESPACE
CREATE INDEX index_name
ON TableName (column1, column2, ...);



