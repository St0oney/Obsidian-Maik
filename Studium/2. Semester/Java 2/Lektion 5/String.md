der String ist in Java kein Primitiver Datentyp, sondern eine Klasse. Es ist jedoch so ein Elementarer Teil der Programmiersprache, das Java einige Möglichkeiten bietet, damit zu arbeiten. 

Zeichenketten werden zwischen "das ist ein String" geschrieben. Um einen String mit einem anderen String zu verbinden, nutzt man den + Operator.

 Außerdem lassen sich damit auch primitive Datentypen mit Strings verknüpfen:
 "das ist ein String" + "und das ist ein" + 2 + ". String"

*String bietet mehrere Konstruktoren an:*
-> parameterloser Konstruktor = leerer String
-> Copy Konstruktor = erzeugt eine Kopie
-> String(char[] value) = String aus gesamten Array+

um aus Booleans einen String zu erstellen nutzt man entweder einen leeren String + "boolean" oder man nutzt die statische Methode .valueOf()

für die umgekehrte Version, kann man die Methode der Wrapper Klassen nutzen. 

*Umwandlung von Strings in primitive Datentypen:*
![[Pasted image 20250422193853.png]]

*Für Vergleiche oder zum überprüfen des Inhalts eines Strings gibt es die folgenden Methoden*
-> .endsWith 
-> .startsWith 
-> .contains 
-> equals()
-> equalsIgnoreCase()
-> compareTo()
	-> wird lexikografisch verglichen (alphabetisch)

-> indexOf() -> erstes vorkommen 
-> lastIndexOf() -> letztes vorkommen

**Ein String lässt sich nicht direkt manipulieren, da sie immutable sind.**
*Es gibt jedoch einige Methoden, um neue Strings aus bestehenden Strings heraus zu erstellen.:*
-> substring(int beginIndex)
-> toLowerCase()
-> toUpperCase()
-> trim()
-> replace(char oldChar, char NewChar)
-> replace(CharSequence target, CharSequence replacement)
-> split(String regex)
	-> gibt immer ein Array zurück
		-> regex ist ein Trennzeichen ( , oder ; oder + oder ähnliches)

Beim arbeiten mit Strings entstehen oft viele temporäre Strings, die keine lange Lebensdauer haben, jedoch trotzdem Speicher verbrauchen. Insbesondere bei Verkettungen ist das der Fall. 
Das ist eine Konsequenz daraus, das Strings unveränderlich sind. 

Um das zu vermeiden, gibt es in Java die Klasse StringBuffer. 
### StringBuffer
Eine Instanz der Klasse StringBuffer kann man beliebig viele Strings anhängen, ohne das dabei ein neuer String erzeugt wird. Dafür wird die Methode append() benutzt.

Dabei werden die hinzugefügten Strings in einem Puffer gehalten und beim Aufruf der Methode toString, wird der resultierende String zusammengestellt. 









