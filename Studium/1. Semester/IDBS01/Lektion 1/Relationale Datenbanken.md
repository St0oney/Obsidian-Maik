*Relationale Datenbanken werden genutzt, um große Datenmengen effizient und Konsistent abzuspeichern. Außerdem muss es in der Lage sein, das viele Nutzer gleichzeitig darauf Zugreifen und Daten änder, löschen und neue  Daten hinzufügen können. 
*** 
*Der Aufbau eines solchen Systems umfasst 3 bzw 2 Teile.

**1. Das DBMS**   
*Das DBMS ist das Datenbankmanagementsystem. Über dieses System, wird die Datenbank verwaltet. 
Es kann die Datenbank ändern, löschen, Zugriffe für Benutzer gewähren und sorgt dafür, das die Integrität der Daten gewahrt bleibt - Konsistenz.*

**2. Die Datenbank***
*Die Datenbank selbst, beinhaltet die Daten. Die Daten werden innerhalb der Datenbank in Tabellen (Relationen) gespeichert. In den Tabellen werden die Daten in Datensätze unterteilt die Datensätze haben Attribute, die über die Spalten definiert werden.

*diese 2 Systeme zusammen werden als Datenbanksystem bezeichnet.
Die Benutzer, die nachher mit dem System arbeiten, arbeiten nicht auf dem DBMS, sondern auf einer externen Anwendung, die Zugriff auf die Datenbank gibt.*
***
### SQL
*wenn man mit einem DBMS arbeitet, kommt man ncht umhin, SQL zu benutzen.
SQL - Structured Query Language ist eine Programmiersprache, mit der man die Daten einer Datenbank bearbeiten kann. 
Sie teilt sich in die folgenden Bereiche auf. 

**Data Manipulation Language**
*beinhaltet Befehle, um die Daten in einer Datenbank zu lesen und zu manipulieren*

**Data  Definition Language**
*beinhaltet die Befehle zu Änderung des Datenschemas*

**Transaction Control Language**
*beinhaltet die Befehle, um bei Transaktionen die Konsistenz - die referentielle Integrität bei Ausführungen der DML zu sichern.*

**Data Control Language**
*beinhaltet die Befehle, um den Zugriff auf die Daten zu managen - Zugriffsrechte*

**Builin Functions der DBMS Systeme**
*Builin Functions sind z.b. DAtumsfunktionen, zum abrufen von Zeitwerten, Zeichenkettenfunktionen, Numerische Funktionen und Aggregatfunktionen *

*Die Builtin Funcrtions umfassen alle Funktionen, mit denen die Ergebnismenge einer Abfrage manipuliert werden kann.*

**Klauseln**
*Klauseln, werden dazu verwendet, die Ergebnismenge zu sortieren*


