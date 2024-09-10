##### Database Application 
	software that helps business users interact with database systems 

## Database Roles 
##### Database Administrator 
	responsible for securing the database system against unauthorized users. A database adminstrator enforces procedures for user access and database systems availability 
##### Authorization 
	limited access to specific tables based on user. Only authorized users to access specific data

##### Rules
	Database systems ensure data is consistent with structural and business rules 

##### Query Processor
	interprets queries, creates a plan to modify the database or retrieve data, and returns query results to the application 
	Performs query optimization to ensure the most efficient instructions are executed on the data 

##### Storage Manager 
	translates the query processeor instructions into low-level file-system commands that modify or retrieve data
	Database size range from megabytes to terabytes so storage manager use **Indexes** to quickly locate data

##### Transaction Manager 
	Ensures transactions are properly executed. 
	Prevents conflicts between concurrent transactions 
	Transaction manager also restores the database to a consistent state in the event of a transaction or system failure 

MongoDB, NoSQL, Opensource, 5 

##### INSERT
	inserts rows into a table
##### SELECT
	retrieves data from a table
##### UPDATE
	modifies data in a table 
##### DELETE 
	deletes rows from a table

##### CREATE TABLE 
	creates a new table by specifying the table and column names. Each column is assigned **data type** that indicates the format of column value. Data types can be numeric, textual, or complex 

##### INT
	stores integer values
##### DECIMAL 
	stores fractional numeric values 
##### VARCHAR
	stores textual values
##### DATE
	stores Year-Month-Day

## ANALYSIS, LOGICAL DESIGN, PHYSICAL DESIGN 

##### Analysis
	specifies database requirements without regard to specific database system 
	Requirements represented as entities, relationships, and attributes
		Entitiy: Person place or thing 
		Relationship: Link between two entitites 
		Attribute: Description of an entity 
	has many alternative names
		Conceputal Design, Entitiy-Relationship Modeling, and requirement definition 

##### Logical Design
	phase implements database requriements in specific database systems 
	For relational dB systems, logical design converts entities, relationships, and attributes into tables, keys, and columns 

##### Physical Design
	phase adds indexes and specifies how tables are organized on storage media
	Physical design effects query processing speed but never query processing results
###### Data Independence: Idea that physical design does not alter results

##### Application Programming Interface/API
	simplifies use of SQL with general-purpose language, dB programs typically use any application programming interface 

##### MySQL Command-Line Client
	text interface included with MySQL server download 
###### Error Code
	MySQL server returns when SQL statement is syntatically incorrect or dB cannot execute the statement 

##### Tuple
	an ordered collection of elements enclosed in parenthesis 
		(a,b,c) and (c,b,a) are different ordered tuples


The data structure organizes data in tables: 
##### Table
	has a name, fixed tuple of columns, and a varying set of rows
##### Column 
	has a name and a data type 
##### Row 
	Unamed tuple of values. 
	Each value corresponds to a column and belongs to the column's data type 
##### Data Type
	named set of values, from which column values are drawn 
##### Cell
	a single column of a single row 

A table must have one column but any number of rows 

##### Empty Table
	table without rows

Since a table is a set of rows, the rows have no inherent order 
Some common synonyms: 
Table: 
	File, Relation
Row:
	Record, Tuple
Column: 
	Field, Attribute 

##### Business Rules 
	based on business policy specific to particular database 

##### Literals
	Explicit values that are string, numeric, or binary 
	Strings must be surrounded by single quotes or double quotes 
	Binary values are represented with x '0' where 0 is any hex value
		Examples:
		'String'
		"String"
		123
		x'0fa2'

##### Keywords
	Words with special meaning in SQL
	Examples:
		SELECT
		WHERE
		FROM

##### Identifiers
	Objects from the database like tables, columns, etc 
	Examples:
		City
		Name
		Population

##### Comments 
	You know 
	-- for single line comments
	/* XYZ */ for multi line comments

SQL Languages is divided into five sub languages: 
##### Data Definition Language (DDL)
	Defines the structure of the database
##### Data Query Language (DQL)
	Retrieves data from the database
##### Data Manipulation Language (DML)
	manipulates data stored in database
##### Data Control Language (DCL)
	controls database user access
##### Data Transaction Language (DTL)
	Manages dB transactions

##### Data Independence
	allows dB Admins to improve query performance by changing the organization of data on storage devices, without affecting query results 

##### CREATE TABLE
	creates a new table by specifying the table name, column name, and column data type
		CREATE TABLE table_name (
		column1 datatype,
		column2 datatype,
		.....
		);
##### DROP TABLE
	drops existing table in a dB along with table's rows/data
		DROP TABLE table_name;

Examples of Data Types:
##### INT or INTEGER 
	integer values
##### VARCHAR(N)
	values with 0 to N characters
##### DATE
	date values YYYY-MM-DD
##### DECIMAL(M,D)
	numeric value with M digits and D decimals

##### ALTER TABLE
	adds, deletes, or modifies columns of an existing table 
		ALTER TABLE table_name
		ADD column_name datatype;
##### Data Type
	named set of values from which column values are drawn from

##### Integer
	can represent positive and negative numbers
	several integer data types exist
	TINYINT
		1 byte
		Signed: -128 to 127
		Unsigned: 0 to 255
	SMALLINT
		2 bytes
		Signed: -32,768 to 32,767
		Unsigned: 0 to 65,535
	MEDIUMINT
		3 bytes
		Signed: -8,388,608 to 8,388,607
		Unsigned: 0 to 16,777,215
	INT
		4 bytes
		Signed: -2,147,483,648 to 2,147,483,647
		Unsigned: 0 to 4,294,967,295

##### %(Modulo)
	divides one numeric number by another and returns remainder
		5 % 2 = 1

##### ^
	raises one numeric power to another
		5^2 = 25
#####  =
	compares two values for equality
		1 = 2 -> FALSE
##### !=
	compares two values for inequality
		1 != 2 -> TRUE

##### UPDATE
	modifies existing rows in a table
	uses the SET clause to specify the new column value 
	optional WHERE clause for condition 
		UPDATE table_name
		SET column1 = value1, column2 = value2,...
		WHERE condition;

##### DELETE
	deletes existing rows in table 
	keyword FROM is followed by table who's rows are to be deleted 
	optional WHERE clause for condition 
		DELETE table_name 
		WHERE condition;

##### TRUNCATE
	statement deletes all rows from a table
	nearly IDENTICAL to  DELETE with no WHERE clause

##### MERGE
	selects data from one table, called the source, and inserts the data to another table, called the target


##### Primary Key
	a column, or group of columns, used to identify a row
	Primary key is usually the table's first column 

##### Simple Primary Key
	primary key consisting of one column
##### Composite Primary Key
	Primary key consisting of more then one column
##### Auto-Increment Column 
	is a numeric column that is assigned an automatically increasing value when a new row is inserted

##### Common Mistakes when Inserting Primary Keys
	Inserting values for auto-incrementing primary keys
	Omitting values for primary keys that are not auto-incrementing

##### Foreign Key
	Column or group of columsn taht refer to a primary key 
		Datatypes must be the same, but names can differ

##### Foreign Key Constraint
	added to a CREATE TABLE statement with the FOREIGN KEY and REFERENCES keyword
	When constraint is specified, dB rejects inserts, updates, and deletes that violate referential integrity 

##### Referential Integrity Actions
	dB's can automatically correct statements that violate referntial integrity 
	need SQL constraints as keywords in the statement

##### RESTRICT
	rejects an insert, update, or delete that violates referential integrity 
##### SET NULL
	set invalid foreign keys to NULL
##### SET DEFAULT 
	sets invalid foreign keys to the foreign key default value 
##### CASCADE
	propegates primary key changes to foreign keys

##### Constraint
	a rule that governs allowable values in a dB 
	based on relational and business rules
	constraints are added and dropped with the ALTER TABLE statement 
		ALTER TABLE table_name
		ADD constraint;

##### BETWEEN 
	provides alternative way to determine if value is between two other values 
		value BETWEEN minValue AND maxValue 
			inclusive

##### LIKE 
	used in WHERE clause, matches text against a pattern using the two wildcard characters % and __
	%
		Matches any number of characters 
		'L%T' will match 'Lt' and 'Loot'
	_
		matches one character exactly 
		'L_T' will match 'Lot' but not 'Loot'

##### ORDER BY
	clause orders selected rows by ASC or DESC values 

##### ABS(n)
	returns absolute value of n
	SELECT ABS(-5); -> returns 5

##### LOWER(s)
	returns lowercase string s
		SELECT LOWER('MySQL'); -> returns 'mysql'
##### TRIM(s)
	returns string s without leading and trailing spaces
		SELECT LOWER('MySQL'); -> returns 'mysql'
##### HOUR(t), MINUTE(t), SECOND(t)
	returns hour, minute, or second from time t
		SELECT MINUTE('22:11:00') -> returns 11

##### Aggregate Function
	processes values from a set of rows and returns a summary value 
	appear in the SELECT clause and process all rows that meet the WHERE condition, if no WHERE Then all rows

##### COUNT()
	counts number of rows in the set
##### MIN()
	finds minimum value in the set
##### MAX()
	finds max value in the set
##### SUM()
	sums all value in the set
##### AVG()
	Finds mean of all values in the set

##### HAVING
	clause used with the GROUP BY clause to filter group results

##### Join
	a SELECT statement that combines data from two tables known as the left table and the right table into a single result 
	columns must have compareable datatypes

##### AS
	alias keyword 

##### join clause
	determines how query handles unmatched rows

##### INNER JOIN
	selects only matching left and right table rows
##### FULL JOIN
	select all left and right table rows regardless of match 
		matches with null for unpartnered rows

##### LEFT JOIN
	Selects all left table rows, only matches right table rows
##### RIGHT JOIN
	selects all right table rows, only matches left table rows

##### Outer join
	any join that selects unmatched rows including left, right, and full joins 

##### UNION
	combines the two results into one table

##### Equijoin
	compares columns of two tables with the = operator
	most joins are equijoin

##### Non-Equijoin
	compares columns with an operator other than =, such as < and > 

##### Self-Join
	joins a table to itself

##### Cross-Join
	combines two tables without comparing column 

##### Subquery
	query within another SQL query
		nested or inner query 
		

##### Alias
	temporary name assigned to column or table 
		Uses AS keyword

##### Materialized View
	view for which selected data can be stored 

##### WITH CHECK OPTION
	dB rejects inserts and updates that do not satisfy the view query WHERE clause 

##### Entity-Relationship Model 
	high-level representation of data requirements, ignoring implementations details

##### Entity Type
	set of things
	Ex: All employees in a company
##### Relationship Type
	a set of related things
	Ex: Employee-Manages-Departmnets
##### Attribute Type
	set of values
	Ex: Employee Salaries

##### Entity Instance
	Individual Thing
##### Relationship Instance
	Statement about entity instance
##### Analysis 
	develops entity-relationship-model capturing data requirements while ignoring implementation details 
##### Logical Design
	converts entity-relationship-model into tables, columns, and keys for particular dB system
##### Physical Design 
	adds indexes and specifies how tables are organized on storage media 

##### Analysis Steps:
	1. Discover entities, relationships, and attributes
	2. Determine Cardinality
	3. Distinguish strong and weak entities 
	4. Create supertype and subtype entities
##### Logical Design Steps
	5. Implement Entities
	6. Implement Relationships
	7. Implement Attributes
	8. Apply Normal Form

##### Cardinality
	Refers to maxima and minima of relationships and attributes
##### Relationship Maximum
	greatest number of instances of one entity that can relate to a single instance of another entity
##### Relationship Minimum 
	least number of instances of one entity that can relate to a single instance of another entity 
	minimums appear in parenthesis 

##### Subtype Entity 
	subset of another entity type called the supertype entity 

##### IsA Relationship 
	identifying relationship 

##### Partition 
	group of mutually exclusive subtype entities 

After entities, relationships, attributes, cardinality, and strong and weak entities are determined, dB designer llooks for supertype and subtype entities 

Creating supertype and subtype entities is the last of four analysis steps

Logical design converts entity-relationship models to tables columns and keys in a specific dB system

##### Crows Foot Notation
	depicts cardinality as a circle (zero), a short line (one), or three short lines (many). The three short lines look like a bird's foot, hence the name 'crow's foot notation'

##### Primary Keys:
###### Stable
	Primary key value should not change. When PK value changes, statements that specify old value must also change. New primary key value must cascade to matching foreign keys
###### Simple
	PK values should be easy to type and store 
	Small values are easy to specify in an SQL where clause and speed up query processing. 
###### Meaninglessness
	Not containing any descriptive information 

##### Artificial Key
	single-column primary key created by dB designer when no suitable single-column or composite key exists 
	usually integer, usually auto generated

##### Functional Dependence 
	dependence of one column on another

##### Redundancy 
	repetition of related values in a table
##### Normal forms 
	rules for designing tables with less reduncancy 
##### Candidate Key
	simple or composite column that is unique and minimal 
##### Minimal 
	means all columsn are necessary for uniqueness 
	table can have several candidate keys
	designates one candidate key the primary key
##### non-key
	column not contained in candidate key
##### Third normal form
	whenever a non-key column A depends on column B, then B is unique
