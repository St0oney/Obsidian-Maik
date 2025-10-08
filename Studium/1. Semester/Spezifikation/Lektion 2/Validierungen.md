Damit in Eingabeelemente, in die beliebige Werte eingetragen werden können, auch Werte eingetragen werden, die für das System nutzbar sind, müssen Validierungsregeln festgelegt werden. 

**Validierungsregeln** 
sind häufig ein Boolescher Ausdruck (Ja / Nein) nach dem dann ausgewertet wird, ob die Bedingung erfüllt ist. 

*Pflichtfeld*
wurden alle erforderlichen Werte eingegeben

*Umwandlung*
ist das Format korrekt und kann vom System genutzt werden?
	-> danach folgt die Konvertierung
	
*Plausibilität*
prüft ein oder mehrere Felder auf das logische Zusammenspiel, ggf. auch über mehrere Dialogmasken verteilt.
Bsp.: Alter, Startdatum, etc. 

***

**Zeitpunkt der Auswertung (Transaction Level)**
manche Validierungsregeln müssen nicht sofort ausgewertet werden, sondern sind abhängig davon, wann Werte eingegeben werde. 
Bei der Plausibilitätsprüfung zum Beispiel werden bestimmte Bedingungen manchmal über mehrere Dialogmasken verteilt und können dementsprechend erst zu einem bestimmten Zeitpunkt ausgewertet werden. 

folgende Beispiele gibt es

- Verlassen eines GUI Elementes
- Verlassen einer Seite (Dialogmaske)
- Zwischenspeichern der Daten
- Senden der Daten an das System

***

**Art der Validierung**
Validierungen werden nicht nur dazu eingesetzt, um Eingaben auf Fehler zu überprüfen. Es bietet auch die Möglichkeit, dem User Hinweise zu geben. Beispielsweise, man kauft ein Ticket für einen Zu und dieser hat Verspätung. Dann kann ein Hinweisfeld auftauchen, in dem gewarnt wird, dass es bei dieser Verbindung zu Verspätungen kommen kann. 

***

**Darstellung fehlgeschlagener Validierungen**
Wenn eine Validierung fehlschlägt, wird dies oft mit einem Rot umrandeten Feld, bei den entsprechenden Eingabeelementen angezeit, oder ein roter hilfetext erscheint, um dem User zu beschreiben, was der Fehler ist. 

