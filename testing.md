---
layout: page
title: Testing
---

## **Testen**

#### **Testarten**

**Modultest**: Dienen dazu, einzelne Module oder Komponenten (deshalb auch *Komponententest* genannt) zu testen. Das geschieht in der Regel in Form eines White-Box-Tests durch den Entwickler. Frameworks wie *JUnit* helfen dabei, solche Tests zu automatisieren.

**Integrationstest**: Prüft die einzelnen Komponenten im Zusammenspiel. In der Regel werden Komponenten nach dem Modultest direkt mit einem Integrationstest auf Fehler in der Interaktion mit bestehenden Komponenten geprüft. Auch hier ist Automatisierung möglich.

**Systemtest**: Prüft die komplette Software gegen die definierten Anforderungen. In der Regel findet dieser Test auch in einem Testsystem statt, das die Produktivumgebung nachbildet.

**Abnahmetest**: Auch *User-Acceptance-Test* genannt, wird durch den Auftraggeber durchgeführt. Er prüft das Produkt auf die geforderten Funktionalitäten. Der Test findet in der Regel als Black-Box-Test statt.
