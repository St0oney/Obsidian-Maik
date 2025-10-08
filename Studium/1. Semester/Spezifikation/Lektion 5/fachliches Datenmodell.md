das fachliche Datenmodell ist gewissermaßen die Grundlage für die Spezifikation. Auf Basis des Datenmodells werden GUIs, Komponenten, Systemverhalten und diverse Schnittstellen spezifiziert. 
Das Datenmodell ist sozusagen das Gerüst, mit dem alles weitere gebaut werden kann. 

typische Dokumentationsformen eines Datenmodells sind die folgenden:

## UML Klassendiagramm
Das UML Klassendiagramm ist ein Strukturdiagramm. Hier werden fachliche und technische Elemente auf typebene  spezifiziert. Das fachliche Umfeld wird dabei betrachtet und dargestellt. 
	-> Personen, Objekte, Systeme werden in Klassen abgebildet und mit ihren jeweiligen Eigenschaften und Beziehungen zueinender spezifiziert. 
Dabei handelt es sich bei den Klassen im Klassendiagramm noch nicht um konkrete Objekte, sondern vielmehr das Konzept, aus dem später dann Objekte abgeleitet bzw. spezifiziert werden können. (Objektdiagramm)

folgende Elemente/Aspekte sind dabei zu berücksichtigen:

**ID Attribut**
über das ID Attribut ist ein Objekt eindeutig identifizierbar. Es ist nur über die Dauer des Lebenszyklus des Objektes gültig.

**Vollständigkeit der Attribute**
insbesondere bei Schnittstellen wichtig, dass beide Seiten auch das gleiche Format verwenden und keine Attribute verloren gehen. 

**Detaillierte Eigenschaften der Attribute**
Beispiel hierfür sind Datentypen, Multiplizität (Beziehung), Defaultwert, optionale Eigenschaften - readonly, unique, ..., Constraints

![[Pasted image 20250310203508.png]]

**Enumerations**
Enumarations sind fest vorgegebene Wertemengen, meist aus einem Dropdown menü auswählbar. Diese Werte können nicht verändert werden. 
Enumerations können von allen Klassen des Modells genutzt werden, solange ein dafür vorgesehene Attribut bei der Klasse implementiert ist. 
![[Pasted image 20250310204007.png]]

**Constraints**
Für Datenmodelle können außerdem Contraints spezifiziert werden. siehe Lektion 3.3. Diese definieren, über Terme - Sätze, was wann möglich oder nicht möglich ist. 
*Bsp.:*
„Ein Kunde mit einem durchschnittlichen Jahresbestellwert von >= 2500 EUR erhält den Status Premiumkunde.“

**Beziehungen**
Beziehungen werden mit Linien und der entsprechenden Multiplizität dargestellt. 
0,1,0..*

**Spezifikation von Funktionen**
zum Teil werden auch im Datenmodell schon fachlich wichtige Funktionen als Methoden modeliert. 
z.b. Umsatzrechner, oder ähnliches. 
Keine Trivialen Sachen

## Objektdiagramm
Das Objektdiagramm ist ebenfalls ein Strukturdiagramm und kann dazu genutzt werden, Klassendiagramme zu überprüfen. Dabei werden die Ausprägungen einer Klasse aus einem Klassendiagramm genau spezifiziert. 

Objekte haben konkrete Werte und damit lassen sich bestimmte komplexe Systemzustände darstellen. 
Wenn im Klassendiagramm Beziehungen als Multiplizitäten dargestellt werden, so wird im Objektdiagramm jedes einzelne Objekt dargestellt. 

*Notationselemente*
Objektnamen werden mit einem vorangestellten : und optinal davor einem AttributsID dargestellt. 

Beziehungen werden einfach nur mit einer Linie dargestellt. Der Attributname wird dabei an die Linie geschrieben. 

Wenn man mit dem Objektdiagramm ein Klassendiagramm überprüfen möchte sollte man immer reale Werte nehmen. Damit lassen sich repräsentative Ergebnisse erzielen. 

## Typische Elemente eines fachlichen Datenmodells
Die Einzelnen Elemente in einem fachlichen Datenmodell lassen sich zur besseren Übersicht in die folgenden Kategorisieren

**Entitäten** 
haben eine fachliche identität und einen Lebenszyklus. Die Eigenschaften sind veränderbar. Z.b. Person, Vertrag, etc. 
haben eine relaiv lange Lebensdauer
Historisierung - d.h. es werden Änderungen an der Entität gespeichert, damit man alles nachvollziehen kann. Außerdem haben Entitäten immer eine AttributsID

**Werte/Werteobjekt**
sind Objekte ohne Identität. Sie sind nicht veränderbar, haben keinen Lebenszyklus und kein ID Attribut. 
Werteobjekte enthalten z.B. Werte von Attributen, die von Entitäten ausgelagert werden können. Ein gutes Beispiel sind Adressen. 

**Dienste**
sind zustandlose Fachfunktionen, die keiner Entität oder einem Werteobjekt zugeordnet werden können. 
Sie haben keine eigenen Attribute, sondern Arbeiten nur mit den Parametern und Rückgabewerten anderer Entitäten. 






