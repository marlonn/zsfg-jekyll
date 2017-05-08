---
layout: page
title: Normalformen
---

# **Normalformen**

[Quelle: Wikipedia]("https://de.wikipedia.org/wiki/Normalisierung_(Datenbank)")
[Quelle: "IT-Handbuch für Fachinformatiker" von Sascha Kersken]

Unter Normalisierung eines relationalen Datenschemas (Tabellenstruktur) versteht man die Aufteilung von Attributen (Tabellenspalten) in mehrere Relationen (Tabellen) gemäß den Normalisierungsregeln (s. u.), so dass eine Form entsteht, die keine vermeidbaren Redundanzen mehr enthält.

Ein konzeptionelles Schema, das Datenredundanzen enthält, kann dazu führen, dass bei Änderungen der damit realisierten Datenbank die mehrfach enthaltenen Daten nicht konsistent, sondern nur teilweise und unvollständig geändert werden, womit sie obsolet oder widersprüc+hlich werden können. Man spricht von auftretenden Anomalien. Zudem belegt mehrfache Speicherung derselben Daten unnötig Speicherplatz. Um Redundanz zu verhindern, normalisiert man solche Tabellen.

Man bringt ein relationales Datenschema in eine Normalform, indem man fortschreitend anhand für sie geltender funktionaler Abhängigkeiten seine Relationen in einfachere zerlegt, bis keine weitere Zerlegung mehr möglich ist. Dabei dürfen jedoch auf keinen Fall Daten verloren gehen.

### **Erste Normalform**

>Jedes Attribut der Relation muss einen atomaren Wertebereich haben, und die Relation muss frei von Wiederholungsgruppen sein.

Das heißt, zusammengesetzte, mengenwertige oder geschachtelte Wertebereiche (relationenwertige Attributwertebereiche) sind nicht erlaubt. Damit sind auch Wiederholungsgruppen nicht zugelassen.

Beispiel:   
Die Adresse darf nicht als Attribut verwendet werden, sondern muss in PLZ, Ort, Straße und Hausnummer aufgeteilt werden.

Beispiel für eine Wiederholungsgruppe:  
Eine Spalte { Telefon }, die mehrere Telefonnummern enthält, oder auch eine Spaltengruppe { Telefon1, Telefon2, Telefon3 }.

### **Zweite Normalform**

> Eine Relation ist in der zweiten Normalform genau dann, wenn die erste Normalform vorliegt und kein Nichtprimärattribut (Attribut, das nicht Teil eines Schlüsselkandidaten ist) funktional von einer echten Teilmenge eines Schlüsselkandidaten abhängt.

Kersken:
>Die zweite Normalform (2NF) fordert zusätzlich, dass Datensätze nur direkte Informationen über ein und denselben Sachverhalt enthalten. Formal gesagt dürfen alle Felder in einer Tabelle, die die zweite Normalform erfüllt, nur vom Primärschlüssel dieser Tabelle abhängen. Beispielsweise dürfte eine Person mit zwei Wohnsitzen nicht zweimal in eine Kundentabelle aufgenommen werden. In diesem Fall müssten die Wohnorte in eine separate Tabelle geschrieben werden; der Bezug auf die Kunden müsste in dieser Tabelle als Fremdschlüssel eingetragen werden.

**Negativbeispiel: Tabelle "CD_Lied"**
<table>
    <tr>
        <th>CD_ID</th><th>Albumtitel</th><th>Interpret</th><th>Erscheinungsjahr</th><th> 	Track </th><th>	Titel</th>
    </tr>
    <tr>
        <td>4711</td><td> 	Not That Kind </td><td>	Anastacia </td><td>	2000 </td><td>	1 </td><td>	Not That Kind  </td>
    </tr>
    <tr>
        <td>4711 </td><td>	Not That Kind </td><td>	Anastacia </td><td>	2000 </td><td>	2 </td><td>	I’m Outta Love  </td>
    </tr>
    <tr>
        <td>4711 </td><td>	Not That Kind </td><td>	Anastacia </td><td>	2000 </td><td>	3</td><td> 	Cowboys & Kisses  </td>
    </tr>
    <tr>
        <td>4712 </td><td>	Wish You Were Here 	</td><td>Pink Floyd </td><td>	1975 </td><td>	1 </td><td>	Shine On You Crazy Diamond  </td>
    </tr>
    <tr>
        <td>4713 </td><td>Freak of Nature</td><td>	Anastacia</td><td>2001</td><td>1</td><td>Paid my Dues </td>
    </tr>
</table>

- Der Primärschlüssel der Relation ist aus den Feldern CD_ID und Track zusammengesetzt. (Grundsätzlich darf ein Primärschlüssel aus mehreren Attributen bestehen, jedoch entsteht daraus im genannten Beispiel ein Konflikt.)

- Die Felder Albumtitel, Interpret und Erscheinungsjahr sind vom Feld CD_ID abhängig, aber nicht vom Feld Track. Dieser (Punkt 2) verletzt die 2. Normalform, da die drei nicht-primären Attribute nicht nur von einem Teil des Schlüssels (hier CD_ID) abhängen dürfen. Wäre der Schlüssel nicht zusammengesetzt (siehe Punkt 1), so könnte dies nicht passieren.

**Lösung: Zwei Tabellen**

Tabelle CD   
<table>
    <tr>
        <th>CD_ID</th><th> 	Albumtitel </th><th>	Interpret </th><th>	Erscheinungsjahr</th>
    </tr>
    <tr>
        <td>  4711 </td><td>	Not That Kind </td><td>	Anastacia </td><td>	2000
    </tr>
    <tr>
        <td>4712 </td><td>	Wish You Were Here </td><td>	Pink Floyd </td><td>	1975  </td>
    </tr>
    <tr>
        <td>  4713 </td><td>	Freak of Nature </td><td>	Anastacia </td><td>	2001  </td>
    </tr>
</table>

Tabelle Lied   
<table>
    <tr>
        <th>CD_ID </th><th>	Track </th><th>	Titel</th>
    </tr><tr><td>
4711  </td><td>	1  </td><td>	Not That Kind  
</tr><tr><td>
4711  </td><td>	2  </td><td>	I’m Outta Love  
</tr><tr><td>
4711  </td><td>	3  </td><td>	Cowboys & Kisses  
</tr><tr><td>
4712  </td><td>	1  </td><td>	Shine On You Crazy Diamond  
</tr><tr><td>
4713 	 </td><td>1  </td><td>	Paid my Dues  
</tr>
</table>

Das Attribut CD_ID aus der Tabelle Lied bezeichnet man als Fremdschlüssel, der auf den Primärschlüssel der Tabelle CD verweist. Zugleich stellen die Attribute CD_ID und Track den zusammengesetzten Primärschlüssel der Tabelle Lied dar.


### **Dritte Normalform**

> Die dritte Normalform ist genau dann erreicht, wenn sich das Relationenschema in der 2NF befindet, und kein Nichtschlüsselattribut  von einem Schlüsselkandidaten transitiv abhängt.

Kersken:
>Die dritte Normalform (3NF) ist erfüllt, wenn alle Felder funktional unabhängig voneinander sind. Der Unterschied zur zweiten Normalform erscheint geringfügig. Eine Tabelle, die zwar die zweite, aber nicht die dritte Normalform erfüllt, belässt eine eindeutig zu einem bestimmten Feld gehörende Zusatzinformation innerhalb einer Tabelle, in der dieses Feld keinen Schlüssel bildet. Beispielsweise hat in der Personaltabelle einer Unternehmensdatenbank, in der in einem Feld die Abteilung eines Mitarbeiters steht, der Name des Abteilungsleiters nichts zu suchen, weil er nur von der Abteilung, aber nicht vom Mitarbeiter abhängt.

**Negativbeispiel; 3NF verletzt**

CD  
<table><tr>
    <th>CD_ID</th>
    <th>Albumtitel</th>
    <th>Interpret</th>
    <th>Gründungsjahr</th>
</tr>
<tr>
    <td>4711</td><td>Not That Kind</td><td>Anastacia</td><td>1999</td>
</tr><tr>
    <td>4712</td><td>Wish You Were Here </td><td>Pink Floyd</td><td>1965</td>
</tr><tr>
    <td>4713</td><td>Freak of Nature</td><td>Anastacia</td><td>1999</td>
</tr></table>

Offensichtlich lässt sich der Interpret einer CD aus der CD_ID bestimmen, das Gründungsjahr der Band/Interpreten hängt wiederum vom Interpreten und damit transitiv von der CD_ID ab.

**Lösung:**

Tabelle CD  
<table><tr>
    <th>CD_ID</th>
    <th>Albumtitel</th>
    <th>Interpret_ID</th>
</tr>
<tr>
    <td>4711</td><td>Not That Kind</td><td>311</td>
</tr><tr>
    <td>4712</td><td>Wish You Were Here</td><td>312</td>
</tr><tr>
    <td>4713</td><td>Freak of Nature</td><td>311</td>
</tr></table>

Tabelle Künstler
<table>
    <tr>
        <th>Interpret_ID</th><th>Interpret</th><th>Gründungsjahr</th>
    </tr>
    <tr>
        <td>311</td><td>Anastacia</td><td>1999</td>
    </tr>
    <tr>
        <td>312</td><td>Pink Floyd</td><td>1965</td>
    </tr>
</table>
