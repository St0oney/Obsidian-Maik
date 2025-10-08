eine Dialogmaske besteht aus mehreren Elementen, die für die Ein/Ausgabe von Informationen zuständig sind. 

**Atomare Elemente**
Atomare Elemente sind Elemente, die sich nicht weiter zerlegen lassen und mit denen einzelne Werte angezeigt oder bearbeitet werden können. Zu den atomaren Elementen gehören Labels, Textfelder, Checkboxen, Drop Down-Feld, Button, Links, Bilder und Icons

**Komposit-Elemente**
Komposit-Elemente bestehen aus mehreren atomaren Elementen und dienen der Strukturierung der GUI. 
Optionsfelder, Tabellen und Gruppierungen z.b. von mehreren Checkboxen sind Beispiele dafür. 

**Komplexe Elemente**
Komplexe Elemente implementieren meistens schon eine Validierungslogik und haben eine komplexe Darstellungslogik. Bsp. ein eingebetteter Kalender oder eine Map, eine Directory Struktur oder ein Editor.

*heutzutage bieten viele GUI Frameworks eine vielzahl an fertigen Komposit oder Komplexen Elementen zur verwendung an. Die atomaren Elemente können von nahezu jeder Plattform bereitgestellt werden.*

**Eingabe und Ausgabe von Datentypen**
Damit die fachlichen Daten korrekt vom System übernommen werden, muss man genau spezifizieren,welche Datentypen über welches Element eingegeben werden können. 
Tabelle1

für die Ausgabe z.b. Read Only Ansichten muss man spezifizieren, wie die einzelnen Datentypen ausgegeben werden sollen. 
Tabelle2

**Tabelle1**

| Datentyp                                                             | Beschreibung                                                                                                                                | Element für Dateneingabe                                                             |
| -------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------ |
| Zeichenkette (String);<br><br>bis 1000 Zeichen                       | Kurze Zeichenketten beliebiger Zeichen                                                                                                      | Textfeld<br><br>Mehrzeiliges Textfeld                                                |
| Text (String);<br><br>ab 1000 Zeichen                                | Lange Zeichenketten beliebiger Zeichen                                                                                                      | Mehrzeiliges Textfeld                                                                |
| Ganze Zahlen<br><br>(Integer, Long)                                  | Werte, die ganzen Zahlen entsprechen; erlaubte Zeichen 0–9, ggf. Vorzeichen                                                                 | Textfeld                                                                             |
| Zahlen<br><br>(Float, Double)                                        | Werte, die Zahlen mit Komma entsprechen (sogenannte Gleitkommazahlen), erlaubte Zeichen 0–9, „,“, ggf. Vorzeichen                           | Textfeld                                                                             |
| Geldbeträge<br><br>(Amount)                                          | Angaben von Geldbeträgen, typischerweise mit zwei Nachkommastellen                                                                          | Textfeld                                                                             |
| Datum<br><br>(Date)                                                  | Angabe von Datumswerten, typischerweise mit Tag, Monat und Jahr; ggf. auch die genaue Uhrzeit                                               | Textfeld<br><br>Kalender                                                             |
| Wahrheitswert<br><br>(3-state-Boolean)                               | Angabe von Wahrheitswerten (Ja/Nein) unter Berücksichtigung, dass auch gespeichert wird, ob der Anwender diesen Wert bewusst eingegeben hat | Checkbox (nur ja/nein)<br><br>Drop-Down-Box (für 3-state-Boolean)<br><br>Optionsfeld |
| 1-aus-N-Auswahl; Aufzählungstypen<br><br>(Zeichenketten oder Zahlen) | Auswahl genau eines Wertes aus einer Menge vorgegebener Werte                                                                               | Drop-Down-Box<br><br>Optionsfeld<br><br>Mehrere Checkboxen                           |
| M-aus-N-Auswahl; Aufzählungstypen<br><br>(Zeichenketten oder Zahlen) | Auswahl von mehreren Werten aus einer Menge vorgegebener Werte<br><br>Hinweis: Wird häufig durch mehrere Einzelauswahlen realisiert.        | Mehrere Checkboxen                                                                   |
**Tabelle2**

| Element für Dateneingabe | Elemente für Datenausgabe                                                                                                                            |
| ------------------------ | ---------------------------------------------------------------------------------------------------------------------------------------------------- |
| Textfeld                 | Einfacher Text, skaliert automatisch nach unten,<br><br>Leerer Text wird durch „---“ dargestellt                                                     |
| Mehrzeiliges Textfeld    | Einfacher Text, skaliert automatisch nach unten, berücksichtigt Zeilenumbrüche;<br><br>Leerer Text wird durch „---“ dargestellt                      |
| Kalender, Datumseingabe  | Einfacher Text, formatiert, Datumsformat typischerweise abhängig von der Lokalisierung des Nutzers;<br><br>Leeres Datum wird durch „---“ dargestellt |
| Drop Down-Box            | Einfacher Text,<br><br>Keine Auswahl wird durch „---“ dargestellt                                                                                    |
| Optionsfeld, Checkbox    | Für jede gewählte Option jeweils festgelegte Labels oder Icons                                                                                       |
|                          |                                                                                                                                                      |

***

**Aufzählungstypen**
Wenn das System in mehreren Sprachen verfügbar sein soll, dann muss zusätzlich spezifiziert werden, wie Auswahlmenüs angezeigt werden. Die Namen von Städten, Ländern oder Orten ist nicht in jeder Sprache gleich. Außerdem ändert sich dadurch evtl. auch die Reihenfolge in der diese angezeigt werden. Das System selbst arbeitet z.b. mit einem technischen Label, das in jeder Sprache gleich ist. Basierend auf der Sprachauswahl des Benutzers, soll dem User aber das sprachlich korrekte Label angezeigt werden. 

folgende Tabelle veranschaulicht das

|Aspekt|Beschreibung|
|---|---|
|Fachliches Label<br><br>(pro Wert);<br><br>Ggf. mit Berücksichtigung von Internationalisierung|Text, der dem Nutzer als auswählbarer Wert in der GUI angezeigt wird; in der Regel abhängig von der gewählten Sprache<br><br>Im Beispiel: Name der Stadt in der gewählten Sprache<br><br>Jeder auswählbare Wert muss in jede der in der Anwendung verfügbaren Sprachen übersetzt werden, ggf. muss ein Standardwert festgelegt werden, falls eine konkrete Übersetzung nicht verfügbar ist.<br><br>Im Beispiel: Übersetzung des Stadtnamens in alle relevanten Sprachen|
|Technisches Label<br><br>(pro Wert)|Zeichenkette, die intern in der GUI verwendet wird, um einen auswählbaren Wert zu identifizieren; unabhängig von den Spracheinstellungen des Anwenders<br><br>Im Beispiel: internationale Abkürzung der Stadt|
|Defaultwert<br><br>(pro Eingabeelement)|Für jedes Eingabeelement kann bei Bedarf ein Defaultwert festgelegt werden, der dem Anwender als Vorauswahl erscheint.<br><br>Im Beispiel: der dem aktuellen Standort des Nutzers am nächsten gelegene Flughafen|
|Reihenfolge der möglichen Werte<br><br>(pro Eingabeelement)|Für jedes Eingabeelement muss die Reihenfolge der Auswahloptionen festgelegt werden. Die Reihenfolge kann unter Umständen von der aktuellen Sprache der GUI abhängig sein.<br><br>Im Beispiel: alphabetisch aufsteigend in der gewählten Sprache sortiert|

***

**Konvertierung**
das System arbeitet intern meist mit werten, die für den menschlichen User nicht auf den ersten Blick lesbar sind. Deswegen findet bei bestimmten Ein/Ausgaben eine Konvertierung statt, die die Informationen in das für den jeweiligen beteiligten (System oder Mensch) korrekte Format bringen.