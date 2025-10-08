*Transaktionen gibt es, um die Konsistenz einer Datenbank zu gewährleisten, im Falle eines Ausfalls der Hardware, Fehler in der Anwendung oder im Betriebssystem.
Durch die Benutzung von Transaktionen im Mehrbenutzerbetrieb (große Datenbanken werden meistens von mehreren 1000 Benutzern gleichzeitig bearbeitet) entstehen durch Transaktionen jedoch weitere Fehlerquellen.
Diese nennt man Isolationsphänomene und werden im folgenden Beschrieben*

### Isolationsphänomene ###

**Dirty Read**   
*Beim Dirty Read Phänomen, laufen 2 Transaktionen parallel ab. Transaktion A startet, ruft den Preis ab (10,99) und ändert ihn (8,99) (UPDATE).
Gleich danach Startet die Transaktion B und ruft den Preis ab (8,99)Transaktion 1 hatte jedoch einen Fehler und führt deswegen einen ROLLBACK aus. Der Preis ist nun wieder bei (10,99).
Transaktion B hat jedoch den faslchen Wert gelesen. *

**Lost Update**   
*beim Lost Update Phänomen, laufen 2 Transaktionen parallel ab. Transaktion A ruft z.b. einen Preis ab (10,99), danach kommt Transaktion B und ruft den Preis ab (10,99), gleich im Anschluss wird der Preis von Transaktion B erhöht(13,99) (UPDATE)
und der COMMIT ausgeführt. Im Anschluss daran wird der Preis von Transaktion A niedriger gesetzt (8,99) und der COMMIT ausgeführt.*

**Non-repeatable Read**   
*Beim Non-repeatable Read, wird in einer Transaktion ein Wert 2 mal abgefragt. eine andere Transaktion führt jedoch zwischen den beiden abfragen eine Abfrage durch und ändert den Wert. Somit hat die Transaktion 2 unterschiedliche Werte abgefragt.
Ein Beispiel hierfür wäre ein Konto.: man fasst in einer Transaktion eine Abfrage des Kontostandes, eine Überweisung und dann nochmals eine Abfrage des Kontostandes zusammen. Nach oder vor der ersten Überweisung kommt aus einer 2. Transktion jedoch eine andere Überweisung, die den Kontostand ebenfalls ändert. Die 2. Abfrage stimmt dann nicht mit der differenz aus der 1. Abfrage und der Überweisung überein.*

**Phantom Read**   
*Das Phantom Read  Phänomen ist ähnlich dem Non-repeatable, jedoch wird hier das Datenschema manipuliert. Eine Spalte könnte gelöscht oder hinzugefügt werden*

### Isolationslevel ###   
*Um nun diese Phänomene zu umgehen gibt es verschiedene Isolationslevel.*

**Read Uncommited**   
*beim Read Uncommited, wird keines der oben beschriebenen Isolationsphänomene verhindert.*

**Read Commited**   
*Beim Commited, wird das Dirty Read und das Lost Update Phänomen verboten*

**Repeatable Read**   
Beim Repeatable Read, werden alle bis auf das Phantom Read verboten

**Serializable**   
*hier werden alle Transaktionen nacheinander ausgeführt. Das hat den Nachteil, dass die Transaktionen länger dauern, da der Zugriff öfter und länfer blockiert ist.*

#### Transaktionsschema ####
```
START TRANSACTION
STATEMENT 1
STATEMENT 2
...
COMMIT;
```
