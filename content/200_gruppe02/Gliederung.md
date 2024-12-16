## 1. Einleitung

- Ziel und Zweck des Artikels
- Vorstellung der untersuchten Engines: Unity, Unreal Engine, Godot
- Methodik des Vergleichs

## 2. Erfahrungsberichte der Teams

- 2.1 Unity
    - Persönliche Erfahrungen bei der Arbeit mit Unity
    - Herausforderungen und Lösungen
    - Gesamteindruck: Usability, Lernkurve, Stärken und Schwächen

- 2.2 Unreal Engine
    - Persönliche Erfahrungen bei der Arbeit mit Unreal
    - Herausforderungen und Lösungen
    - Gesamteindruck: Usability, Lernkurve, Stärken und Schwächen

- 2.3 Godot
    - Persönliche Erfahrungen bei der Arbeit mit Godot
    - Herausforderungen und Lösungen
    - Gesamteindruck: Usability, Lernkurve, Stärken und Schwächen

## 3. Vergleich der Engines nach Kategorien
###  3.1 Benutzerfreundlichkeit und Usability

- Vergleich der Bedienbarkeit und Lernkurve
- Integration von 3rd-Party-Add-Ons und Ökosystem-Analyse
- Dokumentation, Tutorials und Community-Support

### 3.2 Performance

- FPS, Speicherverbrauch, Ladezeiten unter ähnlichen Bedingungen
- Ergebnisse aus einem automatisierten Benchmark mit einem Demo-Spiel
- Stärken und Schwächen in unterschiedlichen Plattform-Szenarien

### 3.3 Programmiersprachen, Umgebung und Tooling

- Unterstützte Sprachen: Erlernbarkeit und Debugging-Möglichkeiten
- Tooling: Debugger, Profiler und IDE-Integration
- Möglichkeiten zur Zusammenarbeit (z. B. Version Control)

### 3.4 Grafikqualität

- Licht- und Schatteneffekte, Partikelsysteme, Postprocessing
- Visuelle Limitierungen und Anpassungsmöglichkeiten

### 3.5 Unterstützte Plattformen

- VR/AR, Smartphones, Konsolen, PC
- Plattform-Vielfalt und Integration

### 3.6 Rentabilität und Kosten

- Lizenzmodelle und langfristige Flexibilität
- Kostenanalyse (Pay-per-Use vs. Pay-per-Sale)

### 3.7 Animation und Physics

- Umsetzung einer Character-Animation: Aufwand und Workflow
- Vergleich der Physics-Features und Bedienung

## 4. Zusammenfassung der Ergebnisse

- Tabellarische Übersicht der wichtigsten Erkenntnisse
- Stärken und Schwächen der Engines in unterschiedlichen Szenarien
- Empfehlungen für verschiedene Anwendungsfälle

## 5. Fazit

- Reflexion der Ergebnisse
- Bedeutung des Erfahrungsberichts für den Vergleich
- Zukunftsausblick: Trends und mögliche Entwicklungen

## 6. Anhang

- Detailtabellen
- Links und Ressourcen (z. B. zu Tutorials oder Dokumentationen)
- Verwendete Tools und Quellen



# Überarbeitete Gliederung:

## 1. Einleitung
### 1.1 Ziel der Analyse
- Vorstellung der untersuchten Game Engines: Unity, Unreal Engine, Godot
- Ziel: Vergleich der Engines anhand von Benutzerfreundlichkeit, Performance, Tools, Grafikqualität, Plattformunterstützung, Kosten und weiteren relevanten Kriterien

### 1.2 Methodik
- Erfahrungsberichte der Teams als zentraler Bestandteil
- Durchführung standardisierter Tests und Generierung messbarer Werte
    - Physik Benchmark: 
        - Becken mit Kugeln füllen
        - Abbruch wenn Frametime > 100ms -> Wie viele Kugeln wurden instanziiert?
        - Dimension Becken 20 x 20 Units, 10 hoch
        - Kugelradius 0,25 -> Durchmesser 0,5
        - Kamera Pos: senkrecht, Beckenrand = Bildschirm von 1
        - Bildschirmauflösung: 1920 x 1080p
    - Grafik Benchmark:
        - Wir ein Grid aus Blöcken gespawnt 
        - pro iteration um eine Spalte und Reihe vergrößert
        - Kamera um Mittelpunkt zentriert, die um das Gebilde rotiert
        - Wird so lange Wiederholt, bis 100ms Frametime erreicht
        - Wird eine Art Turm gebaut
- Kombination aus qualitativer und quantitativer Analyse

### 1.3 Facts über die Engine
- Lizenzmodelle und Kostenanalyse (z. B. Pay-per-Use vs. Pay-per-Sale)
    - ![Tabellenbild 1](content\200_gruppe02\Tabelle1.png)
    - ![Tabellenbild 2](content\200_gruppe02\Tabelle2.png)
    - Es wurde angekündigt, dass es eine Runtime Gebühr geben soll. Diese wurde allerdings nach Beschwerden innerhalb der Community verworfen.
- Verbreitung und Community-Support
    - Unity wird hauptsächlich für 2D und VR Anwendungen benutzt

---

## 2. Erfahrungsberichte der Teams
- **Lernkurve**: Wie einfach war der Einstieg in die Engine?
    - Dokumentation/Hilfestellung
        - Gute Code Dokumentation über das [Unity Manual](https://docs.unity3d.com/Manual/index.html)
        - Guter Einstieg mit Hilfe von [Unity Learn](https://learn.unity.com/)
        - Sehr gute Community Hilfe über Youtube, Reddit und andere Platformen
        - Gutes Unity Forum [Discussion](https://discussions.unity.com/)
- **Probleme und Lösungen**: Welche Herausforderungen sind aufgetreten, und wie wurden sie gelöst?
    - Beim Importieren von 3D-Modellen traten kleine Schwierigkeiten auf, insbesondere bei der Nutzung von `.blend`-Dateien. 
    Blender musste installiert werden, da es sonst zu Errornachrichten in der Engine kam.
    Um das Material des Objekts korrekt darzustellen, mussten die Texturen manuell extrahiert und an die entsprechenden Stellen im Material gezogen werden. 
    Im Vergleich dazu war der Import mit `.fbx`-Dateien wesentlich einfacher, da diese direkt per Drag-and-Drop integriert werden konnten.
    - Ragdolls
        - Keine Einfache Ragdoll funktion, Ragdolls bestehen aus Character Joint, Capsule Collider und Rigidbody.
        - Bones werden nicht automatisch erkannt und müssen manuell gesetzt werden. ![Ragdoll](content\200_gruppe02\image_Ragdoll.png)
        - Ragdolls können nur aktiviert werden solange der AnimationnController nicht unter verwendung ist, daher gibt es keine einfache möglichkeit von Animation zu Ragdoll zu wechseln.
        - Die Lösung dafür ist ein Ragdoll enabler skript https://www.youtube.com/watch?v=RB18IyKZiB0

    - Animation (Mixamo to Unity)
        - Problem: Mixamo erlaubt nicht den Export der Animationalleine
        - Um mehrere Animation von Mixamo auf einen Character zu verwenden muss die Animation aus dem Importiert herauskopiert werden um im AnimationController verwendbar zu sein

- **Usability**: Wie intuitiv sind Benutzeroberfläche und Workflow? Gibt es hilfreiche Tutorials und Dokumentationen?
    - Das Arbeiten mit dem Partikelsystem war mit einem Tutorial verhältnismäßig einfach, um beispielsweise ein explodierendes 
    Fass zu erstellen. Ohne Anleitung wäre die Erstellung jedoch deutlich anspruchsvoller, was allerdings nur an den vielen Möglichkeiten liegt, 
    wie das Partiklesystem genutzt werden kann. 
    Die Vielfalt der Möglichkeiten, die das Partikelsystem bietet, wurde als sehr beeindruckend bewertet.
- **Programmiersprache/umgebung und Tooling**:
    - C# 
    - Man kann über verschiedene IDEs debuggen. Hierfür werden verschiedene Plugins zur Verfügung gestellt.
        - IDEs die Supportet werde sind unter anderem: Visual Studio Code, Visual Studio, Rider
    - Profiling: Man kann ein Spiel aufzeichnen und im nachhinein nachschauen, wie viele Frames vorhanden waren und wie lange jeder Engine Part pro Frame gedauert hat ![Profiler](content\200_gruppe02\image_Profiler.png)
    - unity unterstütz zudem Visual Scripting. Allerdings wird dieses kaum genutzt. 
- **Grafikqualität**: 

- **Gesamteindruck**: Persönliche Einschätzung der Arbeit mit der jeweiligen Engine

---

## 3. Vergleich nach Kategorien
### 3.1 Tests durchführen und Messwerte generieren
- Benchmarks zur Performance: FPS, Speicherverbrauch, Ladezeiten
- Grafiktests: Licht- und Schatteneffekte, Partikelsysteme, Postprocessing
- Tooling: Debugger, Profiler, Version Control
- Animation und Physics: Umsetzung von Animationen und physikalischen Simulationen

### 3.2 Messwerte zusammenfassen
- Präsentation der Ergebnisse in Tabellen und Diagrammen
- Vergleich der Engines anhand der generierten Daten

### 3.3 Unterstütze Platformen
- Desktop: Windows, Linux, Mac OS, 
- Mobile: Android, IOS
- Web: Web Assembly/OpenGL


---

## 4. Fazit
- **Stärken und Schwächen** der Engines
- **Empfehlungen**: Welche Engine eignet sich für welche Anwendungsfälle?

---

## 5. Anhang
- Tabellen mit Benchmark-Ergebnissen
- Links zu Tutorials und offiziellen Dokumentationen
- Verwendete Tools und Quellen

