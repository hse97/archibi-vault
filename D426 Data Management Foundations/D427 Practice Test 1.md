1. d
2. d
3. c
4. b 
5. d WRONG CREATE INDEX IS DDL DATA DEFINITION LANGUAGE 
6. c
7. b
8. d
9. c
10. b,c
```
11.
CREATE TABLE Customer (
CustomerID INT UNSIGNED,
FirstName VARCHAR(50),
MiddleInitial CHAR(1),
LastName VARCHAR(50),
DateOfBirth DATE,
CreditLimit DECIMAL(6 ON DELETE SET NULL,2) UNSIGNED CHECK (CreditLimit < 20,000,000)
);
```

```
12.
CREATE TABLE Book (
Title VARCHAR(30),
GenreCode VARCHAR(5),
FOREIGN KEY (GenreCode) REFERENCES Genre(GenreCode);
);
```

```
13.
ALTER TABLE Automobile
ADD SafetyRating DECIMAL (3,1) UNSIGNED CHECK (SafetyRating < 80);
```

```
14.
CREATE VIEW MyBooks AS 
SELECT Title, Genre, Year 
FROM Book;
```

```
15.
DROP VIEW BookView; 
```

```
16.
ALTER TABLE Book
ADD PRIMARY KEY (ID); 
```

```
17.
ALTER TABLE Book
ADD FOREIGN KEY (Year) REFERENCES YearSales(Year);
```

```
18.
CREATE INDEX idx_year
ON Book(Year);
```

```
19.
INSERT INTO Book (Title, Genre, Year)
VALUES ('The Joy Luck Club', NULL, 1989);
```

```
20.
DELETE FROM Book
WHERE ID = 3; 
```

```
21.
UPDATE Book 
SET Year = 2022
WHERE Year = 2020;
```

22. c

23. a

```
24.
SELECT * 
FROM Book;
```

```
25.
SELECT Title, Genre
FROM Book
WHERE Year = 2020;
```

```
26.
SELECT Title
FROM Book
ORDER BY Title ASC;
```

```
27.
SELECT Genre, COUNT(Genre)
FROM Book
GROUP BY Genre
ORDER BY Genre DESC; 
```

27.
Being asked to count number of Movies having each type of Genre
Need to use GROUP BY clause to gruop all movies with each genre together and then do a COUNT 
Attribute you are grouping on must be listed first
DISTINCT keyword is for unique Genres

SELECT **DISTINCT** Genre, COUNT(* ) AS GenreCount
FROM Book
GROUP BY Genre
ORDER BY Genre DESC; 


```
28a.
SELECT TotalSales, Title
FROM YearSales
INNER JOIN Book ON YearSales.Year = Book.Year;
```

```
28b.
SELECT Title, TotalSales
FROM Book
INNER JOIN YearSales ON Book.Year = YearSales.Year; 
```

```
28c.
SELECT Title, TotalSales
FROM Book
LEFT OUTER JOIN YearSales ON Book.Year = YearSales.Year; 

```

```
29.
UPDATE Book
SET COST = COST + 1
WHERE COST <= 50.0; 
```

```
30.
SELECT COUNT(*)
FROM Book
WHERE Year = 2019;
```

```
31.
a. 
SELECT MAX(Cost)
FROM Movie; 
b.
SELECT AVG(Cost)
FROM Movie;
```

```
32.
SELECT EmployeeType, MAX(Salary)
FROM Employee
GROUP BY EmployeeType; 
```