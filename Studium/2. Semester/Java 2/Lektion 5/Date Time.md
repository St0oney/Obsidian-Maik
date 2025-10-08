vvvUm in Java mit Datum und Uhrzeit zu arbeiten, gibt es unterschiedliche Optionen. Die grundlegendste Klasse hierfür ist die Klasse Date
-> java.util.Date

Objekte dieser Klasse, erstellen einen Zeitpunkt dar und umfassen Das Datum und die Uhrzeit bis auf die Millisekunde. 
Der Default Konstruktor erzeugt ein Objekt mit dem Datum und der Zeit des Erzeugungszeitpunkt. 
Es gibt aber auch überladene Konstruktoren, sodass man die einzelnen Werte selbst bestimmen kann. 

**Der Großteil von java.util.Date ist veraltet**

um Formatierungen der Klasse java.util.Date vorzunehmen, wird SimpleDateFormat genutzt. 
SimpleDateFormat ist jedoch auch veraltet.

*Seit 2014 gibt es die Klasse Java.time, die alle Probleme der Klassen java.util.Date und 
Calendar behebt.*

