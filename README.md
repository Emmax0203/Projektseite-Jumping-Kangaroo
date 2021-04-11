# Projektseite-Jumping-Kangaroo


## Einleitung<a name="Einleitung"></a>
Im zweiten Halbjahr des 12. Jahrgangs haben wir im Rahmen des wöchentlichen Informatikunterrichts innerhalb von ungefähr drei Monaten das jump and run Spiel "Jumping Kangaroo" programmiert. Dazu haben wir das Programm Greenfoot Javascript verwendet, da diese für Fortgeschrittene mit etwas Vorkenntnissen im Programmieren geeignet schien, die wir bereits im ersten Halbjahr erlangt haben. Dieses Programm arbeitet mit komplexeren Ausdrücken und nur Text. Demnach bot es eine Möglichkeit zur Steigerung für unsere Informatikkenntnisse. Nachdem wir uns die Einführungsvideos zu Greenfoot ausführlich angesehen haben, kamen wir mit den grundlegenden Prinzipien zurecht und konnten uns so das restliche Können aneignen.
Da wir dafür lediglich drei Monate Zeit hatten, sind wir mit dem Ergebnis zufrieden.

## Spielidee<a name="Spielidee"></a>
"Jumping Kangaroo" ist ein jump and run Spiel, bei dem es darum geht Kirschen einzusammeln und so den Sieg zu erlangen. Dabei gibt es einen Mindestscore von sieben Kirschen, welchen man erreichen muss, um das Spiel zu gewinnen. Die Kirschen kann man einsammeln, indem man von Plattform zu Plattform springt und auf dem Weg alle Kirschen mitnimmt. Pro gesammelter Kirsche kriegt man einen Pluspunkt, welcher im Score angezeigt wird. 

## Screens<a name="Screens"></a>
Für die Gestaltung der Screens haben wir das Programm "Paint" verwendet, um unsere eigenen Designs zu erstellen und in Greenfoot zu verwenden. Mithilfe der Spacetaste kann man aufgrund eines Befehls im Startscreen zum tatsächlichen Screen und Spiel gelangen. Hat man am Ende des Spiels alle Kirschen eingesammelt und somit den Mindestscore erreicht, wird der Gewinnscreen aufgerufen und angezeigt.

## actor<a name="actor"></a>
Bei Greenfoot arbeitet man vor allem mit sogenannten "actorn". Diese können verschiedene Funktionen besitzen. Im Spiel "Jumping Kangaroo" gibt es vier verschiedene "actor", nämlich: kangaroo, platform, cherry und victory.
Das Känguru ist die Hauptfigur des Spiels und sammelt die Kirschen ein. Hierzu kann es sich nach links und rechts bewegen, sowie springen und nach unten fallen. 

Die Platformen bilden die Sprung- und Landeflächen für das Känguru und sorgen dafür, dass dieses zu den Kirschen gelangen kann. Des Weiteren kann man nicht von unten durch diese durchspringen, da sie aus einem festen Material sind. Man kann nur von oben auf den Platformen landen und von diesen wieder abspringen. 

Die Kirschen sind die Objekte, welche eingesammelt werden müssen und Punkte bringen. Sie sorgen dafür, dass man das Spiel gewinnen kann, da sie die Variable "eatenCherries" verändern und so die Punktzahl erhöhen.

Victory bildet den Endscreen, wenn jemand alle Kirschen eingesammelt und somit das Spiel gewonnnen hat. 

## Funktionen<a name="Funktionen"></a>
Startscreen: Der Startscreen hat nur eine if-Funktion, durch die beim Drücken der Spacetaste der Startscreen verschwindet und der Screen myworld geöffnet wird.

MyWorld: Wir haben eine Variable "eatenCherries", die den Score festlegt, sowie ein Textfeld, das diese Variable anzeigt. Außerdem haben wir eine "Prepare-Funktion"(public void prepare), welche die Ausgangslage unserer Welt gestlegt. In dieser Funktion ist die Anzahl, Platzierung und Art aller Objekt in dieser Welt, festgelgt. Das sind bei uns sieben Kirschen, sieben Platformen und ein Känguru. Hinzu kommt eine Funktion für das Ende des Spiels (public void act), in der geschrieben steht, dass wenn der Wert der Varibale "eatenCherries" höher als sechs ist, der Victoryscreen abgerufen wird. 

Kangaroo: Zum Bewegen des Kängurus nach links und rechts bedarf es einer Funktion (public void move). Diese legt fest, dass beim Drücken der Rechts- und Linkspfeile der Tastatur die Position des Kängurus verändert wird. Dabei hat das Känguru eine Schrittweite von drei in beide Richtungen. Die Funktion dient nur zur Bewegung in horizontaler Richtung und beeinflusst somit die y-Koordinate nicht. Um einen springenden actor zu erschaffen, mussten wir erst eine statische Variable erstellen, die für die Gravitation steht (gravity). 
