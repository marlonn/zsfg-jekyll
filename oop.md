---
layout: page
title: OOP
---

# **Objektorientierte Programmierung**
Quellen:  
- Kersken
- http://openbook.rheinwerk-verlag.de/oop/
- https://de.wikipedia.org/wiki/Objektorientierte_Programmierung

### **Definition**

Drei Grundelemente, die als Basis von objektorientierten Programmiersprachen gelten:

- Unterstützung von Vererbungsmechanismen

- Unterstützung von Datenkapselung

- Unterstützung von Polymorphie

Alan Kay, der Erfinder der Programmiersprache Smalltalk und des Begriffs „object oriented“, definierte ihn im Kontext von Smalltalk 1993 folgendermaßen:

>1. Everything is an object,
2. Objects communicate by sending and receiving messages (in terms of objects),
3. Objects have their own memory (in terms of objects),
4. Every object is an instance of a class (which must be an object),
5. The class holds the shared behavior for its instances (in the form of objects in a program list),
6. To eval a program list, control is passed to the first object and the remainder is treated as its message

Jedoch drückte Alan Kay später seine Unzufriedenheit über den von ihm gewählten Begriff „Objektorientierung“ aus, dieser würde den eigentlichen Kernaspekt aus seiner Sicht, das Messaging, zu kurz kommen lassen.


### **Kapselung von Daten**

Daten gehören explizit einem Objekt, ein direkter Zugriff wie auf die Datenstrukturen in der strukturierten Programmierung ist nicht erlaubt.

Objekte haben das alleinige Recht, ihre Daten zu verändern oder auch lesend auf sie zuzugreifen. Möchte ein Aufrufer (zum Beispiel ein anderes Objekt) diese Daten lesen oder verändern, muss er sich über eine klar definierte Schnittstelle an das Objekt wenden und eine Änderung der Daten anfordern.

Vorteile:
- Konsistenz der Daten wird gewährleistet
- Korrektheit des Programm leichter feststellbar
- geringerer Aufwand bei Änderungen des Programms(-> DRY)

### **Polymorphie**

Im Bereich der Objektorientierung bezieht sich Polymorphie darauf, dass verschiedene Objekte bei Aufruf derselben Operation unterschiedliches Verhalten an den Tag legen können.

Vorteile:
- höhere Flexibilität
- erhöhte Wartbarkeit/Änderbarkeit

**Dynamische Polymorphie (oder Laufzeitpolymorphie):**  
Objektorientierte Systeme, die dynamische Polymorphie unterstützen, sind in der Lage, einer Variablen Objekte unterschiedlichen Typs zuzuordnen. Dabei beschreibt der Typ der Variablen selbst lediglich eine Schnittstelle. Der Variablen können dann aber alle Objekte zugewiesen werden, deren Klasse diese Schnittstelle implementiert. Welche Methode beim Aufruf einer Operation aufgerufen wird, hängt davon ab, welche Klassenzugehörigkeit das Objekt hat, das der Variablen zugeordnet ist. Der Typ der Variablen ist nicht entscheidend. Der Aufruf der Operation erfolgt damit polymorph, also abhängig vom konkreten Objekt. Wenn der Variablen während der Laufzeit des Programms Objekte mit unterschiedlicher Klassenzugehörigkeit zugewiesen werden, so werden jeweils andere Methoden aufgrund des Aufrufs derselben Operation ausgeführt.

**Überladung (statische Polymorphie):**  
Von Überladung sprechen wir, wenn der Aufruf einer Operation anhand des konkreten Typs von Variablen oder Konstanten auf eine Methode abgebildet wird. Im Gegensatz zur dynamischen Polymorphie spielen die Inhalte der Variablen bei der Entscheidung, welche konkrete Methode aufgerufen wird, keine Rolle. Überladung kann nur von Sprachen mit statischem Typsystem unterstützt werden.

Rheinwerk:
> Wir möchten Stellen in unserem Code haben, die es uns erlauben, einzelne Elemente auszutauschen – wie eine Fassung für Glühbirnen: Ein Berechnungsverfahren für eine bestimmte Aufgabe ist nicht mehr schnell genug für Ihre Ansprüche? Tauschen Sie es doch einfach gegen ein effizienteres Verfahren aus, und klinken Sie es in die dafür vorgesehene Fassung ein. Ein neues Übertragungsprotokoll für Daten muss unterstützt werden? Schrauben Sie es in die Fassung, in die schon alle anderen Übertragungsprotokolle eingesetzt werden konnten.

IHK-Lösungvorschlag zur Frage "Was soll mit Kapselung erreicht werden?":
- Daten und Methoden innerhalb einer Struktur zusammenfassen
- Kontrollierter Zugriff auf Daten und Methoden über Schnittstelle (Geheimnisprinzip)

### **Vererbung**

Wikipedia:
>Vererbung heißt vereinfacht, dass eine abgeleitete Klasse die Methoden und Attribute der Basisklasse ebenfalls besitzt, also „erbt“. Somit kann die abgeleitete Klasse auch darauf zugreifen. Neue Arten von Objekten können auf der Basis bereits vorhandener Objektdefinitionen festgelegt werden. Es können neue Bestandteile hinzugenommen werden oder vorhandene überlagert werden.

Rheinwerk unterscheidet zwischen:
- Vererbung der Spezifikation
- Vererbung der Implementierung


### **Komposition und Aggregation**

**Aggregation:**  
Von einer Aggregation sprechen wir, wenn ein Objekt ein Teil von mehreren zusammengesetzten Objekten sein kann. Die zusammengesetzten Objekte nennen wir in diesem Fall Aggregate. Die Lebensdauer der Teile kann dabei länger sein als die Lebensdauer der Aggregate.  
Ein Beispiel für eine Aggregation ist die Beziehung zwischen einer Mannschaft und ihren Spielern. Ein Mensch kann in mehreren Mannschaften spielen, und wird eine Mannschaft aufgelöst, bedeutet es in den allermeisten Fällen nicht das Ende für ihre Ex-Spieler.

**Komposition:**  
Bei einer Komposition kann ein Teil immer nur in genau einem zusammengesetzten Objekt enthalten sein, und die Lebensdauer des zusammengesetzten Objekts entspricht immer der Lebensdauer seiner Komponenten. Das zusammengesetzte Objekt wird hier als Kompositum bezeichnet.  
Ein Beispiel für eine Komposition ist die Beziehung zwischen einer Bestellung und den einzelnen Posten der Bestellung. Ein Bestellungsposten gehört in genau eine Bestellung, und wird die Bestellung gelöscht, löscht man automatisch auch alle ihre Posten.
