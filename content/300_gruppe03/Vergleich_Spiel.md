
# Vergleich der Game-Engines Gruppe 3

# Vergleich der Spiele-Engines: Unity, Unreal Engine, Godot

## 1. Benutzerfreundlichkeit / Usability der Engine

### Wie vergleichen?
- **Einstieg**: Jedes Team dokumentiert, wie einfach oder schwer es ist, mit der jeweiligen Engine zu starten (Erstellung des ersten Projekts, Benutzeroberfläche). Vermerkt, wie lange es dauert, die ersten spielbaren Elemente zu erstellen (z.B. Spielfigur, Steuerung).
- **UI und Workflow**: Analysiere die Benutzeroberfläche jeder Engine. Wie intuitiv ist der Workflow, z.B. für Level-Design, Asset-Integration und Debugging? Gibt es vorgefertigte Tutorials, die Einsteigern helfen?
- **Feature-Tabelle**: Erstellt eine Tabelle der Standard-Features (Physics, Kollisionsabfrage, Partikelsysteme, Licht und Schatten) und bewertet, wie einfach sie zu verwenden sind.
- **Beispiel**: Setzt eine einfache Spielfunktion um (z.B. Kollisionsabfrage in einem Jump'n'Run). Wie lange dauert es, dies in jeder Engine zu realisieren?

## 2. Integration von 3rd-Party Add-Ons in das Engine-Ökosystem (Marketplace etc.)

### Wie vergleichen?
- **Add-On Verfügbarkeit**: Jedes Team untersucht, wie viele Add-Ons im jeweiligen Marketplace verfügbar sind. Zum Beispiel KI-Module, Visual Scripting oder Audio-Plugins.
- **Funktionsumfang**: Teste die Funktionalität und Komplexität der verfügbaren Add-Ons, indem ein Beispiel-Add-On integriert wird (z.B. ein Animation-Paket).
- **Update-Geschwindigkeit**: Analysiere, wie häufig Add-Ons und die Engine selbst aktualisiert werden, und ob diese Updates neue Features oder Stabilitätsverbesserungen bringen.
- **Beispiel**: Installiere ein Partikelsystem-Plugin und integriere es in das Spiel. Vergleiche den Installationsprozess und die Funktionsweise in Unity, Unreal, und Godot.

## 3. Visuelle Qualität der Engines

### Wie vergleichen?
- **Licht und Schatten**: Jedes Team baut eine Szene mit Standard-Lichteffekten und dynamischen Schatten. Wie gut sehen die Effekte in jeder Engine aus? Welche Anpassungen sind erforderlich, um hochwertige Licht- und Schatteneffekte zu erzielen?
- **Partikelsysteme**: Teste, wie gut Partikelsysteme in jeder Engine integriert und anpassbar sind. Erstelle einfache Effekte wie Rauch, Feuer oder Funken.
- **Postprocessing**: Wende Standard-Postprocessing-Effekte (z.B. Bloom, Motion Blur, Depth of Field) an. Dokumentiere, wie gut die visuelle Qualität und die Anpassbarkeit sind.
- **Beispiel**: Erstelle eine Szene mit einer realistischen Lichtquelle, komplexen Schatten, und einem Partikelsystem. Vergleiche die visuelle Qualität unter den gleichen Bedingungen.

## 4. Plattformunterstützung (VR/AR, Smartphones, Konsolen, PC)

### Wie vergleichen?
- **Plattform-Export**: Jedes Team testet die Export- und Kompilierungsprozesse für verschiedene Plattformen (PC, Mobile, VR). Wie schnell und einfach lassen sich Projekte für verschiedene Plattformen vorbereiten?
- **Beispiel**: Exportiere das Spiel für PC und Mobile. Vergleiche die Dateigröße, Leistung und Stabilität auf beiden Plattformen.
- **Unterstützte Technologien**: Teste, ob und wie einfach VR/AR-Implementierungen in den jeweiligen Engines sind, falls relevant.

## 5. Rentabilität/Kosten

### Wie vergleichen?
- **Lizenzmodelle**: Untersuche die Kostenstrukturen (Unity Abonnement, Unreal Revenue Share, Godot kostenlos). Welche ist für ein langfristiges Projekt am kosteneffektivsten?
- **Kostenanalyse**: Berechne, wie teuer es wäre, ein fertiges kommerzielles Spiel zu veröffentlichen, basierend auf den Lizenzgebühren (z.B. Unreal Revenue-Share nach 1 Million Dollar Umsatz).
- **Beispiel**: Erstelle eine Kostenprognose für jedes Team, basierend auf dem angenommenen Spielumsatz.

## 6. Performance

### Wie vergleichen?
- **FPS, Ladezeiten und Speicherverbrauch**: Jedes Team misst die FPS (min, max, avg), Ladezeiten und Speicherverbrauch in einer standardisierten Spielszene.
- **Automatisierte Benchmarks**: Verwende Tools wie Unreal's Profiler, Unity's Frame Debugger und Godot’s Performance Monitor, um Daten zu sammeln.
- **Plattformübergreifende Performance**: Teste die Spiele auf mehreren Plattformen und vergleiche die Performance. Wie verhalten sich die Engines auf mobilen Geräten im Vergleich zu PCs?
- **Beispiel**: Miss die Ladezeiten zwischen Levels und die durchschnittliche FPS während intensiver Spielszenen.

## 7. Programmiersprache, Programmierumgebung und Tooling

### Wie vergleichen?
- **Lernkurve**: Jedes Team bewertet die Lernkurve der jeweiligen Programmiersprachen (Unreal C++/Blueprints, Unity C#, Godot GDScript). Wie einfach oder schwer ist es, in die Sprache einzusteigen und erste Funktionen zu programmieren?
- **Debugger und Profiler**: Teste die Verfügbarkeit und Qualität von Debugging- und Profiler-Tools. Gibt es Möglichkeiten, Speicherverbrauch und Performance zu analysieren?
- **Version Control und Teamarbeit**: Überprüfe, wie gut die Version-Control-Integration (z.B. mit Git) funktioniert und ob mehrere Entwickler effizient zusammenarbeiten können.
- **Beispiel**: Implementiere die Spiellogik für eine zentrale Mechanik (z.B. Gegner-KI im FPS) und bewerte die Effizienz der Programmierumgebung.


## 1. Benutzerfreundlichkeit / Usability der Engine

### Endless Runner
- **Was wird getestet**: Erstellen eines einfachen Levels mit endlosen Laufmechaniken und Hindernissen.
- **Vergleichspunkte**:
  - Wie einfach ist es, die Laufmechaniken und die Platzierung der Hindernisse zu programmieren?
  - Wie intuitiv ist der Workflow für die Erstellung von prozeduralen Levels?
  - Gibt es vorgefertigte Tools oder Add-ons für die prozedurale Generierung?

### FPS Shooter
- **Was wird getestet**: Implementierung von Spielersteuerung, Kamerabewegung und Gegner-Interaktion (z. B. Schießen).
- **Vergleichspunkte**:
  - Wie einfach ist die Steuerung des Spielers (z. B. Bewegung, Schießen)?
  - Wie benutzerfreundlich sind die Tools für KI-Gegner und Animationen?
  - Gibt es vorgefertigte Assets wie Blueprints (Unreal) oder Standard Assets (Unity), die helfen?

### Auto Game
- **Was wird getestet**: Erstellen eines Levels, bei dem sich ein Auto auf einer Rennstrecke bewegt, einschließlich Kollisionsabfrage.
- **Vergleichspunkte**:
  - Wie einfach ist es, realistische Fahrzeugbewegungen und Kollisionen umzusetzen?
  - Gibt es integrierte Tools für Fahrzeugphysik?
  - Wie intuitiv ist die Benutzeroberfläche beim Bau der Rennstrecke?

## 2. Integration von 3rd-Party Add-Ons in das Engine-Ökosystem

### Endless Runner
- **Was wird getestet**: Verwenden eines 3rd-Party-Add-ons für prozedurale Level-Generierung.
- **Vergleichspunkte**:
  - Wie gut integrieren sich Add-ons für prozedurale Generierung?
  - Gibt es Add-ons für Power-Ups oder Level-Design?

### FPS Shooter
- **Was wird getestet**: Hinzufügen eines KI-Plugins für Gegnerintelligenz.
- **Vergleichspunkte**:
  - Wie viele Add-ons für KI und Waffen sind verfügbar? Wie einfach lassen sie sich integrieren?
  - Gibt es Add-ons für FPS-spezifische Mechaniken wie Schießen und Deckungssysteme?

### Auto Game
- **Was wird getestet**: Verwenden eines Fahrzeugphysik-Add-ons für realistische Fahrmechaniken.
- **Vergleichspunkte**:
  - Wie viele Add-ons sind für Fahrzeugphysik verfügbar?
  - Wie gut lässt sich ein Plugin für realistisches Fahren integrieren?

## 3. Grafikqualität

### Endless Runner
- **Was wird getestet**: Erstellen einer Szene mit Hintergründen, Beleuchtung und Partikeleffekten (z. B. Funken oder Wolken).
- **Vergleichspunkte**:
  - Wie gut ist die Beleuchtungs- und Schattenqualität für dynamische Umgebungen?
  - Wie leistungsstark ist das Partikelsystem für endlose Szenarien?

### FPS Shooter
- **Was wird getestet**: Implementierung von dynamischer Beleuchtung und Schatten in einer FPS-Umgebung.
- **Vergleichspunkte**:
  - Wie gut funktionieren die Beleuchtungs- und Schatteneffekte, wenn sich der Spieler durch verschiedene Bereiche bewegt?
  - Wie ist die Partikelqualität für Effekte wie Schussfeuer oder Explosionen?

### Auto Game
- **Was wird getestet**: Anwenden verschiedener Wetter- und Lichteffekte auf einer Rennstrecke.
- **Vergleichspunkte**:
  - Wie gut funktioniert die dynamische Beleuchtung (z. B. Sonne, Schatten) in Bewegung?
  - Wie leistungsstark sind Partikeleffekte (z. B. Staub oder Rauch)?

## 4. Plattformunterstützung

### Endless Runner
- **Was wird getestet**: Exportieren des Spiels auf mobile Plattformen.
- **Vergleichspunkte**:
  - Wie einfach ist es, das Spiel auf Smartphones zu kompilieren und zu testen?
  - Wie gut funktioniert es auf mobilen Geräten?

### FPS Shooter
- **Was wird getestet**: Testen des Spiels auf PC und VR.
- **Vergleichspunkte**:
  - Wie gut unterstützt die Engine VR? Gibt es integrierte VR-Plugins?
  - Wie gut läuft das Spiel auf PCs mit unterschiedlichen Spezifikationen?

### Auto Game
- **Was wird getestet**: Exportieren des Spiels auf Konsolen und PC.
- **Vergleichspunkte**:
  - Wie einfach ist es, das Spiel für Konsolen (z. B. PS4/5, Xbox) zu exportieren?
  - Wie stabil ist das Spiel auf Konsolen und PCs mit unterschiedlichen Grafikkarten?

## 5. Rentabilität/Kosten

### Endless Runner
- **Vergleichspunkte**:
  - Was sind die Entwicklungs- und Veröffentlichungskosten für einen Endless Runner auf Mobilgeräten? Vergleiche Lizenzgebühren (z. B. Unity-Abo vs. Unreal's Umsatzbeteiligung).
  - Welches Modell bietet die beste langfristige Flexibilität für Updates und Add-ons?

### FPS Shooter
- **Vergleichspunkte**:
  - Welche Engine bietet die beste Rentabilität für ein FPS-Spiel mit In-App-Käufen oder kostenpflichtigen Erweiterungen?
  - Welche Kosten entstehen bei der Veröffentlichung auf Steam und Konsolen?

### Auto Game
- **Vergleichspunkte**:
  - Welche Engine bietet die beste Preisstruktur für ein Auto-Rennspiel, das auf mehreren Plattformen (z. B. Mobilgeräte und Konsolen) veröffentlicht wird?
  - Wann ist Pay-per-Use vorteilhafter als einmalige Lizenzgebühren?

## 6. Performance

### Endless Runner
- **Was wird getestet**: Messen von FPS, Ladezeiten und Speicherverbrauch auf mobilen Geräten.
- **Vergleichspunkte**:
  - Wie hoch ist die FPS bei kontinuierlichem Gameplay (endlos)?
  - Wie schnell sind die Ladezeiten zwischen Levels oder Spielphasen?

### FPS Shooter
- **Was wird getestet**: Testen des Spiels auf PCs und Konsolen, insbesondere in intensiven Szenen (z. B. viele Gegner).
- **Vergleichspunkte**:
  - Wie gut bewältigt die Engine hohe FPS-Anforderungen (schnelle Bewegung, viele Effekte)?
  - Wie stabil ist die Framerate bei unterschiedlichen Hardwarekonfigurationen?

### Auto Game
- **Was wird getestet**: Messen von FPS und Ladezeiten während eines Rennens mit mehreren Autos und dynamischen Umgebungen.
- **Vergleichspunkte**:
  - Wie gut hält die Performance bei komplexen Berechnungen wie Fahrzeugphysik und Partikeleffekten?
  - Wie schnell laden Streckenabschnitte und wie viel Speicher wird für Texturen und Modelle verwendet?

## 7. Programmiersprache, Programmierumgebung und Tooling

### Endless Runner
- **Vergleichspunkte**:
  - Wie einfach ist es, Spielmechaniken zu programmieren (prozedurale Levels, Hindernisgenerierung)? (GDScript vs. C# vs. Blueprints)
  - Wie gut unterstützt die Engine Debugging und Profiling?

### FPS Shooter
- **Vergleichspunkte**:
  - Wie einfach ist es, KI für Gegner zu implementieren? Wie gut ist das Debugging-Erlebnis?
  - Gibt es spezialisierte Tools für FPS-Mechaniken (z. B. Waffen, Schießmechaniken)?

### Auto Game
- **Vergleichspunkte**:
  - Wie einfach ist es, Fahrzeugphysik und Steuerung zu programmieren?
  - Gibt es Tools oder Add-ons, die den Programmieraufwand reduzieren (z. B. vorgefertigte Physiksysteme)?

---



