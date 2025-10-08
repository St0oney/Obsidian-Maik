Topic: [[*Datenbanken*]]
***

  **INNER JOIN**
-> führt alle Datensätze zusamen, zu denen das Verbundkriterium erfüllt ist
-> Alle Spalten sind in der Ergebnistabelle enthalten
-> Beim Inner Join muss mit On oder Using angegeben werden, anhand welcher Kriterien der Join ausgeführt werden soll

Bsp.: Verbundkriterium ist der ForeignKey/PrimKey der Tabelle1
```
SELECT * FROM Table1 INNER JOIN Table2 ON table1.tableID=table2.table1ID;
```

**LEFT/RIGHT JOIN**
-> fürt alleSpalten der links vom Join stehenden Tabelle mit der rechts vom Join stehenden zusammen. Falls dadurch Lüclen in den Spalten der rechten Tabelle entstehen sollten, werden diese mit NULL befüllt 
-> der Right Join funktioniert genau umgekehrt
-> mit ON oder Using als Parameter gibt man das Kriterium an, nachdem die Datensätze verbunden werden
```
SELECT * FROM Table1 LEFT JOIN Table2 ON Table1.Table1ID = Table2.Table1ID;
```
**NATURAL JOIN**
-> führt alle Datensätze der angegebenen Tabellen mit gleichen Spalten zusammen
-> benötigt keine explizites Kriterium
```
SELECT * FROM Table1 NATURAL JOIN Table2;
```

