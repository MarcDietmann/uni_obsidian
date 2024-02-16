## Was ist unter dem Postkutschenproblem zu verstehen
Bei dem Postkutschenproblem existiert ein gerichteter Digraph. In diesem möchte man jetzt vom Startknoten zum Zielknoten mit den günstigsten Kosten kommen. 
## Was ist unter dem Knapsack-Problem zu verstehen
Bei dem Knapsack-Problem haben wir ein Binäres Entscheidungsproblem, bei dem wir Objekte haben welche einen bestimmten Wert und bestimmte Kosten haben. Wir können uns nur zwischen *wählen* und *nicht wählen* {1, 0} der einzelnen Objekte entscheiden. 
## Welche Bestandteile hat eine dynamische Optimierung (Variablen)
Ein dynamische Optimierung besteht aus: 
- $z_i$ Der Zustand in Periode i
- $Z_i$ Zustandsmenge in Periode i
- $z_0$/ $z_n$ Anfangszustand/ Endzustand
- $x_{i-1}$  Die Entscheidung welche dich in den Zustand der Periode i bringt
- $X_i(z_{i-1})$ Menge aller zustände um von $z_{i-1}$ in $z_i$ zu gelangen
- $f_i(z_{i-1}, x_i)$ Die Kosten für Entscheidung $x_i$ 
- $F_i^{*}(z_i)$ Die Kosten für die Optimale Entscheidung zum nächsten Schritt

## Was ist der Unterschied zwischen Vorwärts und Rückwärtsrekursion?
Beide dieser Methoden werden bei der dynamischen Optimierung benutz. Sie liefern beide das selbe optimale Ergebnis. Der Unterschied ist der, dass bei der Rückwärtsrekursion beim Ziel gestartet wird und von dort aus zum Startknoten gewandert wird. Bei der Vorwärtsrekursion ist es genau umgekehrt.

## Wie funktioniert eine dynamische Optimierung?
Wir gehen bei dieser Erklärung davon aus, dass wir die Rückwärtsrekursion anwenden, bei der Vorwärtsrekursion funktioniert alles identisch nur umgekehrt. 
Wir Starten bei unserem Zielknoten $z_n$ und erstellen eine Tabelle mit allen $X_n(z_{n-1})$ wir berechnen nun für alle diese Zustände, welche vor dem Ziel erreicht werden die Kosten, welche gleichzeitig auch die optimalen Kosten sind. 

| $z_{n-1}$ | $x_n$ | $f_n(z_{n-1}, x_i)$ |  |
| ---- | ---- | ---- | ---- |
|  |  |  |  |
Im nächsten Schritt betrachten wir $X_{n-1}(z_{n-2})$ und wiederholen alle Schritte. Wir berechnen jetzt allerdings noch zusätzlich $F_{n-2}(z_{n-1})$ welches die Kosten von Zustand n-2 zum Zielzustand beschreibt, dieser ist wichtig, da wir das Optimum für den nächsten Schritt bestimmen müssen
In der Klausur werden die einzelnen Spalten vorgegeben sein. 
## Gibt es einen Unterschied bei der Lösung des Knapsack-Problems und dem Postkutschenproblem?