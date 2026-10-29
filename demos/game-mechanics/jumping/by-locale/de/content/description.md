# Links- und Rechtsbewegung

Wie sich die Figur bewegt ist nicht das eigentliche Thema von dieser
Demo, aber es könnte hilfreich dabei sein sich anzuschauen, wie sich
das Kostüm verändert um den Charakter in die Richtung zeigen zu lassen
in die er sich bewegt.  Der Code überprüft nicht, wo der Charakter
sich am Bildschirm befindet, also kannst du ihn off-screen bewegen.


# Springen

Der Charakter springt wenn du die Leertaste drückst, daher ist der
Code im Skript _Wenn Taste Leertaste gedrückt wird_. Die
hauptsächliche Logik fürs Springen befindet sich in dem Abschnitt mit
der Variable `y_geschw`.  Zu Beginn bewegen wir den Charakter recht
schnell nach oben, indem wir die dessen _y_-Koordinate um 8
ändern. Dann reduzieren wir die Geschwindigkeit langsam zu -8, um den
Charakter zurück zur Erde zu bewegen. All diese Änderungen an _y_
ergeben in Summe Null, weshalb der Charakter am Ende die exakt gleiche
Höhe wie am Anfang hat.  Dieser gesamte Prozess imitiert, wie die
Schwerkraft funktioniert.


# Vermeiden von Doppelsprüngen

Wir wollen sicherstellen, dass der Charakter keinen neuen Sprung
beginnt während er sich noch mitten im vorherigen Sprung befindet. Der
Code benutzt eine Boolean-Variable `springen` um diesen Zustand zu
verfolgen. Zu Beginn (_Wenn die grüne Flagge angeklickt_) springt der
Charakter _nicht_, also hat `springen` den Wert `False`. Im Skript
_Wenn Taste Leertaste gedrückt wird_ prüfen wir zuerst, ob der
Charakter sich in einem Sprung befindet, und halten das Skript an,
falls das der Fall ist.  Dann setzen wir `springen` zu `True` während
die Auf- und Abwärtsbewegung passiert und zurück zu `False` nachdem
das Sprung fertig ist.


# Credits

Danke an [GrafxKid](https://opengameart.org/content/green-robot) für
das Kostüm!
