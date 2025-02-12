+++
title = 'Game Engine Vergleich'
date = 2024-09-28T15:40:23+02:00
draft = false
weight = 600

+++


Hier soll der gesamte Artikel zusammengeführt werden. 


Ein Beispiel-Bild:
![Example Image](images/example_image.png)

## Einleitung
Die Wahl der richtigen Game-Engine spielt eine entscheidende Rolle bei der Entwicklung von Computerspielen und beeinflusst sowohl die Effizienz des Arbeitsprozesses als auch die Qualität des Endprodukts. In diesem Bericht untersuchen wir drei der bekanntesten und am weitesten verbreiteten Game-Engines: Godot, Unreal Engine und Unity. Durch eine detaillierte Analyse möchten wir ihre Eigenschaften sowie die dazugehörigen Stärken und Schwächen aufzeigen, um Entwicklern und Interessenten eine fundierte Entscheidungsgrundlage zu bieten.
   
### Ziel der Analyse
Die Analyse konzentriert sich auf zentrale Aspekte wie Benutzerfreundlichkeit, technische Leistungsfähigkeit, Tool-Unterstützung und die Entwicklungsumgebung. Darüber hinaus spielt die Eignung der Engines für bestimmte Projekte – wie zum Beispiel das Entwickeln von Spielen, Simulationen, Software etc. – eine wesentliche Rolle. Neben der theoretischen Bewertung stellen wir daher auch praktische Erfahrungen vor, um einen praxisnahen Einblick in die Stärken und Schwächen der Engines zu geben. Unsere Ergebnisse sollen sowohl für professionelle Entwicklerteams als auch für Einzelpersonen nützlich sein, die sich in der Planung oder Umsetzung ihrer Projekte befinden. Durch die Ergebnisse unserer Arbeiten, möchten wir nicht nur technische Unterschiede aufzeigen, sondern auch Empfehlungen geben, welche Engine sich für spezifische Anwendungen und Anforderungen besonders eignet. Ziel ist es, einen umfassenden und zugleich verständlichen Überblick zu bieten, der eine informierte Entscheidung ermöglicht.

### Methodik
Um die Leistungsfähigkeit und Benutzerfreundlichkeit verschiedener Game Engines zu analysieren, haben wir zwei verschiedene Verfahren angewendet. Dieses umfasst sowohl objektive, messbare Tests als auch subjektive Erfahrungsberichte, die während der Entwicklung eines Beispielprojekts gewonnen wurden. Ziel ist es, die Stärken und Schwächen der Engines zu evaluieren und eine fundierte Grundlage für Empfehlungen bereitzustellen.

- Objektive Tests nach Kategorien

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

- Entwicklung eines Beispielprojekts: Endless Runner

    Neben den Benchmarks wurde ein Endless-Runner-Spiel entwickelt, um die Engines unter praxisnahen Bedingungen zu testen. Das Projekt umfasst wesentliche Spielelemente wie prozedural generierte Levelabschnitte und verschiedene Gameplay Mechaniken wie Laufen und Springen

    Die Entwicklung des Projekts diente dazu, qualitative Eindrücke über die Benutzerfreundlichkeit, die Arbeitsabläufe und die Lernkurve der jeweiligen Engines zu sammeln. Aspekte wie die Zugänglichkeit der Dokumentation, die Effizienz der Entwicklungsumgebung und die Eignung der Engines für ein prozedurales Spiel wurden hierbei bewertet.

- Kombination qualitativer und quantitativer Analyse

    Die gewonnenen Ergebnisse aus den Benchmarks und der Entwicklung des Endless Runners wurden miteinander kombiniert, um eine ganzheitliche Bewertung zu ermöglichen. Damit konnten sowohl die technische Leitungs, als auch die praktischen Vor- und Nachteile geschickt erfasst werden.

    Mit diesem Verfahren wird sicher gesellt, dass die Analyse sowohl fundierte, datenbasierte Einblicke bietet, als auch die Erfahrungen der Teams und der tatsächlichen Entwicklung berücksichtigt.


## Unity

### Die Engine
- Lizenzmodell

    Unity bietet verschiedene Lizenzmodelle an, darunter kostenlose und kostenpflichtige Versionen. Eine Runtime-Gebühr wurde angekündigt, jedoch nach massiven Beschwerden der Community wieder verworfen.
         
    - Personal, also die kostenfreie Version, ist Ideal für Einsteiger, da selbst kein Geld investiert werden muss und trotz allem die grundlegenden Funktionen wie Echtzeit-Entwicklung, Startbildschirm-Anpassung und der Unity Asset Manager verfügbar sind. 
    - Die Pro-Version ist ab 1.877€ im Jahr erhältlich und eignet sich für profesionelle Entwickler. Es werden zusätzliche Features wie ein erweiterter LZS-Support und ein größerer Asset Manager angeboten.
    - Enterprise ist auf große Teams und Firmen ausgerichtet. Diese Version umfasst Pro-Features und zusätzliche Optionen wie Build-Server-Lizenzen und einen vollen Zugriff auf den Quellcode. 
    - Bei der Industry-Lizenz ist der Fokus auf Unternehmen in spezifischen Branchen gelegt und es werden Branchenspezifische Toolkits angeboten. 
	
	Als referenz werden Screenshots eingefügt, um einen genaueren Vergleich zu ermöglichen.
     ![Tabellenbild 1](/content/200_gruppe02/Tabelle1.png)
     ![Tabellenbild 2](/content/200_gruppe02/Tabelle2.png)

- Verbreitung

    Unity ist vor allem für 2D- und VR-Anwendungen weit verbreitet. Dank einer starken Community bietet die Engine zahlreiche Ressourcen:
    - Gute Code-Dokumentation über das [Unity Manual](https://docs.unity3d.com/Manual/index.html)
    - Unkomplizierter Einstieg mit Hilfe von [Unity Learn](https://learn.unity.com/)
    - Sehr gute Community Hilfe über Youtube, Reddit und andere Platformen
    - Unterstützung durch Foren ([Unity Discussion](https://discussions.unity.com/)) und Plattformen wie Reddit und Youtube


### Benutzerfreundlichkeit, Usability
Die Benutzeroberfläche ist übersichtlich und intuitiv, auch wenn die Vielzahl der Funktionen anfangs überwältigend wirken kann.

Tutorials erleichtern den Einstieg enorm, z. B. beim Partikelsystem: Mit Anleitung war es einfach z. B. ein explodierendes Fass zu erstellen. Ohne ein Tutorial wäre dies aufgrund der Funktionsvielfalt anspruchsvoller gewesen.

Insgesamt beeindruckt Unity durch die Flexibilität und Anpassungsfähigkeit, die jedoch mit einer steileren Lernkurve verbunden ist.
### Programmierumgebung, Tools
- Unity verwendet C# als Programmiersprache und unterstützt gängige IDEs wie Visual Studio, Visual Studio Code und Rider.
    - Debugging und Profiling:
        - Die integrierten Tools ermöglichen detaillierte Analysen, wie z. B. die Nutzung des Profilers zur Überprüfung der Frame-Time.
        ![Profiler](/content/200_gruppe02/image_Profiler.png)
    - Visual Scripting wird unterstützt, ist jedoch wenig verbreitet.

### Grafikqualität
Die Grafikqualität ist stark von den eingesetzten Renderpipelines (URP, HDRP oder Built-in) abhängig. Besonders bei prozedural generierten Levels, wie im Endless Runner, konnte Unity mit flüssigen Übergängen und guter Darstellung überzeugen.

### Character Animation
Unity bietet einen leistungsstarken Animator mit einer State-Maschine, die Übergänge zwischen Animationen steuert. zudem können Übergangszeiten und Bedingungen einfach angepasst werden.
- Mixamo zu Unity Problem:
    - Mixamo erlaubt keinen direkten Export von Animationen.
    - Lösung: Animationen müssen aus dem Import extrahiert werden, um sie im Animator verwenden zu können.
- Ragdoll-System:
    - Die Erstellung von Ragdolls ist komplex, da keine automatische Erkennung der Bones erfolgt.
    - Zudem gibt es keine einfache Möglichkeit, zwischen Animation und Ragdoll zu wechseln, da Ragdolls nur aktiviert werden können, solange der Animation Controller nicht verwendet wird
    - Lösung: Ein Ragdoll-Enabler-Skript (siehe [YouTube-Tutorial](https://www.youtube.com/watch?v=RB18IyKZiB0)) 
### Lernkurve
Der Einstieg in Unity ist dank umfassender Ressourcen wie Unity Learn und der großen Community relativ einfach. Für spezifische Themen wie das Partikelsystem oder Animationen können jedoch zusätzliche Tutorials notwendig sein. 

Insgesamt bietet Unity eine moderate Lernkurve mit viel Unterstützung, allerdings erfordert die Vielzahl der Funktionen eine Einarbeitungszeit.
### Probleme & Lösungen, Eigenheiten
- Import von 3D-Modellen:
    - Probleme beim Importieren von .blend-Dateien ohne installiertes Blender.
    - Manuelles Extrahieren und Zuweisen von Texturen notwendig.
    - Lösung: Verwendung von .fbx-Dateien für einen reibungslosen Workflow.

- Ragdolls:
    - Keine automatische Erkennung von Bones; manuelles Setup notwendig.
    - Animation zu Ragdoll-Übergang nicht nativ möglich.
    - Lösung: Ragdoll-Enabler-Skript.

- Mixamo-Animationen:
    - Problematischer Export mehrerer Animationen.
    - Lösung: Manuelles Extrahieren und Einbinden in den Animation Controller.

### Gesamteindruck
Die Engine bietet eine Vielzahl an Tools und Funktionen, die jedoch mit einer gewissen Komplexität einhergehen. Besonders hervorzuheben sind die engagierte Community und die gute Dokumentation, die den Einstieg und die Fehlerbehebung erleichtern. Für den Endless Runner hat sich Unity als eine geeignete Wahl erwiesen, da die Engine sowohl prozedurale Levelgenerierung als auch komplexe Animationen gut unterstützt. Trotz kleinerer Eigenheiten und Herausforderungen ist Unity eine vielseitige und leistungsstarke Engine, die sich sowohl für Anfänger als auch für erfahrene Entwickler eignet.


## Unreal


## Überblick
Die Unreal Engine 5 (UE5), entwickelt von Epic Games, ist eine der leistungsstärksten Spiele-Engines auf dem Markt. Sie ist bekannt für ihre beeindruckenden High-End-Rendering-Fähigkeiten und professionellen Tools, die von AAA-Studios und Indie-Entwicklern gleichermaßen genutzt werden. UE5 unterstützt eine Vielzahl von Plattformen, darunter PC, Konsolen, mobile Geräte sowie VR/AR. Zu den herausragenden Features gehören:

- **Lumen:** Dynamische globale Beleuchtung in Echtzeit.
- **Nanite:** Virtualisierte Geometrie, die hochdetaillierte Umgebungen effizient darstellt.
- **Chaos Physics:** Fortschrittliche Physik-Engine für realistische Simulationen.

Offizielle Website: [Unreal Engine](https://www.unrealengine.com)

---

## Lizenzmodell
- **Kosten:** Die Unreal Engine ist grundsätzlich kostenlos nutzbar. Epic Games erhebt jedoch eine Umsatzbeteiligung von 5 %, wenn der Jahresumsatz eines Titels 1 Million USD überschreitet.
- **Epic Games Store:** Für Umsätze, die über den Epic Games Store generiert werden, entfällt die Lizenzgebühr.
- **Flexibilität:** Besonders attraktiv für Indie-Entwickler, da keine Vorabkosten anfallen. Größere Studios können individuelle Verträge aushandeln.

Weiterführende Informationen: [Unreal Engine Lizenzmodell](https://www.unrealengine.com/en-US/release)

---

## Verbreitung und Community
Die Unreal Engine ist sowohl in der AAA-Spieleentwicklung als auch bei Indie-Entwicklern weit verbreitet. Beispiele für bekannte Spiele sind **Fortnite**, **Gears of War** und **Final Fantasy VII Remake**. 

### Community und Ressourcen:
- **Foren und Discord-Gruppen:** Sehr aktiv und hilfreich für Problemlösungen und Feedback.
- **YouTube-Tutorials und Online-Kurse:** Eine große Auswahl an kostenlosen und kostenpflichtigen Lernressourcen.
- **Unreal Marketplace:** Umfangreiche Bibliothek an Plugins, Assets und Tools.

Nützliche Links:
- [Unreal Engine Forum](https://forums.unrealengine.com)
- [Unreal Engine Marketplace](https://www.unrealengine.com/marketplace)
- [YouTube-Tutorials für UE5](https://www.youtube.com/results?search_query=unreal+engine+5+tutorial)

---

## Benutzerfreundlichkeit und Usability

### Editor-Oberfläche
Die Editor-Oberfläche der Unreal Engine ist modular aufgebaut und bietet intuitive Panels wie den Content Browser, das Details Panel und den Blueprint Editor. Sie ist mächtig und anfangs etwas überwältigend, aber logisch strukturiert.

### Blueprints
- **Visuelles Scripting-System**, das ohne Programmierkenntnisse genutzt werden kann.
- Ideal für Prototyping und einfache Mechaniken.
- **Empfohlener Einstieg:** [Blueprint Visual Scripting Dokumentation](https://docs.unrealengine.com/5.0/en-US/blueprints-visual-scripting-in-unreal-engine/)

### Workflow
- **Hot Reload:** Änderungen im Code können sofort im Editor getestet werden.
- **Projektvorlagen:** FPS, Third Person, Side Scroller und weitere Vorlagen erleichtern den Einstieg.

---

## Programmierumgebung und Tools
- **Programmiersprachen:** Unterstützung für C++ und Blueprints.
- **IDE-Integration:** Nahtlose Integration mit Visual Studio, Rider und Xcode.
- **Debugging und Profiling:** Tools wie **Unreal Insights** und eingebaute Debug-Funktionen in Blueprints.

### Teamarbeit
- **Version Control:** Unterstützung für Git und Perforce.
- **Herausforderungen:** Bei binären Assets (UAssets) können Merge-Konflikte auftreten.

Nützliche Tools:
- [Unreal Insights](https://docs.unrealengine.com/5.0/en-US/unreal-insights-overview-in-unreal-engine/)

---

## Grafikqualität
- **Lumen und Nanite:** Revolutionieren das Rendering und ermöglichen realistische Beleuchtung und detaillierte Umgebungen.
- **Post-Processing:** Effekte wie Bloom, Depth of Field und Motion Blur.
- **Skalierbarkeit:** Einstellbare Qualität für verschiedene Hardware-Anforderungen.

### Beispiel:
Eine fotorealistische Landschaft mit Nanite und Lumen:
- [Landschaftserstellung mit Nanite und Lumen](https://www.youtube.com/watch?v=1NKOiLrX4r8)

---

## Charakteranimation
- **Animationssystem:** Umfassend mit State Machines, Inverse Kinematik und Layered Animation.
- **Tools:** Full Body IK (UE5) und Layered Animation ermöglichen präzise Steuerung.
- **Asset-Import:** Unkomplizierter Import von Animationen, z. B. von Mixamo.

### Nützliche Ressourcen:
- [Unreal Engine Animation Dokumentation](https://docs.unrealengine.com/5.0/en-US/animation-blueprint-in-unreal-engine/)

---

## Lernkurve und Einstieg
- **Schwierigkeit:** Der Einstieg kann komplex sein, besonders wegen der Vielzahl an Funktionen.
- **Blueprints:** Ideal für Einsteiger ohne Programmierkenntnisse.
- **C++ und APIs:** Für fortgeschrittene Entwickler wichtig, um das volle Potenzial der Engine auszuschöpfen.
- **Ressourcen:** Umfangreiche Tutorials, Beispielprojekte und die offizielle Dokumentation.

### Empfehlenswerte Tutorials:
- [Endless Runner Tutorial (YouTube)](https://www.youtube.com/results?search_query=unreal+engine+endless+runner+tutorial)
- [Offizielle Unreal Engine Dokumentation](https://docs.unrealengine.com)

---

## Erfahrungsbericht: Erstellung eines Endless Runners

### Projektplanung und Konzeptualisierung
- **Spielmechanik:** Der Spieler läuft automatisch und muss durch Springen oder Ducken Hindernisse überwinden.
- **Thema und Design:** Festlegung des grafischen Stils, z. B. futuristisch oder Cartoon-artig.

### Erstellung der Spielmechanik
- **Blueprints:** Ideal, um die grundlegende Bewegung und Kollisionsabfragen zu realisieren.
- **Level-Streaming:** Endlose Level durch modulare Abschnitte und zufälliges Spawn von Hindernissen.

### Beispiel-Assets und Ressourcen:
- [Endless Runner Starter Kit](https://www.unrealengine.com/marketplace/en-US/product/endless-runner-starter-kit)
- [Beispielprojekt: Side Scroller](https://docs.unrealengine.com/5.0/en-US/side-scroller-template-in-unreal-engine/)

---

## Probleme, Lösungen und Eigenheiten
- **Binäre Assets:** Merge-Konflikte bei UAssets können die Zusammenarbeit in Teams erschweren.
- **Hardware-Anforderungen:** Für Lumen und Nanite sind leistungsstarke GPUs erforderlich.
- **Komplexität:** Die Vielfalt an Features kann Neulinge überfordern.

### Lösungen:
- **Virtual Assets** zur Verbesserung von Versionskontrollproblemen.
- **Performance-Optimierungen** für mobile Geräte, z. B. durch Anpassungen in den Rendering-Einstellungen.

---

## Gesamteindruck
Die Unreal Engine überzeugt durch ihre herausragende Grafikqualität, vielseitige Tools und professionelle Funktionalität. Trotz der anfänglichen Komplexität erleichtern umfangreiche Tutorials, Blueprints und Community-Ressourcen den Einstieg. Besonders für ambitionierte Projekte geeignet, bietet die Engine aber auch eine solide Grundlage für kleinere Vorhaben.



## Godot

### Die Engine
Die Godot Engine, welches 2014 veröffentlicht wurde, ist eine MIT - lizensierte Open-Source Engine. Die MIT-Lizenz erlaubt es die Software frei zu nutzen, zu modifizieren und zu verteilen, solange der ursprüngliche Lizenztext beibehalten wird. Sie bietet zudem keinen Haftungsausschluss für Schäden. Godot wird von einer aktiven Community sowie einem Kernteam kontinuierlich weiterentwickelt. Godot unterstützt sowohl 2D- als auch 3D-Spieleentwicklung, wobei der Fokus besonders auf der 2D- Performance liegt, allerdings gab es bereits schon wesentliche Fortschritte im 3D - Bereich. Die Engine bietet eine umfassende Plattformunterstützung und erlaubt die Veröffentlichung von Spielen auf Windows, macOS, Linux, Android, iOS und Konsolen. Ein Alleinstellungsmerkmal von Godot ist das integrierte Szenensystem, das Spielelemente hierarchisch organisiert und den Entwicklungsprozess stark vereinfacht.

### Benutzerfreundlichkeit, Usability
Godot zeichnet sich durch eine intuitive Benutzeroberfläche und ein klar strukturiertes Layout aus, das sowohl für Einsteiger als auch für erfahrene Entwickler leicht verständlich ist. Besonders die Drag- and-Drop-Funktionalität und der Node-basierte Aufbau tragen dazu bei, dass die Engine schnell erlernt werden kann. Tutorials und Dokumentationen sind gut verfügbar, wobei die Community eine Vielzahl zusätzlicher Ressourcen bereitstellt. Ein Nachteil könnte jedoch die kleinere Community im Vergleich zu Unity oder Unreal darstellen, was die Verfügbarkeit spezifischer Plugins oder Lösungen einschränken könnte. 

### Programmierumgebung, Tools
Die Programmierung in Godot erfolgt primär mit der hauseigenen Skriptsprache GDScript, die Python-ähnlich ist und sich durch ihre Einfachheit und Lesbarkeit auszeichnet. Alternativ unterstützt Godot auch C# und externe Skriptsprachen. Die integrierte Entwicklungsumgebung (IDE) bietet viele hilfreiche Funktionen wie einen eingebauten Code-Editor, Debugging-Tools und ein Live-Update-System, mit dem Änderungen sofort getestet werden können. Besonders hervorzuheben ist die Modularität der Engine: Entwickler können problemlos eigene Plugins und Erweiterungen integrieren, um den Entwicklungsprozess weiter zu optimieren. Dabei zu beachten, ist, dass nicht alle Plugins auf den neusten Stand gehalten werden, da viele von ihnen kostenlos angeboten werden und es auf eine freiwillige Tätigkeit basiert und der finanzielle Anreiz fehlt. Zusätzlich kann man die Engine modifizieren mithilfe von C++.

### Grafikqualität
Mit der Einführung des Vulkan-Renderers in Version 4.3 hat Godot erhebliche Fortschritte erzielt. Vulkan ermöglicht moderne Rendering-Technologien wie realistische Lichteffekte, dynamische Schatten, High Dynamic Range (HDR), Global Illumination und Screen-Space Reflections, die die visuelle Darstellung deutlich verbessern. Dennoch wurden in einigen Fällen Performance-Einbußen festgestellt, insbesondere bei der Verwendung von OmniLight3D-Schatten, was auf eine erhöhte Anzahl von Draw Calls zurückzuführen ist. 

### Character Animation
Godot bietet umfangreiche Tools für Animationen, darunter den AnimationPlayer und den AnimationTree, die komplexe Animationsabläufe ermöglichen. Skeletale Animationen lassen sich einfach importieren und bearbeiten. Mit Blend Spaces und State Machines können fließende Übergänge zwischen Animationen realisiert werden. Dennoch wurden in der Community Performance-Probleme bei Animationen diskutiert, insbesondere im Vergleich zu anderen Engines. Allerdings kam es in unserem Projekt nicht zu Performance Problemen bezüglich der Animationen.

### Lernkurve
Godot zeichnet sich durch eine intuitive Benutzeroberfläche und ein flexibles Node-basiertes System aus, was besonders für Einsteiger den Einstieg erleichtert. Die Skriptsprache GDScript, die Python-ähnlich ist, ermöglicht einen einfachen und schnellen Start in die Spieleentwicklung. Alternativ bietet Godot Unterstützung für C#. Die umfangreiche Dokumentation und eine aktive Community bieten zusätzliche Hilfestellung. Der Umstieg von anderen Engines kann jedoch aufgrund der einzigartigen Konzepte von Godot anfangs herausfordernd sein. Es ist wichtig zu beachten, dass Visual Scripting in Godot 4 entfernt wurde, da es wenig genutzt wurde und der Wartungsaufwand hoch war. Es gibt jedoch Community-Plugins wie "Orchestrator", die ähnliche Funktionalitäten bereitstellen. 

### Probleme & Lösungen, Eigenheiten
Ein bekanntes Problem der Godot Engine betrifft die Physics Engine, insbesondere im 3D-Bereich. Die Kollisionserkennung und die Physikberechnungen sind nicht immer präzise, was oft zusätzliche Optimierungen erfordert. Auch der Asset-Import, vor allem aus Blender, kann problematisch sein, insbesondere bei Materialien und Texturen. Bei der Shader - Programmierung gab es Performance - Probleme. Diese wurden durch Anpassungen an den Einstellungen in der Godot Engine selbst und der Nodes behoben.

### Gesamteindruck
Die Godot Engine 4.3 ist eine Open-Source-Spielentwicklungsumgebung, die sowohl 2D- als auch 3D-Spielentwicklung unterstützt. Sie wird unter der MIT-Lizenz vertrieben, was Entwicklern maximale Freiheit bietet, den Code anzupassen und zu verteilen. Godot hat eine wachsende Community und ist besonders bei Indie-Entwicklern beliebt, da es kostenlos und leicht zugänglich ist. 

Die Engine ist bekannt für ihre benutzerfreundliche Oberfläche und das Node-basierte System, das die Strukturierung von Projekten erleichtert. Godot bietet eine integrierte Entwicklungsumgebung (IDE) mit einem umfassenden Toolset, einschließlich eines visuellen Editors und einer relativ einfach zu verstehenden Script-Sprache namens GDScript, die besonders gut auf die Engine angepasst ist. Es unterstützt auch C# und C++. 

Die Grafikqualität in 3D scheint akzeptabel zu sein, jedoch konnten wir in diesem Projekt nicht tief darauf eingehen. Animationen lassen sich einfach importieren und bearbeiten. Die Engine verfügt über integrierte Tools wie den AnimationPlayer, um Animationen direkt in der Engine zu erstellen. Die Lernkurve ist moderat. Für Anfänger gibt es viele Tutorials und eine aktive Community, die Unterstützung bietet. 

Es gibt einige Herausforderungen, insbesondere mit der Physics Engine von Godot 4.3. In unserem Fall, bei der Entwicklung eines kleinen 3D-Spiels, stellte sich heraus, dass die Physics Engine nicht besonders akkurat und performant ist. Diese Schwierigkeiten erforderten zusätzliche Anpassungen und Optimierungen, um die gewünschte Funktionalität zu erreichen. Insgesamt bietet die Godot Engine 4.3 jedoch eine robuste und vielseitige Plattform für Spieleentwickler, die bereit sind, sich in die Engine einzuarbeiten und individuelle Lösungen für spezifische Herausforderungen zu finden. 


## Vergleich

  - Testkategorien:
	 - Unterstützte Plattformen
	 - Rentabilität/Kosten 
	 - Performance
	   - Rendering (nach u. s. Benchmark)
	   - Physik(nach u. s. Benchmark)
    - TODO
      - Tests durchführen und Messwerte/Ergebnisse generieren (***G***)
 	   - Messwerte zusammenfassen und tabellarisch darstellen (***Ü***)

## Fazit
   
### Stärken/Schwächen

#### Unity
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
#### Unreal 

#### Godot
##### Stärken 
- **Open-Source und kostenlos:** Keine Lizenzgebühren oder Einschränkungen bei der Nutzung.
- **Benutzerfreundlichkeit:** Intuitive Oberfläche und ein Node-basiertes System, das die Projektstrukturierung erleichtert.
- **GDScript:** Eine einfach zu erlernende Script-Sprache, die gut auf die Engine angepasst ist und für Entwickler mit Programmiererfahrung leicht verständlich ist.
- **Plattformübergreifend:** Unterstützung für zahlreiche Plattformen, einschließlich Windows, macOS, Linux, Android, iOS, HTML5 und mehr.
- **Integrierte Entwicklungsumgebung (IDE):** Umfassendes Toolset, einschließlich visueller Editor und Debugging-Tools.
- **2D- und 3D-Unterstützung:** Flexible Entwicklungsmöglichkeiten sowohl für 2D- als auch für 3D-Projekte.
- **Community und Support:** Eine aktive Community und zahlreiche Tutorials und Ressourcen, die den Einstieg erleichtern.
- **Dokumentation:** Sehr gute und auch offline verfügbare Dokumentation.
- **Anpassbarkeit:** Einfacher Zugang zum Quellcode ermöglicht tiefgreifende Anpassungen und Erweiterungen der Engine.
- **Plugins:** Vielzahl verfügbarer Plugins, die die Funktionalität der Engine erweitern können.

##### Schwächen 
- **Physics Engine:** In 3D-Projekten kann die Physics Engine ungenau und leistungsschwach sein, was zusätzliche Optimierungen erfordert.
- **Asset-Import:** Probleme beim Import von Blender-Assets und anderen Modellen, insbesondere im Hinblick auf Materialien und Texturen.
- **Rendering-Leistung:** In 3D-Projekten kann die Rendering-Leistung akzeptabel, aber nicht herausragend sein, was bei umfangreicheren Projekten zu Einschränkungen führen könnte.
- **Plugins:** Obwohl Plugins eine positive Erweiterung darstellen, können sie Probleme verursachen, wenn sie nicht sorgfältig integriert werden.

### Empfehlungen
- Unity kann besonders gut für 2D Spiele oder VR-Anwendungen empfohlen werden. Auch 3D-Entwicklungen sind möglich. Diese können aber bei grafisch anspruchsvollen Spielen nicht mit anderen Engines mithalten. Auch Erwähnenswert ist die starke Community, die mit verschiedensten Tools, Addons und Tutorials die Spieleentwicklung enorm erleichtern. Zudem ist Unity eine budgetfreundliche Option die zudem eine breite Plattformunterstützung bietet.
- Auch Godot ist besonders stark in der 2D-Spieleentwicklung und bietet eine großartige Auswahl von Tools um Spiele effizient zu entwickeln. zudem gibt es einen visuellen Editor, der die Arbeit mit Sprites und Animationen vereinfacht. Besonders hervorzuheben ist das Prototyping, das in Godot hervorragend realisiert werden kann.
- Unreal Engine überzeugt durch herausragende Grafik, vielseitige Tools und professionelle Funktionalität besonders in der 3D-Umgebung. Trotz der anfänglichen Komplexität wird der Einstieg durch umfangreiche Tutorials, Blueprints und Community-Ressourcen erleichtert. Die Engine ist besonders für ambitionierte Projekte geeignet, bietet aber auch für kleinere Vorhaben eine solide Grundlage.

#### Unity

#### Unreal

#### Godot
##### Spieleentwicklung 
- **2D-Spiele:** Godot ist besonders stark in der 2D-Spieleentwicklung. Die Engine bietet eine Fülle von Tools, um 2D-Spiele effizient und effektiv zu erstellen, einschließlich eines visuellen Editors, der die Arbeit mit Sprites, Tilesets und Animationen erleichtert.
- **3D-Spiele:** Während Godot historisch eher auf 2D-Spiele fokussiert war, hat die 4.3-Version erhebliche Verbesserungen in der 3D-Entwicklung mit sich gebracht. Die Engine bietet nun bessere Rendering-Fähigkeiten, Shader-Unterstützung und eine Vielzahl von Tools, um 3D-Welten zu erschaffen.
- **Prototyping:** Durch die benutzerfreundliche Oberfläche und Skripting-Tools eignet sich Godot hervorragend für das schnelle Prototyping von Spielideen.

##### Anwendungen und Tools 
- **Interaktive Anwendungen:** Godot kann für die Entwicklung von interaktiven Anwendungen und Tools verwendet werden, die auf verschiedenen Plattformen laufen, einschließlich Desktop, Mobile und Web.

##### Lern- und Bildungstools 
- **Bildung und Lehre:** Godot ist aufgrund seiner Zugänglichkeit und der umfassenden Dokumentation eine großartige Wahl für Bildungseinrichtungen und Lernende, die in die Spielentwicklung einsteigen möchten. Die Engine bietet eine ideale Plattform, um grundlegende Konzepte der Programmierung und Spieleentwicklung zu erlernen.

## Anhang

