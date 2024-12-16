+++
title = 'Artikel Infos'
date = 2024-09-28T15:40:23+02:00
draft = false
weight = 500

+++

## Gliederung des Artikels

Legende: (***Ü***) - Gruppenübergreifender Abschnitt. (***G***) - von jeder Gruppe zu erstellender Abschnitt.

1. Einleitung (***Ü***)
   - Ziel der Analyse
     - Überblick über Engines, Gemeinsamkeiten und Unterschiede ggf. Empfehlungen
   - Methodik
     - Zweigeteiltes Verfahren: Objektive Tests nach Kategorien PLUS Erfahrungsbericht beim Erstellen eines Beispiel-Game 
	 - Beschreibung der Vorgehensweise

2. Unity (Erfahrungsbericht zur Erstellung eines Endless Runner mit der Engine) (***G***)
   - Facts über Engine
     - Lizenzmodell
     - Verbreitung
   - Benutzerfreundlichkeit, Usability
   - Programmierumgebung, Tools
   - "Grafikqualität"
   - Character Animation
   - Lernkurve
   - Probleme & Lösungen, Eigenheiten
   - Gesamteindruck

3. Unreal (***G***)
   - Struktur wie Unity

4. Godot (***G***) 
   - Struktur wie Unity

5. Vergleich (nach Kategorien)
   - Testkategorien:
	 - Unterstützte Plattformen
	 - Rentabilität/Kosten 
	 - Performance
	   - Rendering (nach u. s. Benchmark)
	   - Physik(nach u. s. Benchmark)
    - TODO
      - Tests durchführen und Messwerte/Ergebnisse generieren (***G***)
 	 - Messwerte zusammenfassen und tabellarisch darstellen (***Ü***)

6. Fazit
   - Stärken/Schwächen der Engine (***G***)
   - Empfehlungen (***G***)

5. Anhang (***G***)


## Specs Physik-Benchmark

- Becken mit Kugeln Füllen (eine Kugel pro Sekunde)
- Abbruch, wenn Frame-Time (Delta) > 100 ms (Framerate <= 10 FPS)
- Messergebnis: Wieviele Kugeln sind bis dahin instanziiert?
- World-Aufbau:
	- Dimension Becken: 20x20 m (Units)
	- Kugelradius 0.05 m; (Durchmesser 0,1m)
	- Kamera-Position über Becken, senkrecht nach unten blickend
	- Kamera-Öffnungswinkel 60°
	- Kamera-Abstand so, dass oberer und unterer Beckenrand jewwils am oberen und unteren Bildschirmrand liegen


## Specs Rendering-Benchmark
- Viewing-Frustum mit komplexem Objekt (TBD) Füllen
- Abbruch, wenn Frame-Time (Delta) > 100 ms (Framerate <= 10 FPS)

 