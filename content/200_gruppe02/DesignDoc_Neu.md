# Style / Welt

## Brainstorm (aus Dokument Version 1)

Springen, Sliden, Laufen/FRWD Movement, 3<sup>rd</sup> Person, Explosive Attack
<br/>Sci-fi space style: [Example 1](https://quaternius.com/packs/ultimatespacekit.html), [Example 2](https://quaternius.com/packs/ultimatemodularscifi.html)
<br/> Weg ist immer gerade, ohne Kurven.
<br/> Collectibles (?)

Das Spiel wird im Sci-fi space style realisiert.
Hierfür stehen beispielsweise folgende Asset-Packs zur Verfügung:
- Ultimate Space Kit
- Ultimate Modular Sci-Fi Pack
- Die Assets sind als "OBJ" und "FBX" verfügbar
    - Komptabilität mit Unity/Unreal/Godot

# Welt

- Da es sich um einen Endless-Runner handelt, wird die Welt prozedural generiert
    - Jeweils n verschiedene Abschnitte für drei verschiedene Schwierigkeitsgrade
    - Je nach erreichter Distanz erhöht sich die Schwierigkeit
    - Die Abschnitte können nahtlos aneinander gefügt werden
    - Ggf. verschiedene Farbcodierung der Abschnitte je nach Schwierigkeit
        - Grün => Einfach
        - Orange => Mittel
        - Rot => Schwer
    - Material / Gegebenheit der Bahn
        - Meist normales Material ohne physikalische Eigenschaften
        - Lava: Sofortiger Tod Gruppe 1
        - Ice: Slippery => Schwammigere Steuerung, automatisches rutschen Gruppe 1
    - Der Spieler kann sich frei auf der Bahn bewegen (Keine festgelegten lanes)

# Movement

- Der Charakter läuft/rennt automatisch vorwärts, hierfür wird kein Input benötigt
- Horizontale Bewegung
    - Die Tasten/Buttons müssen gehalten werden
    - Desktop: A/D Tasten
    - Mobile: Links/Rechts Buttons
- Springen
    - Dauert ein kurzes Zeitintervall an
    - Die Höhe bleibt konstant
    - Kann durch Crouch/Slide frühzeitig unterbrochen werden
        - Schnellere Beschleunigung nach unten
    - Desktop: Leertaste
    - Mobile: Nach oben swipen
- Sliden
    - Beim rutschen verkleinert sich der Charakter in eine geduckte/liegende Haltung und kann somit Hindernisse ausweichen/umgehen
    - Die Geschwindigkeit bleibt konstant
    - Desktop: Ctrl Taste
    - Mobile: Crouch/Slide button

# Kamera

- 3rd Person Kameraverfolgung des Charakters von hinten

# Power-Ups

Die Power-Ups sind für einen vordefinierten Zeitraum aktiviert, kann durch einen Timer visualisiert werden. 
- High-Jump: Erhöhte Sprunghöhe (10 Sekunden) 
- Shield: Spieler erhält keinen Schaden wenn er "aus der Welt fällt" 
- Distance Boost: Der Charakter schwebt über die Bahn/Welt für x Sekunden 
    - Verhindert die Möglichkeit mit Hindernissen zu kollidieren

# Hindernisse
- Low/Mid/High Block

    - Low Block: Kleines Hindernis, das durch Sprünge oder seitliche Bewegung umgangen werden kann
    - Mid Block: Mittelgroßes Hindernis, das ebenfalls durch einen Sprung oder horizontaler Bewegung umgangen werden kann
        - Unterschied zu "Low Block": Benötigt präziseres timing des Sprungs um Kollisionen zu vermeiden
    - High Block: Kann nur durch seitliche Bewegung umgangen werden

- Float Blöcke

    - Float Block: Schwebendes Hindernis, das nur durch sliden, springen oder seitliche Bewegung umgangen werden kann
    - High Float Block: Kann nur durch sliden oder seitlicher Bewegung umgangen werden

- Low/Mid/High Platform

    - Low Platform: Kleines Hindernis, das durch Sprünge oder seitlicher Bewegung umgangen werden kann => Es ist möglich auf dem Hindernis weiterzulaufen (Bsp.: Züge / Subway Surfers)
    - Mid Platform: Mittelgroßes Hindernis, wie "Low Platform", benötigt aber präziseres timing für den Sprung
    - High Platform: Kann nur seitlich umgangen werden, mit verbesserter Sprunghöhe durch das "High-Jump" Power-Up ist es dennoch möglich darauf zu springen

# Misc

- ~~Breakable Wall: Eine Wand die dem Spieler den Weg blockiert und durch Beschuss durchbrochen/zerstört werden kann Gruppe 1 / Wir~~
- ~~Curved Slides: Tunnel ähnliche Struktur die man durch sliden und seitlicher Bewegung durchqueren kann~~
- Explosive Barrels: Kollision mit Barrel sorgt für Explosion, behindert den Spieler nicht, Bruchstücke interagieren aber mit der Welt Gruppe 1
- Wrecking Ball: Pendelt seitlich als Abrissbirne hin und her Gruppe 1 / Wir
    - Seitliche Kollision schleudert Spieler aus der Welt (?)
- Piston: Schiebt Spieler aus der Bahn, ggf. in Hindernis Gruppe 1 / Wir
