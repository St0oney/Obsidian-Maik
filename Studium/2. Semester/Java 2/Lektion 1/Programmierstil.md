# Code Dokumentation

Um Code zu Dokumentieren, gibt es in Java ein Programm - Javadoc
Javadoc nutzt die Kommentare im Quellcode und erstellt daraus automatisch eine Dokumentation in Form eines HTML Dokumentes. 

**Kommentare**
einzeilige Kommentare werden mit // vorne gekennzeichnet. 
mehrzeilige Kommentare werden mit slash stern und stern slash "umklammert" 
Sie werden dazu verwendet, Erklärungen und Zweck von Klassen, Attributen und Methoden und deren Parametern direkt im Quellcode zu hinterlegen. 

um nun Javadoc zu nutzen, wird der Kommentar mit slash und 2 Sternchen begonnen und mit einem und einem slash beendet. 

Da Javadoc eine HTML Datei erstellt, kann man im Kommentar auch die Syntax von HTML nutzen. 

*Javadoc hat folgende Schlüsselworter*

@param - Beschreibung eines Parameters
@return - Rückgabe einer Methode
@throws - Mögliche Exceptions/Errors
@author - Informationen zum Author
@version - Verisonierung
@...

# Code Annotation

Code-Annotationen sind Metadaten, die Java während des Kompilierungsprozesses liest.
Hierüber werden Informationen weitergegeben, die den Sourcecode betreffen. 

*@Override* - zeigt, dass es sich um eine überschriebene Methode handelt. 
*@Deprecated* - zeigt an, dass es sich um veralteten Teil des Source Codes handelt

Code Annotationen werden direkt im Code und nicht in einem Kommentar gecodet
# Code Konvention

Code Konventionen haben sich über die Jahre hinweg etabliert, und dienen dazu, dass der Code übersichtlicher, strukturierter und auch für andere lesbar ist. Code Konventionen sind nicht obligatorsich, sind aber dadurch, dass man sich daran hält durchaus nützlich. 

**Beispiele**

- Klassen werden als Substantive benannt und immer mit einem großen Anfangsbuchstaben geschrieben. Wenn mehrere Wörter enthalten sind, werden diese auch mit großem Anfangsbuchstaben begonnen (CamelCase)

- Paketnamen werden immer klein geschrieben

- Methodennamen sind immer Verben mit kleinem Anfangsbuchstaben und folgend CamelCase

- Klassenkonstanten werden komplett  groß geschrieben und Wörter mit Unterstrich getrennt

- Attribute und Variablen sollten sinnvoll benannt werden - Hinweis auf Inhalt

- Zusammengehörige Dinge sollten zusammen stehen 
	- Aufbau von Klassen:
		  Paketdeklaration
		  Importe
		  Klassenvariablen/konstanten
		  Instanzvariablen
		  Konstruktoren
		  Getter u. Setter
		  andere  Methoden

![[Pasted image 20250325134428.png]]

- Codeblöcke
- Einrückung von Codeblöcken
	- Variablen zuerst
	- Jede deklaration in eine Zeile
	- Leerzeichen zwischen Anweisungsabschnitten die semantisch zusammenhängen
	- Leerzeichen zwiaschen Operanden
