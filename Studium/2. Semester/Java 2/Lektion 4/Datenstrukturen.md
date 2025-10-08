Um Daten zu organisieren und zu speichern, gibt es Datenstrukturen. Dafür werden Daten zusammen in definierten Strukturen gespeichert, was zu einem effizienteren Zugriff und struktuierterem Programm führt.

***Es gibt unterschiedliche Arten von Datenstrukturen:***

### Arrays
Arrays dienen dazu Daten vom gleichen Typ zu speichern. Dafür wird ein Array im Programm deklariert und eine Kapazität zugewiesen (Anzahl der Elemente im Array)
Daten in einem Array werden sequenziell gespeichert. 
Arrays können in unterschiedlichen Dimensionen genutzt werden.
- 1. Dimension, sie speichert Die Daten in einer "Liste" ab
- 2. Dimension speichert die Daten in einer Matrizze ab und wird oft für Tabellen genutzt
- 3. Dimension kann man sich als Würfel vorstellen, in dem die einzelnen Zellen belegt werden. Wird für 3D Volumen genutzt

Ein Array wird in Java mit dem Sichtbarkeitsmodifikator, dem Datentyp und eckigen Klammern und anschließend dem Bezeichner (Namen) deklariert.

*Beispiel aus dem Onlineshop*
	
	private Kunde[] kunden;

Anschließend muss das Array noch instanziiert werden. Bei der Instanziierung, wird dem Array die Kapzität mitgegeben,. 

	private Kunde[42] kunden;
	
Man kann auch direkt bei der instanziierung schon Werte mitgeben (Initialisierung), dadurch wird die Kapazität implizit festgelegt und muss nicht mit angegeben werden. 

	privat Kunde[] kunden;
	kunden = new Kunde[] {new Kunde("Name", "Nachname"),
						new Kunde("Name", "Nachname"),
						new Kunde("Name", "Nachname")	};

Die Kapazität eines Arrays kkann nachträglich nicht mehr geändert werden. Wenn man das machen möchte, muss man ein neues Array erstellen und die Werte übertragen. 

Arrays werden z.b. dafür genutzt, Anweisungen für mehrere Objekte anzuwenden, ohne das man für jedes Objekt die Anweisung neu programmieren muss. 
Das geschieht über das Attribut length des Arrays, damit kann man dan für jedes Objekt in dem Array eine bestimmte Anweisung ausführen lassen

*Beispiel:*
![[Pasted image 20250328121107.png]]

