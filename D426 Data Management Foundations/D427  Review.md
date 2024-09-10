##### CREATE VIEW
CREATE VIEW view_name AS 
SELECT column1, column2, ...
FROM table_name
WHERE condition;
##### CREATE INDEX
CREATE INDEX index_name
ON table_name (column1, column2, ....);

##### WHICH COMMAND IS AN EXAMPLE OF DATA DEFINITION LANGUAGE (DDL)
ALTER, CREATE, DROP
anything that creates, defines, or deletes the definitions of the database

![[Pasted image 20240908184416.png]]

##### UPDATE Statement
UPDATE table_name
SET Column = Parameter
WHERE condition; 
DO NOT USE TABLE KEYWORD

##### A new column must be added to the Table
Use the 
ALTER TABLE table_name
ADD column_name datatype 

##### Create A View 
CREATE VIEW view_name AS 
SELECT col1, col2, ... AS view_name 
FROM table_name

##### Delete a View 
DROP VIEW view_name; 

##### Add Primary Key 
ALTER TABLE table_name
ADD PRIMARY KEY (pk_column)

### Create Index 
ADD INDEX index_name 
ON table_name (column_to_be_indexed)

##### Inserting Values into Table
INSERT INTO table_name (col1, col2, col3, ....)
VALUES (value1, value2, value3, ....);

##### Deleting a row from a table 
DELETE FROM table_name 
WHERE condition; 

### Update Rows in Table 
UPDATE table_name
SET col = new_value
WHERE condition; 

DOES NOT USE THE TABLE KEYWORD

##### Order Results
SELECT columns
FROM table_name
WHERE condition 
ORDER BY column ASC/DESC; 

##### INNER JOINS ON SELF 
SELECT Alias.Attribute AS Alias, 2ndAlias.Attribute AS 2ndAlias
FROM table_name Alias
INNER JOIN table_name 2ndAlias ON Alias.PrimaryKey = 2ndAlias.ForeignKey; 

Inner joins do not need alias but are necessary 
Can use alias before declaring them with AS, recursive declaration 
DOES NOT USE LEFT/RIGHT keyword 

##### CREATING TABLES WITH CONSTRAINTS
In a create table statement, to check that data is within a certain list use
Attribute DataType CHECK (Attribute IN ('value1', 'value2', 'value3'))
	`Breed VARCHAR(20) CHECK (Breed IN ('Saddlebred', 'Paint',...))`
