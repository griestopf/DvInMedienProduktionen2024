Angelehnt an: https://www.gamingnexus.com/Article/5807/Marble-It-Up!/

![Image of example game.](content\200_gruppe02\image_Kugel.png)

Beschreibung:
Das Ziel besteht darin mit einer Murmel durch verschiedene Level zu navigieren und das Ziel schnellstmöglichst zu erreichen.
Die Level an sich bieten Zahlreiche Hindernisse und Sprungpassagen und zudem Power-ups die aufgesammelt werden können und verschiedene Fähigkeiten liefern.

# Mögliche Integration der Vergleichskategorien

## Benutzerfreundlichkeit / Usability der Engine
- Mit wie viel Aufwand ist es verbunden X zu realisieren?
	- Einfache Dokumentation, z.B.:
		- Wie wurde die Kamera implementiert?
		- Wie wurde die Physik implementiert?
		- Wie wurde die Gamelogik geskriptet? (z.B. Power-up aufsammeln)
- Wie schwer ist der Einstieg?
	- Ergibt sich anhand der Spielentwicklung
		- Benutzen der Dokumentation
		- Onlinerecherche
## Performance
- FPS unter verschiedenen Bedienungen und Plattformen
	- Logging für die verschiedenen Metriken (Min, Max, Avg FPS, Frametime..)
	- Benchmarks eines Demo-Levels das automatisch durchlaufen wird unter verschiedenen Plattformen

## Grafikqualität
- Standard-Licht und Schatten-Effekte
	- Können in die Level integriert werden
		- Schattenwurf von Hindernissen
		- Diverse Lichtquellen in den Level
- Partikelsysteme
	- Könnten getestet werden bei
		- Erreichen des Ziels
		- Aufsammeln von Power-ups
		- Zerstörung der Murmel (Zersplittern)
- Postprocessing-Effekte
	- Können als diverse Effekte in das Spiel integriert werden

## Programmiersprache, Programmierumgebung und Tooling (inkl. Source Control)

- Kollaboration:
	- Gemeinsames Szene-Editing mit Source Control
		- Ist es möglich an der gleichen Szene gleichzeitig zu arbeiten mit einfach zu handhabenden merge conflict?
- Debugging, Profiling
	- Kann anhand des Spiels getestet und dokumentiert werden
- IDE-Integration
	- Test während der Spielentwicklung
- 

## Unterstützte Plattformen
- Export für verschiedene Plattformen (PWA, WebGL, Desktop (Windows, Linux))
	- Hindernisse / Hürden