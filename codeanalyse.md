---
layout: page
title: Code-Analyse
---

# **Debugging und Analyse von Quellcode**

**Anweisungsüberdeckung**: Hier wird jede Anweisung im Quellcode geprüft. Die Anweisungsüberdecking ist somit eine Vorraussetzung für eine Fehlerfreiheit, aber keinesfalls eine Garantie. Auch C0-Test genannt, ist das einfachste der drei Verfahren.

**Zweigüberdeckung**: Schließt alle Verzweigungen in die Prüfung mit ein, läuft aber nur genau einmal durch jede Iteration und kann deshalb keine Fehler aufdecken, die in einer beliebigen Iteration verborgen sind. Auch C1-Test genannt.

**Pfadüberdeckung**: Schließt die anderen beiden Test ein und durchläuft alle Pfade des Quellcodes. Damit können Iterationen theoretisch beliebig oft durchlaufen werden - der Test wird dadurch zu aufwändig. In der Praxis entscheidet man sich dann dafür, dass Iterationen keinmal, genau einmal und in einer festgelegten Häufigkeit durchlaufen werden. Dadurch soll die vollständige Überdeckung angenähert werden.  
Auch C2-Test genannt.

**Woher stammt der Name "Debugger"?** Der Name beruht auf einem Vorfall aus den Anfängen der Computer. In den 1940ern hatte sich eine Motte in einem Relais eines der ersten Computer verfangen und sorgte für eine Fehlfunktion. Dieser Fehler im Computer wurde dann "Bug" genannt. Ein Debugger ist also ein Werkzeug, mit dem ein Computervon Bugs befreit werden kann.

**Was ist ein Haltepunkt?** Eine Markierung im Programmcode. Nach dem Starten stoppt das System an dieser Stelle und der Entwickler kann bspw. den Zustand von Variablen betrachten.  
**Was ist ein *konditionaler* Haltepunkt?** Hier kann eine Bedingung angegeben werden, wann das Programm zu stoppen hat. Damit wird das Debugging besser steuerbar.

**Was ist "Just-in-time-Debugging"?** Die Möglichkeit, dass während des Debugging-Prozesses Anweisungen im Quelltext geändert werden können und der weitere Programmablauf direkt darauf reagiert. Damit wird das Debugging sehr flexibel.
