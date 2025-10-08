Bei der Spezifizierung von Komponenten, werden ebenfalls unterschiedliche Arten von UML Diagrammen eingesetzt. 
Das Verhalten einer Komponente kann mit einem Use Case Diagramm dargestellt werden. 

**Aktivitätendiagramm**
Die internen Abläufe in einer Komponente, können mit einem Aktivitätendiagramm (acd) dargestellt werden. 
Bei einem acd werden die einzelnen Akteure einer Komponente als Partition (Spalte) dargestellt. Hier wird dann klar ersichtlich, welcher Akteur, welche Funktionen und welche Entscheidungen übernimmt. 

**Geschäftsregeln**
Mit Geschäftsregeln, lassen sich die Fukntionen einer Komponente, bzw. das zusammenspiel der Komponenten verfeinern und klar regeln. Sie dienen dem Kontrollfluss und der Ablaufsteuerung. 
Sie bestehen aus einem Kontext
-> Bezug zur fachlichen Funktion
Bedingung (WENN)
-> Wann wird die Regel angewendet
Aktion (DANN,SONST)
-> was soll passieren

Geschäftsregeln müssen immer Widerspruchsfrei und Vollständig sein
-> es dürfen keine Bedingugskombinationen existieren, bei denen nicht definiert ist, was passiert (Vollständigkeit)
-> Es dürfen keine Widersprüche in der Regel existieren (Bedingung darf nicht auf unterschiedliche Ergebnissaktionen führen)

**Entscheidungstabellen**
Wenn man nun komplexere Geschäftregeln hat, lassen sich diese einfach über Entscheidungstabellen darstellen. 

in einer Entscheidungstabelle stehen die Bedingungen über den Aktionen.
Dadurch werden die Unterschiedlichen Bedingungs-Kombinationen und Aktions-Kombinationen ersichtlich und können einfach zugeordnet werden. 

|                              |     |     |     |     |     |     |     |     |
| ---------------------------- | --- | --- | --- | --- | --- | --- | --- | --- |
| Bedingungen                  |     |     |     |     |     |     |     |     |
| Bestellwert >= 2000 EUR      | N   | J   | N   | J   | N   | J   | N   | J   |
| Alter Kunde >= 18 Jahre      | N   | N   | J   | J   | N   | N   | J   | J   |
| Kundenstatus == Premiumkunde | N   | N   | N   | N   | J   | J   | J   | J   |
| Aktionen                     |     |     |     |     |     |     |     |     |
| Ratenzahlung                 |     |     |     | X   |     |     |     | X   |
| Zahlung in 8 Wochen          |     |     | X   | X   |     |     | X   | X   |
| per Rechnung                 |     |     | X   | X   | X   | X   | X   | X   |
| Vorkasse                     | X   | X   | X   | X   | X   | X   | X   | X   |

**Zustandstabellen**
mit Zustandstabellen wird in einem System definiert, wie sich das System in unterschiedlichen Zuständen verhält. - Ähnlich den Entscheidungstabellen, aber mit dem Unterschied, dass sich die Zustandstabelle auf das innere des Systems konzentriert während die Entscheidungstabelle durch äußere Einflüsse bestimmt wird. 

| Aktionen        | Aktionen   | Aktionen        | Aktionen             |     |
| --------------- | ---------- | --------------- | -------------------- | --- |
| Zustände        | Stornieren | Bestellen       | Lieferadresse ändern |     |
| In Warenkorb    | –          | In Vorbereitung | In Warenkorb         |     |
| In Vorbereitung | Storniert  | –               | In Vorbereitung      |     |
| In Auslieferung | –          | –               | –                    |     |
| Bezahlt         | –          | –               | –                    |     |
| Storniert       | –          | In Vorbereitung | –                    |     |
| Zurückgesendet  | –          | –               | –                    |     |
