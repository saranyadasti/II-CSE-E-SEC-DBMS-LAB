## CREATING SAILORS TABLE
```
CREATE TABLE Sailors(
sid NUMBER,
sname VARCHAR2(20),
rating NUMBER,
age REAL );
```

##  DESCRIBE THE SAILORS TABLE
```
DESC sailors;
```


## INSERTING VALUES INTO SAILORS TABLE
```
INSERT INTO sailors VALUES(22,'Dustin',7,45.0),(29,'Brutus',1,33.0);
INSERT INTO sailors VALUES(31,'Lubber',8,55.5),(32,'Andy',8,25.5),(58,'Rusty',10,35.0),(64,'Horatio',7,35.0),(71,'Zorba',10,16.0),(74,'Horatio',9,35.0),
(85,'Art',3,25.5),(95,'Bob',3,63.5); 
```


## DISPLAY THE SAILORS TABLE
```
SELECT * FROM Sailors;
```
