## To create reserves table
```
CREATE TABLE Reserves(
sid NUMBER,
bid NUMBER,
day DATE );
```
## Describe the values
```
DESC Reserves;
```
## Inserting the values into the reserves table
```
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
```
## Display the table
```
SELECT *FROM Reserves;
```
