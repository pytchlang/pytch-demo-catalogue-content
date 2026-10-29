# Einfache Bewegung ohne Grenzen

Du kannst das Schwein mit den `wasd`-Tasten bewegen. Es bewegt sich
gleichmäßig, aber ein Problem ist, dass du es komplett off-screen
bewegen kannst.

## Erklärung vom Code

Das Skript vom Schwein bestimmt dessen Startposition. Dann startet es
eine Endlossschleife und überprüft darin ob die Tasten `w`, `a`, `s`,
oder `d` gedrückt werden und, falls ja, bewegt sich das Schwein etwas
(indem die _x_ oder _y_-Koordinate aktualisiert wird). Um wieviel sich
das Schwein bewegt, wird in der Variable `tempo` bestimmt. Es ist
hilfreich diese Zahl in einer Variable zu speicher auch wenn sie sich
nicht verändert, weil der Code dadurch leichter anpassbar und lesbarer
wird.


# Einfache Bewegung, nur am Bildschirm.

Du kannst die Kuh mit den Pfeiltastn bewegen. Du kannst sie nicht
außerhalb des Bildschirms bewegen.

## Erklärung vom Code

Der Code ist sehr ähnlich zu dem des Schweins. Die neuen Teile sind:

* Es gibt eine Variable `x_limit` die uns sagt, wie weit nach links
  und rechts sich die Kuh bewegen kann. In der Schleife erlauben wir
  der Kuh nur mehr sich nach rechts zu bewegen, falls ihre
  _x_-Koordinate weniger als `x_grenze` ist.  Wir erlauben der Kuh nur
  mehr sich nach links zu bewegen, falls ihre _x_-Koordinate mehr als
  `-x_grenze` (das Negativ von `x_grenze`) ist.

* Es gibt eine Variable `y_grenze`, die dieselbe Aufgabe für Auf- und
  Abbewegung erfüllt.


# Bewegung mit Trägheit

Du kannst die Ziege mit den Tasten `ijkl` bewegen. Es benötigt etwas
Zeit um zu beschleunigen oder abzubremsen.

## Erklärung vom Code

Der Code der Ziege ist der komplizierteste. Wir beobachten die
Geschwindigkeit der Links- und Rechtsbewegungen sowie der Auf- und
Abwärtsbewegungen der Ziege.  Geschwindigkeit ist ähnlich zu Tempo,
nur dass die Geschwindigkeit auch die Richtung in die sich die Ziege
bewegt beinhaltet.

Das Drücken der Taste `i` bewegt die Ziege nicht direkt nach
oben. Stattdessen erhöht es den Wert der Variable `y_geschw` um den
Wert der Variable `beschl`, bis zu einer bestimmten Grenze. Ähnlich
dazu, reduziert das Drücken der Taste `k` den Wert der Variable
`y_geschw`. Falls weder `i` noch `k` gedrückt werden, nähert sich die
Geschwindigkeit der Zahl Null an.

Für Links- und Rechtsbewegungen machen wir genau dasselbe, indem wir
die Variable `x_geschw` anpassen. Dann ändern wir die _x_-Koordinate
um `x_geschw` und die _y_-Koordinate um `y_geschw`, aber gehen sicher,
dass die Ziege sich nicht außerhalb ihrer Grenzen bewegt.

Wir verwenden Pythons `min()`- und `max()`-Funktionen um
sicherzugehen, dass die Geschwindigkeitsvariablen nicht zu groß
werden, und, sodass sich die Ziege nicht außerhalb des Bilschirms
bewegt.


# Credits

Danke an Pexels-User*in [Damir K.](https://www.pexels.com/@damir/) für
die Außenaufnahme (die wir bearbeitet haben), und an
[FreePixel.art](https://freepixel.art/) für die Tiergrafiken.
