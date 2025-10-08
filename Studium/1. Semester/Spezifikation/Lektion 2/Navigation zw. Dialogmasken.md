ein in Prozess wird auf mehrere Dialogmasken aufgeteilt, weil das je nach Menge der Informationen viel übersichtlicher ist. 
Bei mehreren Dialogmasken muss spezifiziert werden, in welcher Reihenfolge die Masken aufgerufen werden, sowie Manuelle Möglichkeiten, wie man durch die Masken navigieren kann. 
Außerdem wird spezifiziert, ob die Navigation automatisiert werden kann. Beispielsweise, wenn manche Masken übersprungen werden können, da sie durch eine Benutzereingabe überflüssig geworden sind. 

der Dialogfluss wird meistens mit einem UML Zustandsdiagramm dokumentiert. 
Es werden alle Möglichen durchläufe durch die Masken in einem Diagramm abgebildet. 

![[Pasted image 20250221130903.png]]

**Standardnavigationen**
Außer dem normalen Ablauf eines Prozesses, müssen noch gewisse Standardnavigationen spezifiziert werden. 
Dazu gehört z.b. der Aufruf der Hilfeseite oder des Impressums

**Ausnahmenavigationen**
dazu zählt z.b. das schließen einer Maske oder, wenn ein unerwarteter Fehler auftritt. 

Diese Arten der Navigationen müssen von allen Masken aus Möglich sein. 
Die Spezifikation hierür sollte bei allen Masken gleich, deswegen lässt sich das veralgemeinert einmal in der Dokumentation darstellen und muss nicht für jede Maske einzeln nochmal gemacht werden, da dies ein erheblicher Mehraufwand wäre. 
