die Spezifikation von technischen Systemschnittstellen wird mit Aktivitätsdiagrammen und Sequenzdiagrammen abgebildet. 

**Aktivitätsdiagramm**
Im Aktivitätsdiagramm sind Partitionen abgebildet, die die Komponenten darstellen. zwischen den Partitionen befinden sich die Objektknoten, die als Nachrichtenaustausch zwischen den Komponenten dienen. 
der Objektknoten ist dabei ein Parameter oder Rückgabewert, der von einer Funktionen einer der Komponenten an die andere weitergereicht wird. 
Im Aktivitätsdiagramm werden komplexe Abläufe unter einbeziehung der Kommunikation der Sschnittstellen abgebildet. 

**Sequenzdiagramm**
Das Sequenzdiagramm stellt einen detaillierten Ablauf dar, der sich zwischen den Komponenten bzw. Systemen abspielt. 
Es werden alle Details des Ablaufs beschrieben. 
-> Authentifizierung
-> Autorisierung
->etablieren eines Kommunikationskanals
-> Status, Prüf oder Fehlermeldungen
Außerdem wird aus dem Sequenzdiagramm ersichtlich, zu welchem Zeitpunkt was stattfindet. 

*Das Sequenzdiagramm besteht aus:*
 -> Interaktionspartnern 
	 -> Rechteck mit Beschriftung
	 
 -> Lebenslinien
	 vom Interaktionspartner ausgehend nach unten (gestrichelt)
	 beschreibt den Zuständigkeitsbereich

-> Aufruf
	-> durchgezogene Linie mit Pfeilspitze

-> Antwort
	-> gestrichelte Linie mit Pfeilspitze

-> Aktivierungsbalken
	-> zeigt an, wann der Interaktionspartner aktiv ist

-> kombiniertes Fragment
	-> ein Rahmen mit einer Kennzeichnung oben links
		-> Parallelisierung
		-> Wiederholung
		-> Alternativen
		-> optionale Nachrichten

mit dem kombinierten Fragment, kann man die oben genannten Beispiele in einem Diagramm dokumentieren. 
