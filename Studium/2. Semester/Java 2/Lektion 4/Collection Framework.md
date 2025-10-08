Collections sind eine Gruppe von Objekten
- Listen
- Maps
- Queues
- Stacks
- Sets
Mithilfe des *Collection Frameworks* kann man mit diesen Mengen arbeiten und sie bearbeiten. 

das Collection Interface hat folgende Methoden
![[Pasted image 20250402210920.png]]

Außerdem sieht man auf dem Bild, dass durch die Iterable SChnittstelle, die Methode iterator implementiert ist, und diese ein Objekt vom Typ E zurückgibt. 

Iterable ist eine Schnittstelle, die es einer Collection ermöglicht, für jedes einzelne Element einer Collection eine Anweisung durchzulaufen. 
Iterable wird von der Collection SChnittstelle erweitert. 

### Listen

Listen sind Teil des Collection Frameworks und erben direkt von der Schnittstelle Collection.
-> java.util.List

eine Liste speichert ihre Daten mit einem Index ab und haben somit eine feste Reihenfolge. Zusätzlich zu den von Collection implementierten Methoden, bietet Lists noch folgende Methoden an:

```void add(int index E element) ```
-> Fügt ein Element an der Stelle index ein

```boolean addAll(int index, Collection<? extends E> c)```
-> Wie oben, kann allerdings ein anderes Objekt sein, dass allerdings in einer Vererbungsbeziehung mit dem ursprünglich implementierten Objekt stehen muss. 

```E remove(int index)```
-> Löscht ein Objekt an der Stelle index

```subList(int fromIndex, int toindex)```
-> liefert einen entsprechenden Ausschnitt der Liste

Es gibt 2 unterarten der Liste - ArrayList und LinkedList

*ArrayList*
speichert ihre Elemente in einem Array 
-> schnellet Zugriff
-> aufwändigere Änderung

*LinkedList*
-> doppelt verkettet - Referenz auf Nachfolger und Vorgänger
-> Zugriff dauert länger, da die Liste von vorne oder von hinten durchlaufen werden muss, bis das gewünschte Element erreicht ist. 

### Sets
Ein Set ist eine Menge von Objekten, die in keiner Reihenfolge gespeichert. Ein Set lässt keine doppelten Objekte zu. 
java.util.set erweitert ebenfalls die Schnittstelle Collection. 

Set bietet keine zusätzlichen Methoden zu denen aus der Collection Schnittstelle an. 
Set hat aber in seiner Dokumentation Regeln bestimmt, die bei der Implementierung der SChnittstelle eingehalten werden müssen - Contracts

Es gibt 2 häufig eingesetze Sets

*TreeSet*
sortiert die Elemente in einer Baumstruktur

*HashSet*
nutzt intern eine Hash-Tabelle
-> eine *Hashtabelle* errechnet aus dem Wert eines Elementes und einem SChlüssel einen Hash, der dann als Index dient. Das Element wird dann in einem Bucket gespeichert
	-> falls eine Kollision auftritt - 2 Elemente haben den gleichen Hash, dann kann man eine Bucketlist verwenden - das Element wird in dem Bucket einer Elementliste angehängt oder es wird nach dem nächsten freien Slot gesucht und dieser wird genutzt - muss dann bei der Suche auch implementiert werden. 


### Stacks
Ein Stack arbeitet nach dem Last In First Out Prinzip. 
Stacks sind eigentlich eine veraltete Schnittstelle, die aus der ebenfalls veralteten Schnittstelle Vector, welche wiederum von List und diese weiderum von Collection erbt. 

Als Alternative, bzw. als Empfehlung der Entwickler von Java, wird deswegen die Schnittstelle Deque genutzt und deren Implementierung ArrayDeque genutzt. 

Deque erweitert die Schnittstelle Queue welche die SChnittstelle Collection erweitert. 

Für die Nutzung als Stack, werden bei der Schnittstelle ArrayDeque folgende Methoden implementiert:_

*addFirst*
-> fügt ein Element an erster Stelle hinzu

*peekFirst*
-> ürüft, ob eine Element vorhanden ist

*removeFirst*
-> entfernt das erste Element


### Queues 
Eine Queue arbeitet nach dem First In First Out Prinzip und erweitert ebenfalls die Collection Schnittstelle. 
Die Methoden *add(), remove() und element()* der Schnittstelle Collection, haben in Queue eine Alternative, da sie im Fehlerfall eine Exception auswerfen. 
*offer(), poll() und peek()* geben dafür einen Rückgabewert aus. 

Queue hat sehr viele erweiterungen und bietet für viele Fälle unterschiedliche Queues an
![[Pasted image 20250409191508.png]]



# Maps

Die Maps Schnittstelle gehört auch zum Collections Framework, erbt aber nicht von Collection. 

Maps funktionieren prinzipiell so, dass sie Schlüssel auf Werte abbilden. es wird also eine Assoziation zwischen einem Wert eines Objektes und einem definierten Schlüssel hergestellt. 

-> Schlüssel einer Map sind immer eindeutig
-> Wenn ein Schlüssel bereits existiert, wird der Wert einfach überschrieben
-> Es gibt unterschiedliche implementierungen der Klasse Map

*HashMap*
-> intern eine Hashtable
-> unsortiert
-> schneller Zugriff
-> längere dauer zum speichern eines Elementes

*TreeMap*
-> Baumstruktur
-> Sortierung anhand des Schlüssels
-> Bei der Suche muss ggf. der gesamte Baauam durchlaufen werden
-> einsortierung ist schneller, da kein Hashwert errechnet werden muss (vgl. HashMap)

*LinkedHashMap*
-> doppelt verkettete Liste
-> Form der HasahMap, kombiniert mit LinkedList

*WeakHashMap*
-> Form der HashMap 
-> Laufzeitumgebung kann bei Speicherknappheit Elemente löschen
-> 


---
### Wrapper-Klassen
mit Wrapper Klassen, lassen sich primitive Datentypen als Objekte darstellen. Das ist sehr hilfreich, da Collections keine primitiven Datentypen nativ speichern kann. 
Mit den Wrapper Klassen, lässt sich dies aber umgehen.

-> Wrapper Klassen eines primitiven Datentypen sind immutable (unveränderlich)
-> 
