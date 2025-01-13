+++
title = 'Artikel Infos'
date = 2024-09-28T15:40:23+02:00
draft = false
weight = 500

+++

## Gliederung des Artikels

Legende: (***Ü***) - Gruppenübergreifender Abschnitt. (***G***) - von jeder Gruppe zu erstellender Abschnitt.

# 1. Einleitung (***Ü***)
   ## Ziel der Analyse
   Überblick über Engines, Gemeinsamkeiten und Unterschiede ggf. Empfehlungen

   ## Methodik

   Um die Leistungsfähigkeit und Benutzerfreundlichkeit verschiedener Game Engines zu analysieren, haben wir ein zweigeteiltes Verfahren angewendet. Dieses umfasst sowohl objektive, messbare Tests als auch subjektive Erfahrungsberichte, die während der Entwicklung eines Beispielprojekts gewonnen wurden. Ziel ist es, die Stärken und Schwächen der Engines zu evaluieren und eine fundierte Grundlage für Empfehlungen bereitzustellen.

   - ### Objektive Tests nach Kategorien

      **Physik-Benchmark:**

      Ein rechteckiges Becken (20 × 20 Meter) wird kontinuierlich mit Kugeln gefüllt, die pro Sekunde nacheinander instanziiert werden. Die Simulation wird beendet, sobald die Frame-Time (Delta) 100 ms überschreitet, was einer Framerate von ≤ 10 FPS entspricht. Das Messergebnis gibt an, wie viele Kugeln instanziiert werden konnten, bevor die Leistungsgrenze erreicht wurde.

      - Szenenaufbau:
         - Beckenabmessungen: 20 × 20 Meter.
         - Kugelradius: 0,05 Meter (Durchmesser: 0,1 Meter).
         - Kameraposition: Senkrecht über dem Becken zentriert.
         - Kamera-Öffnungswinkel: 60°.
         - Kameraabstand: So gewählt, dass das Becken den oberen und unteren Bildschirmrand vollständig ausfüllt.

      **Grafik-Benchmark:**

      Zur Überprüfung der Grafikleistung wird ein Turm aus Blöcken schrittweise aufgebaut. Dabei wird in jeder Iteration das Grid um eine Spalte und eine Reihe vergrößert, wodurch die Gesamtanzahl der Blöcke exponentiell ansteigt. Eine Kamera, die um den Mittelpunkt des Turms rotiert, stellt sicher, dass möglichst viele Flächen gerendert werden. Der Test endet, wenn die Frame-Time 100 ms überschreitet. Das Messergebnis gibt an, wie groß der Turm (in Blockanzahl) wird, bevor die Leistungsgrenze erreicht wird.

      - Szenenaufbau:
         - Die Kamera bleibt zentriert auf den Turm ausgerichtet und rotiert um diesen herum.
         - Turm wird pro Iteration um eine Spalte und Reihe vergrößert


   - ### Entwicklung eines Beispielprojekts: Endless Runner

      Neben den Benchmarks wurde ein Endless-Runner-Spiel entwickelt, um die Engines unter praxisnahen Bedingungen zu testen. Das Projekt umfasst wesentliche Spielelemente wie:

      - Prozedural generierte Levelabschnitte.
      - Gameplay-Mechaniken wie Laufen, Springen und Hindernisse.
      - Eine 3D-Welt mit Sci-Fi-Thematik, die Assets und Partikel verwendet.

      Die Entwicklung des Projekts diente dazu, qualitative Eindrücke über die Benutzerfreundlichkeit, die Arbeitsabläufe und die Lernkurve der jeweiligen Engines zu sammeln. Aspekte wie die Zugänglichkeit der Dokumentation, die Effizienz der Entwicklungsumgebung und die Eignung der Engines für ein prozedurales Spiel wurden hierbei bewertet.

   - ### Kombination qualitativer und quantitativer Analyse

      Die gewonnenen Ergebnisse aus den Benchmarks und der Entwicklung des Endless Runners wurden miteinander kombiniert, um eine ganzheitliche Bewertung zu ermöglichen. So konnten sowohl die technische Leistungsfähigkeit als auch die praktischen Vor- und Nachteile der Engines erfasst werden.

      Mit diesem Verfahren wird sicher gesellt, dass die Analyse sowohl fundierte, datenbasierte Einblicke bietet, als auch die Erfahrungen der Teams und der tatsächlichen Entwicklung berücksichtigt.

# 2. Unity (Erfahrungsbericht zur Erstellung eines Endless Runner mit der Engine) (***G***)
   - ### Facts über Engine
     - Lizenzmodell

         Unity bietet verschiedene Lizenzmodelle an, darunter kostenlose und kostenpflichtige Versionen. Eine Runtime-Gebühr wurde angekündigt, jedoch nach massiven Beschwerden der Community wieder verworfen.
         - ![Tabellenbild 1](/content/200_gruppe02/Tabelle1.png)
         - ![Tabellenbild 2](/content/200_gruppe02/Tabelle2.png)

     - Verbreitung

         Unity ist vor allem für 2D- und VR-Anwendungen weit verbreitet. Dank einer starken Community bietet die Engine zahlreiche Ressourcen:
         - Gute Code-Dokumentation über das [Unity Manual](https://docs.unity3d.com/Manual/index.html)
         - Unkomplizierter Einstieg mit Hilfe von [Unity Learn](https://learn.unity.com/)
         - Sehr gute Community Hilfe über Youtube, Reddit und andere Platformen
         - Unterstützung durch Foren ([Unity Discussion](https://discussions.unity.com/)) und Plattformen wie Reddit und Youtube
   - ### Benutzerfreundlichkeit, Usability
      - Die Benutzeroberfläche ist übersichtlich und intuitiv, auch wenn die Vielzahl der Funktionen anfangs überwältigend wirken kann.
      - Tutorials erleichtern den Einstieg enorm, z. B. beim Partikelsystem:
         - Mit Anleitung war es einfach z. B. ein explodierendes Fass zu erstellen. Ohne Anleitung wäre dies aufgrund der Funktionsvielfalt anspruchsvoller gewesen.

      - Insgesamt beeindruckt Unity durch die enorme Flexibilität und Anpassungsfähigkeit, die jedoch mit einer steileren Lernkurve verbunden ist.
   - ### Programmierumgebung und Tools
      - Unity verwendet C# als Programmiersprache und unterstützt gängige IDEs wie Visual Studio, Visual Studio Code und Rider.
      - Debugging und Profiling:
         - Die integrierten Tools ermöglichen detaillierte Analysen, wie z. B. die Nutzung des Profilers zur Überprüfung der Frame-Time.
         - ![Profiler](/content/200_gruppe02/image_Profiler.png)
      - Visual Scripting wird unterstützt, ist jedoch wenig verbreitet.
   - ### "Grafikqualität"
      - Die Grafikqualität ist stark von den eingesetzten Renderpipelines (URP, HDRP oder Built-in) abhängig.
      - Besonders bei prozedural generierten Levels, wie im Endless Runner, konnte Unity mit flüssigen Übergängen und hochwertiger Darstellung überzeugen.
   - ### Character Animation
      - Unity bietet einen leistungsstarken Animator mit einer State-Maschine, die Übergänge zwischen Animationen steuert.
      - Übergangszeiten und Bedingungen können einfach angepasst werden.
      - Mixamo zu Unity Problem:
         - Mixamo erlaubt keinen direkten Export von Animationen.
         - Lösung: Animationen müssen aus dem Import extrahiert werden, um sie im Animator verwenden zu können.
      - Ragdoll-System:
         - Die Erstellung von Ragdolls ist komplex, da keine automatische Erkennung der Bones erfolgt.
         - Zudem gibt es keine einfache Möglichkeit, zwischen Animation und Ragdoll zu wechseln, da Ragdolls nur aktiviert werden können, solange der Animation Controller nicht verwendet wird
         - Lösung: Ein Ragdoll-Enabler-Skript (siehe [YouTube-Tutorial](https://www.youtube.com/watch?v=RB18IyKZiB0)) 
   - ### Lernkurve
      - Der Einstieg in Unity ist dank umfassender Ressourcen wie Unity Learn und der großen Community relativ einfach.
      - Für spezifische Themen wie das Partikelsystem oder Animationen können jedoch zusätzliche Tutorials notwendig sein.
      - Insgesamt bietet Unity eine moderate Lernkurve mit viel Unterstützung, allerdings erfordert die Vielzahl der Funktionen eine Einarbeitungszeit.
   - ### Probleme & Lösungen, Eigenheiten
      - Import von 3D-Modellen:
         - Probleme beim Importieren von .blend-Dateien ohne installierten Blender.
         - Manuelles Extrahieren und Zuweisen von Texturen notwendig.
         - Lösung: Verwendung von .fbx-Dateien für einen reibungslosen Workflow.

      - Ragdolls:
         - Keine automatische Erkennung von Bones; manuelles Setup notwendig.
         - Animation zu Ragdoll-Übergang nicht nativ möglich.
         - Lösung: Ragdoll-Enabler-Skript.

      - Mixamo-Animationen:
         - Problematischer Export mehrerer Animationen.
         - Lösung: Manuelles Extrahieren und Einbinden in den Animation Controller.
   - ### Gesamteindruck
      - Die Engine bietet eine Vielzahl an Tools und Funktionen, die jedoch mit einer gewissen Komplexität einhergehen.
      - Besonders hervorzuheben sind die engagierte Community und die gute Dokumentation, die den Einstieg und die Fehlerbehebung erleichtern.
      - Für den Endless Runner hat sich Unity als eine geeignete Wahl erwiesen, da die Engine sowohl prozedurale Levelgenerierung als auch komplexe Animationen gut unterstützt.
      - Trotz kleinerer Eigenheiten und Herausforderungen ist Unity eine vielseitige und leistungsstarke Engine, die sich sowohl für Anfänger als auch für erfahrene Entwickler eignet.

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
   - Stärken/Schwächen der Engine ((***G***) - Stichwortartig erfassen
   - Unity:
      - Stärken:
        - Gute Community mit vielen Hilfestellungen via YouTube, Reddit und anderen Foren
        - Viele Open Source Ressourcen
        - Eigener Asset Store mit viele Inhalten
        - Weitreichende Platformunterstützung
        - Flexibilität bei Betriebssystemen 
        - Umfangreiche Tools, die die Entwicklung vereinfachen
      - Schwächen: 
        - Komplexe Ragdoll-Implementierung
        - UI System ist umständlich

    (***Ü***) Zusammentragen und als Kapitel niederschreiben)
   - Empfehlungen ((***G***) - Stichwortartig erfassen; 
   - Unity:
      - Ideal für VR und 2D-Anwendungen: 

         Unity hat sich in diesen Bereichen durchgesetzt und bietet hier starke Unterstützung.

      - Geeignet für grafisch weniger anspruchsvolle 3D-Spiele: 
      
         Während 3D-Entwicklung mit Unity möglich ist, wird Unreal Engine häufig bevorzugt, wenn Spiele eine sehr hohe Grafikqualität erfordern.

      - Budgetfreundliche Option: 
            
         Für kleinere oder mittelgroße Projekte mit begrenztem Budget, bei denen eine breite Plattformunterstützung und schnelle Prototypenerstellung benötigt wird, ist Unity eine exzellente Wahl.

   - Empfehlung im Vergleich:
      
      Für Projekte, die höchste Anforderungen an Grafik stellen, wie realistische Simulationen oder AAA-Titel, könnte Unreal Engine die bessere Wahl sein. Für Projekte mit mittlerer bis niedriger Grafikqualität, besonders bei kleineren Teams, spielt Unity seine Stärken aus. 
   
   
   (***Ü***) Zusammentragen und als Kapitel niederschreiben) STILL TODO

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

 