---
layout: page
title: Testing
---

# **Softwaretests**

##### **Testarten:**

**Modultest**:  
Dienen dazu, einzelne Module oder Komponenten (deshalb auch *Komponententest* genannt) zu testen. Das geschieht in der Regel in Form eines White-Box-Tests durch den Entwickler. Frameworks wie *JUnit* helfen dabei, solche Tests zu automatisieren.

**Integrationstest**:  
Prüft die einzelnen Komponenten im Zusammenspiel. In der Regel werden Komponenten nach dem Modultest direkt mit einem Integrationstest auf Fehler in der Interaktion mit bestehenden Komponenten geprüft. Auch hier ist Automatisierung möglich.

**Systemtest**:  
Prüft die komplette Software gegen die definierten Anforderungen. In der Regel findet dieser Test auch in einem Testsystem statt, das die Produktivumgebung nachbildet.

**Abnahmetest**:  
Auch *User-Acceptance-Test* genannt, wird durch den Auftraggeber durchgeführt. Er prüft das Produkt auf die geforderten Funktionalitäten. Der Test findet in der Regel als Black-Box-Test statt.

**Black-Box-Test:**  
Betrachtet das System als Black Box. Es geht also nicht darum, den Quellcode zu testen, sondern nur darum zu prüfen, ob die Software die geforderten Funktionalitäten besitzt. Er sollte deshalb von Personen durchgeführt werden, die keine Einsicht in den Quellcode des Systems haben. Damit soll ein möglichst objektiver Test ermöglicht werden.

**White-Box-Test:**  
Hier wird der Quellcode auf Korrektheit geprüft. Das kann durch Debugging und ähnliche Techniken unterstützt werden. Dieser Test wird in der Regel vom Entwickler durchgeführt. Wenn in einem White-Box-Test keine Fehler erkannt werden, heißt das aber noch nicht, dass die Software den Anforderungen entspricht.

**Funktionstest:**  
Bestimmen die Testfälle auf Basis der Spezifikationen. Bspw. prüft der Modultest die Software gegen Modulspezifikatione oder der Abnahmetest gegen die Anforderungen des Kunden.

**Oberflächentest (GUI-Test):**  
Prüft die Benutzerschnittstelle des Systems auf Verständlichkeit, Bedienbarkeit und Erwartungskonformität. (Entspricht die Oberfläche den Erwartungen des Nutzers? Verhält sie sich auch entsprechend?)

**Lasttest:**  
Hier wirdeine außergewöhnliche Last auf dem System erzeugt. Das kann bspw. die Simulation von sehr vielen parallelen Zugriffen auf ein Softwaresystem sein. danach wird geprüft, ob das Softwaresystem weiterhein den Anforderungen entspricht, oder ob Fehler auftreten, die ohne Last nicht bemerkt worden wären.
