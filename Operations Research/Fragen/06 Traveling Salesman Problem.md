*Übungsaufgaben*
SoSe 16 Aufgabe 5
SoSe 13 Aufgabe 6

## Wozu wird das TSP benutzt
Das TSP soll die Frage beantworten, was die kürzeste Rundreise über alle Knoten in einem Digraphen ist.
## Wie funktioniert das Eröffnungsverfahren *des nächsten Nachbarn*?
Bei der Eröffnungsheuristik des nächsten Nachbarn nimmt man einen Startknoten und wählt als nächsten Knoten den, der den geringsten Abstand zum jetzigen Knoten hat. Das wiederholt man solange, bis man alle Knoten besucht hat. Danach muss nur noch die Kante hinzugefügt werden, welche zum Startknoten verbindet.
## Wie funktioniert das Eröffnungsverfahren *der sukzessiven Einbeziehung*?
Bei dieser Anfangsheuristik startet man mit einem Zyklus, welcher möglichst weit auseinander liegt. Man geht davon aus, dass man so schon auf eine sehr gute Lösung kommt. 
Als nächstes berechnet man für alle Knoten die nicht im Zyklus sind den Abstand zum Zyklus. Von diesen Knoten nimmt man dann den, welcher am weitesten entfernt ist. 
**arg max(min(c<sub>ij</sub>))**
Danach muss man nur noch die optimale Einfügeposition berechnen, das macht man durch Ausprobieren. 
Das wiederholt man solange bis man alle Knoten eingefügt hat. 

## Wie kann man mit dem Branch and Bound verfahren das TSP lösen?
Wie man konkret das TSP mit dem B&B löst hängt immer ganz von der Aufgabenstellung ab. Eine Übungsaufgabe gibt es in 06 Aufgabe 4
