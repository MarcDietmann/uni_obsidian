## Wozu dient das Branch and Bound Verfahren?
Das B&B dient dazu, um ein Problem der linearen Optimierung zu lösen bei der man nicht direkt auf eine Lösung kommt. Das funktioniert indem man erst ein vereinfachtes Problem P' des Ursprungsproblems P löst. Dieses vereinfachte Problem wird dann solange verzweigt, bis man eine Lösung findet, die sowohl in einem Teilproblem von P' optimal ist, als auch in P zulässig ist. 
## Nach welchen Regeln wird gebrancht?
Beim Branching wird immer so verzweigt, dass alle zulässigen Lösungen des Ausgangsproblems P<sub>0</sub> in den Verzweigten Teilproblemen P'<sub>2</sub> und P'<sub>3</sub> wiederfindet.
Liegt eine in P<sub>0</sub> unzulässige Lösung vor, so muss immer so verzweigt werde, dass dieser Punkt sich nicht mehr in den Teilproblemen wiederfindet. 
Um möglichst schnell zu kleineren Teilen den Ausgangsproblems zu kommen sollte immer die Dimension gewechselt werden in die gebrancht wird.

## Wozu dient das Bounding?
Um zu verstehen wie geboundet wird klären wir zunächst mal ein Paar Grundbegriffe: 
### (Globale) Obere Schranke
Das ist ein Wert, welcher für ein Teilproblem den maximalen Wert der Zielfunktion angibt. Das gilt für ein Maximierungsproblem und ein Minimierungsproblem
### (Globale) Untere Schranke
Das ist ein Wert, welcher für ein Teilproblem den Wert angibt, den die Zielfunktion mindestens annehmen wird. Sowohl für Maximierung- als auch Minimierungsproblem.
### Was ist eine LP-Relaxation
Bei einer Relaxation spricht man davon, dass ein gegebenes Problem vereinfacht wird. 
X(P) ist Teilmenge von X(P') => F*(P)<= F*(P') in worten: 
*Die Menge aller zulässigen Lösungen ist eine Teilmenge des relaxierten Problems. Daraus folgt, das die optimale Lösung des relaxierten Problems größer oder gleich der optimalen Lösung des Ausgangsproblems ist.* 

## Wann wird ein Knoten ausgelotet?
Sobald ein Knoten ausgelotet worden ist, wird dieses Teilproblem nicht mehr untersucht und wir sparen uns Rechenleistung.
Es gibt 3 Fälle in den wir ausloten:
### Fall a *Nur Käse*
Ist die lokale obere Schranke kleiner gleich der Globalen unteren Schranke, so kann man hiervon nichts besseres erwarten. Dieser Knoten muss nicht mehr weiter untersucht werden. (Gilt nur für Maximierungsprobleme, Minimierung wäre andersherum)
### Fall b *Besser wirds nicht*
Ist die lokale Obere Schranke größer als die globale untere Schranke, so ist diese Schranke ein Optimum des verzweigten Teilproblem. Egal wie man diesen Knoten verzweigt, es wird nicht besser als das Optimum. Außerdem muss die globale untere Schranke geupdatet werden. wichtig zu beachten ist, das das gefundenen Optimum der Relaxation auch im Ausgangsproblem eine zulässige Lösung sein muss.
### Fall c *Nichts und wieder nichts*
Falls die Relaxation keine zulässige Lösung für das Ausgangsproblem hat so kann dieser Knoten auch ignoriert werden.
## Nach welchen Regeln kann verzweigt werden
### Maximum Upper Bound (MUB)
Es werden alle oberen Schranken der Verzweigten Teilprobleme gebildet und dann werden sie absteigend nach ihrer oberen Schranke in K einsortiert. Vermutlich wird das bei Maximierungsproblemen so gemacht, da bei diesen Knoten das höchste Potential zu erwarten ist. 
### Minimum Lower Bound (MLB)
Vermutung: Es wird wie bei der MUB vorgegangen mit dem Unterschied, dass die niedrigste untere Schranke als erste einsortiert wird. Vermutlich wird das bei Minimierungsproblemen so gemacht, da bei diesen Knoten das höchste Potential zu erwarten ist. 
### Last in First out (LIFO)
Bei der LIFO Methode werden sie der Reihe nach in K einsortiert und auch hier immer das erste als nächstes genommen und verzweigt.