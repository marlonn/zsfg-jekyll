---
layout: page
title: Architekturmuster
---

## **Architekturmuster**

**Hintergrundinformation:** Architekturmuster können als eine Vorlage für ein zu entwickelndes Software-System betrachtet werden. Sie regeln den Aufbau der Kommunikation innerhalb des Systems und auch die Verteilung von Aufgaben an Komponenten des Software-Systems. Durch die Verwendung von Architekturmustern soll die Übersichtlichkeit, Wartbarkeit, Testbarkeit und Wiederverwendbarkeit verbessert werden.

**Charakterisieren Sie den Begriff des Software-Architekturmusters:** Ein Architekturmuster soll die Grundstruktur eines Software-Systems festlegen. Diese erprobten Muster helfen dabei das neue System möglichst übersichtlich, wartbar und testbar zu gestalten. Ebenso soll dadurch die Effizienz des Entwicklungsprozesses gesteigert werden.

**Schichtenarchitekturmuster:** Liefert einen Entwurf für ein Software-System, das über mehrere Komponenten (Schichten, engl. *tier*) verfügt, die auch physikalisch getrennt sein können und über ein Netzwerkprotokoll miteinander kommmunizieren. Häufig genutzt werden das Zwei-Schichten-Modell (engl. *two tier*) und das Drei-Schichten-Modell. Das Zwei-Schichten-Modell ist oftmals das klassische Client-Server-Modell.  
In der Web-Programmierung wird ein Drei-Schichten-Modell sehr oft durch einen Client in Form eines Browsers und durch die Anzeige mit HTML, XHTML oder XML umgesetzt. Die Geschäftslogik liegt dann auf einem Web-Server und wird mit einer Skriptsprache wie PHP oder PERL implementiert. Die Daten werden von einem zusätzlichen Server mithilfe geeigneter Schnittstellen ausgelesen.

**Pipe and Filters-Architekturmuster:** Wird für Software-Systeme verwendet, die Datenströme verarbeiten. Jeder Verarbeitungschritt wird durch einen Filter realisiert und die eigentlichen Daten werden durch Kanäle (engl. *pipes*) geleitet. Die Filter sind dabei sehr flexibel und lassen sich beliebig anordnen und austauschen. Ein bekanntes Beispiel für ein solches System ist der Kommandozeileninterpreter unter UNIX/LINUX. Der AUfruf eines Kommandos liefert Daten, die dann über eine Pipe direkt an das nächste Kommando weitergeleitet werden.

**Model-View-Controller (MVC):**

Begriffszuordnung:
<table><tr><th>Architekturmuster</th><th>Begrifflichkeit</th></tr>
<tr><td>Schichtenarchitekturmuster</td><td>Präsentation, three tier, Client-Server, Geschäftslogik, Steuerung</td></tr>
<tr><td>Pipes and Filters-Architekturmuster</td><td>Datenfluss, Datensenke, Push/Pull-Mechanismus</td></tr>
<tr><td>Broker-Architekturmuster</td><td>entkoppelte Komponenten, Component Object Model (COM), CORBA, Remote Method Invocation (RMI)</td></tr></table>
