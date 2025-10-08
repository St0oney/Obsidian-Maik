**Austauschformate**
um an technischen Schnittstellen Daten auszutauschen können verschiedene Formate genutzt werden. 
-> binäre Daten
	0 und 1, hat den Vorteil, dass sie sehr effizient gespeichert werden können. 
-> unstrukturierter Text
	darunter fallen z.b. .txt Dateien, SMS, etc. Sie haben kein Format.
-> strukturierter Text
	strukturierter Text kann sowohl vom Mensch als auch vom System gelesen werden. Sie haben eine strukturierte Form und müssen bestimmte Regeln einhalten
	Beispiele hierfür sind JSON oder XML

## XML
strukturiert die Informationen in einer hierarchischen Textdatei. 
Sie besteht aus verschiedenen Elementen.Die Namen der Elemente werden immer mit <> eingeklammert und danach folgt der Inhalt. Am Ende wird nochmals der Name mit </> eingeklammert. 
-> <> öffnendes tag
-> </> schließendes tag

**Wurzelelement**
Eine XML Datei hat immer genau ein Wurzelelement, welches am Anfang der Datei steht (nach der obligatorischen xml version und dem encoding)
darunter werden dann verschiedene Elemente eingeordnet.

**einfaches Element**
ein einfaches Element hat als Inhalt nur Zeichenketten

**komplexes Element**
enthalten weitere Elemente und Attribute

**Attribute**
stehen nur im anfangstag des Elements und erweitern dieses um eine Eigenschaft
es können mehrere Attribute in einem Element vorhanden sein 
-> kleinste Informationseinheit in XML

Es gibt zwei Stufen, zur Überprüfung einer XML Datei. Damit eine XML Datei Korrekt übermittelt werden kann, wird sie geprüft, ob sie wohlgeformt ist. 
-> alle tags sind mit einem Ende Tag geschlossen
-> nur ein Wurzelelement
-> alle Attribute in ""

Die meisten Systeme nehmen wohlgeformte XML Dateien an, allerdings  gibt es auch Systeme , die eine gültige XML Datei fordern. 

Wenn die XML Datei außerdem noch nach einem angegebenen Schema aus einer XSD Datei definiert ist, handelt es sich um eine gültige XML Datei. 
## XSD - Definition von XML Sprachen

das Schema für XML Dateien wird in Form von XML Sprache in einer .xsd Datei gespeichert. 
Eine XSD Datei gibt das Schema für eine XML Datei vor. In ihr werden Elemente definiert, die unterschiedliche Typen haben können

-> simpleType
	-> einfache Datentypen
-> complexType
	-> enthalten eine festgelegte Menge von einfachen und komplexen Elementen

außerdem unterscheidet XML noch zwischen lokalen Elementtypen und globalen Elementtypen. 

**lokale Elementtypen**
sind selbst Teil eines Elementes und nur in diesem nutzbar

**globale Elementtypen**
werden am Anfang oder am Ende des Schemas definiert und können von allen Elementen verwendet werden. 

**Kompositoren**
durch Kompositoren wird definiert, wie Kindelemente eines komplexen Elementes  definiert werden dürfen 

-><xs:sequence> gibt die Reihenfolge vor
-> <xs:choice> gibt eine Auswahl, wobei nur eins davon möglich ist
-> <xs:all> gibt an, dass alle enthalten sein müssen, egal in welcher Reihenfolge

**Häufigkeiten**
wenn man nun ein Element hat, das ein Attribut hat, dass nicht überall vorhanden sein muss, so kann man das mit den Attributen minOccurs und maxOccurs definieren. Dadurch kann man Multiplizitäten abbilden -> analogie zum Klassendiagramm 

## Ableitung aus XML in ein Klassendiagramm
aus einer XML Datei lässt sich ein Klassendiagramm ableiten. Dazu identifiziert man alle globalen und Elemente aus dem Schema und alle komplexen Elemente. 
-> Diese bilden die Klassen ab. 
-> Anschließend werden alle Subelemente und Attribute als Attribute der Klassen modelliert. 
-> Zum Schluss werden dann über die Kompositoren und die Häufigkeit der auftretenden Elemente die Assoziationen definiert. Die Attribute minOccurs und maxOccurs werden dabei als Multiplizitäten dargestellt. 

## Spezifikation von Webservices mit WDSL
WDSL ist eine Art der XML, die für Webservices genutzt wird. Ein Webservice ist eine Funktion, die zustandlos arbeitet, d.h. er liefert bei der eingabe des gleichen Parameters immer das gleiche Ergebnis. 
Ein Webservice hat außerdem eine URL, über die er aufgerufen werden kann. 





