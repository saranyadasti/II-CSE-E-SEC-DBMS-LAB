## Sailors table created
```
CREATE TABLE Sailors(
sid NUMBER,
sname VARCHAR2(20),
rating NUMBER,
age REAL );
```
## sailors values inserted
```
INSERT INTO sailors VALUES(22,'Dustin',7,45.0),(29,'Brutus',1,33.0);
INSERT INTO sailors VALUES(31,'Lubber',8,55.5),(32,'Andy',8,25.5),(58,'Rusty',10,35.0),(64,'Horatio',7,35.0),(71,'Zorba',10,16.0),(74,'Horatio',9,35.0),
(85,'Art',3,25.5),(95,'Bob',3,63.5);

```
## displaying sailors table
``` 
SELECT * FROM Sailors;
DROP TABLE Sailors:tt6i5u85 xjhflklq/j xiuxip4j z

CREATE TABLE Reserves(
sid NUMBER,
bid NUMBER,
day DATE );
DESC Reserves;
INSERT INTO Reserves VALUES(22,101,'10/10/98');
INSERT INTO Reserves VALUES(22,102,'10/10/98');
INSERT INTO Reserves VALUES(22,103,'10/8/98');
INSERT INTO Reserves VALUES(22,104,'10/7/98');
INSERT INTO Reserves VALUES(31,102,'11/10/98');
INSERT INTO Reserves VALUES(31,103,'11/6/98');
INSERT INTO Reserves VALUES(31,104,'11/12/98');
INSERT INTO Reserves VALUES(64,101,'9/5/98');
INSERT INTO Reserves VALUES(64,102,'9/8/98');
INSERT INTO Reserves VALUES(74,103,'9/8/98');
SELECT *FROM Reserves;


CREATE TABLE Boat(
bid NUMBER,
bname VARCHAR2(20),
color VARCHAR2(30) );
DESC Boat;
INSERT INTO Boat VALUES(101,'Interlake','blue'),(102,'Interlake','red'),(103,'Clipper','green'),(104,'Marine','red');
SELECT * FROM Boat;

```
### Screen Shots

![ exp2 output](op1.png)

