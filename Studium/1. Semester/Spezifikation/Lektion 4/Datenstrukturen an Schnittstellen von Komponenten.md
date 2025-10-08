Um die Datenstruktur an einer Schnittstelle zu spezifizieren, eignet sich am besten ein UML Klassendiagramm. 

Zuerst müssen alle Schnittstellen der Komponente ausgemacht werden. Diese lassen sich aus einem Use-Case oder Komponentendiagramm ablesen. 

**Spezifikation von Interfaces**
Eine Schnittstelle muss mit einem Namen (Schnittstellendefinition), den benötigten Nachrichten und Ergebnistypen modelliert werden.
Schnittstellendefinition ergibt sich schon beim identifizieren der Schnittstelle aus einem anderen Diagramm. 
Die benötigten Nachrichten und Ergebnistypen lassen sich aus dem Aktivitäts und Sequenzdiagramm ablesen - jeder Aufruf und jede Antwort ist einer Funktion der Schnittstelle zugeordnet.
Im Aktivitätsdiagramm können die Objektknoten als Rückgabewert oder Parameter der jeweiligen Funktion abgelesen werden. 

**Spezifikation von Datenstrukturen**
Durch die Spezifikation der ausgetauschten Daten an einer Schnittstelle, wird festgelegt, wie die Daten strukturiert sein müssen und welche Informationen der Komponente zur Verfügung stehen. 

Grundsätzlich können Datenstrukturen in Form von Tabellen, ER Modellen oder einfachem Text beschrieben werden. 

die modellierung in einem UML Klassendiagramm lässt sich jedoch einfach in andere Diagrammarten integrieren und wird daher häufig dafür verwendet. 

Als Ergebnis haben wir eine Interfacebeschreibung, mit den zugehörigen Funktionen und Datenstrukturen
