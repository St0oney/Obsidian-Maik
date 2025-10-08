*Es gibt unterschiedliche arten, um Datensätze zu manipulieren:*

**aktualisieren - UPDATE**
*Schema des Update Befehls für Datensätze*
```
UPDATE article SET preis = "preis+2" WHERE preis <10
```
*wenn keine Bedingung gesetzt wird, werden alle werte in der Spalte geändert.*

**löschen - DELETE**
*Das DELETE Statement ist recht simpel*
```
DELETE  FROM tabelle WHERE bedingung;
```
*es werden alle Inhalte der Tabelle gelöscht, wenn kein Auswahlkriterium gesetzt wird.*

**ändern - ALTER**
*das ändern einer Tabelle/Datensätze ist ein spezieller Fall. Es beinhaltet folgende Elemente:*

*festlegen der Tabelle*
```ALTER TABLE <table1>```
*hinzufügen einer Spalte*
```ADD <Spaltendefinition>```
*ändern einer Spalte*
```*ALTER <Spaltendefinition>*``` *oder* ```MODIFY``` *je nach DBMS*
*löschen einer Spalte*
```DROP <Spaltendefinition>```
*hinzufügen / löschen eines Constraints*
``ADD <Constraint>
```DROP <Constraint>```

**referentielle Integrität**
*Wenn man Datensätze in einer DB manipuliert, muss man immer darauf achten, dass die referentielle Integrität erhalten bleibt. 
Um diesen Prozess zu vereinfachen, bzw. zu automatisieren gibt es die Statements 
ON DELETE und ON CASCADE,
außerdem müssen die fachlichen Abhängigkleiten der DB dem Entwicklerteam bekannt sein*



