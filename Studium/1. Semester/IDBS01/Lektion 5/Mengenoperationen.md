Topic: [[*Datenbanken*]]
***

*Das Ergebnis einer SELECT Abfrage ist aus mathematischer Sicht immer eine Menge.
die Mengen, die bei SELECT Abfragen herauskommen, lassen sich mit verschiedenen Mengenoperationen kombinieren.*

folgende Mengenoperationen gibt es:

**UNION**
-> Duplikat-frei - doppelte Zeilen werden entfernt
-> Anzahl und Datentyp der Spalten, der SELECT Statements müssen gleich sein

**UNION ALL**
-> alle Zeilen werden ausgegeben
-> Anzahl und Datentyp der Spalten, der SELECT Statements müssen gleich sein

**INTERSECT**
-> Schnittmenge - gibt alle Zeilen zurück, die in beiden Abfragen vorkommen
-> Duplikat-frei
-> Anzahl und Datentyp der Spalten, der SELECT Statements müssen gleich sein

**EXCEPT/MINUS**
-> Duplikat-frei
-> Gibt die Zeilen zurück, die in der ersten Abfrage ausgegeben werden, Minus denen, die gleich sind wie in der zweiten
-> SELECT1 - Schnittmenge von SELECT1+SELECT2
