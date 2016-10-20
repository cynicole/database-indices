Write an SQL query to:

* Find all rows that have an ingredient name of Brussels sprouts.
* Calculate the total count of rows of ingredients with a name of Brussels sprouts.
* Find all Brussels sprouts ingredients having a unit type of gallon(s).
* Find all rows that have a unit type of gallon(s), a name of Brussels sprouts or has the letter j in it.

Finally
* Implement a database index to speed up your above SQL queries.

* Find all rows that have an ingredient name of Brussels sprouts.
```
EXPLAIN ANALYSE
SELECT * FROM ingredients
WHERE name = 'Brussels sprouts';
```
![alt](http://i26.photobucket.com/albums/c150/cynicolersn/LaunchAcademy/01-01.png)
![alt](http://i26.photobucket.com/albums/c150/cynicolersn/LaunchAcademy/01-02.png)


* Calculate the total count of rows of ingredients with a name of Brussels sprouts.
```
EXPLAIN ANALYSE
SELECT COUNT(*) FROM ingredients
WHERE name = 'Brussels sprouts';
```
![alt](http://i26.photobucket.com/albums/c150/cynicolersn/LaunchAcademy/02-01.png)
![alt](http://i26.photobucket.com/albums/c150/cynicolersn/LaunchAcademy/02-02.png)

* Find all Brussels sprouts ingredients having a unit type of gallon(s).
```
EXPLAIN ANALYSE
SELECT * FROM ingredients
WHERE name = 'Brussels sprouts' AND unit = 'gallon(s)';
```
![alt](http://i26.photobucket.com/albums/c150/cynicolersn/LaunchAcademy/03-01.png)
![alt](http://i26.photobucket.com/albums/c150/cynicolersn/LaunchAcademy/03-02.png)

* Find all rows that have a unit type of gallon(s), a name of Brussels sprouts or has the letter j in it.
```
EXPLAIN ANALYSE
SELECT * FROM ingredients
WHERE unit = 'gallon(s)'
AND (name = 'Brussels sprouts' OR name LIKE '%j%');
```
![alt](http://i26.photobucket.com/albums/c150/cynicolersn/LaunchAcademy/04-01.png)
![alt](http://i26.photobucket.com/albums/c150/cynicolersn/LaunchAcademy/04-02.png)

```
CREATE INDEX ON ingredients(name);
```
