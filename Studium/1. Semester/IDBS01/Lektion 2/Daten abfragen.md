***
*Daten abfrage geschieht in einem DBMS mit den Key Words SELECT und FROM *  
```SELECT * FROM Table1;```
```SELECT <Spalte1>,<Spalte2> FROM Table1;```
*ein SELECT Statement schließt immer mit einem ; ab.*
***
*Die Ergebnismenge einer Abfrage lässt sich durch sogenannte Klauseln modifizieren. folgende Klasueln gibt es*   

**Klauseln**   
DISTINCT -> gibt jeden Wert nur einmal aus

ORDER BY <Spalte1>(ASC),<Spalte2>(ASC) ASC/DESC -> sortiert auf oder absteigend
	-> Defaultwert ist aufsteigend (ASC)
	
GROUP BY <Spalte> -> Gruppiert Daten, die mit Aggregatsfunktionen bearbeitet werden können *Bsp.:*

```
SELECT Fach, AVG(Note) AS Durchschnitt
FROM Schülernoten
GROUP BY Fach;
```
HAVING -> mit HAVING, lassen sich gruppierte Ergebnismengen weiter einschränken
***

*Man kann eine Abfrage auch an eine Bedingung knüpfen. Das geschieht mit dem Key Word WHERE*

```SELECT <Spalte1> FROM Table1 WHERE <Spalte2>=<Bedingung1>```

*folgende Vergleichsoperatoren gibt es in SQL:*

'=' -> Gleichheit
'!=' -> Ungleichheit
'>,<' -> größer als, kleiner als
'>=,<=' -> größer gleich, kleiner gleich
'BETWEEN' -> Einschränkungen auf Werteberich
'LIKE' -> Einschränkungen auf Muster <_uster>
'IS NULL' -> Kein Wert
'IS NOT NULL' -> auf jeden Fall Wert
'IN' -> Einschränkung auf Werteberich 

*Außerdem lassen sich die Bedingunen noch mit Logischen Operatoren erweitern:*

AND -> Verknüpfung von Bedingungen
OR -> entweder oder
NOT -> Negation

*Zudem gibt es noch die sogenannten Builtin Functions. Das sind Funktinen in einem DBMS, die bspw. das aktuelle Datum oder die Uhrzeit ausgeben.*

**Datumsfunktionen**
CURRENT_TIMESTAMP -> aktuelle Zeit
 CURRENT_DATE -> aktuelles Datum

**Numerische Funktionen**
ROUND() -> rundet eine Zahl auf definierte Stellen
MOD() -> Restdivision (Modulo)
ABS() -> Absolutwert

**Textfunktinen**
UPPER() -> Wandelt Zeichenkette in großbuchstaben
LOWER() -> Wandelt Zeichenkette in Kleinbuchstaben
REPLACE() -> Ersetzt einen Teil einer Zeichenkette

**Aggregatfunktionen**
*es werden mehrere Werte aggregiert - zusammengefasst*
SUM() -> Summe einer Spalte
AVG() -> Durchsnitt einer Spalte
COUNT() -> Anzahl der Zeilen
MIN() -> min Wert der Spalte
MAX() -> max Wert der Spalte
***
*Das Schlüsselwort AS kann dazu verwendet werden, Tabellen oder Spalten einen Alias zu geben - also die Ergebnismenge kann dadurch umbenannt werden.
wird in Verbindung mit KLasueln genutzt ist jedoch selbst keine Klausel*
***

SELECt Statements lassen sich außerdem verschachteln. Man kann also eine Abfrage mit SELECT erstellen und innerhalb dieser Abfrage, z.b. in der Bedingung noch eine Weitere SELECT Abfrage erstellen, mit deren Ergebnis dann die Parent Abfrage weitermacht.
