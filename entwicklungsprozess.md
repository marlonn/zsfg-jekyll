---
layout: page
title: Entwicklungsprozess
---

# **Entwicklungsprozess**

### **Wasserfallmodell**

Planung => Analyse => Entwurf => Realisierung => Test => Einsatz

### **Lastenheft**

Das Lastenheft ist die vom Auftraggeber festgelegte Gesamtheit der Forderungen an die Lieferungen und Leistungen eines Auftragnehmers innerhalb eines Auftrages (nach DIN 66901).

### **Pflichtenheft**

Das Pflichtenheft umfasst die vom Auftragnehmer erarbeiteten Realisierungsvorgaben aufgrund des vom Auftraggeber vorgegebenen Lastenheftes. Die Anforderungen aus dem Lastenheft werden mit den Details der technischen Umsetzung ergänzt. Der Auftragnehmer kann sich das Pflichtenheft vom Auftraggeber bestätigen lassen, um dann mit der Umsetzung

### **Strukturierte Analyse**

Die Strukturierte Analyse wird zur formalen Beschreibung des entwickelnden Systems benutzt. In der Regel geht es dabei um Softwaresysteme, die auf der strukturierten Programmierung basieren. Ansonsten kommt eher die objektorientierte Analyse in Betracht. Als Werkzeuge der struktierten Analyse kommen das Kontextdiagramm (Übersicht der Schnittstellen des Systems) oder auch das Datenflussdiagramm (Darstellung der Daten und deren Veränderung) in Betracht. Zur Darstellung von Algorithmen können Pseudo-Code, Struktogramme oder auch Programmablaufpläne (PAP) genutzt werden.

### **Objektorientierte Analyse**

Die objektorientierte Analyse betrachtet das zu entwickelnde System aus der objektorientierten Sichtweise. Als Werkzeuge sind alle Diagramme der UML zu nutzen. Dabei helfen die statischen Diagramme der UML wie das Klassendiagramm für die Darstellung der Klassen des Systems und deren Beziehungen untereinander und die dynamischen Diagramm wie das Sequenzdiagramm helfen bei der Darstellung der Kommunikation der Objekte untereinander (Botschaften, engl *messages*).

### **grobe Einteilung**

**sequentielle Entwicklungsmodelle:**  
Diese Modelle sind in der Regel in Phasen eingeteilt, die Schritt für Schritt abgearbeitet werden. Das klassische Beispiel ist das *Wasserfallmodell*. Jede Phase muss komplett abgeschlossen sein, um zur nächsten zu kommen. Rücksprünge in vorherige Phasen sind beispielsweise nur im erweiterten Wasserfallmodell möglich.

**iterative Entwicklungsmodelle:**  
Diese Modello zeichnen sich durch wiederholtes Durchlaufen von festgelegten Phasen aus. Das *Spiralmodell* ist ein bekanntes Beispiel für ein solches Modell. Dort werden vier Phasen (Zielfestlegung, Risikoanalyse, Entwicklung und Planung des nächsten Zyklus) immer wieder durchlaufen. Damit sollen nötige Anpassungen an die Software besser möglich sein und Probleme schneller erkannt und behoben werden. Das Scheitern der Entwicklung soll damit frühzeitig verhindert werden - viele Softwareprojekte scheitern daran, dass die Probleme zu spät erkannt und gelöst werden.

**agile Entwicklungsmodelle:**  
Soll die Antwort auf die Probleme der klassischen Softwareentwicklung sein. Durch Flexibilität, erhöhte Kommunikation und weniger Bürokratie möchten diese Modelle die oben angesprochenen Problematiken vermeiden. Agile modelle sind natürlich nicht die Antwort auf jedes Problem, aber sie helfen dabei, dass Entwicklungen erfolgreicher werden. Der bekannteste Vertreter dieser Art ist *Scrum*.

### **V-Modell**
Ist eine Fortführung des Wasserfallmodells und teilt die Entwicklung ebenfalls in Phasen ein. Von der Analyse bis zur Realisierung werden diese Phasen durhclaufen. Parallel dazu werden zu jeder Phase die entsprechenden Testfälle berücksichtigt. Bei einem Durchlauf der Phasen von oben nach unten und den entsprechenden Test von unten nach oben entsteht ein V.  
Phasen:

<table>
    <tr><th>Phasen</th><th>Tests</th></tr>
    <tr><td>Anforderungsdefinition</td><td>Abnahmetest </td></tr>
    <tr><td>Systementwurf</td><td> Integrationstest</td></tr>
    <tr><td>Softwareentwurf</td><td> Modultest</td></tr>
    <tr><td> Quellcode </td></tr>
</table>

### **Scrum**

Kersken zu Scrum:

Scrum definiert drei verschiedene, klar voneinander getrennte Rollen:

##### **Product Owner:**
Der **Product Owner** ist eine Art klassischer Projektmanager, der die allgemeinen Projektziele vorgibt und gegenüber dem Kunden verantwortlich ist. Er hält sich jedoch aus der Selbstorganisation des Teams heraus.  

Prüfungsvorbereitung aktuell:

>Trägt die Verwantwortung für die Produktentwicklung im Hinblick auf Wirtschaftlichkeit sowie Terminsetzungen. Er kommuniziert mit dem Kunden und prüft, ob die Ergebnisse nach einem Sprint den Erwartungen entsprechen.

Das **Team**, idealerweise bestehend aus fünf bis neun Mitgliedern, setzt die Anforderungen des Projekts selbstverwaltet um. Dabei entscheidet jedes Teammitglied – in Absprache mit dem Rest des Teams – selbst über seine Aufgaben. Vor dem Beginn eines jeden Projektschritts (beim Scrum als **Sprint** bezeichnet) bestimmen die Teammitglieder ihre Ziele.    

##### **Scrum Master:**
Der **Scrum Master** überwacht die Produktivität des Teams und sorgt dabei für die Klärung von Problemen, die das Team am Erreichen der Projektziele hindern.

Prüfungsvorbereitung aktuell:

>Ist verantwortlich für das Gelingen der Entwicklung, indem er das Entwickler-Team betreut und dafür sorgt, dass das Team möglichst ungestört arbeiten kann. Er entwickelt nicht selbst, sondern moderiert die anfallenden Besprechungen und hilft bei Kommunikationsproblemen zwischen Produkt-Owner und Entwicklungs-Team.

##### **Sprint:**
Ein **Sprint** oder Projektzyklus dauert im Allgemeinen zwei bis vier Wochen. Zu Beginn des Sprints finden zwei Meetings statt. Das erste Planungstreffen wird vom **Product Owner** organisiert; hier definiert er zusammen mit dem Team die Anforderungen des aktuellen Sprints. Das zweite Meeting wird vom **Team** selbst organisiert, um die Aufgaben nach Neigungen und Kenntnissen möglichst gleichmäßig auf die Teammitglieder zu verteilen.

Prüfungsvorbereitung aktuell:
> Der Sprint ist die eigentliche Phase der Entwicklung. Die Zeitdauer des Sprints beträgt zwischen einer und vier Wochen. Während des Sprints sollte das Entwickler-Team möglichst nicht abgelenkt werden. Der Scrum Masteer sorgt für den reibungslosen Ablauf des Sprints. Am Ende des Sprints steht ein sogenannter Review, der dazu dient, die Ergebnisse mit den festgelegten Zielen zu vergleichen.

Die einzelnen Aufgaben werden meist in Form sogenannter **User Stories** (Anforderungen in Alltagssprache, ein bis zwei Sätze lang) formuliert. Die Teammitglieder schätzen, wie aufwendig die Umsetzung jeder Aufgabe sein könnte. Dabei werden nicht Manntage, sondern Story Points als Maßeinheit gewählt, wobei die Umrechnung in Manntage je nach Erfahrung des Teams und Vertrautheit mit dem Projekt flexibel ist.

Alle Aufgaben des aktuellen Sprints werden in einem **Sprint Backlog** gesammelt – idealerweise als einzelne Papiere auf einer Tafel, die in drei Bereiche unterteilt ist: »zu erledigen«, »in Arbeit« und »erledigt«. In einem separaten Bereich werden Probleme gesammelt, die zu Verzögerungen führen können – beispielsweise, wenn der Kunde notwendige Entscheidungen zu treffen oder Daten zu liefern hat.

Prüfungsvorbereitung aktuell:
> Im **Product-Backlog** stehen die Anforderungen (In Form von sogenannten User Stories) an das zu entwickelnde System. Der **Product Owner** ist verantwortlich für das Backlog. Er setzt auch die Prioritäten der einzelnen Anforderungen fest, die in den einzelnen Sprints dann umgesetzt werden. Das Backlog ist keine vollständige Liste, sondern erweitert oder vermindert sich flexibel im Laufe der Entwicklung.

##### **Daily Scrum:**
Jeden Tag – idealerweise jeweils zur selben Uhrzeit – führt das Team ein **Daily Scrum** durch, ein kurzes Meeting von maximal 15 Minuten Dauer. Hier werden eventuelle Verzögerungen und Probleme erörtert, es findet ein Austausch statt, und es wird definiert, welche Aufgaben erledigt sind. Aus Letzterem ergibt sich ein **Burndown Chart** – eine grafische Darstellung, die die lineare Abwärtsbewegung der zu erledigenden Story Points mit dem Ist-Zustand vergleicht.

Prüfungsvorbereitung aktuell:
> Eine etwa 15-minütige tägliche Zusammenkunft des Entwickler-Teams zu Beginn des Arbeitstages, um über die Tagesziele und Probleme zu sprechen. Es dient hauptsächlich dazu, dass alle Beteiligten über den aktuellen Stand informiert sind. Größere Probleme werden nicht diskutiert, sondern erst einmal vom **Scrum Master** aufgenommen, der sich dann um die weitere Lösung kümmert.

Nach dem Abschluss eines Sprints findet eine **Retrospektive** statt, bei der jedes Teammitglied kurz die Ereignisse des Sprints aus seiner Sicht schildert. Die entscheidenden Fragen, die auch schriftlich fixiert werden sollten, sind »Was war gut?« (Best Practices) und »Was könnte verbessert werden?«.

### **Test-driven Development (TDD)**

Definiert die Testfälle vor der eigentlichen Implementierung. Ein sehr bekanntes Verfahren ist das Uni-Testing. Dabei werden zuerst Tests für die zu entwickelnden Komponenten (Units) entwickelt und anschließend werden die Komponenten implementiert. Frameworks wie JUnit (unter Java) unterstützen diese Methode. Meistens werden Unit-Tests in der agilen Entwicklung eingesetzt (bspw. beim *extreme Programming*)
