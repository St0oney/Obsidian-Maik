in Java werden Klassen zu Paketen zusammengepackt. Diese können dann wiederum über Bibliotheken bereitgestellt werden. Es gibt die Java-Standard-Bibliothek, die einige nützliche Klassen enthält. Sie ist so in die Sprache integriert, das sie nicht dem Classpath hinzugefügt werden muss, jedoch nicht alle Klassen können dadurch automatisch genutzt werden. Manche erfordern das Schlüsselwort import am Anfang des Quellcodes, damit die Klassen eines bestimmten Paketes genutzt werden können. 

***folgende Pakete gibt es in der Standardbibliothek***
**java.applet** -> Programmierung html basiertert im Browser ausführbarer Oberflächen
**java.awt** -> GUI-Programmierung mit AWT
**java.beans** -> Datencontainer zur Übertragung, Datenobjekte für  Persistenzframeworks
**java.io** -> Ein-/Ausgabe-Operationen, Datenströme
**java.lang** -> Fundamentale Klassen wie z.b. String (muss nicht importiert werden)
**java.net** -> Netzwerkfunktion
**java.nio** -> Zugriff auf virtuelle Dateisysteme, z.B. über FTP
**java.rmi** -> Entfernter Objektzugriff, Zugriff wie lokaler Zugriff, aber Ausnahmen abfangen
**java.security** -> Zertifikate, Kryptographie
**java.sql** -> Datenbankfunktion
**java.util** -> Klassen für Datenstrukturen
**javax.swing** -> GUI-Programmierung mit Swing

Wenn man nun einen externe Bibliothek in sein Programm einbinden möchte, muss man die kompilierten Dateien der Bibliothek zunächst dem Classpath/Buildpath hinzufügen. 
Anschließend kann man im Source Code mit dem Schlüsselwort import die Klasse oder ganze Pakete, die man benötigt (in dem man nach dem Paketname ein * setzt) hinzufügen. 

zu jeder Bibliothek sollte eine passende Dokumentation existieren, die Infos über die Paketstruktur, Klassen und Methoden, die die Bibliothek beinhaltet gibt. Außerdem beinhaltet die Dokumentation

