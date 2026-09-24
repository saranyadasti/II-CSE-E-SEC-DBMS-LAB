## 
```
SELECT sname,age FROM sailors;
```

## 2.
```
SELECT *FROM sailors
WHERE rating>7;
```

## 3.
```
SELECT sname
FROM sailors s,Reserves r
WHERE s.sid = r.sid
AND r.bid=103;
```

## 4.
```
SELECT DISTINCT r.sid FROM Reserves r, Boat b
WHERE r.bid=b.bid 
AND b.color='red';
SELECT DISTINCT r.sid FROM Reserves r, Boat b
WHERE r.bid = b.bid
AND b.color = 'red';
```

## 5.
```
SELECT DISTINCT sname FROM sailors s, Reserves r, Boat b
WHERE s.sid=r.sid AND r.bid=b.bid AND b.color='red';
```

## 6.
```
SELECT DISTINCT b.color
FROM sailors s, Reserves r, Boat b
WHERE s.sid = r.sid
AND r.bid = b.bid
AND sname = 'Lubber';
```

## 7.
```
SELECT DISTINCT s.sname
FROM sailors s,Reserves r
WHERE s.sid=r.sid;
```

## 8.
```
UPDATE sailors
SET rating = rating+1
WHERE sid IN (
SELECT r1.sid FROM Reserves r1,Reserves r2
WHERE r1.sid = r2.sid
AND r1.day = r2.day
AND r1.bid<>r2.bid 
);
```

## 9.
``` 
SELECT age FROM sailors
WHERE sname LIKE 'B-%B';
```

## 10.
```
SELECT DISTINCT bname
FROM sailors s,Reserves r,Boat b
WHERE s.sid = r.sid
AND r.bid = b.bid
AND b.color IN('red','green');
```

## 11.
```
SELECT s.sname 
FROM sailors s
WHERE EXISTS (
SELECT * FROM Reserves r, Boat b
WHERE s.sid = r.sid
AND r.bid = b.bid
AND b.color = 'red' )
AND EXISTS (
SELECT * FROM Reserves r,Boat b
WHERE s.sid = r.sid
AND r.bid = b.bid
AND b.color = 'green' );
```

## 12.
```
SELECT DISTINCT r.sid
FROM Reserves r,Boat b
WHERE r.bid = b.bid
AND b.color = 'red'
MINUS
SELECT DISTINCT r.sid FROM Reserves r,Boat b
WHERE r.bid = b.bid
AND b.color = 'green';
```

## 13.
```
SELECT sid FROM sailors
WHERE rating = 10 UNION
SELECT sid FROM Reserves 
WHERE bid=104;
```

## 14.
```
SELECT sname FROM sailors 
WHERE sid IN(
SELECT sid FROM Reserves
WHERE bid=103 );
```

## 15.
```
SELECT DISTINCT sname
FROM sailors s,Reserves r,Boat b
WHERE s.sid = r.sid
AND r.bid = b.bid
AND b.color = 'red';
```

## 16.
```
SELECT sname FROM Sailors
WHERE sid IN (
SELECT sid FROM Reserves
WHERE bid = 103 );
```

## 17.
```
SELECT * FROM Sailors
WHERE rating > ANY (
SELECT rating FROM Sailors
WHERE sname = 'Horatio' );
```

## 18.
```
SELECT * FROM Sailors
WHERE rating > ALL (
SELECT rating FROM Sailors
WHERE sname = 'Horatio' );
```

## 19.
```
SELECT * 
FROM Sailors
WHERE rating = (
SELECT MAX(rating) 
FROM Sailors );
```

## 20.
```
SELECT s.sname
FROM Sailors s
WHERE EXISTS (
SELECT * 
FROM Reserves r, Boat b
WHERE s.sid = r.sid
AND r.bid = b.bid
AND b.color = 'red')
AND EXISTS (
SELECT * 
FROM Reserves r, Boat b
WHERE s.sid = r.sid
AND r.bid = b.bid
AND b.color = 'green' );
```

## 21.
```
SELECT sname
FROM Sailors s
WHERE NOT EXISTS (
SELECT bid 
FROM Boat
MINUS
SELECT bid 
FROM Reserves
WHERE sid = s.sid);
```

## 22.
```
SELECT AVG(age) FROM Sailors;
```

## 23.
```
SELECT AVG(age) FROM Sailors
WHERE rating = 10;
```

## 24.
```
SELECT sname, age FROM Sailors
WHERE age = (
SELECT MAX(age) FROM Sailors);
```

## 25.
```
SELECT COUNT(*) FROM Sailors;
```

## 26.
```
SELECT COUNT(DISTINCT sname) FROM Sailors;
```

## 27.
```
SELECT sname FROM Sailors
WHERE age > (
SELECT MAX(age) FROM Sailors
WHERE rating = 10);
```

## 28.
```
SELECT rating, MIN(age)
FROM Sailors
GROUP BY rating;
```

## 29.
```
SELECT rating, MIN(age)
FROM Sailors
WHERE age >= 18
GROUP BY rating
HAVING COUNT(*) >= 2;
```

## 30.
```
SELECT b.bid, COUNT(*)
FROM Boat b, Reserves r
WHERE b.bid = r.bid
AND b.color = 'red'
GROUP BY b.bid;
```

## 31.
```
SELECT rating, AVG(age)
FROM Sailors
GROUP BY rating
HAVING COUNT(*) >= 2;
```

## 32.
```
SELECT rating, AVG(age)
FROM Sailors
WHERE age >= 18
GROUP BY rating
HAVING COUNT(*) >= 2;
```

## 33.
```
SELECT rating, AVG(age)
FROM Sailors
WHERE age >= 18
GROUP BY rating
HAVING COUNT(*) >= 2;
```

## 34.
```
SELECT rating FROM Sailors
GROUP BY rating
HAVING AVG(age) <= ALL (
SELECT AVG(age) FROM Sailors
GROUP BY rating);
```
