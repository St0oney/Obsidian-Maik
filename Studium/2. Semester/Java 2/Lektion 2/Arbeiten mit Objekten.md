*beim Arbeiten mit Objekten, hat die Klasse Objekt eine zentrale Rolle. Sie ist die oberste aller Klassen und alle erben von ihr.*
*Wenn man nun mit Objekten arbeitet, gibt es einige nützliche Methoden, die von dieser Klasse implementiert (überschrieben) werden können.* 

***toString()* Methode**
die toString Methode dient dazu, Objekte als Strings darzustellen. Wenn sie nicht überschrieben wird, gibt sie Standardmäßig den Klassennamen des Objektes und seinen Hashwert aus. 
Damit die toString Methode die gewünschten Informationen ausgibt, muss sie überschrieben werden. 

*Beispiel*
![[Pasted image 20250327112700.png]]

Das hat den Vorteil, dass nun jedes Objekt dieser Klasse, wenn ein String erforderlich ist. Die oben definierten Inofrmationen ausgibt. 

***equals()* Methode**
die equals() Methode dient dazu, Objekte miteinander zu Vergleichen. In ihrer Standardform, vergleicht sie zwei Objekte nach ihren Referenzobjekten, wie der == Operator.
Der == Operator dient hauptsächlihch dazu, primitive Datentypen miteinander zu vergleichen. 
Sobald man aber den Inhalt komplexer Datentypen vergleichen möchte, muss man die equals Methode heranziehen und überschreiben. 

Damit lässt sich beispielsweise bei der Identifikation einer Person in einem System, die Methode so überschreiben, dass man eine Attributs-ID als vergleich nehmen kann.

*Beispiel*
- zuerst wird sichergestellt, ob die beiden Objekte auf das gleiche Objekt verweisen
- Dann wird überprüft, ob das Objekt den gleichen Typ hat
- Da die Signatur der Methode gleich ist, wie die der Oberklasse Object, muss dem Compiler in der überschriebenen Methode noch mit einem Typecast der Typ der Klasse mitgegeben werden. Da er sonst von einem beliebigen Objekt ausgeht. 
- Anschließend findet der Vergleich der Attribute statt. 
![[Pasted image 20250327114349.png]]

Es gibt bestimmte Regeln, die beim überschreiben der equals Methode beachtet werden müssen. 

- **Reflexiv**: Wird in der Methode dasselbe Objekt verglichen, muss das Ergebnis immer „true“ sein, d. h. x.equals(x) == true.
    
- **Symmetrisch**: Es ist egal, in welcher Richtung der Vergleich stattfindet, d. h. x.equals(y) muss das gleiche Ergebnis liefern wie y.equals(x).
    
- **Transitiv**: Wenn ein Objekt mit jeweils zwei anderen Objekten identisch ist, dann sind die anderen beiden Objekte ebenfalls identisch, d. h. wenn x.equals(y) und x.equals(z), dann auch y.equals(z).
    
- **Konsistent**: Solange die relevanten Attribute unverändert bleiben, liefert eine Vergleichsoperation stets das gleiche Ergebnis.
    
- **Existent**: Wenn ein zu vergleichendes Objekt nicht existiert, dann wird der Vergleich immer zu „false“ ausgewertet, d. h. x.equals(null) == false.

Außerdem ist es sehr wichtig, dass wenn man die equals Methode überschreibt, gleichzeitig die hashCode Methode mit überschrieben werden muss.

***hashCode()* Methode**
die hashCode Methode kann ebenfalls für Vergleiche herangezogen werden. Dafür bietet es sich an, wenn es sich Um Strings handelt, die bereits existierende Implementierung dieser Methode, der String Klasse zu verwenden. Diese Klasse wandelt die Strings in hash Werte um, und vergleicht sie miteinander. 

bei primitiven Datentypen, muss man eine eigene Implementierung erstellen, die die Werte mit einer Primzahl verrechnet und damit einen hashwert erzeugt. 
	für Boolean Werte gibt es eine eigene Methode, der Klasse Boolean, die genutzt werden kann. 

Wichtig dabei, dass die Attribute in der überschriebenen Methode, die gleichen sind, wie die in der equals Methode. 

***clone()* Methode**
die clone Methode wird dazu genutzt, Objekte zu klonen. Wenngleich diese Methode sehr kontrovers diskutiert wird, da sie einige Probleme mit sich bringt. 

die clone() Methode benötigt immer auch ihre zugehörige Schnittstelle Cloneable, die eine Klasse als kopierbar, definiert. Wenn sie nicht implementiert ist, wirft clone() eine Exception aus - CloneNotSupportedException

clone() im Standard, erstellt eine flache Kopie des Objektes. D.h., wenn ein Objekt weitere Objekte enthält (Referenzen), dann werden diese Referenzen mit kopiert. Das kann zu Problemen führen.

Dafür gibt es tiefe Kopien, die für die kopierten Objekte, neue Objekte anlegen. 

***compareTo()* Methode**
die compareTo Methode ist nicht Teil der Klasse Object, sondern Teil des Comparable Interfaces. 

die compareTo Methode, prüft 2 Objekte anhand ihrer Ordnung. Das bedeutet, dass Objekte z.b. ihrer Größe nach, oder dem Alphabet nach geordnet werden. 

Die Methode gibt immer einen integer Wert zurück, dafür gibt es  unterschiedliche Implementierungen in manchen Klassen. Bsp. String

in der String Klasse, wird ein String lexikalisch geprüft, d.h. die Zeichen der Strings werden Über ihren Unicode miteinander verglichen und anhand dessen wird definiert, welcher String "größer" bzw. "kleiner" ist. 










