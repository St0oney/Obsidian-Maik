Topic: [[*Datenbanken*]]
***

**INSERT INTO**
-> Um neue Datensätze zu einer Tabelle hinzuzufügen, nutzt man INSERT INTO 
*Bsp.:*
```
INSERT INTO table1 (spalte1,...,spalteN)
VALUES
(
	wert1,
	...,
	wertN
);
```

-> manche Spalten werden automatisch befüllt oder führen zum Fehler
*Bsp. automatische Werte*
	-> auto_increment
	-> Default Wert
	-> NULL Wert

**implizite Typumwandlung**
-> Wenn beim einfügen eines Wertes in eine Spalte, der Wert nicht mit dem, der beim erstellen der Tabelle deklariert wurde übereinstimmt, dann kommt es entweder zum Fehler oder der Wert wird automatisch (implizit) umgewandelt.
z.b. werden Decimalwerte gekürtzt, wenn ein INT wert deklariert ist, oder ein varchar() wird abgeschnitten etc. 

-> bei komplexen Datentypen, wird bspw. dann einfach ein Defalut wert genommen
*Bsp.:*
```
INSERT INTO KTEST 
VALUES 
(
’2014–11–11’, 
’12:12:12’, 
’2014–11–11 12:12:12’, 
’2014–11–11’, 
’12:12:12’, 
’2014–11–11 12:12:12’
);
 
INSERT INTO KTEST 
VALUES 
(
’2014’,
’122X’, 
’2014 122’, 
’2014’, 
’122’, 
’2014 122’);
```

*resultiert in:*

| datumNull  | zeitNull | zeitpunktNull       | datumNotNull | zeitNotNull | zeitpunktNotNull    |
| ---------- | -------- | ------------------- | ------------ | ----------- | ------------------- |
| 2014–11–11 | 12:12:12 | 2014–11–11 12:12:12 | 2014–11–11   | 12:12:12    | 2014–11–11 12:12:12 |
| 0000–00–00 | 00:01:22 | 0000–00–00 00:00:00 | 0000–00–00   | 00:01:22    | 0000–00–00 00:00:00 |

-> für solche Fälle, gibt es Umwandlungsfunktionen, mit denen Der Wert explizit gesetzt werden kann


DATE(), TIME(), TIMESTAMP()

*Bsp.:*
```
INSERT INTO KTEST 
VALUES 
(
DATE(’2014’), 
TIME(’122X’), 
TIMESTAMP(’2014 122’), 
DATE(’2014’), 
TIME(’122’), 
TIMESTAMP(’2014 122’)
);
```

**Kopieren von Datensätzen**
-> Beim kopieren von Datensätzen, werden INSERT INTO und SELECT kombiniert
-> Anzahl der Spalten und Datentypen müssen bei Quelle und Ziel gleich sein

