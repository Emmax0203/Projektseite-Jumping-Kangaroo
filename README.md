# Projektseite-Jumping-Kangaroo

## Inhaltsverzeichnis

[1. Einleitung](#Einleitung)

[2. Spielidee](#Spielidee)

[3. Screens](#Screens)

[4. Actor](#Actor)

[5. Funktionen](#Funktionen)

[6. Spielende](#Spielende)

[7. Schlusswort](#Schlusswort)

## Einleitung<a name="Einleitung"></a>
Im zweiten Halbjahr des 12. Jahrgangs haben wir im Rahmen des wöchentlichen Informatikunterrichts innerhalb von ungefähr drei Monaten das jump and run Spiel "Jumping Kangaroo" programmiert. Dazu haben wir das Programm Greenfoot Javascript verwendet, da dieses für Fortgeschrittene mit etwas Vorkenntnissen im Programmieren geeignet schien, die wir bereits im ersten Halbjahr erlangt haben. Dieses Programm arbeitet mit komplexeren Ausdrücken und nur Text. Demnach bot es eine Möglichkeit zur Steigerung für unsere Informatikkenntnisse. Nachdem wir uns die Einführungsvideos zu Greenfoot ausführlich angesehen haben, kamen wir mit den grundlegenden Prinzipien zurecht und konnten uns so das restliche Können aneignen. Da wir dafür lediglich drei Monate Zeit hatten, sind wir mit dem Ergebnis sehr zufrieden.

## Spielidee<a name="Spielidee"></a>
"Jumping Kangaroo" ist ein jump and run Spiel, bei dem es darum geht, Kirschen einzusammeln und so den Sieg zu erlangen. Dabei gibt es einen Mindestscore von sieben Kirschen, welchen man erreichen muss, um das Spiel zu gewinnen. Die Kirschen kann man einsammeln, indem man von Plattform zu Plattform springt und auf dem Weg alle Kirschen mitnimmt. Pro gesammelter Kirsche kriegt man einen Pluspunkt, welcher im Score angezeigt wird. 

## Screens<a name="Screens"></a>
Für die Gestaltung der Screens haben wir das Programm "Paint" verwendet, um unsere eigenen Designs zu erstellen und in Greenfoot zu verwenden. Mithilfe der Spacetaste kann man aufgrund eines Befehls im Startscreen zum tatsächlichen Screen und Spiel gelangen. Hat man am Ende des Spiels alle Kirschen eingesammelt und somit den Mindestscore erreicht, wird der Gewinnscreen aufgerufen und angezeigt.

## Actor<a name="actor"></a>
Bei Greenfoot arbeitet man vor allem mit sogenannten "actor". Diese können verschiedene Funktionen besitzen. Im Spiel "Jumping Kangaroo" gibt es drei verschiedene "actor", nämlich: kangaroo, platform und cherry.
Das Känguru ist die Hauptfigur des Spiels und sammelt die Kirschen ein. Hierzu kann es sich nach links und rechts bewegen, sowie springen und nach unten fallen. 

Die Platformen bilden die Sprung- und Landeflächen für das Känguru und sorgen dafür, dass dieses zu den Kirschen gelangen kann. Des Weiteren kann man nicht von unten durch diese durchspringen, da sie aus einem festen Material sind. Man kann lediglich von oben auf den Platformen landen und von diesen wieder abspringen. 

Die Kirschen sind die Objekte, welche eingesammelt werden müssen und Punkte bringen. Sie sorgen dafür, dass man das Spiel gewinnen kann, da sie die Variable "eatenCherries" verändern und so die Punktzahl erhöhen. 

## Funktionen<a name="Funktionen"></a>
Startscreen: Der StartScreen hat nur eine if-Funktion, durch die beim Drücken der Spacetaste der Startscreen verschwindet und der Screen MyWorld geöffnet wird.

MyWorld: Wir haben eine Variable "eatenCherries", die den Score festlegt, sowie ein Textfeld, das diese Variable anzeigt. Außerdem haben wir eine "Prepare-Funktion"(public void prepare), welche die Ausgangslage unserer Welt festlegt. In dieser Funktion ist die Anzahl, Platzierung und Art aller Objekt in dieser Welt festgelgt. Das sind bei uns sieben Kirschen, sieben Platformen und ein Känguru. Hinzu kommt eine Funktion für das Ende des Spiels (public void act), in der geschrieben steht, dass wenn der Wert der Varibale "eatenCherries" höher als sechs ist, der EndScreen abgerufen wird. 

Kangaroo: Zum Bewegen des Kängurus nach links und rechts bedarf es einer Funktion (public void move). Diese legt fest, dass beim Drücken der Rechts- und Linkspfeile der Tastatur die Position des Kängurus verändert wird. Dabei hat das Känguru eine Schrittweite von drei in beide Richtungen. Die Funktion dient nur zur Bewegung in horizontaler Richtung und beeinflusst somit die y-Koordinate nicht. Um einen springenden actor zu erschaffen, mussten wir erst eine statische Variable erstellen, die für die Gravitation steht (gravity). Springt man nun mit Hilfe des festgelegten Knopfes, wirkt diese Schwerkraft entgegengesetzt nach unten, bis sie auf einen bestimmten Untergrund trifft. Dieser ist durch eine weitere Funktion definiert, nämlich "solid ground". In diesem Begriff sind die untere Linie der Welt und die Platformen zusammengefasst. Von diesen kann das Känguru abspringen und auf ihnen landen. Eine weitere Eigenschaft der Platformen wird auch im Känguru bestimmt, nämlich, dass das Känguru nicht von unten durch die Platformen springen kann. Hierzu dient die Funktion public boolean didBumpHead. Außerdem kann das Känguru Kirschen essen. Hierzu dient eine if-Funktion, die bei Berührung der Kirsche einerseits den Faktor eins zu der Variable "eatenCherries" addiert und andererseits die berührte Kirsche aus der Welt entfernt, damit sie nicht ein weiteres Mal eingesammelt werden kann. Dadurch kann jede Kirsche nur einen Punkt bringen.

## Spielende<a name="Spielende"></a>
Ziel des Spiels ist es, alle Kirschen einzusammeln. Daher wird das Ende des Spiels durch die Variable "eatenCherries" bestimmt; ist diese nämlich höher als sechs, hat man alle sieben Kirschen gesammelt, das Spiel gewonnen und der EndScreen erscheint.

## Schlusswort<a name="Schlusswort"></a>
Gerade in Anbetracht der kurzen Zeit und dem Anteil der eigenständigen Arbeit im Homeschooling, sind wir froh, unsere Ideen umgesetzt zu haben. Dabei haben wir uns anhand von YouTubevideos einen roten Faden geschaffen und durch fleißiges Probieren auch die letzten Probleme beheben können. Das Projekt war eine tolle Möglichkeit unsere bisherigen Informatikkenntnisse, besonders in Bezug auf Variablen und if-Funktionen, weiter zu bilden und nun auch eigenständig ohne Bausteine programmieren zu können. 
